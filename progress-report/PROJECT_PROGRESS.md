# BÁO CÁO TIẾN ĐỘ DỰ ÁN LALACOFFEE

**Đề tài:** Xây dựng website bán cà phê và nước giải khát LalaCoffee  
**Học phần:** Chuyên đề ASP.NET  
**Sinh viên thực hiện:** Lê Bình Phương Thao  
**Giảng viên hướng dẫn:** TS. Nguyễn Nhất Lam  
**Mã nguồn:** `src/`  
**Repository GitHub:** `https://github.com/thaolbp160688/ASPNET-DK25TTC5-LEBINHPHUONGTHAO-COFFEE`  
**Ngày cập nhật báo cáo:** `28/11/2026`  

## 1. Tổng quan dự án

LalaCoffee là website bán cà phê và nước giải khát xây dựng trên **ASP.NET MVC 5, .NET Framework 4.8, C#, Entity Framework 6 và SQL Server**. Website phục vụ hai nhóm người dùng chính:

- **Khách hàng:** xem trang chủ, danh mục và thông tin sản phẩm; lựa chọn kích cỡ/topping; quản lý giỏ hàng; đặt hàng thanh toán khi nhận hàng (COD); tra cứu trạng thái đơn; đăng ký, đăng nhập và cập nhật hồ sơ.
- **Quản trị viên:** quản lý danh mục, sản phẩm, thuộc tính, tùy chọn, bài viết, đơn hàng, người dùng và phân quyền.

Về tổ chức kỹ thuật, dự án sử dụng mô hình **MVC**, **Repository / Unit of Work**, **Dependency Injection với Unity**, các dịch vụ xử lý giỏ hàng, đặt hàng và email. Giao diện được xây dựng bằng **Razor, HTML, CSS, JavaScript** và các thư viện hỗ trợ.

## 2. Mục tiêu quản lý tiến độ trên GitHub

1. Tổ chức repository có cấu trúc rõ ràng, đặt source và solution trong `src/`.
2. Đưa các thành phần mã nguồn đã hoàn thành lên GitHub.
3. Ghi nhận tiến độ từng đợt bằng lịch sử commit thực tế.
4. Lưu tài liệu tiến độ trong thư mục **`progress-report/`**; lưu báo cáo, slide và tài liệu nộp trong **`thesis/`**.
5. Cung cấp README và hướng dẫn cài đặt để giảng viên có thể đọc cấu trúc và triển khai dự án.

**Phạm vi:** Báo cáo này tập trung vào phân bổ mã nguồn, tài liệu và lịch sử cập nhật repository.

## 3. Nhật ký tiến độ 10 đợt

| Đợt | Ngày dự kiến | Nội dung mã nguồn/tài liệu đưa lên | Vị trí chính trong repository | Commit message | Trạng thái |
|---|---|---|---|---|---|
| **01** | 15/11/2026 | Khởi tạo cấu trúc thư mục, `.gitignore`, README khởi tạo và các `.gitkeep`. | `src/`, `progress-report/`, `setup/`, `thesis/`, `README.md` | `chore: scaffold LalaCoffee repository structure` | `Đã xong` |
| **02** | 16/11/2026 | Bổ sung solution, project ASP.NET MVC 5, cấu hình định tuyến, bundle, Unity DI, logging và package manifest. | `src/LalaCoffee.sln`, `src/LalaCoffee/App_Start/`, `src/LalaCoffee/Web.config`, `src/LalaCoffee/packages.config` | `chore: add ASP.NET MVC project configuration` | `Đã xong` |
| **03** | 17/11/2026 | Bổ sung script cơ sở dữ liệu, Entity Framework, các model và Repository / Unit of Work. | `src/Database_Deploy.sql`, `src/LalaCoffee/Data/`, `src/LalaCoffee/Models/` | `feat: add database schema and entity models` | `Đã xong` |
| **04** | 18/11/2026 | Bổ sung các dịch vụ và tiện ích nghiệp vụ: giỏ hàng, đơn hàng, tính tiền, email và xử lý hình ảnh. | `src/LalaCoffee/Services/`, `src/LalaCoffee/Helpers/` | `feat: add business services and shared utilities` | `Đã xong` |
| **05** | 19/11/2026 | Bổ sung trang chủ, danh mục, bài viết, layout người dùng, CSS/JS và hình ảnh giao diện. | `src/LalaCoffee/Controllers/`, `src/LalaCoffee/Views/`, `src/LalaCoffee/Content/`, `src/LalaCoffee/Scripts/` | `feat: add storefront layout and catalog pages` | `Đã xong` |
| **06** | 20/11/2026 | Bổ sung trang chi tiết sản phẩm, lựa chọn cấu hình món, giao diện và xử lý giỏ hàng. | `src/LalaCoffee/Controllers/ProductController.cs`, `CartController.cs`, `src/LalaCoffee/Views/Product/`, `Views/Cart/` | `feat: add product configuration and shopping cart` | `Đã xong` |
| **07** | 21/11/2026 | Bổ sung đặt hàng COD, xác nhận và tra cứu đơn; thêm báo cáo tiến độ tuần 1. | `src/LalaCoffee/Controllers/OrderController.cs`, `src/LalaCoffee/Views/Order/`, `progress-report/week-01.md` | `feat: add COD checkout and order tracking` | `Đã xong` |
| **08** | 22/11/2026 | Bổ sung đăng ký, đăng nhập, quản lý tài khoản và hồ sơ người dùng. | `src/LalaCoffee/Controllers/AccountController.cs`, `src/LalaCoffee/Data/ApplicationUserManager.cs`, `src/LalaCoffee/Views/Account/` | `feat: add account and profile management` | `Đã xong` |
| **09** | 23/11/2026 | Bổ sung khu vực quản trị danh mục, sản phẩm, topping, thuộc tính, bài viết và tài nguyên giao diện admin. | `src/LalaCoffee/Areas/Admin/`, `src/LalaCoffee/Content/Layout/Admin/` | `feat: add admin product and content management` | `Đã xong` |
| **10** | 24/11/2026 | Bổ sung quản trị đơn hàng, người dùng, phân quyền; hoàn thiện README, hướng dẫn triển khai và báo cáo tuần 2. | `src/LalaCoffee/Areas/Admin/Controllers/`, `Areas/Admin/Views/`, `README.md`, `setup/README.md`, `progress-report/week-02.md` | `feat: complete admin orders and project documentation` | `Đã xong` |

## 4. Kết quả của sản phẩm đã xây dựng

Các nhóm chức năng trong mã nguồn LalaCoffee và báo cáo đồ án hiện có gồm:

| Nhóm | Nội dung |
|---|---|
| Giao diện khách hàng | Trang chủ, danh mục, sản phẩm, chi tiết món, bài viết |
| Cấu hình sản phẩm | Chọn thuộc tính/kích cỡ và các tùy chọn thêm (topping) |
| Giỏ hàng | Quản lý món đã chọn, số lượng và thành tiền |
| Đặt hàng | Thanh toán khi nhận hàng (COD), tạo đơn hàng và mã tra cứu |
| Tài khoản | Đăng ký, đăng nhập, thông tin cá nhân và phân quyền |
| Quản trị | Quản lý danh mục, sản phẩm, thuộc tính, tùy chọn, bài viết, đơn hàng, tài khoản và vai trò |
| Dữ liệu & kiến trúc | SQL Server, Entity Framework 6, MVC, Repository / Unit of Work, Unity DI |

---

**Người cập nhật:** Lê Bình Phương Thao
