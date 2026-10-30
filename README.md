# Thủy lực mương – gói tạo ứng dụng Android (APK)

Gói này chứa dự án Android bọc ứng dụng tính thủy lực mương. GitHub sẽ tự biên dịch ra file APK miễn phí, bạn không cần cài Android Studio.

## Tạo file APK
1. Đăng nhập github.com (tạo tài khoản miễn phí nếu chưa có), tạo một repository mới, đặt tên tùy ý.
2. Giải nén gói này, rồi tải TOÀN BỘ nội dung lên repository: bấm "Add file", chọn "Upload files", kéo cả các thư mục `app`, `.github` và các file `build.gradle`, `settings.gradle`, `gradle.properties` vào, bấm "Commit changes". Thư mục `.github` là bắt buộc. Nếu máy ẩn thư mục bắt đầu bằng dấu chấm, hãy bật hiển thị file ẩn.
3. Vào tab "Actions". Chọn "Build APK", bấm "Run workflow". Đợi khoảng 3–6 phút đến khi có dấu xanh.
4. Mở lần chạy đó, kéo xuống mục "Artifacts", tải `ThuyLucMuong-apk` về, giải nén ra `app-debug.apk`.

## Cài lên điện thoại Android
1. Chép `app-debug.apk` sang điện thoại (Zalo, email, cáp USB, Google Drive).
2. Mở file bằng ứng dụng Files. Khi được hỏi, cho phép "Cài đặt ứng dụng từ nguồn này".
3. Nếu Google Play Protect cảnh báo ứng dụng chưa được xác minh, chọn "Vẫn cài đặt".
4. Biểu tượng "Thủy lực mương" xuất hiện trong danh sách ứng dụng.

## Ghi chú
- Toàn bộ phần tính nằm trong `app/src/main/assets/index.html`, chạy hoàn toàn trên máy. Phông chữ lấy từ Google Fonts khi có mạng; mất mạng thì dùng phông hệ thống, kết quả tính không đổi.
- Dữ liệu nhập lưu trong ứng dụng trên từng máy. Chuyển máy: tab "Bảng tuyến" → "Nhập / xuất dữ liệu" → "Xuất toàn bộ dữ liệu (JSON)".
- APK này ký bằng khóa debug, phù hợp dùng nội bộ. Muốn đưa lên Google Play cần ký bằng khóa riêng.
- Sửa ứng dụng: thay file `index.html` trong `app/src/main/assets/`, commit lại, chạy lại workflow.
