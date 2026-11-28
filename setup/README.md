# Hướng dẫn cài đặt LalaCoffee

1. Mở `src/LalaCoffee.sln` bằng Visual Studio 2019/2022 với .NET Framework 4.8 Developer Pack.
2. Từ Visual Studio chọn **Restore NuGet Packages**.
3. Trong SQL Server Management Studio, chạy `setup/Database_Deploy.sql` để tạo database mẫu.
4. Sửa chuỗi kết nối `DefaultConnection` trong `src/LalaCoffee/Web.config` theo instance SQL Server của máy.
5. Nếu cần gửi email, cấu hình các khóa SMTP trong `src/LalaCoffee/Web.config`.
6. Chạy project bằng IIS Express.
7. Thay đổi tài khoản và mật khẩu demo trong database trước khi triển khai thực tế.