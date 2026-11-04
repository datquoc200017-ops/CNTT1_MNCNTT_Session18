# BÀI TẬP VỀ NHÀ
## Bài 3 : Khắc phục sự cố rò rỉ thông tin đăng nhập
### Bài làm
**3. Yêu cầu đầu ra**

**_Báo cáo phân tích (IPO)_**

1.   Xác định Input (Dấu hiệu nhiễm), Process (Các bước xử lý), Output (Hệ thống sạch).
- Dấu hiện Input là khi bạn tải một phần mềm crack và khi vào tài khoảng ví dụ như facebook đột nhiên bị thoát ra tài khoản đột ngột.
- Process (Các bước xử lý) Tắt lập tức mạng wifi và bật Windows security và quét toàn bộ xem có file mã độc nào xâm nhập không, bật xác thực hai bước ngay lập tức, đổi hoàn toàn mật khẩu mới và đăng xuất tất cả các thiết bị hiện đang đăng nhập.
- Output : Khi bạn check lại và thấy không còn lịch sử đăng nhập từ thiết bị lạ nữa và không còn thông báo đăng nhập lạ nữa, Windows security thông báo giải quyết xóa hết mã độc. 

    

**_Triển khai_**

1.   Mô tả chi tiết cách thực hiện "Đổi mật khẩu từ thiết bị khác" và "Revoke Token" trên GitHub.
- Lấy thiết bị ví dụ như điện thoại đã đăng nhập tài khoản đó và đổi mật khẩu sau đó ấn đăng xuất các thiết bị từng đăng nhập và bật xác thực hai bước. 
- Vào github sau đó vào quyền của  quản trị viên chọn token muốn xóa và sau đó thu hồi token đó.
