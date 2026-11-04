# 1. Báo cáo phân tích (IPO)

| Thành phần | Nội dung |
|---|---|
| Input | Máy tính có dấu hiệu nhiễm Infostealer: tài khoản Facebook, Gmail liên tục bị mất quyền kiểm soát. |
| Process | Thực hiện 4 bước: ngắt kết nối Internet, đổi mật khẩu từ thiết bị khác, thu hồi Token trên GitHub, quét và làm sạch máy tính. |
| Output | Máy tính được làm sạch mã độc, mật khẩu mới được thiết lập, Token cũ bị thu hồi và tài khoản được bảo vệ. |

# 2. Triển khai 

1. Đổi mật khẩu từ thiết bị khác

-   Sử dụng điện thoại hoặc máy tính an toàn.
    
-   Đăng nhập vào tài khoản cần bảo vệ.
    
-   Vào phần Cài đặt → Bảo mật → Đổi mật khẩu.
    
-   Tạo mật khẩu mới, mạnh và không trùng mật khẩu cũ.
    
-   Đăng xuất các thiết bị lạ và bật xác thực 2 lớp (2FA).
    

2. Revoke Token trên GitHub

-  Đăng nhập GitHub.
    
-  vào chọn  Settings.
    
-  chọn Developer settings.
    
-  Chọn Personal access tokens.
    
-  Chọn Tokens (classic) hoặc Fine-grained tokens.
    
-  Kiểm tra Token lạ hoặc nguy hiểm , chọn Token cần thu hồi đó và nhấn Delete.

