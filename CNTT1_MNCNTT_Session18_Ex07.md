# BÀI TẬP VỀ NHÀ
## 
### Bài làm
**4. Yêu cầu đầu ra**

### Phần 1: Phân tích 2 Giải pháp

1.  **Yếu tố xác thực:** Mật khẩu là **Something You Know**, mã OTP là **Something You Have**.
    
2.  **Nguyên lý TOTP:** Ứng dụng tự sinh mã ngoại tuyến nhờ dùng chung **Khóa bí mật (Shared Secret)** và **Đồng hồ chuẩn UTC** với máy chủ, hoàn toàn không cần Internet/SMS.
    
### Phần 2: So sánh & Lựa chọn
-   **Chọn:**  **Giải pháp 2 (TOTP Authenticator)**.
    
-   **Lý do:** Chống hoàn hảo tấn công SIM Swapping (bảo vệ mã nguồn & tài chính studio) và hoạt động 100% offline khi kỹ sư đi công tác nước ngoài/trên máy bay.
    
### Phần 3: Quản lý Backup Codes
-   **Mục đích:** Đăng nhập cứu hộ khi mất/hỏng điện thoại.
    
-   **2 nơi lưu an toàn:** In ra giấy cất két sắt; hoặc lưu vào trình quản lý mật khẩu cá nhân có mã hóa mạnh.
    
-   **Sai lầm tai hại cần tránh:**  **Chụp ảnh màn hình lưu vào thư viện điện thoại** hoặc gửi lên chat/cloud không mã hóa.
