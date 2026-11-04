# BÀI TẬP VỀ NHÀ
## 
### Bài làm
**4. Yêu cầu đầu ra**

### **5. Yêu cầu**

### **Phần 1 –** Nhận diện rủi ro và xử lý sự cố

1.  **Tình huống 1:** gọi đúng tên loại tấn công (trong số **Phishing / Spear Phishing / Typosquatting**) và chỉ ra chính xác **chi tiết nào** trong email cho thấy đây là giả mạo.
- Đầu tiên chúng ta có thể dễ nhận tháy rằng đường link gmail `https://githuh-security.com/verify` sai rõ ràng chữ huh tức là trong đường link này chứa mã độc đánh cắp dữ liệu  nó là loại tấn cống Phishing gửi hàng loạt gmail tấn công nhằm đánh vào tâm lý, spear phishing nghiên cứu kĩ các trang web chúng ta thường truy cập và gửi gmail đánh lừa, typosquatting giả mạo tên mình sát với tên gốc ta thường truy cập và sau đò chúng ta lầm tưởng và đánh cắp dữ liệu.
    
2.  **Tình huống 2:** gọi đúng tên cạm bẫy và giải thích vì sao yêu cầu **"tắt Windows Defender"** là dấu hiệu cực kỳ nguy hiểm.
- Cạm bẫy đó gọi là crack khi tải một phần mềm vốn mất phí mà tai free trên mạng dễ kèm theo mã độc viruss điều khiển máy tính và khi windows defender quét phát hiện sẽ chặn ngay, nên thường yêu cầu tắt để mã độc xâm nhập vào máy tính.
    
### Đối chiếu **Quy tắc 5 KHÔNG**

-   **Tình huống 1:**  **KHÔNG click link lạ / tải file không rõ nguồn gốc** (để chặn mã độc xâm nhập).
    
-   **Tình huống 2:**  **KHÔNG dùng phần mềm crack / KHÔNG chạy file với quyền Admin** (để tránh tạo cửa hậu cho hacker).
    
 **4 Bước Cấp cứu** khi lỡ chạy file crack

1.  **Ngắt mạng ngay lập tức** (rút dây mạng / tắt Wi-Fi) để chặn hacker đánh cắp dữ liệu.
    
2.  **Kiểm tra Task Manager** để tìm các tiến trình lạ đang chạy ngầm.
    
3.  **Quét virus toàn bộ hệ thống** bằng phần mềm bảo mật (Windows Defender).
    
4.  **Sao lưu dữ liệu và đổi mật khẩu** các tài khoản quan trọng trên thiết bị khác.
    

### **1. Hậu quả khi lộ mật khẩu email chung & Tên kiểu tấn công**

-   **Hậu quả:** 2 tài khoản còn lại (nếu sử dụng chung một mật khẩu với email) cũng sẽ bị kẻ xấu xâm nhập và chiếm quyền kiểm soát.
    
-   **Tên kiểu tấn công:**  **Credential Stuffing** (Tấn công nhồi thông tin xác thực) hoặc **Password Reuse Attack** (Tấn công do tái sử dụng mật khẩu).
    

### **2. Vì sao Zero-Knowledge Architecture giúp dữ liệu an toàn?**

-   Mọi dữ liệu được mã hóa và giải mã **ngay trên thiết bị cá nhân** của người dùng trước khi gửi lên máy chủ Bitwarden.
    
-   Máy chủ chỉ lưu trữ dữ liệu dạng mã hóa (ciphertext) và hoàn toàn không biết Master Password hay khóa giải mã. Do đó, nếu máy chủ bị xâm nhập, hacker cũng chỉ thu được các chuỗi ký tự mã hóa vô nghĩa.
    

### **3. Thông số cấu hình công cụ Generator (tạo 3 mật khẩu riêng biệt)**

Để tạo 3 mật khẩu mạnh và độc lập cho **GitHub**,  **Vercel** và **Email nhóm**, hãy thiết lập bộ lọc trong Generator như sau:

-   **Độ dài (Length):** 16 – 20 ký tự (hoặc bật tùy chọn _Passphrase_ từ 4 từ trở lên).
    
-   **Bật các tùy chọn ký tự:**
    
    -   [x] Chữ hoa (`A-Z`)
        
    -   [x] Chữ thường (`a-z`)
        
    -   [x] Chữ số (`0-9`)
        
    -   [x] Ký tự đặc biệt (`!@#$%^&*...`)
        
-   _Lưu ý:_ Bấm nút tạo lại (Regenerate) 3 lần khác nhau để lấy **3 mật khẩu hoàn toàn riêng biệt** cho 3 dịch vụ trên.
    



### **Phần 3 –** Kích hoạt 2FA cho tài khoản GitHub tổ chức

1.  Trưởng nhóm định dùng **SMS OTP**. Giải thích vì sao nên dùng **Authenticator App (TOTP)** thay thế, nêu đúng **2 nhược điểm** của SMS OTP.
    
2.  Liệt kê đúng thứ tự các bước kích hoạt 2FA bằng **Google Authenticator** cho tài khoản GitHub tổ chức (từ mở cài đặt bảo mật đến khi có mã 6 số).
    
3.  Sau khi bật 2FA, hệ thống cấp **10 mã khôi phục** dự phòng. Nêu đúng nơi **nên** lưu trữ và nơi **không nên** lưu các mã này.
    

### **Phần 4 –** Bảo vệ Secrets trước khi push code

1.  Từ đoạn code ở mục 3b, chỉ ra chính xác **2 giá trị Secrets** đang bị hardcode.
    
2.  Viết lại đoạn code đúng chuẩn: dùng `process.env` để đọc biến môi trường thay vì hardcode.
    
3.  Viết nội dung đầy đủ của:
    
    -   File `.env` (chứa giá trị thật)
        
    -   File `.gitignore` (đảm bảo `.env` không bị đẩy lên Git)
        
    -   File `.env.example` (chia sẻ an toàn cho các thành viên khác)
        
4.  Áp dụng **Quy tắc 4 Bước Kiểm tra trước khi Push**, liệt kê những gì bạn kiểm tra trước khi bấm `git push` lần cuối để bàn giao dự án.
