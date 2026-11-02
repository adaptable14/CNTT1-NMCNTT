

# Phần 1: Báo cáo phân tích kiến trúc đa Profile

### 1. Nguyên nhân xảy ra Session Conflict là :

Khi nhiều người dùng chung một Profile Chrome, các tài khoản sử dụng chung Cookies và dữ liệu đăng nhập trong thư mục User Data. Khi người này đăng nhập tài khoản khác, phiên đăng nhập trước có thể bị thay đổi hoặc đăng xuất.

### 2.  3 mô hình Profile chuyên dụng là :

| Profile | Mục đích sử dụng | Màu Theme | Dữ liệu lưu trữ |
|---|---|---|---|
| Work | Bác sĩ sử dụng CarePulse và tra cứu bệnh án. | Xanh dương | Cookies, History, Bookmarks, Extensions riêng. |
| Personal | Nhân viên sử dụng tài khoản cá nhân. | Xanh lá | Cookies, History, Bookmarks, Extensions riêng. |
| Sandbox/Test | Bác sĩ thực tập học tập và kiểm tra. | Cam | Cookies, History, Bookmarks, Extensions riêng. |

## Phần 2: Thiết kế hệ thống Bookmark và quy trình an toàn

### 3. Cây thư mục Bookmark :



```
📁 Bookmarks Bar
├── 📁 01_CarePulse_Clinic
│   ├── CarePulse
│   ├── Cổng BHYT
│   └── Hồ sơ bệnh nhân
│
├── 📁 02_Pharma_Portal
│   ├── Dược thư Quốc gia
│   ├── Cục Quản lý Dược
│   └── Tra cứu thuốc
│
└── 📁 03_Medical_Tools
    ├── Google Dịch
    ├── Google Scholar
    └── PubMed
```

### 4. Hướng dẫn áp dụng mẹo Favicon-Only cho 4 trang web dùng hàng ngày là 

Thực hiện trên 4 trang web: CarePulse, Cổng BHYT, Dược thư và Google Dịch.

Các bước thực hiện là :

1.  Mở trang web cần thêm vào thanh dấu trang.
    
2.  Nhấn `Ctrl + D` để lưu trang vào thanh dấu trang.
    
3.  Nhấn chuột phải vào dấu trang vừa lưu, chọn Edit (Chỉnh sửa).
    
4.  Xóa nội dung trong ô Name (Tên), giữ nguyên địa chỉ URL.
    
5.  Nhấn Save (Lưu). 

 6. Thực hiện tương tự với 3 trang web còn lại.

### 5. Xử lý Bẫy an ninh :

Chế độ lựa chọn: Guest Profile (Hồ sơ khách).

- Lý do: Guest Profile tạo phiên duyệt web riêng, không sử dụng dữ liệu của Profile nhân viên. Khi đóng cửa sổ Guest, lịch sử và dữ liệu duyệt web của khách sẽ được xóa. Incognito không tạo Profile riêng nên không phù hợp bằng Guest Profile trong trường hợp này.

- Cảnh báo Cloud Sync: Không bật Cloud Sync tài khoản Google cá nhân trên máy tính phòng khám vì có thể đồng bộ mật khẩu, lịch sử duyệt web và Bookmark, gây nguy cơ lộ thông tin cá nhân khi nhiều người dùng chung máy tính.
