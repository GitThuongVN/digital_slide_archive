---
layout: page
permalink: /system-overview/

# Banner Content
# =================================
title: System Overview
subtitle: Infographic overview of DSA, covering the key components and setup options.
hero_image: assets/img/home-callouts/system-overview.jpg
---
<div class="system-overview-page" markdown="1">

Kho lưu trữ Digital Slide thường được cài đặt trên một máy tính duy nhất hoặc trên một máy tính chính với một hoặc nhiều máy worker để chạy các thuật toán hình ảnh được gọi thông qua HistomicsUI hoặc API. Có các tùy chọn bổ sung, chẳng hạn như lưu trữ cơ sở dữ liệu ở một vị trí bên ngoài, nhưng chúng không phổ biến.

## Thiết lập trên một máy tính

![Single Computer Diagram](../assets/img/system-diagrams/system-diagram-single-computer-setup.svg "Single Computer Diagram"){:width="75%"}

Cài đặt mặc định của Digital Slide Archive là trên một máy tính duy nhất. Đây là cách đơn giản nhất để triển khai DSA, mặc dù các tác vụ phân tích hình ảnh bị giới hạn bởi sức mạnh xử lý của một hệ thống duy nhất.

Tệp hình ảnh và các tệp dữ liệu khác, cơ sở dữ liệu và tệp nhật ký đều được lưu trữ trên hệ thống tệp cục bộ. Các tệp dữ liệu cũng có thể được lưu trữ hoặc nhập từ các kho tài sản bên ngoài, chẳng hạn như Amazon S3.

Khi `docker compose` được sử dụng để cài đặt với tệp `docker-compose.yml` mặc định trong thư mục `devops/dsa`, một bộ năm container docker được khởi động để cung cấp tất cả các dịch vụ cần thiết bởi DSA. Khi một tác vụ phân tích hình ảnh được thực hiện thông qua HistomicsUI hoặc API, ví dụ: phát hiện nhân trên hình ảnh toàn bộ slide bằng bộ công cụ HistomicsTK, một container docker bổ sung được tạo để chạy tác vụ. Container này chỉ tồn tại miễn là cần thiết cho việc phân tích hình ảnh. Kết quả được lưu trữ trở lại cơ sở dữ liệu và kho tài sản tệp.

---

## Thiết lập worker phân tán

![Distributed Workers Setup](../assets/img/system-diagrams/system-diagram-distributed-workers-setup.svg "Distributed Workers Setup Diagram"){:width="75%"}

Để mở rộng sức mạnh tính toán và tăng tốc phân tích hình ảnh, Digital Slide Archive có thể được cài đặt trên một máy tính chính và bất kỳ số lượng máy worker nào.

Tệp hình ảnh và các tệp dữ liệu khác, cơ sở dữ liệu và tệp nhật ký đều được lưu trữ trên hệ thống tệp cục bộ của máy tính chính, giống như trong cấu hình một máy tính. Tất nhiên, các tệp dữ liệu cũng có thể được lưu trữ hoặc nhập từ các kho tài sản bên ngoài, chẳng hạn như Amazon S3.

Để bắt đầu ở chế độ này, hãy xem hướng dẫn trong thư mục devops external-worker. Điều này cho phép một hoặc nhiều worker được khởi động trên các máy khác. Worker có thể được khởi động hoặc dừng bất kỳ lúc nào. Ví dụ: có thể thêm nhiều worker hơn khi chạy nhiều tác vụ và sau đó dừng lại khi chúng không còn cần thiết. Nếu hệ thống tệp mạng chia sẻ được sử dụng, các lệnh gắn kết thích hợp có thể được thêm vào làm tùy chọn bổ sung cho cả máy tính chính và các lệnh worker; điều này có thể giảm đáng kể lưu lượng mạng.

Trên máy tính chính, bốn container docker được khởi động để cung cấp hầu hết các dịch vụ cần thiết bởi DSA. Trên mỗi worker, một container docker được khởi động ban đầu. Khi một tác vụ phân tích hình ảnh được thực hiện, một container docker bổ sung được tạo trên worker để chạy tác vụ. Container này chỉ tồn tại trong suốt thời gian của tác vụ. Kết quả được lưu trữ trở lại cơ sở dữ liệu và kho tài sản tệp.

Khi có nhiều worker, mỗi worker lần lượt được giao nhiệm vụ cho đến khi tất cả chúng đều bận. Khi các worker hoàn thành một tác vụ, chúng sẽ được giao các tác vụ mới. Nếu một worker bị dừng hoặc mất kết nối mạng với một tác vụ chưa hoàn thành, tác vụ đó sẽ được gán lại cho một worker khả dụng khác. Các máy tính worker không cần phải giống hệt nhau; các worker nhanh hơn sẽ kết thúc xử lý nhiều tác vụ hơn các worker chậm hơn.
