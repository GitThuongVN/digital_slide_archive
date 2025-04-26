Hướng dẫn Di chuyển
===================

Tài liệu này nhằm giúp chuyển đổi giữa các phiên bản chính của Digital Slide Archive. Phương pháp cài đặt hiện tại sử dụng ``docker compose`` và dựa trên Girder 3.x.

Từ deploy_docker.py sang docker compose
-----------------------------------------

Trước năm 2021, Digital Slide Archive sử dụng script ``deploy_docker.py``. Nếu bạn đã triển khai phần mềm bằng phương tiện khác, những hướng dẫn này sẽ cần một số điều chỉnh.

Script ``deploy_docker.py`` được phát triển trước khi docker compose xử lý tất cả các tính năng mong muốn. Nếu bạn đang sử dụng các tùy chọn dòng lệnh trên ``deploy_docker.py``, bạn sẽ cần tìm hiểu xem mỗi tùy chọn đó được chuyển đổi như thế nào sang ký pháp docker compose. Đối với triển khai mặc định không có bất kỳ tùy chọn dòng lệnh nào, bạn có thể chuyển đổi bằng cách thực hiện::

    chown -R $(id -u):$(id -g) ~/.dsa

Sau đó, thêm ``docker-compose.override.yml`` vào thư mục ``devops/dsa``, thay thế ``/home/ubuntu`` bằng độ phân giải của ``~``::

    ---
    services:
      girder:
        volumes:
          - /home/ubuntu/.dsa/assetstore:/opt/digital_slide_archive/assetstore # assetstore là thư mục lưu trữ dữ liệu
          - /home/ubuntu/.dsa/logs:/logs #logs là thư mục chứa các logs của hệ thống
      mongodb:
        volumes:
          - /home/ubuntu/.dsa/db:/data/db #db là thư mục chứa database

Bây giờ, từ thư mục ``devops/dsa``, ``docker compose`` sẽ hoạt động.


Từ Girder 2.x và Kho lưu trữ HistomicsTK
-------------------------------------------

Việc triển khai Digital Slide Archive ban đầu được bao gồm như một phần của kho lưu trữ HistomicsTK và sử dụng Girder 2.x làm máy chủ cơ bản. Để di chuyển từ phiên bản Girder 2.x sang phiên bản trong kho lưu trữ này, không cần thay đổi đặc biệt nào -- chỉ cần sử dụng script ``deploy_docker.py`` hiện tại từ kho lưu trữ này.

Mongo
-----

Theo mặc định, phiên bản chính mới nhất của MongoDB được sử dụng. Tuy nhiên, Mongo không tự động nâng cấp các file cơ sở dữ liệu để hoạt động với nhiều phiên bản chính hơn ngoài bản cập nhật cuối cùng. Ví dụ: cơ sở dữ liệu được tạo trong Mongo 3.4 sẽ hoạt động với Mongo 3.6 nhưng không hoạt động với Mongo 4.0.

Nếu bạn có một phiên bản đang chạy của Digital Slide Archive, bạn có thể tìm hiểu phiên bản Mongo nào tương thích với cơ sở dữ liệu bằng cách đưa ra lệnh::

  docker exec histomicstk_mongodb mongo girder --eval \
  'db.adminCommand({getParameter: 1, featureCompatibilityVersion: 1})'

Nếu đây không phải là phiên bản Mongo hiện tại, bạn có thể nâng cấp phiên bản tương thích của cơ sở dữ liệu. Ví dụ: lệnh::

  docker exec histomicstk_mongodb mongo girder --eval \
  'db.adminCommand({setFeatureCompatibilityVersion: "4.2"})'

sẽ nâng cấp lên Mongo 4.2.

Bạn có thể khởi động Digital Slide Archive với phiên bản Mongo cũ hơn bằng cách chỉ định phiên bản trong file ``docker-compose.override.yml`` của bạn như một phần của tên image của container mongo. Nếu cơ sở dữ liệu của bạn đủ cũ, bạn có thể cần phải di chuyển mỗi lần một phiên bản chính, điều chỉnh phiên bản tương thích mỗi lần.
