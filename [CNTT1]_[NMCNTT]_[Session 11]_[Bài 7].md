## PHẦN 1: PHÂN TÍCH LỖI

**1. Lỗi cụ thể từng dòng tiêu đề & Nguyên nhân mục lục bị trống:**

-   **Nguyên nhân mục lục bị trống:** Tính năng Auto TOC trong Word chỉ đi tìm các dòng được gán nhãn **Heading 1, Heading 2, Heading 3...** để đưa vào mục lục. File này đang làm thủ công (chỉ bôi đen rồi chỉnh to chữ, in đậm, đổi màu), bản chất tất cả vẫn là chữ thường (**Normal**). Do Word không tìm thấy nhãn Heading nào nên mục lục xuất ra bị rỗng.
    
-   **Lỗi cụ thể từng dòng:**
    
    -   `1. Thông tin chung hội nghị`: Dùng Normal + cỡ 16, in đậm, tô vàng $\rightarrow$ Thiếu nhãn **Heading 1**.
        
    -   `1.1. Tên hội nghị`: Dùng Normal + cỡ 14, in đậm $\rightarrow$ Thiếu nhãn **Heading 2**.
        
    -   `1.2. Thời gian & địa điểm`: Dùng Normal + cỡ 14, in đậm $\rightarrow$ Thiếu nhãn **Heading 2**.
        
    -   `2. Cơ cấu ban tổ chức`: Dùng Normal + cỡ 16, in đậm, tô vàng $\rightarrow$ Thiếu nhãn **Heading 1**.
        
    -   `2.1. Ban Nội dung`: Dùng Normal + cỡ 13, màu xanh $\rightarrow$ Thiếu nhãn **Heading 2**.
        
    -   `2.1.1. Tiểu ban Kỹ thuật`: Dùng Normal + cỡ 13, màu xanh $\rightarrow$ Gán sai cấp và thiếu nhãn (phải là **Heading 3**).
        
    -   `3. Lịch trình sự kiện`: Chữ thường Normal, không định dạng $\rightarrow$ Thiếu nhãn **Heading 1**.
        

**2. Tác hại của việc nhầm cấp Heading (H2 sang H3 hoặc ngược lại):**

-   Bảng mục lục tự động dùng khoảng thụt lùi đầu dòng để thể hiện cấp bậc: Heading 1 sát lề trái, Heading 2 thụt vào 1 đoạn, Heading 3 thụt vào sâu hơn.
    
-   Nếu nhầm `Heading 3` thành `Heading 2`, dòng _"2.1.1. Tiểu ban Kỹ thuật"_ sẽ bị nhô ra ngoài, đứng ngang hàng với mục cha _"2.1. Ban Nội dung"_. Điều này làm mục lục nhìn bị lệch cấp và sai logic con - cha.
    

## PHẦN 2: SỬA LỖI & NGHIỆM THU

**3. Các bước thao tác sửa đúng cấu trúc Heading:**

-   **Bước 1: Gán lại nhãn Heading cho 7 dòng tiêu đề bằng phím tắt**
    
    1.  Đặt con trỏ ở dòng `1. Thông tin chung hội nghị` $\rightarrow$ Bấm **Ctrl + Alt + 1** (để gán Heading 1).
        
    2.  Đặt con trỏ ở dòng `1.1. Tên hội nghị` $\rightarrow$ Bấm **Ctrl + Alt + 2** (để gán Heading 2).
        
    3.  Đặt con trỏ ở dòng `1.2. Thời gian & địa điểm` $\rightarrow$ Bấm **Ctrl + Alt + 2** (để gán Heading 2).
        
    4.  Đặt con trỏ ở dòng `2. Cơ cấu ban tổ chức` $\rightarrow$ Bấm **Ctrl + Alt + 1** (để gán Heading 1).
        
    5.  Đặt con trỏ ở dòng `2.1. Ban Nội dung` $\rightarrow$ Bấm **Ctrl + Alt + 2** (để gán Heading 2).
        
    6.  Đặt con trỏ ở dòng `2.1.1. Tiểu ban Kỹ thuật` $\rightarrow$ Bấm **Ctrl + Alt + 3** (để gán Heading 3).
        
    7.  Đặt con trỏ ở dòng `3. Lịch trình sự kiện` $\rightarrow$ Bấm **Ctrl + Alt + 1** (để gán Heading 1).
        
-   **Bước 2: Xuất bảng mục lục tự động**
    
    -   Đặt con trỏ chuột ở trang đầu tiên $\rightarrow$ Chọn tab **References** trên thanh menu $\rightarrow$ Chọn **Table of Contents** $\rightarrow$ Click chọn **Automatic Table 1**.
        

**4. Xử lý bẫy dữ liệu (Khi mục 3 bị nhảy từ trang 2 sang trang 4):**

-   **Trả lời:** Mục lục **KHÔNG** tự hiện đúng số trang mới nếu mình không làm thêm thao tác cập nhật.
    
-   **Thao tác cần làm:**
    
    1.  Click chuột vào bảng mục lục.
        
    2.  Bấm phím **F9** trên bàn phím (hoặc bấm nút **Update Table...** ở ngay trên đầu bảng mục lục).
        
    3.  Chọn dòng **Update page numbers only** (chỉ cập nhật lại số trang) rồi bấm **OK**.
