

# PHẦN 1 – NHẬN DIỆN RỦI RO VÀ XỬ LÝ SỰ CỐ

### 1. Tình huống 1: Typosquatting.
    
-   Dấu hiệu giả mạo: Đường link `githuh-security.com` gần giống tên miền chính thức `github.com` nhưng đã thay đổi chữ `b` thành `h`.
    
-   Mục đích: Dụ người dùng truy cập trang web giả để đánh cắp mật khẩu GitHub.
    

### 2. Tình huống 2: mã độc crack

    
-   Phần mềm crack có thể chứa virus, Trojan hoặc Infostealer. Việc yêu cầu tắt Windows Defender là dấu hiệu nguy hiểm vì sẽ làm giảm khả năng phát hiện và ngăn chặn mã độc.
    

### 3. Quy tắc 5 KHÔNG:

- Tình huống 1:

Không bấm vào link lạ, không nhập mật khẩu vào trang web không rõ nguồn gốc.

- Tình huống 2:

Không tải và chạy phần mềm crack, không tắt Windows Defender.

### 4. Quy trình Cấp cứu 4 Bước:

-  Ngắt kết nối mạng: Tắt Wi-Fi, rút dây mạng để ngăn mã độc kết nối ra bên ngoài.
    
-   Cô lập thiết bị: Ngừng sử dụng máy bị nhiễm và báo cho người phụ trách IT để kiểm tra.
    
-  Bảo vệ tài khoản: Dùng thiết bị sạch để đổi mật khẩu, thu hồi các phiên đăng nhập đáng ngờ.
    
-  Khôi phục hệ thống: Quét và xử lý mã độc, cài đặt lại hệ điều hành nếu cần, khôi phục dữ liệu từ bản sao lưu sạch.
    

# PHẦN 2 – CHUYỂN SANG PASSWORD MANAGER

### 1. Rủi ro khi sử dụng chung mật khẩu:

Nếu email nhóm bị lộ mật khẩu, hacker có thể dùng mật khẩu đó để đăng nhập vào GitHub và Vercel.

-   Tên kiểu tấn công: Credential Stuffing (tấn công nhồi nhét thông tin đăng nhập).
    
-   Hậu quả: Hacker có thể chiếm quyền truy cập mã nguồn và hệ thống triển khai dự án.
    

### 2. Zero-Knowledge Architecture:

Dữ liệu được mã hóa ngay trên thiết bị người dùng trước khi lưu lên máy chủ Bitwarden. Vì vậy, máy chủ chỉ lưu dữ liệu đã mã hóa và không thể đọc được mật khẩu nếu không có khóa giải mã của người dùng.

### 3. Cấu hình Generator tạo mật khẩu:

| Thông số | Giá trị cấu hình |
|---|---|
| Độ dài | 24 ký tự |
| Chữ hoa (A–Z) | Bật |
| Chữ thường (a–z) | Bật |
| Chữ số (0–9) | Bật |
| Ký tự đặc biệt | Bật |
| Mật khẩu mỗi tài khoản | Khác nhau, không dùng chung |


# PHẦN 3 – KÍCH HOẠT 2FA CHO TÀI KHOẢN GITHUB TỔ CHỨC

### 1.  nên dùng Authenticator App thay SMS OTP vì
+) vì Authenticator App có thể :
-   Tạo mã OTP thay đổi sau mỗi khoảng 30 giây.
    
-   Xác minh người đăng nhập có thiết bị đã đăng ký.
    
-   Ngăn người khác đăng nhập trái phép dù biết mật khẩu.
    
-   Tăng thêm một lớp bảo mật cho tài khoản GitHub, Google, Facebook...
+) còn SMS OTP thì lại có nhược điểm là :

-   SIM Swapping: Hacker có thể chiếm quyền sử dụng SIM để nhận mã OTP.
    
-   SMS Interception: Tin nhắn OTP có thể bị chặn hoặc đánh cắp.
    

### 2. Các bước kích hoạt 2FA bằng Google Authenticator:

1.  Đăng nhập tài khoản cần tạo OTP
    
2.  Chọn Settings.
    
3.  Chọn Password and authentication.
   
5.  Chọn Authenticator app.
    
6.  Mở Google Authenticator trên điện thoại.
    
7.  Quét mã QR hiển thị trên ứng dụng cần tạo OTP
    
8.  Nhập mã OTP gồm 6 chữ số để xác nhận.
    

### 3. Nơi lưu trữ 10 mã khôi phục:

| Nên lưu | Không nên lưu |
|---|---|
| Password Manager | Nhóm chat |
| Bản in giấy cất ở nơi an toàn | Ảnh trong thư viện điện thoại |
| USB được mã hóa | File văn bản không có mật khẩu bảo vệ |

## PHẦN 4 – BẢO VỆ SECRETS TRƯỚC KHI PUSH CODE

### 1. Hai giá trị Secrets đang bị hardcode là :

-   `API_KEY = "sk-proj-abc123456789"`
    
-   `DB_PASSWORD = "SmartCampus@2026"`
    

2. Code sau khi sửa trong file `config.js`:

```
const API_KEY = process.env.API_KEY;
const DB_PASSWORD = process.env.DB_PASSWORD;

function connectDatabase() {
  return connect(DB_PASSWORD);
}
```

3. Nội dung các file:

File `.env` (chứa giá trị thật):

```
API_KEY=YOUR_REAL_API_KEY
DB_PASSWORD=YOUR_REAL_DB_PASSWORD
```

File `.gitignore`:

```
.env
.env.*
!.env.example
node_modules/
*.log
```

File `.env.example` 

```
API_KEY=
DB_PASSWORD=
```

### 4. Quy tắc 4 Bước Kiểm tra trước khi Push:

1.  Kiểm tra code: Tìm API Key, mật khẩu và các Secret bị viết trực tiếp trong mã nguồn.
    
2.  Kiểm tra `.gitignore`: Đảm bảo file `.env` đã được thêm vào danh sách bỏ qua.
    
3.  Kiểm tra `.env.example`: Đảm bảo file chỉ có tên biến, không chứa giá trị Secret thật.
    
4.  Kiểm tra Git: Sử dụng `git status` và `git diff --cached` để kiểm tra các file chuẩn bị push, đảm bảo không có Secret.
    


