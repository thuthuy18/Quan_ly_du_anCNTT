
# 📚 WEBSITE QUẢN LÝ THƯ VIỆN

## 1. Giới thiệu dự án

Website quản lý thư viện được xây dựng nhằm hỗ trợ quản lý các hoạt động của thư viện như quản lý sách, nhân viên, độc giả, mượn trả sách và xử lý vi phạm.

Hệ thống giúp tối ưu quy trình quản lý, giảm thao tác thủ công, lưu trữ dữ liệu tập trung và hỗ trợ nhân viên thư viện theo dõi tình trạng hoạt động một cách thuận tiện.

Dự án được xây dựng bằng PHP theo mô hình MVC thuần, sử dụng MySQL làm hệ quản trị cơ sở dữ liệu.

---

## 2. Mục tiêu dự án

- Xây dựng website quản lý thư viện với giao diện dễ sử dụng.
- Quản lý thông tin sách và số lượng sách tồn.
- Quản lý thông tin nhân viên và độc giả.
- Quản lý quá trình mượn và trả sách.
- Theo dõi tình trạng phiếu mượn.
- Quản lý biên bản vi phạm và tiền phạt.
- Áp dụng mô hình MVC trong xây dựng ứng dụng PHP.

---

## 3. Chức năng chính

### 📖 Quản lý sách
- Xem danh sách sách.
- Thêm sách mới.
- Chỉnh sửa thông tin sách.
- Xóa sách.
- Quản lý số lượng sách tồn.

### 👨‍💼 Quản lý nhân viên
- Xem danh sách nhân viên.
- Thêm nhân viên.
- Chỉnh sửa thông tin nhân viên.
- Xóa nhân viên.

### 👥 Quản lý độc giả
- Quản lý thông tin độc giả.
- Thêm độc giả mới.
- Cập nhật thông tin độc giả.
- Xóa độc giả.

### 🔄 Quản lý mượn – trả sách
- Lập phiếu mượn sách.
- Theo dõi ngày mượn và hạn trả.
- Cập nhật trạng thái mượn.
- Xử lý trả sách.
- Theo dõi số lượng sách mượn.

### ⚠️ Quản lý vi phạm
- Lập biên bản vi phạm.
- Ghi nhận loại vi phạm.
- Nhập mô tả vi phạm.
- Tính hoặc nhập tiền phạt.
- Theo dõi trạng thái xử lý vi phạm.

---

## 4. Công nghệ sử dụng

| Công nghệ | Mục đích |
|---|---|
| PHP | Xử lý logic phía máy chủ |
| PHP MVC thuần | Tổ chức mã nguồn theo mô hình MVC |
| MySQL | Lưu trữ dữ liệu |
| HTML5 | Xây dựng cấu trúc giao diện |
| CSS3 | Thiết kế giao diện |
| Bootstrap 5 | Hỗ trợ giao diện responsive |
| JavaScript | Xử lý tương tác trên giao diện |
| XAMPP | Môi trường chạy Apache và MySQL |
| phpMyAdmin | Quản lý cơ sở dữ liệu |

---

## 5. Cấu trúc thư mục

```text
PHPMVCDemo/
│
├── app/
│   ├── controllers/
│   │   ├── BookController.php
│   │   ├── EmployeeController.php
│   │   ├── BookLoanController.php
│   │   ├── ViolationController.php
│   │   └── HomeController.php
│   │
│   ├── models/
│   │   ├── Book.php
│   │   ├── NhanVien.php
│   │   ├── BookLoan.php
│   │   └── BienBanViPham.php
│   │
│   ├── services/
│   │   ├── BookService.php
│   │   ├── EmployeeService.php
│   │   ├── BookLoanService.php
│   │   └── ViolationService.php
│   │
│   └── views/
│       ├── books/
│       ├── employees/
│       ├── loans/
│       ├── violations/
│       └── layouts/
│
├── config/
│   └── database.php
│
├── public/
│   ├── index.php
│   └── assets/
│       ├── css/
│       ├── js/
│       └── images/
│
└── README.md
```

---

## 6. Cài đặt và chạy dự án

### Bước 1: Cài đặt XAMPP

Tải và cài đặt XAMPP:

https://www.apachefriends.org/

Khởi động hai dịch vụ:
- Apache
- MySQL

### Bước 2: Clone repository

```bash
git clone https://github.com/USERNAME/REPOSITORY.git
```

Hoặc tải source code về máy và giải nén vào thư mục:

```text
C:\xampp\htdocs\
```

### Bước 3: Tạo cơ sở dữ liệu

1. Truy cập phpMyAdmin:

```text
http://localhost/phpmyadmin
```

2. Tạo database mới cho dự án.
3. Import file SQL của dự án (nếu có).

### Bước 4: Cấu hình kết nối database

Mở file cấu hình kết nối MySQL và thiết lập:

- Host: `localhost`
- Username: `root`
- Password: (mặc định XAMPP thường để trống)
- Database: tên database đã tạo

### Bước 5: Chạy website

Truy cập đường dẫn:

```text
http://localhost/PHPMVCDemo/public/
```

---

## 7. Quy trình sử dụng

1. Truy cập website quản lý thư viện.
2. Thực hiện quản lý sách, nhân viên và độc giả.
3. Lập phiếu mượn sách cho độc giả.
4. Theo dõi các phiếu mượn đang xử lý.
5. Cập nhật thông tin trả sách.
6. Lập biên bản nếu phát sinh vi phạm.
7. Kiểm tra và quản lý tiền phạt.

---

## 8. Mô hình MVC

Dự án sử dụng mô hình MVC (Model – View – Controller):

- **Model:** Quản lý dữ liệu và các đối tượng nghiệp vụ.
- **View:** Hiển thị giao diện cho người dùng.
- **Controller:** Tiếp nhận yêu cầu, xử lý luồng hoạt động và kết nối Model với View.

Mô hình MVC giúp phân chia rõ ràng các thành phần trong chương trình, dễ bảo trì, nâng cấp và phát triển thêm chức năng.

---

## 9. Thành viên thực hiện

| Thành viên | Công việc |
|---|---|
| Ngân | Xem chi tiết |
| Sơn | Chỉnh sửa thông tin |
| Hòa | Thêm dữ liệu |
| Thủy | Chức năng xóa và cơ sở dữ liệu |
| Hùng | Thiết kế giao diện |

---

## 10. Định hướng phát triển

- Bổ sung đăng nhập và phân quyền người dùng.
- Thống kê số lượng sách mượn và trả.
- Tìm kiếm sách và độc giả.
- Cải thiện giao diện responsive.
- Nâng cao tính bảo mật và kiểm tra dữ liệu đầu vào.

---

© 2026 - Website quản lý thư viện
