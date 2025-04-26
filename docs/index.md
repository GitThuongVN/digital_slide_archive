---
layout: home

# Nội dung Banner
# =================================
title: Khai thác tối đa tiềm năng của dữ liệu bệnh lý kỹ thuật số của bạn
subtitle: Một nền tảng dựa trên web, được container hóa để phân tích, trực quan hóa, quản lý và chú thích dữ liệu hình ảnh bệnh lý kỹ thuật số toàn phiến

hero_image: assets/img/dsa_hero.jpg

hero_buttons: 
  - link_text: Xem bản Demo
    link: https://demo.kitware.com/histomicstk/#collection/5bbdeb97e629140048d017ba/folder/5bbdeba3e629140048d017bb 

  - link_text: View on GitHub
    link: https://github.com/DigitalSlideArchive

  - link_text: Installation
    link: https://github.com/DigitalSlideArchive/digital_slide_archive/blob/master/devops/dsa/README.rst

# Phần DSA là gì?
# ================================= 
about_title: DSA là gì? 
about_text: Digital Slide Archive (DSA) là một nền tảng cung cấp khả năng lưu trữ, quản lý, trực quan hóa và chú thích các bộ dữ liệu hình ảnh lớn. DSA bao gồm một bộ công cụ phân tích (HistomicsTK), một giao diện để trực quan hóa các phiến và quản lý chú thích (HistomicsUI), một lớp cơ sở dữ liệu (sử dụng Mongo) và một máy chủ web cung cấp một API phong phú và các công cụ quản lý dữ liệu (sử dụng Girder). Hệ thống này có thể 

# Khả năng của DSA
about_list:
  - list_item: Tổ chức hình ảnh từ nhiều kho tài sản khác nhau, chẳng hạn như hệ thống tệp cục bộ và S3.
  - list_item: Cung cấp kiểm soát truy cập người dùng. 
  - list_item: Chú thích và đánh giá hình ảnh. 
  - list_item: Chạy các thuật toán trên toàn bộ hoặc một phần của hình ảnh. 

# Liên kết tài nguyên
about_resources_title: Tài nguyên 

about_system_diagram: assets/img/system-diagrams/system-diagram.svg
about_system_diagram_caption: "Sơ đồ hệ thống DSA."
about_system_overview_page_button: ( Xem tổng quan hệ thống chi tiết )
about_system_link: system-overview/

about_resources:
  - name: Thảo luận trên GitHub 
    link: https://github.com/DigitalSlideArchive/digital_slide_archive/discussions
    icon: fab fa-github

  - name: Jupyter 
    link: https://digitalslidearchive.github.io/HistomicsTK/examples.html
    icon: fas fa-book

  - name: Youtube 
    link: https://www.youtube.com/channel/UCe9RJmSdEJLTWkRhSOIVAlg
    icon: fab fa-youtube

