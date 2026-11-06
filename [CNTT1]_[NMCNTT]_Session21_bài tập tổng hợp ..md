# PHẦN 1. GO OGLING ĐÚNG CÁCH

### Câu 1. Vì sao Bad Query cho kết quả kém?

Câu hỏi dùng văn nói, không có từ khóa kỹ thuật và thông báo lỗi cụ thể nên Google khó tìm đúng vấn đề.

### Câu 2. Bóc tách lỗi

| Mảnh ghép | Nội dung trong tin nhắn |
|---|---|
| Context | Em sử dụng Node.js trên Windows 11, chạy lệnh trong Terminal VS Code. |
| Expected | Khi nhập `npm -v`, máy hiển thị phiên bản npm. |
| Actual | Máy báo lỗi `'npm' is not recognized as an internal or external command, operable program or batch file.` |
| Log & Screenshot | Em đã thêm đường dẫn Node.js vào PATH và mở Terminal mới nhưng lỗi vẫn xuất hiện. |

### Câu 3. Ba câu truy vấn của e với Google là :

-   `site:stackoverflow.com npm not recognized Windows 11 Node.js`
    
-   `"npm is not recognized as an internal or external command"`
    
-   `npm not recognized Windows 11 Node.js PATH -Windows-XP`
    

# PHẦN 2. THẨM ĐỊNH STACKOVERFLOW

### Câu 1. So sánh hai câu trả lời là :

| Tiêu chí | Câu trả lời A | Câu trả lời B |
|---|---|---|
| Vote & Tích xanh | +186, có tích xanh | +2, không có tích xanh |
| Thời gian đăng | 2 năm trước | 9 năm trước |
| Tags | node.js, windows, npm | node.js, windows-xp |

### Câu 2. Kết luận :

Em chọn câu trả lời A vì có nhiều lượt bình chọn, có tích xanh và phù hợp với Windows 11.

Câu B là bẫy vì hướng dẫn cài driver mạng cho Windows XP, không liên quan đến lỗi npm trên Windows 11. Làm theo có thể gây mất thời gian và ảnh hưởng cấu hình máy.

### Câu 3. Quy trình đọc lướt 30 giây

1.  Đọc tiêu đề câu hỏi.
    
2.  Kiểm tra Tags.
    
3.  Xem dấu tích xanh.
    
4.  Kiểm tra lượt bình chọn.
    
5.  Xem thời gian đăng.
    
6.  Đọc nội dung câu trả lời và bình luận.
    

# PHẦN 3. HỎI AI ĐÚNG CÁCH VÀ NHẬN DIỆN RỦI RO

### Câu 1. Prompt hoàn chỉnh


**Ngữ cảnh** : Em sử dụng Node.js trên Windows 11 và chạy lệnh trong Terminal của VS Code.

**Lỗi nguyên văn**: `'npm' is not recognized as an internal or external command, operable program or batch file`.

**Yêu cầu**: Hãy giải thích nguyên nhân và hướng dẫn sửa lỗi từng bước. Em đã thêm đường dẫn Node.js vào PATH và mở Terminal mới nhưng vẫn bị lỗi. Hãy đưa ra cách kiểm tra an toàn.


### Câu 2. Đánh giá câu trả lời AI là :

Đây là câu trả lời không an toàn vì:

-   Lệnh có thể xóa các tệp hệ thống quan trọng.
    
-   Không kiểm tra kỹ nguyên nhân lỗi.
    
-   Có nguy cơ làm Windows không hoạt động bình thường.
    

+) Em không chạy lệnh này vì vi phạm nguyên tắc an toàn là : hiểu rõ lệnh trước khi chạy, kiểm chứng thông tin và không thực hiện thao tác có nguy cơ phá hủy dữ liệu.

### Câu 3. Câu phản hồi AI của e là :

 lệnh này có nguy cơ xóa tệp hệ thống. Hãy hướng dẫn cách kiểm tra PATH và Node.js bằng các lệnh an toàn hơn, không làm mất dữ liệu .

# PHẦN 4. VIẾT BUG REPORT

### Câu 1. Tin nhắn kèm là : 
- Thầy ơi, máy em bị lỗi npm rồi ạ. Thầy giúp em với ạ.
### Câu 2. Tin nhắn chuẩn theo 4 mảnh ghép của Bug Reporting Framework là :
| Mảnh ghép | Nội dung trong tin nhắn |
|---|---|
| Context | Em sử dụng Node.js trên Windows 11, chạy lệnh trong Terminal VS Code. |
| Expected | Khi nhập `npm -v`, máy hiển thị phiên bản npm. |
| Actual | Máy báo lỗi `'npm' is not recognized as an internal or external command, operable program or batch file.` |
| Log & Screenshot | Em đã thêm đường dẫn Node.js vào PATH và mở Terminal mới nhưng lỗi vẫn xuất hiện. |
### Câu 3. Ba câu truy vấn Google của e là :

1.  Tìm cách sửa lỗi npm không được nhận diện trên StackOverflow khi sử dụng Windows 11.
    
2.  Tìm kiếm chính xác thông báo lỗi `'npm' is not recognized as an internal or external command`.
    
3.  Tìm cách khắc phục lỗi npm trên Windows 11, loại bỏ các kết quả liên quan đến Windows XP.
