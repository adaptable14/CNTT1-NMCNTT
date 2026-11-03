# Phần 1. Phân tích
- Input : phong-dieu-phoi.grenlog .vn 
- Output:  DNS_PROBE_FINISHED_NXDOMAIN
-  Sơ đồ DNS :
Nhập tên miền
↓
Kiểm tra DNS Cache
↓
DNS Resolver
↓
Root DNS Server
↓
TLD DNS Server
↓
Authoritative DNS Server
↓
Trả về địa chỉ IP
↓
Trình duyệt kết nối máy chủ
# Phần 2. Triển khai 

 thực hiện các bước sau:

1.  Mở trình duyệt và nhập đúng địa chỉ website.
2.  Nhấn `F12` để mở Developer Tools.
3.  Chọn tab Network.
4.  Kiểm tra cột Status để xem mã trạng thái HTTP

# Phần 3. Kiểm thử
Giả định Nam sửa đúng tên miền nhưng vẫn nhận mã `404 Not Found` thì hệ thống gặp vấn đề là 

Vấn đề hệ thống: Máy chủ không tìm thấy trang hoặc tài nguyên mà Nam yêu cầu. Có thể trang quản trị chưa tồn tại, đã bị xóa hoặc đường dẫn trên máy chủ bị sai.


