# PHẦN 1. THIẾT KẾ PROMPT 3 THÀNH PHẦN CHUẨN HÓA

### Câu 1.  câu hỏi của nhân viên khiến AI trả lời sai lệch là :

Câu hỏi “AI ơi phần mềm trạm sạc của tôi bị hỏng rồi làm sao đây?” chưa cung cấp đủ thông tin để AI hiểu vấn đề.

-   Không nêu tên phần mềm và hệ điều hành.
    
-   Không đưa thông báo lỗi cụ thể.
    
-   Không nói rõ thao tác đang thực hiện.
    

Vì thiếu dữ liệu, AI có thể tự suy đoán và đưa ra câu trả lời không chính xác. Hiện tượng này gọi là AI Hallucination (ảo giác AI). Ví dụ, AI lại hướng dẫn kiểm tra dây điện trong khi lỗi thực tế là lỗi quyền truy cập phần mềm.

### Câu 2.  Prompt 3 thành phần hoàn chỉnh là 

**[ Ngữ cảnh]**

Tôi là nhân viên kỹ thuật mới, đang trực vận hành trạm sạc xe điện VoltCharge #04 tại Bến xe Miền Đông. Máy tính điều khiển sử dụng Windows 11. Hiện tại, phần mềm ControllerDaemon không thể khởi động.

**[ Lỗi nguyên văn]**

```
2026-09-21 21:15:30 [FATAL] ControllerDaemon failed to start.
System.UnauthorizedAccessException: Access to the path 'C:\Program Files\VoltCharge\data\session.log' is denied.
at System.IO.FileStream.ValidateFileHandle(SafeFileHandle handle)
at VoltCharge.Core.SessionManager.Initialize()
InnerException: None. Process terminated with exit code 5 (0x00000005).
Suggestion: Run the application with elevated administrator privileges or verify NTFS file permissions.
```

**[ Yêu cầu]**

Hãy dịch thông báo lỗi sang tiếng Việt đơn giản, giải thích nguyên nhân và đưa ra 3 bước khắc phục cụ thể trên Windows 11. Hướng dẫn dễ hiểu cho người mới học IT và chú ý đến an toàn của hệ thống trạm sạc.

# PHẦN 2. GIẢI MÃ LỖI VÀ KỊCH BẢN KHẮC PHỤC

### Câu 3. Dịch và giải thích nguyên nhân gốc rễ của lỗi là :

| Nội dung lỗi | Ý nghĩa |
|---|---|
| `ControllerDaemon failed to start` | Chương trình ControllerDaemon không thể khởi động. |
| `UnauthorizedAccessException` | Lỗi không được phép truy cập. |
| `Access to the path ... is denied` | Windows từ chối quyền truy cập vào đường dẫn file. |
| `InnerException: None` | Không có lỗi phụ được ghi nhận. |
| `Exit code 5 (0x00000005)` | Mã lỗi báo thao tác bị từ chối quyền truy cập. |
Nguyên nhân gốc rễ là :

Phần mềm VoltCharge cần ghi dữ liệu vào file `session.log` trong thư mục `Program Files` nhưng không có đủ quyền ghi. Vì vậy, Windows 11 từ chối truy cập khiến chương trình không thể khởi động.

### Câu 4.  3 bước xử lý cụ thể trên Windows 11 là :

+) Bước 1: Kiểm tra quyền quản trị viên

Kiểm tra tài khoản Windows đang sử dụng có quyền phù hợp hay không. Nếu không có, cần nhờ quản trị viên hỗ trợ.

+) Bước 2: Chạy phần mềm bằng quyền Administrator

-   Nhấn chuột phải vào biểu tượng VoltCharge Controller.
    
-   Chọn `Run as administrator`.
    
-   Xác nhận nếu Windows yêu cầu và được người phụ trách cho phép.
    

+) Bước 3: Kiểm tra quyền ghi thư mục data

-   Mở thư mục `C:\Program Files\VoltCharge`.
    
-   Nhấn chuột phải vào thư mục `data`, chọn `Properties` → `Security`.
    
-   Nhờ quản trị viên cấp quyền `Write` cho đúng tài khoản chạy phần mềm.
    
-   Khởi động lại phần mềm và kiểm tra lỗi.
    


### Câu 5. Cách xử lý mã bí mật API_KEY là :

- Nếu trong đoạn mã lỗi có chứa:

`API_KEY: volt_secret_token_889922`

Kỹ thuật viên cần xóa hoặc thay thế mã bí mật trước khi gửi nội dung lên ChatGPT hoặc Gemini.
Lý do vì :

-   API Key là thông tin bí mật dùng để xác thực hệ thống.
    
-   Nếu bị lộ, người khác có thể sử dụng trái phép dịch vụ.
    
-   Có thể làm lộ dữ liệu và ảnh hưởng đến bảo mật của công ty.
    
-   Nếu đã gửi nhầm mã thật, cần báo quản trị viên để thu hồi và tạo mã mới.
