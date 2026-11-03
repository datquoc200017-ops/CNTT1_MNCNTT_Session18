# BÀI TẬP VỀ NHÀ
## Bài 1 : Sự cố không truy cập được hệ thống quản trị
### Bài Làm
**4. Yêu cầu đầu ra**

**_Phần 1. Phân tích_**

1.   Xác định Input (Tên miền) / Output (IP address) và mô tả sơ đồ luồng dữ liệu của DNS.
- INPUT đầu vào là tên miền [**phong-dieu-phoi.greenlog.vn**](http://phong-dieu-phoi.greenlog.vn) và khi nhập tên miền vào sẽ ra OUPUT là lỗi **"DNS_PROBE_FINISHED_NXDOMAIN"**
    

**_Phần 2. Triển khai_**

1.   Đề xuất quy trình kiểm tra mã trạng thái HTTP Status Code để xác nhận xem yêu cầu đã chạm tới máy chủ hay chưa.
- Đâu  tiên mở Developer Tools (F12) ở trình duyệt web và chọn vào thanh trạng thái Network và vào status code và kiểm tra đã chạm tới máy chủ hay chưa. 

    

**_Phần 3. Kiểm thử_**

1.   Giả định Nam sửa đúng tên miền nhưng vẫn nhận mã **404 Not Found**, hệ thống đang gặp vấn đề gì?
- Nếu sửa đúng tên miền mà vẫn gặp lỗi 404 Not Found thì hệ thống đang gặp lỗi trang, không tìm thấy trang.
    
