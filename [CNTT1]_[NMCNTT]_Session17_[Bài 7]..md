

# Phần 1: Phân tích vấn đề

### 1.  4 điểm sai trong bản giải trình là :

| Nội dung | Nhận định sai | Giải thích đúng |
|---|---|---|
| DNS | Gửi URL trực tiếp đến Server. | DNS chuyển tên miền thành địa chỉ IP. |
| TCP/TLS | HTTPS không cần bắt tay. | Phải thiết lập TCP và TLS Handshake để tạo kết nối an toàn. |
| HTTP | Database sập trả về lỗi 404. | Server gặp lỗi nội bộ thì trả về 500. |
| DOM | Sửa chữ trên Elements làm thay đổi Database. | Chỉ thay đổi nội dung tạm thời trên trình duyệt. |.

### 2. máy chủ cơ sở dữ liệu bị sập vì :

-   **500:** Máy chủ gặp lỗi nội bộ, không thể xử lý yêu cầu do Backend hoặc Database gặp sự cố.
    
-   **404:** Không tìm thấy trang hoặc tài nguyên được yêu cầu.
    


# Phần 2: Sửa lỗi và hoàn thiện giải pháp

### 3.  biên bản kỹ thuật theo 4 bước là :

**BIÊN BẢN SỰ CỐ CAREPULSE – CA BỆNH ÁN #8821**





| Bước | Quy trình | Nội dung |
|---|---|---|
| 1 | DNS Lookup | Phân giải tên miền thành địa chỉ IP của máy chủ. |
| 2 | TCP/TLS Handshake | Thiết lập kết nối TCP và mã hóa HTTPS bằng TLS. |
| 3 | HTTP Request & Response | Trình duyệt gửi yêu cầu xem kết quả, Server xử lý và trả dữ liệu hoặc mã lỗi 500 nếu gặp sự cố nội bộ. |
| 4 | Rendering | HTML tạo DOM Tree, CSS tạo CSSOM, sau đó thực hiện Layout và Paint để hiển thị trang web. |


HTML tạo DOM Tree, CSS tạo CSSOM, sau đó thực hiện Layout và Paint để hiển thị trang web.


### 4. hành động sửa chữ trên Tab Elements của bạn thực tập sinh hoàn toàn không có giá trị lưu trữ trên máy chủ CarePulse vì :

Khi sửa chữ trong Tab Elements, trình duyệt chỉ thay đổi DOM trong bộ nhớ tạm thời ở máy người dùng. Dữ liệu trên Database của máy chủ không bị thay đổi. Khi nhấn F5, trang tải lại dữ liệu từ Server nên nội dung cũ sẽ xuất hiện.

| Tiêu chí | Client-side | Server-side |
|---|---|---|
| Vị trí | RAM máy người dùng | Database máy chủ |
| Chức năng | Hiển thị nội dung | Lưu trữ dữ liệu gốc |
| Khi chỉnh sửa | Thay đổi tạm thời trên trình duyệt | Cập nhật thông qua Backend và API hợp lệ |
| Khi nhấn F5 | Nội dung sửa thường bị mất | Dữ liệu gốc vẫn được giữ nguyên |

