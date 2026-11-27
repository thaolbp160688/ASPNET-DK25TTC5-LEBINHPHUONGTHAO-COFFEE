# Hướng dẫn cài đặt LalaCoffee

1. Mở `src/LalaCoffee.sln` bằng Visual Studio 2019/2022 với .NET Framework 4.8 Developer Pack.
2. Từ Visual Studio chọn **Restore NuGet Packages**, vì thư mục `packages/` không được đưa lên Git.
3. Trong SQL Server Management Studio, chạy `src/Database_Deploy.sql` để tạo database mẫu.
4. Sửa chuỗi kết nối `DefaultConnection` trong `src/LalaCoffee/Web.config` theo instance SQL Server của máy.
5. Nếu cần gửi email, cấu hình các khóa SMTP trong `src/LalaCoffee/Web.config` bằng tài khoản của chính bạn; mật khẩu không được commit.
6. Chạy project bằng IIS Express.
7. Thay đổi tài khoản và mật khẩu demo trong database trước khi triển khai thực tế.

**Tài nguyên lưu ý:** Gói này không phân phối lại các tệp font; có thể dùng nguồn font hợp pháp/ứng dụng quản lý thư viện phù hợp với license để khôi phục khi cần. Các tài liệu đồ án Word/PDF/PPT/video sẽ được tác giả bổ sung riêng vào `thesis/`.

**Vị trí project:** Không di chuyển riêng file `.sln` ra ngoài `src/`. Khi Restore NuGet, các gói sẽ được tải vào thư mục `src/packages/` (đã ignore trong Git).
