## PHẦN 1: PHÂN TÍCH BÀI TOÁN (I/O)

**1. Bảng xác định thông số VLOOKUP cho các cột:**

**Cột cần điền**

**Lookup_value**

**Table_array**

**Col_index_num**

**Range_lookup**

**Cột D (Tên Tác Giả)**

`TRIM(C2)`

`'DanhMucTacGia'!$A$2:$E$100`

**2**

`FALSE` (0)

**Cột E (Phòng trình bày)**

`TRIM(C2)`

`'DanhMucTacGia'!$A$2:$E$100`

**4**

`FALSE` (0)

**Cột F (Thù lao)**

`TRIM(C2)`

`'DanhMucTacGia'!$A$2:$E$100`

**5**

`FALSE` (0)

**2. Cách xử lý 3 bẫy dữ liệu:**

-   **Bẫy khoảng trắng (dư dấu cách):** Dùng hàm `TRIM` bọc quanh ô mã tác giả (`TRIM(C2)`) để xóa sạch khoảng trắng thừa trước khi đi tìm.
    
-   **Bẫy tác giả ngoài danh sách (báo lỗi `#N/A`):** Dùng hàm `IFERROR` bọc ngoài cùng. Nếu tìm không thấy, Excel sẽ tự đổi thành chữ `"Chưa cập nhật"` cho đẹp mắt.
    
-   **Bẫy trôi bảng tìm kiếm khi kéo công thức:** Dùng dấu `$` (ví dụ `$A$2:$E$100`) để khóa cứng bảng danh mục lại, không bị chạy lệch khi kéo chuột.
    

**3. Các bước làm trong Excel:**

-   **Bước 1:** Nhập công thức dò tìm hoàn chỉnh vào ô **D2**.
    
-   **Bước 2:** Sửa số cột thành **4** để dán sang ô **E2**, và sửa thành **5** để dán sang ô **F2**.
    
-   **Bước 3:** Bôi đen từ ô D2 đến F2, sau đó rê chuột kéo xuống tận dòng 81 để áp dụng cho toàn bộ danh sách.
    

#### PHẦN 2: TRIỂN KHAI & CHỐNG LỖI

**4. Công thức hoàn chỉnh cho ô D2 (Tên Tác Giả):**

Excel

```
=(VLOOKUP(TRIM(C2), 'DanhMucTacGia'!$A$2:$E$100, 2, FALSE), "Chưa cập nhật")

```

**5. Công thức cho ô E2 (Phòng) và F2 (Thù lao):**

-   **Ô E2 (Phòng):**
    
    Excel
    
    ```
    =IFERROR(VLOOKUP(TRIM(C2), 'DanhMucTacGia'!$A$2:$E$100, 4, FALSE), "Chưa cập nhật")
    
    ```
    
-   **Ô F2 (Thù lao):**
    
    Excel
    
    ```
    =IFERROR(VLOOKUP(TRIM(C2), 'DanhMucTacGia'!$A$2:$E$100, 5, FALSE), "Chưa cập nhật")
    
    ```
    
-   **Giải thích:** Cả 3 ô đều đi tìm cùng một mã tác giả trên cùng một bảng danh mục. Điểm khác duy nhất là tên tác giả nằm ở cột số 2, phòng trình bày nằm ở cột số 4, còn thù lao nằm ở cột số 5 trong bảng danh mục. Do đó chỉ cần đổi con số cột là xong, không cần viết lại từ đầu.
    

**6. Hiện tượng khi bỏ dấu `$` trong bảng tra cứu:**

Nếu viết thiếu dấu `$` (thành `A2:E100`), khi kéo công thức từ ô **D2** xuống **D5**, vùng tìm kiếm sẽ bị dịch chuyển trôi theo từng dòng:

-   **Tại D2:** Vùng tìm kiếm là `A2:E100` (Đúng, lấy đủ từ đầu).
    
-   **Tại D3:** Vùng tìm kiếm bị trôi xuống `A3:E101` (Bị mất dòng 2).
    
-   **Tại D4:** Vùng tìm kiếm bị trôi xuống `A4:E102` (Bị mất dòng 2 và 3).
    
-   **Tại D5:** Vùng tìm kiếm bị trôi xuống `A5:E103` (Bị mất dòng 2, 3 và 4).
    
-   **Hậu quả:** Nếu tác giả nằm ở dòng đầu tiên (dòng 2) của bảng danh mục, khi công thức bị trôi xuống các dòng dưới, Excel sẽ không còn nhìn thấy tác giả đó nữa và sẽ trả về lỗi (hoặc hiện chữ "Chưa cập nhật" dù tác giả thực sự có tên trong danh sách).
