---
layout: page
permalink: /documentation/
toc: true

# Banner Content
# =================================
title: Documentation & Examples
subtitle: Checkout some of the amazing things you can do using our platform.
Tìm hiểu những điều tuyệt vời bạn có thể làm được khi sử dụng nền tảng của chúng tôi.
hero_image: assets/img/dsa_hero.jpg

---

<div class="doc-main-section" markdown="1">
## 1. Quản lý dự án chú thích

![](../assets/img/documentation/annotation_interface.png){:class="box"}

Đánh dấu hình ảnh là thành phần thiết yếu trong việc phát triển các thuật toán máy học cho các ứng dụng bệnh học kỹ thuật số. HistomicsUI và DSA được thiết kế để tiến hành các nghiên cứu đa người dùng, phân tán nhằm tạo ra các tập dữ liệu chú thích lớn và đã được sử dụng để tạo ra hơn 250.000 dấu hiệu của con người trong các dự án của chúng tôi. Trong các ví dụ sau, chúng tôi minh họa cách sử dụng các công cụ đánh dấu giao diện HistomicsUI cho người dùng và cách sử dụng API để quản lý các nghiên cứu chú thích đa người dùng lớn cho nhà phát triển.
</div>

<div class="doc-sub-section columns is-variable is-3">
<div class="column is-8" markdown="1">
### [1.1. For Users - using HistomicsTK markup tools](http://www.youtube.com/watch?v=HTvLMyKYyGs)

To introduce users to the HistomicsUI interface we created a video that illustrates how to navigate projects, how to use the markup tools to create annotations, how to edit annotations, how to generate annotation styles, and how to standardize styles using templates.
Để giới thiệu cho người dùng về giao diện HistomicsUI, chúng tôi đã tạo một video minh họa cách điều hướng các dự án, cách sử dụng các công cụ đánh dấu để tạo chú thích, cách chỉnh sửa chú thích, cách tạo kiểu chú thích và cách chuẩn hóa các kiểu bằng cách sử dụng mẫu.
</div>

