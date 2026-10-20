
 BÀI LUYỆN TẬP – NGÀY 1
**Môn:** Nhập môn Công nghệ Thông tin  
**Ngày:** 20/10/2026  

---

## PHẦN A – TỔ CHỨC THƯ MỤC BẰNG GUI
- [x] A1. Bật hiển thị đuôi file và file ẩn.
- [x] A2. Đổi tên thư mục gốc thành `trung-tam-tieng-anh`.
- [x] A3. Tạo 5 thư mục: `docs`, `media`, `data`, `logs`, `archive`.
- [x] A4. Đổi tên các file theo dạng `snake_case`:
  - `logo_trung_tam.png`
  - `anh_lop_hoc.jpg`
  - `lich_hoc.txt`
  - `hoc_vien_khoa_3.xlsx`
  - `access.log`
- [x] A5. Di chuyển `hoc_vien_khoa_3.xlsx` vào `data/`, `access.log` vào `logs/`.
- [x] A6. Sao chép `bai_lam_ngay1.md` và giữ file `.env` tại thư mục gốc.

---

## PHẦN B – THAO TÁC BẰNG CLI

### Danh sách các lệnh đã thực hiện (mỗi lệnh một dòng):
- **B1 (Lệnh):** `pwd`
- **B2 (Lệnh):** `ls -Force` 
- **B3 (Lệnh):** 
  - `mv lich_hoc.txt docs/Lich hoc khoa 3: Thu 2-4-6 (18h00-19h30), Thu 3-5-7 (19h45-21h15).`
  - `mv logo_trung_tam.png media/`
  - `mv anh_lop_hoc.jpg media/`
- **B4 (Lệnh):** `cp media/logo_trung_tam.png archive/`
- **B5 (Lệnh):** 
  - `rm temp_201.tmp`
  - `rm temp_202.tmp`
- **B6 (Lệnh):** `ls -Recurse -Force` 

---

### Kết quả câu B1 (Đường dẫn tuyệt đối):
```text
C:\Users\Admin\Projects\trung-tam-tieng-anh

```

### Kết quả câu B6 (Cấu trúc toàn bộ dự án):

Plaintext

```
Directory: C:\Users\Admin\Projects\trung-tam-tieng-anh

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        20/10/2026  12:00 PM                archive
d-----        20/10/2026  12:00 PM                data
d-----        20/10/2026  12:00 PM                docs
d-----        20/10/2026  12:00 PM                logs
d-----        20/10/2026  12:00 PM                media
-a-h--        20/10/2026  12:00 PM             32 .env
-a----        20/10/2026  12:00 PM           1200 bai_lam_ngay1.md

Directory: C:\Users\Admin\Projects\trung-tam-tieng-anh\archive
-a----        20/10/2026  12:00 PM          15200 logo_trung_tam.png

Directory: C:\Users\Admin\Projects\trung-tam-tieng-anh\data
-a----        20/10/2026  12:00 PM           8500 hoc_vien_khoa_3.xlsx

Directory: C:\Users\Admin\Projects\trung-tam-tieng-anh\docs
-a----        20/10/2026  12:00 PM            420 lich_hoc.txt

Directory: C:\Users\Admin\Projects\trung-tam-tieng-anh\logs
-a----        20/10/2026  12:00 PM           1024 access.log

Directory: C:\Users\Admin\Projects\trung-tam-tieng-anh\media
-a----        20/10/2026  12:00 PM          15200 logo_trung_tam.png
-a----        20/10/2026  12:00 PM          45100 anh_lop_hoc.jpg
```