# Platforms Content
# =================================
platforms:
  # HistomicsUI
  - title: HistomicsUI 
    description: HistomicsUI là một ứng dụng dựa trên web để kiểm tra, chú thích và xử lý hình ảnh mô học nhằm trích xuất các đặc điểm cấp thấp và cao (ví dụ: cấu trúc tế bào, các loại đặc điểm). 
    docs_url: https://github.com/DigitalSlideArchive/HistomicsUI/blob/master/README.rst
    github_url: https://github.com/DigitalSlideArchive/HistomicsUI
    screenshot: assets/img/histomicsui_screenshot.png
    features:
      - name: Quản lý dữ liệu an toàn
        description: DSA cung cấp quyền truy cập chi tiết dựa trên người dùng hoặc vai trò vào bộ dữ liệu, hình ảnh & siêu dữ liệu và chú thích. Hỗ trợ lưu trữ Amazon S3.
        icon: assets/img/feature-icons/icon-secure_data_management.svg

      - name: API RESTful 
        description: Một API phong phú cho phép kiểm soát theo chương trình đối với người dùng, dữ liệu, chú thích và thuật toán, cho phép tự động hóa các tác vụ DSA và tích hợp với các công cụ và nền tảng khác.
        icon: assets/img/feature-icons/icon-restful_apis.svg

      - name: Trực quan hóa và Chú thích 
        description: Giao diện người dùng được tối ưu hóa cung cấp khả năng khám phá linh hoạt các hình ảnh toàn phiến lớn và các công cụ để tạo chú thích hình ảnh hiệu quả.
        icon: assets/img/feature-icons/icon-visualization_annotation.svg

      - name: Công cụ Thực thi 
        description: Girder cung cấp khả năng thực thi và giám sát phân tán các công việc thuật toán và phân tích.
        icon: assets/img/feature-icons/icon-execution_engine.svg

      - name: Hỗ trợ Rộng rãi cho các Định dạng Hình ảnh Mô học 
        description: Một loạt các định dạng hình ảnh được lát gạch được hỗ trợ, bao gồm tiff, svs và jp2. Hình ảnh có thể được lát lại tự động khi cần thiết cho các thuật toán xử lý. Các định dạng bổ sung có thể được thêm vào với giao diện Python có thể cắm được. 
        icon: assets/img/feature-icons/icon-history_image_formats-primary.svg

  # HistomicsTK
  - title: HistomicsTK 
    description: HistomicsTK là một bộ công cụ xử lý hình ảnh Python để phân tích định lượng hình ảnh bệnh lý kỹ thuật số toàn phiến.
    docs_url: https://digitalslidearchive.github.io/HistomicsTK/
    github_url: https://github.com/DigitalSlideArchive/HistomicsTK
    screenshot: assets/img/histomicstk_screenshot.png
    features:
      - name: Tiền xử lý 
        description: HistomicsTK cung cấp các hoạt động chuẩn hóa màu sắc và khử tích chập để cải thiện độ mạnh mẽ của các quy trình phân tích.
        icon: assets/img/feature-icons/icon-preprocessing.svg

      - name: Phát hiện và Phân đoạn Đối tượng 
        description: HistomicsTK chứa một số thuật toán phân tích hình ảnh cổ điển và dựa trên máy học để phát hiện đối tượng và phân đoạn các cấu trúc và mô dưới tế bào.
        icon: assets/img/feature-icons/icon-object_detection.svg

      - name: Trích xuất Đặc trưng và Mô hình Dự đoán
        description: Các đặc trưng cấp độ đối tượng và miếng vá mô tả hình dạng, kết cấu và màu sắc có thể được sử dụng để xây dựng các mô hình học máy.
        icon: assets/img/feature-icons/icon-feature_extraction.svg

      - name: Khả năng mở rộng 
        description: Người dùng có thể tích hợp các thuật toán tùy chỉnh của họ thông qua quy trình container hóa tự động tạo giao diện người dùng DSA.
        icon: assets/img/feature-icons/icon-extensibility.svg

      - name: Hỗ trợ Rộng rãi cho các Định dạng Hình ảnh Mô học 
        description: Cùng một loạt các hình ảnh mô học có thể được xem có thể được sử dụng với bất kỳ thuật toán xử lý nào. Hình ảnh con có thể được xử lý ở kích thước ô và độ phóng đại tùy chỉnh khi cần thiết. 
        icon: assets/img/feature-icons/icon-history_image_formats-secondary.svg 

# Phần Callouts
# =================================
callouts:
  - heading: Tài liệu
    link: documentation/
    link_text: Trường hợp sử dụng & Ví dụ
    image: assets/img/home-callouts/demos_examples.jpg

  - heading: Câu chuyện thành công
    link: success-stories/
    link_text: Xem câu chuyện
    image: assets/img/home-callouts/success_stories.jpg

  - heading: Bài báo & Ấn phẩm
    link: papers-publications/
    link_text: Đọc bài báo
    image: assets/img/home-callouts/papers_publications.jpg

# Collaborators Section
# ================================= 
organizations:
  - name: Feinberg School of Medicine - Northwestern University
    logo: assets/img/collaborators/logo-feinberg_school_of_medicine.png
    link: https://www.feinberg.northwestern.edu/ 
    members:
      - name: Lee A.D. Cooper, PhD 
        role: Trưởng nhóm HistomicsTK 
        title: Phó Giáo sư Bệnh lý học 
        headshot: assets/img/collaborators/headshot-lee_cooper.jpg
        link: https://www.feinberg.northwestern.edu/faculty-profiles/az/profile.html?xid=44206 

  - name: Emory University - School of Medicine
    logo: assets/img/collaborators/logo-emory_school_of_medicine.png
    link: https://www.med.emory.edu/ 
    members:
      - name: David A. Gutman, MD, PhD 
        role: Trưởng nhóm Digital Slide Archive
        title: Phó Giáo sư Thần kinh học 
        headshot: assets/img/collaborators/headshot-david_gutman.jpg
        link: https://winshipcancer.emory.edu/bios/faculty/gutman-david.html 

  - name: Kitware, Inc.
    logo: assets/img/collaborators/logo-kitware.png
    link: https://www.kitware.com/ 
    members:
      - name: David Manthey
        role: Kỹ thuật Phần mềm & Triển khai
        title: Kỹ sư R&D 
        headshot: assets/img/collaborators/headshot-david_manthey.jpg
        link: https://www.kitware.com/david-manthey/
---
