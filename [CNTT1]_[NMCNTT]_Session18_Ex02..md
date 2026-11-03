## Phần 1. Phân tích

### 1. So sánh Cache và Cookies

| Tiêu chí | Cache | Cookies |
|---|---|---|
| Dung lượng | MB đến GB | Khoảng 4KB |
| Công dụng | Lưu hình ảnh, CSS, JavaScript. | Lưu thông tin đăng nhập. |
| Mục đích | Giúp tải trang nhanh hơn. | Ghi nhớ phiên làm việc. |
    

## Phần 2. Triển khai

###  Cấu trúc Cookie

Cookie được tạo từ các thành phần gồm tên Cookie, giá trị và các thuộc tính đi kèm để quy định thời gian lưu trữ và bảo mật.


| Thuộc tính | Chức năng |
|---|---|
| `session_token` | Mã phiên đăng nhập của shipper. |
| `Max-Age=604800` | Lưu Cookie trong 7 ngày. |
| `HttpOnly` | Không cho JavaScript truy cập Cookie. |
| `Secure` | Chỉ gửi Cookie qua HTTPS. |
| `SameSite=Lax` | Hạn chế gửi Cookie từ website khác. |

## Phần 3. Kiểm thử

### Thao tác Hard Reload:

1.  Mở website cần kiểm tra.
    
2.  Nhấn `F12` để mở Developer Tools.
    
3.  Nhấn chuột phải vào nút Reload.
    
4.  Chọn Empty Cache and Hard Reload.
    
5.  Kiểm tra lại giao diện.
