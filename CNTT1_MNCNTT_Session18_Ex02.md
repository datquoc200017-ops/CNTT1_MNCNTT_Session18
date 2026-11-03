# BÀI TẬP VỀ NHÀ
##   Bài 2 : Sự cố phiên làm việc trên hệ thống vận tải
### Bài Làm
**4. Yêu cầu đầu ra**

**_Phần 1. Phân tích_**

1.  So sánh sự đánh đổi giữa dung lượng Cache (**MB/GB**) và Cookies (**~4KB**) trong việc lưu trữ dữ liệu người dùng.
- Dung lượng Cache bộ nhớ đệm được lưu vào trong Ram lưu các file html, css để lần sau truy cập thì tốc độ nhanh.
- Cookies có dung lượng lưu trữ chỉ 4kb việc lưu trữ ít hầu hết chỉ lưu mật khẩu tài khoản của người dùng.

    

**_Phần 2. Triển khai_**

1.   Mô tả cấu trúc mẩu tin Cookie cần thiết (bao gồm Token, Max-Age, và các cờ bảo mật).
- Cờ Token là chuỗi kí tự mã hóa của người dùng.
- Max-Age dùng để set ngày lưu token đến hết hạn sẽ tự động điều chỉnh lại.
- HttpOnly Ngăn chặn JavaScript truy cập vào cookie. Giúp chống lại tấn công Cross-Site Scripting (XSS) cướp đoạn mã phiên.
    

**_Phần 3. Kiểm thử_**

1.   Nếu shipper thay đổi giao diện nhưng trình duyệt vẫn hiện màu cũ, hãy hướng dẫn thao tác Hard Reload để xóa Cache đệm.
- Để shipper thao tác hard reload để xóa Cache đệm shipper thực hiện thao tác Ctrl+F5.

