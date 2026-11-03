# BÀI TẬP VỀ NHÀ
## Bài 4 : Sự cố xung đột phiên đăng nhập trên trình duyệt
### Bài Làm
### Phần 1. Phân tích

-   **Incognito Mode:** Lưu trữ tạm thời trên RAM; mất sạch dữ liệu (cookies, lịch sử) khi đóng trình duyệt, không giữ được trạng thái đăng nhập lâu dài.
    
-   **Dedicated Profile:** Lưu trữ cố định trên ổ cứng; phân vùng độc lập giúp quản lý song song nhiều tài khoản mà không bị xung đột phiên (session conflict).
    

### Phần 2. Triển khai (Tạo Profile & Cloud Sync)

1.  **Tạo Profile:** Mở trình duyệt $\rightarrow$ Chọn biểu tượng tài khoản $\rightarrow$ Nhấn **Add** để tạo 3 profile riêng biệt (Personal, Work, Sandbox).
    
2.  **Đồng bộ Cloud Sync:** Vào **Settings**  $\rightarrow$ Bật **Turn on sync** cho từng profile. Giúp tự động khôi phục bookmark và mật khẩu khi đổi sang máy tính khác.
    

### Phần 3. Kiểm thử (Guest Profile trên máy công cộng)

-   Dùng **Guest Mode** để duyệt web an toàn, không lưu dấu vết lịch sử hay mật khẩu.
    
-   Đóng toàn bộ cửa sổ Guest ngay sau khi xong việc để tự động xóa sạch phiên làm việc.
