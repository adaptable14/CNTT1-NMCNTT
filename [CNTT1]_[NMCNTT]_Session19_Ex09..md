# PHẦN 1: BÁO CÁO PHÂN TÍCH KIẾN TRÚC AN NINH MẬT KHẨU

Câu 1.  Thói quen lưu mật khẩu trên trình duyệt Google Chrome (tệp `Login Data`) lại cực kỳ nguy hiểm đối với lập trình viên khi máy tính bị nhiễm mã độc Infostealer vì :
-  mã độc Infostealer có thể tìm và đánh cắp dữ liệu đăng nhập lưu trong tệp `Login Data` của Chrome. Hacker có thể lấy mật khẩu, Cookie và thông tin đăng nhập để chiếm quyền truy cập vào các tài khoản như GitHub, AWS và Steamworks.

Câu 2.  Zero-Knowledge và Client-side Decryption là :

-   Zero-Knowledge: Bitwarden không biết và không thể đọc mật khẩu của người dùng.
    
-   Client-side Decryption: Dữ liệu được giải mã ngay trên thiết bị của người dùng, không phải trên máy chủ.
    

# PHẦN 2: THIẾT KẾ CHÍNH SÁCH & KỊCH BẢN CHUYỂN ĐỔI

Câu 3.  Master Passphrase

-   Dài tối thiểu 20 ký tự.
    
-   Kết hợp nhiều từ không liên quan để dễ nhớ.
    
-   Có chữ hoa, chữ thường, số và ký tự đặc biệt.
    
-   Không sử dụng tên hoặc ngày sinh cá nhân.
 mật khẩu :GameThu@RongLua27!SaoBang
    
Câu 4. Bảng cấu hình Generator trong Bitwarden

| Tiêu chí | Cấu hình |
|---|---|
| Loại mật khẩu | Ngẫu nhiên |
| Độ dài | 20 ký tự |
| Chữ hoa | Bật |
| Chữ thường | Bật |
| Chữ số | Bật |
| Ký tự đặc biệt | Bật |
| Mật khẩu mỗi tài khoản | Khác nhau, không dùng chung |
Câu 5. Auto-fill của Bitwarden chống Phishing hiệu quả vì :

Bitwarden kiểm tra tên miền trang web trước khi tự động điền mật khẩu. Nếu tên miền không khớp với trang web đã lưu, Bitwarden sẽ không tự động điền. Nhờ đó, hạn chế việc bị đánh cắp mật khẩu qua các trang web giả mạo.

Câu 6. Quy trình lưu trữ Emergency Kit

1.  Tạo Emergency Kit chứa thông tin cần thiết để khôi phục tài khoản.
    
2.  In một bản giấy và cất ở nơi an toàn 
    
3.  Lưu một bản dự phòng ở nơi an toàn, có mã hóa.
    
4.  Chỉ Trưởng nhóm và người được ủy quyền mới được phép sử dụng.
    
5.  Kiểm tra định kỳ để đảm bảo có thể khôi phục tài khoản khi cần.
    