<div class="doc-image column is-4" markdown="1">
[![](http://img.youtube.com/vi/HTvLMyKYyGs/0.jpg)](http://www.youtube.com/watch?v=HTvLMyKYyGs){:target="_blank"}

Video này có thể được sử dụng làm tài liệu hướng dẫn khi tiến hành các nghiên cứu chú thích và có thể giúp cải thiện chất lượng chú thích mà các cộng tác viên của bạn tạo ra trong HistomicsUI.
</div>
</div>

<div class="doc-sub-section" markdown="1">
### [1.2. Giới thiệu API Girder](https://digitalslidearchive.github.io/HistomicsTK/examples/introducing_the_girder_api)
API RESTful cho phép các nhà phát triển tương tác theo chương trình với máy chủ DSA để quản lý dữ liệu, tài khoản người dùng, chú thích và quyền của họ. Các chức năng này là một phần của những gì làm cho DSA trở thành một nền tảng mạnh mẽ để tạo ra các chú thích thông qua các nghiên cứu đa người dùng phân tán. Trong ví dụ này, chúng tôi thảo luận về các yếu tố cơ bản của cơ sở dữ liệu DSA, mô tả cấu trúc của chú thích và minh họa nhiều phương pháp để thực hiện các lệnh gọi API DSA. Truy cập [trang này](https://digitalslidearchive.github.io/HistomicsTK/examples/introducing_the_girder_api) để biết thêm chi tiết.

![](../assets/img/documentation/annotation_definitions.png)

</div>

<div class="doc-sub-section" markdown="1">
### [1.3. Procedure for managing a typical annotation project](https://digitalslidearchive.github.io/HistomicsTK/examples/procedure_for_typical_annotation_project)
Việc tiến hành một dự án chú thích đòi hỏi phải lập kế hoạch cẩn thận và làm quen với cách quản lý người dùng, dữ liệu và chú thích trong DSA. Ở đây, chúng tôi mô tả các cân nhắc trong việc lập kế hoạch cho một dự án chú thích thành công và cung cấp tổng quan về các bước để bắt đầu một dự án. Truy cập [trang này](https://digitalslidearchive.github.io/HistomicsTK/examples/procedure_for_typical_annotation_project) để biết thêm chi tiết.
</div>

<div class="doc-sub-section columns is-variable is-3">
<div class="column is-8" markdown="1">
### [1.4. Mẹo để chia tỷ lệ kết xuất chú thích](https://digitalslidearchive.github.io/HistomicsTK/examples/tips_for_scalable_annotation_rendering)

Các thuật toán phân tích hình ảnh và con người có thể tạo ra số lượng lớn các chú thích. HistomicsUI được triển khai để hiển thị chú thích có thể mở rộng và nếu bạn tuân theo một số nguyên tắc cơ bản, bạn có thể tránh được các vấn đề về hiệu suất khi hiển thị số lượng lớn các phần tử và đỉnh. Truy cập [trang này](https://digitalslidearchive.github.io/HistomicsTK/examples/tips_for_scalable_annotation_rendering) để biết thêm chi tiết.
</div>

<div class="doc-image column is-4" markdown="1">
![](../assets/img/documentation/many_annotations.png)
</div>
</div>

<div class="doc-sub-section columns is-variable is-3">
<div class="column is-8" markdown="1">
### [1.5. Tạo hình ảnh thư viện để xem lại chú thích](http://www.youtube.com/watch?v=Plh39obBg_0)

Các nghiên cứu chú thích thường liên quan đến việc đánh dấu các cấu trúc trong các vùng quan tâm (ROI) thường nhỏ hơn nhiều so với hình ảnh toàn bộ trang chiếu. Khi xem xét các chú thích này, người ta mất nhiều thời gian để điều hướng giữa các ROI trong một trang chiếu và trên toàn bộ bộ sưu tập trang chiếu. Để cho phép xem xét nhanh chóng, HistomicsTK cung cấp các chức năng để tập hợp các ROI đã chú thích thành hình ảnh thư viện mosaic dày đặc để trực quan hóa. Các thư viện này loại bỏ sự cần thiết phải điều hướng giữa các ROI và cũng loại bỏ nhu cầu bật tắt khả năng hiển thị chú thích hoặc điều chỉnh độ phóng đại.
</div>

<div class="doc-image column is-4" markdown="1">
[![](http://img.youtube.com/vi/Plh39obBg_0/0.jpg)](http://www.youtube.com/watch?v=Plh39obBg_0)

This video demonstrates the functionality of these galleries and [this example](https://digitalslidearchive.github.io/HistomicsTK/examples/creating_gallery_images_review) demonstrates the gallery creation process.
</div>
</div> 

<div class="doc-sub-section columns is-variable is-3">
<div class="column is-8" markdown="1">
### [1.6. Sao lưu cục bộ và truy vấn SQL của dữ liệu chú thích](https://digitalslidearchive.github.io/HistomicsTK/examples/annotation_database_backup_and_sql_parser)

Các chú thích thể hiện sự đầu tư thời gian đáng kể của người dùng tạo ra chúng và chúng cần được sao lưu thường xuyên. HistomicsTK có các chức năng tiện ích cho phép sao lưu đệ quy cơ sở dữ liệu girder cục bộ dưới dạng kết hợp các tệp JSON (tương tự nhất với định dạng thô), tệp bảng (.csv) và/hoặc cơ sở dữ liệu SQLite. Cơ sở dữ liệu SQLite có thể dễ dàng được xem bằng cách sử dụng, ví dụ: [trình xem sqlite ngoại tuyến](https://sqlitebrowser.org/dl/){:target="_blank"} hoặc thậm chí là [trình xem sqlite trực tuyến](https://sqliteonline.com/){:target="_blank"}. Có thể tìm thêm chi tiết trong [sổ tay này](https://digitalslidearchive.github.io/HistomicsTK/examples/annotation_database_backup_and_sql_parser).
</div>

<div class="doc-image column is-4" markdown="1">
![](../assets/img/documentation/sqlite.png)
</div>
</div>


<div class="doc-main-section" markdown="1">
## 2. Xử lý chú thích và hình ảnh mặt nạ
Cơ sở dữ liệu DSA lưu trữ các chú thích ở định dạng danh sách tọa độ (x, y). Đối với nhiều tác vụ xử lý như đào tạo các thuật toán máy học hoặc đo lường sự đồng thuận giữa các người quan sát, việc biểu diễn mặt nạ hoặc hình ảnh nhãn sẽ dễ dàng hơn khi làm việc. Tương tự, đầu ra của nhiều thuật toán là hình ảnh nhãn hoặc mặt nạ cần được chuyển đổi thành tọa độ để trực quan hóa trong HistomicsUI. Trong các ví dụ sau, chúng tôi minh họa cách chuyển đổi giữa danh sách tọa độ và các định dạng hình ảnh. Chúng tôi cũng chứng minh cách hợp nhất các chú thích được chia tách bằng cách xử lý xếp ô của hình ảnh toàn bộ trang chiếu.
</div>

<div class="doc-sub-section columns is-variable is-3">
<div class="column is-8" markdown="1">
### [2.1. Chuyển đổi chú thích thành hình ảnh mặt nạ phân đoạn ngữ nghĩa](https://digitalslidearchive.github.io/HistomicsTK/examples/annotations_to_semantic_segmentation_masks)
Mặt nạ phân đoạn ngữ nghĩa là một hình ảnh trong đó giá trị của một pixel mã hóa tư cách thành viên của nó trong một lớp (ví dụ: khối u). Biểu diễn này rất hữu ích trong việc đào tạo và xác thực các thuật toán máy học cho các tác vụ như phân đoạn vùng mô. [Ví dụ này](https://digitalslidearchive.github.io/HistomicsTK/examples/annotations_to_semantic_segmentation_masks) minh họa cách chuyển đổi từ chú thích trong cơ sở dữ liệu DSA sang mặt nạ phân đoạn ngữ nghĩa trong nhiều tình huống khác nhau.
</div>

<div class="doc-image column is-4" markdown="1">
![](../assets/img/documentation/annotations_to_masks.png)
</div>
</div>

<div class="doc-sub-section columns is-variable is-3">
 <div class="column is-8" markdown="1">
  ### [2.2. Chuyển đổi chú thích thành hình ảnh mặt nạ phân đoạn đối tượng](https://digitalslidearchive.github.io/HistomicsTK/examples/annotations_to_object_segmentation_masks)
  Mặt nạ phân đoạn đối tượng là một hình ảnh trong đó giá trị của một pixel mã hóa sự thuộc về của nó đối với một đối tượng hoặc phiên bản cụ thể và tùy chọn lớp đối tượng (ví dụ: một nhân đơn lẻ hoặc nhân khối u). Biểu diễn này rất hữu ích trong việc đào tạo và xác thực các thuật toán máy học để phát hiện, phân loại và phân đoạn đối tượng bao gồm [Mask R-CNN](https://arxiv.org/abs/1703.06870){:target="_blank"}. [Ví dụ này](https://digitalslidearchive.github.io/HistomicsTK/examples/annotations_to_object_segmentation_masks) trình bày cách chuyển đổi chú thích thành mặt nạ phân đoạn đối tượng, cùng với việc trình bày sự khác biệt giữa hình ảnh mặt nạ phân đoạn ngữ nghĩa và đối tượng.
 </div>

<div class="doc-image column is-4" markdown="1">
![](../assets/img/documentation/annotations_to_object_masks.png)
</div>
</div>

<div class="doc-sub-section columns is-variable is-3">
 <div class="column is-8" markdown="1">
  ### [2.3. Chuyển đổi hình ảnh mặt nạ trở lại chú thích](https://digitalslidearchive.github.io/HistomicsTK/examples/segmentation_masks_to_annotations)

Một trong những cách tốt nhất để đánh giá hiệu suất của các thuật toán phân đoạn hình ảnh là trực quan hóa các dự đoán của chúng dưới dạng chú thích trong HistomicsUI. HistomicsTK cung cấp các chức năng để chuyển đổi hình ảnh nhãn được tạo ra bởi các mô hình phân đoạn ngữ nghĩa và đối tượng thành định dạng tọa độ có thể được đưa vào DSA và trực quan hóa. Có thể xem thêm chi tiết [tại đây](https://digitalslidearchive.github.io/HistomicsTK/examples/segmentation_masks_to_annotations).
</div>

<div class="doc-image column is-4" markdown="1">
![](../assets/img/documentation/masks_to_annotations.png)
</div>
</div>

<div class="doc-sub-section columns is-variable is-3">
 <div class="column is-8" markdown="1">
  ### [2.4. Hợp nhất các chú thích từ phân tích xếp ô](https://digitalslidearchive.github.io/HistomicsTK/examples/polygon_merger_from_tiled_masks)

Phân tích xếp ô của hình ảnh toàn bộ trang chiếu có thể chia nhỏ các cấu trúc lớn như vùng mô trải dài trên nhiều ô. HistomicsTK cung cấp các chức năng để hợp nhất các chú thích được tạo thông qua phân tích xếp ô để tạo ra các chú thích mạch lạc trải dài trên nhiều ô. Các chức năng này có thể chấp nhận đầu vào là [mảng xếp ô của mặt nạ phân đoạn](https://digitalslidearchive.github.io/HistomicsTK/examples/polygon_merger_from_tiled_masks) hoặc là [tập hợp không được sắp xếp của danh sách tọa độ (x, y)](https://digitalslidearchive.github.io/HistomicsTK/examples/polygon_merger_using_rtree).
 </div>

<div class="doc-image column is-4" markdown="1">
![](../assets/img/documentation/polygon_merger.png)
</div>
</div>


<div class="doc-main-section columns is-variable is-3">
 <div class="column is-8" markdown="1">
  ## 3. Phân tích hình ảnh với HistomicsTK

HistomicsTK cung cấp các khả năng phân tích hình ảnh cơ bản mà các nhà phát triển có thể sử dụng để xây dựng quy trình công việc bệnh học kỹ thuật số phức tạp. Gói HistomicsTK có thể được cài đặt bằng pip và có thể được sử dụng như một thư viện python độc lập hoặc như một plugin girder để chạy các tác vụ phân tích hình ảnh từ giao diện HistomicsUI. Trong các ví dụ sau, chúng tôi minh họa cách HistomicsTK và thư viện large_image có thể được sử dụng cho các tác vụ phân tích hình ảnh và cách làm việc với các tập dữ liệu hình ảnh cục bộ hoặc dữ liệu được lưu trữ trên các cài đặt DSA từ xa.
 </div>
<div class="doc-image column is-4" markdown="1">
![](../assets/img/documentation/saliency_results.png)
</div>
</div>

<div class="doc-sub-section" markdown="1">
### [3.1. Local processing of whole-slide images using large_image](https://digitalslidearchive.github.io/HistomicsTK/examples/using_large_image)
Thư viện python large_image (là một phần phụ thuộc của HistomicsTK) cho phép người dùng thuận tiện làm việc với hình ảnh đa độ phân giải lớn, cung cấp các chức năng để lặp qua các biểu diễn xếp ô của trang chiếu kỹ thuật số hoặc để làm việc liền mạch trên cùng một vùng ở các độ phóng đại khác nhau. large_image cung cấp một giao diện duy nhất để làm việc với nhiều nguồn ô khác nhau bao gồm openslide, openjpeg, ometiff và nd2. [Ví dụ này](https://digitalslidearchive.github.io/HistomicsTK/examples/using_large_image) cho thấy cách sử dụng large_image để trích xuất dữ liệu pixel trong các mẫu phân tích hình ảnh phổ biến.
</div>

<div class="doc-sub-section" markdown="1">
### [3.2. Analyzing remotely hosted images with the girder client](https://digitalslidearchive.github.io/HistomicsTK/examples/workflows)
Ứng dụng python gider cho phép các nhà phát triển làm việc với hình ảnh được lưu trữ từ xa trong các phiên bản DSA thông qua API web RESTful. [Ví dụ này](https://digitalslidearchive.github.io/HistomicsTK/examples/workflows) cho thấy cách sử dụng ứng dụng girder để trích xuất dữ liệu pixel từ các phiên bản DSA và chạy quy trình công việc phân tích hình ảnh trên dữ liệu này cục bộ.
</div>

<div class="doc-sub-section columns is-variable is-3">
<div class="column is-8" markdown="1">
### [3.3. Color deconvolution, normalization, and data augmentation](https://digitalslidearchive.github.io/HistomicsTK/examples/color_normalization_and_augmentation)

Bước đầu tiên trong việc phân tích hình ảnh bệnh học kỹ thuật số thường là tiền xử lý hình ảnh màu để điều chỉnh các biến thể về nhuộm màu hoặc hình ảnh hoặc để cô lập một màu quan tâm. Các ví dụ này minh họa cách sử dụng HistomicsTK để [khử màu](https://digitalslidearchive.github.io/HistomicsTK/examples/color_deconvolution), đồng thời [chuẩn hóa cấu hình màu](https://digitalslidearchive.github.io/HistomicsTK/examples/color_normalization_and_augmentation) và [tạo hình ảnh màu tăng cường](https://digitalslidearchive.github.io/HistomicsTK/examples/color_normalization_and_augmentation) để máy học.
</div>
<div class="doc-image column is-4" markdown="1">
![](../assets/img/documentation/normalization_and_augmentation.png)
</div>
</div>

<div class="doc-sub-section columns is-variable is-3">
<div class="column is-8" markdown="1">
 ### [3.4. Đếm pixel dương tính và xử lý song song với Dask](https://digitalslidearchive.github.io/HistomicsTK/examples/positive_pixel_count)

Việc đo lường nhuộm màu IHC bằng cách đếm pixel dương tính là một trong những tác vụ phân tích hình ảnh cơ bản nhất trong bệnh học kỹ thuật số. [Ở đây](https://digitalslidearchive.github.io/HistomicsTK/examples/positive_pixel_count), chúng tôi chỉ ra cách áp dụng đếm pixel dương tính cho hình ảnh lớn bằng Dask, một thư viện python để tính toán song song trên các cụm và hệ thống đa lõi.
 </div>
<div class="doc-image column is-4" markdown="1">
![](../assets/img/documentation/positive_pixel.png)
</div>
</div>

<div class="doc-sub-section columns is-variable is-3">
<div class="column is-8" markdown="1">
 ### [3.5. Xác định các vùng nổi bật trong hình ảnh toàn bộ trang chiếu](https://digitalslidearchive.github.io/HistomicsTK/examples/semantic_segmentation_color_thresholding_approach)

Hình ảnh toàn bộ trang chiếu thường chứa các tạo tác như vùng đánh dấu hoặc vùng vô bào cần tránh trong quá trình phân tích. Trong ví dụ này, chúng tôi chỉ ra cách HistomicsTK có thể được sử dụng để phát triển các thuật toán phát hiện nổi bật, phân đoạn trang chiếu ở độ phóng đại thấp để tạo ra bản đồ hướng dẫn các phân tích ở độ phóng đại cao hơn. Đầu tiên, chúng tôi chỉ ra cách [phân tích siêu pixel](https://digitalslidearchive.github.io/HistomicsTK/examples/semantic_segmentation_superpixel_approach) có thể được sử dụng để định vị các vùng tăng tế bào giàu khối u. Sau đó, chúng tôi chỉ ra cách [phân tích không gian màu](https://digitalslidearchive.github.io/HistomicsTK/examples/semantic_segmentation_color_thresholding_approach) có thể phát hiện các yếu tố khác nhau như mực hoặc máu, cũng như các vùng tăng tế bào để cải thiện chất lượng của các tác vụ phân tích hình ảnh tiếp theo.
 </div>
<div class="doc-image column is-4" markdown="1">
![](../assets/img/documentation/saliency_thresholding.png)
</div>
