# PHẦN 1: PHÂN TÍCH HẬU QUẢ & SAI LẦM KỸ THUẬT
Câu 1.  4 Secrets bị lộ và hậu quả là :

| Secrets bị lộ | Hậu quả |
|---|---|
| `OPENAI_API_KEY` | Hacker có thể sử dụng API OpenAI trái phép, làm phát sinh chi phí. |
| `STEAM_WEB_API_KEY` | Hacker có thể sử dụng API Steam trái phép. |
| `MONGO_URI` | Hacker có thể truy cập, đánh cắp hoặc xóa dữ liệu người chơi trong cơ sở dữ liệu. |
| `JWT_SECRET` | Hacker có thể giả mạo Token để truy cập trái phép vào tài khoản người dùng. |
Câu 2.  xóa commit hoặc chuyển Repository sang Private vẫn phải thu hồi Secrets vì :
- các bot có thể quét và lấy Secrets ngay sau khi code được push lên GitHub. Hacker có thể đã lưu lại các khóa bí mật nên việc xóa commit hoặc chuyển sang Private không thể đảm bảo an toàn. Vì vậy, cần Revoke các khóa cũ và tạo khóa mới ngay lập tức.
# PHẦN 2: SỬA LỖI & CHUẨN HÓA AN               
Câu 3. Tệp `.env`

Tạo tệp `.env` trên máy tính cá nhân để lưu 4 thông tin bí mật gồm OpenAI API Key, Steam API Key, MongoDB URI và JWT Secret. Mỗi thông tin được lưu dưới dạng tên biến và giá trị tương ứng. Không chia sẻ tệp này lên GitHub.

Câu 4. Sửa tệp `server.js`

Thay các khóa bí mật viết trực tiếp trong mã nguồn bằng biến môi trường `process.env`. Nhờ đó, chương trình có thể lấy thông tin từ tệp `.env` mà không để lộ Secrets trong mã nguồn.

Câu 5. Tệp `.gitignore`

Thêm `.env` vào danh sách bỏ qua của Git để Git không theo dõi và không đưa tệp chứa mật khẩu, API Key lên GitHub.

Câu 6. Tệp `.env.example`

Tạo tệp `.env.example` chứa tên của 4 biến môi trường nhưng không điền giá trị bí mật. Tệp này được phép đưa lên GitHub để các thành viên trong nhóm dựa vào đó tạo tệp `.env` riêng.
