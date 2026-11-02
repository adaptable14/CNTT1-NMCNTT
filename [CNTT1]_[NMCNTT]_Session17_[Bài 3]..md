# BÀI LÀM: PHÂN TÍCH VÀ SỬA LỖI BOX MODEL

## Phần 1: Báo cáo phân tích (I/O)

### 1. Phân tích lỗi

Sau khi sử dụng F12 và chọn tab Computed, em nhận thấy hai khung "Nội dung bài học" và "Danh sách video" bị chồng lên nhau. Nguyên nhân có thể do Margin, Padding hoặc kích thước của hai phần tử chưa phù hợp.

### 2. Phân tích 4 lớp Box Model

Thành phần

Nội dung

Content

Chứa nội dung bài học và danh sách video.

Padding

Khoảng cách từ nội dung đến đường viền.

Border

Đường viền bao quanh khung.

Margin

Khoảng cách bên ngoài khung.

### 3. Sơ đồ Box Model hiện tại (mô phỏng)

```
       MARGIN
  +-------------------+
  |      BORDER       |
  |  +-------------+  |
  |  |   PADDING   |  |
  |  | +---------+ |  |
  |  | | CONTENT | |  |
  |  | +---------+ |  |
  |  +-------------+  |
  +-------------------+
```

Hai khung có thể đang bị thiếu khoảng cách bên ngoài hoặc có Padding quá lớn. Cần kiểm tra các giá trị Width, Height, Margin và Padding trong Computed để xác định nguyên nhân.

### 4. Dự đoán khi thay đổi Margin mà không kiểm tra Padding

Nếu chỉ tăng Margin mà không kiểm tra Padding, khoảng cách giữa hai khung có thể quá lớn, khiến bố cục bị lệch. Nếu Padding quá lớn, phần nội dung bên trong cũng có thể bị thu hẹp.

## Phần 2: Thiết kế giải pháp

### 1. Các thông số đề xuất trong Styles


| Thuộc tính CSS | Giá trị đề xuất | Tác dụng |
|---|---|---|
| margin-bottom | 20px | Tạo khoảng cách giữa hai khung. |
| padding | 16px | Tạo khoảng trống bên trong khung. |
| border | 1px solid #ddd | Tạo đường viền cho khung. |
| box-sizing | border-box | Giữ kích thước khung ổn định. |
| position | static | Đưa phần tử về vị trí theo bố cục thông thường. |


### 2. CSS đề xuất

```
.lesson-content,
.video-list 
    margin-bottom: 20px;
    padding: 16px;
    border: 1px solid #ddd;
    box-sizing: border-box;
    position: static;

```

