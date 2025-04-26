# Trang đích GitHub Pages
Trang web này sử dụng [Giao diện Bulma Clean](https://github.com/chrisrhymes/bulma-clean-theme) cho Jekyll.

### Chạy trang web cục bộ
1. Mở terminal và clone repo [digital_slide_archive](https://github.com/DigitalSlideArchive/digital_slide_archive)
2. Điều hướng đến thư mục docs – `cd docs`
3. Chạy lệnh `bundle exec jekyll serve`
    * Bạn có thể cần chạy `bundle install && bundle update` nếu bước này thất bại. Sau khi hoàn thành, hãy lặp lại bước 3.

**LƯU Ý:** Bạn sẽ thấy `Invalid theme folder: _sass` khi chạy trang web. Điều này liên quan đến việc sử dụng Giao diện Bulma Clean dưới dạng `remote_theme` trong `config.yml`. `remote_theme: chrisrhymes/bulma-clean-theme` được sử dụng thay vì `theme: bulma-clean-theme` để giao diện hoạt động tốt với các trang GitHub. Vì vậy, hãy bỏ qua cảnh báo thư mục giao diện không hợp lệ.
