# Phần  1 : phân tích
### 1.1. Input và Output

-   Input: Nhiệt độ, độ ẩm đất do cảm biến thu thập.
    
-   Process: SoC xử lý dữ liệu và so sánh với ngưỡng đã cài đặt.
    
-   Output: Bật hoặc tắt máy bơm tưới cây và hiển thị trạng thái.
    
## #1.2. Sơ đồ phần cứng

Cảm biến nhiệt độ, độ ẩm
                    ⬇️
SoC (CPU, RAM)
                    ⬇️
Mạch điều khiển → Máy bơm
                    ⬇️
SoC nhận dữ liệu từ cảm biến, xử lý rồi gửi lệnh điều khiển máy bơm.
# Phần 2 : triển khai 

## 1. Mô tả dự án🚀 Smart-Farm – Hệ thống tưới cây thông minh

Smart-Farm là hệ thống IoT giúp người nông dân theo dõi nhiệt độ, độ ẩm đất và tự động tưới cây tại trang trại Lan. Hệ thống giúp **tiết kiệm thời gian và sử dụng nước hợp lý**.

 
## 2. Hướng dẫn cài đặt

-   Bước 1: Kết nối cảm biến với bộ điều khiển.
    
-   Bước 2: Kết nối máy bơm qua mạch điều khiển.
    
-   Bước 3: Cài đặt ngưỡng nhiệt độ và độ ẩm.
    
-   Bước 4: Khởi động hệ thống và kiểm tra hoạt động.
   

## 3. Tính năng
    
-   Theo dõi độ ẩm đất.
-   Tự động bật, tắt máy bơm.
-   Lưu nhật ký hoạt động.
-   Thêm cảnh báo khi thiết bị gặp lỗi.
-  Tự động điều chỉnh độ mạnh yếu của dòng nước tưới .
  
## 4. Bảng thông số

|thành phần|chức năng|
|--|--|--
cpu|Xử lý lệnh
ram|Lưu dữ liệu tạm thời
công tắc tự động bật tắt |giúp bật tắt máy bớm  
máy bơm|dùng để tưới 
bộ nhớ lưu chữ | lưu trương trình và nhật kí sử dụng của thiết bị 
# **Phần 3. Kiểm thử**
- mục lưu ý cách  sử lí  an toàn khi ram bị đầy là :

1.  Kiểm tra chương trình nào đang sử dụng nhiều RAM.
2.  Giảm các nhật ký không cần thiết.
3.  Lưu nhật ký quan trọng vào bộ nhớ lưu trữ.
4.  Giải phóng bộ nhớ đệm
5.  Kiểm tra lại hệ thống trước khi tiếp tục sử dụng 
