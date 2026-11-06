# PHẦN 1. Phân tích sai lầm trong tư duy tìm kiếm
### 1. Query 1 của bạn thực tập sinh là một 'Bad Query' điển hình vì :
- Query 1 là Bad Query vì sử dụng câu văn nói dài dòng, có nhiều từ cảm thán như “thầy ơi”, “tại sao”, “giúp em với”. Câu tìm kiếm không có những từ khóa quan trọng như tên phần mềm, hệ điều hành và mã lỗi.

- Vì vậy, Google khó xác định đúng vấn đề cần tìm, dẫn đến nhiều kết quả không liên quan như bài viết tâm sự, quảng cáo và hướng dẫn chung chung. Điều này làm mất thời gian tìm kiếm.

 ### 2. Hiểm họa an ninh thông tin khi click vào kết quả Query 3

-   Có thể tải nhầm phần mềm chứa mã độc Trojan.
    
-   Mã độc có thể đánh cắp tài khoản và dữ liệu của công ty.
    
-   Máy tính trạm Kiosk có thể bị kiểm soát trái phép.
    
-   Hoạt động của hệ thống trạm sạc có thể bị gián đoạn.
    
-   Gây mất an toàn thông tin cho công ty.
    

# PHẦN 2. CHUẨN HÓA CÚ PHÁP TÌM KIẾM CHUYÊN NGHIỆP

### 3. Bóc tách thông báo lỗi thành 3 thành phần cốt lõi là :

- Thông báo lỗi:

`Error: Failed to bind OCPP port. System error: Access is denied`

| Thành phần cốt lõi | Nội dung trích xuất chuẩn | Mục đích lọc tìm kiếm |
|---|---|---|
| 1. Tên phần mềm và môi trường | VoltCharge Controller Windows 11 | Tìm đúng phần mềm và hệ điều hành đang sử dụng. |
| 2. Mã lỗi nguyên văn | `"Access is denied"` | Tìm chính xác nội dung thông báo lỗi. |
| 3. Thao tác / Giao thức | `bind OCPP port` | Xác định thao tác đang gây ra lỗi. |

### 4. Xây dựng 3 câu lệnh tìm kiếm Google chuẩn kỹ sư là :

Cú pháp 1: Tìm bài viết trên Microsoft Community dành cho Windows 11, loại bỏ Windows 7 và Windows 8.

```
site:answers.microsoft.com "Access is denied" "Windows 11" -Windows 7 -Windows 8
```

Cú pháp 2: Tìm tài liệu về OCPP và quyền truy cập cổng trên trang Open Charge Alliance.

```
site:openchargealliance.org "OCPP" "port" "Access is denied" -crack -quangcao
```

Cú pháp 3: Tìm hướng dẫn xử lý lỗi trên Stack Overflow, loại bỏ kết quả chứa từ khóa crack và quảng cáo.

```
site:stackoverflow.com "Failed to bind OCPP port" "Access is denied" -crack -quangcao
```
