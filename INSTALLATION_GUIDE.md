# Cài đặt APK kiểm thử — Pixel Meteor Dash BUILD-002

## A. Build APK trên GitHub bằng điện thoại
1. Tạo một repository **Private** trên GitHub.
2. Upload toàn bộ nội dung trong gói `pmd_build002` vào thư mục gốc repository (giữ nguyên `.github/workflows/android-debug.yml`).
3. Mở tab **Actions** → workflow **Android Debug APK** → **Run workflow**.
4. Chờ job kết thúc. Chỉ tiếp tục khi trạng thái workflow là **Success**.
5. Mở lần chạy thành công → phần **Artifacts** → tải `pixel-meteor-dash-webview-test`.
6. Giải nén file ZIP artifact để lấy `app-debug.apk`.

## B. Cài APK trên Android
1. Chuyển `app-debug.apk` sang điện thoại Android.
2. Mở file bằng ứng dụng Files hoặc trình quản lý tệp.
3. Nếu Android hỏi, cho phép cài ứng dụng từ nguồn này đối với ứng dụng quản lý tệp đang dùng.
4. Chọn **Install**.
5. Mở **Pixel Meteor Dash (Debug)**.

## C. Lưu ý kiểm thử
- Đây là APK debug, không phải bản phát hành Google Play.
- Gỡ bản debug cũ trước nếu cài từ package debug khác.
- Kiểm tra Start, trái/phải, giữ nút, Pause/Resume, va chạm, Game Over, Replay và kỷ lục.
- Kiểm tra Logcat với tag `PMD-WebView` để xem JavaScript console errors.
- Không có thiết bị Android trong môi trường build hiện tại; cài đặt và runtime vẫn cần Agent 10 xác nhận.
