# BÀI TẬP VỀ NHÀ
## Bài 9: Thiết Kế Kiến Trúc Két Sắt Số Bitwarden Và Chính Sách Mật Khẩu Game Studio
### Bài làm
**4. Yêu cầu đầu ra**

**Phần 1: Báo cáo phân tích kiến trúc an ninh mật khẩu**

**1.** Phân tích vì sao thói quen lưu mật khẩu trên trình duyệt Google Chrome (tệp `Login Data`) lại cực kỳ nguy hiểm đối với lập trình viên khi máy tính bị nhiễm mã độc Infostealer?


- Vì khi bị nhiễm mã độc infostealer một khi bị nhiễm tài khoản google chrome với tài khoản mật khẩu đã lưu trực tiếp sẽ dễ bị đánh cắp và tuôn ra bên ngoài gây lộ dự án dữ liệu cá nhân của lập trình viên.

**2.** Giải thích bản chất kỹ thuật của Kiến trúc Zero-Knowledge và cơ chế Client-side Decryption: Nếu máy chủ đám mây của Bitwarden bị hacker tấn công, dữ liệu Két sắt của PixelForge Studio có bị giải mã không? Vì sao?
 
- Kỹ thuật của kiến trúc Zero-Knowledge là một phương pháp một bên thuyết phục một bên khác điều ấy là sự thật mà không lộ bất kỳ thông tin nào.
- Cơ chế Client-side Decryption là giải mã dữ liệu mã hóa ngày trên máy tính của mình trước khi hiện thị, thay vì giải mã trên server.
-  Nếu máy chủ đám mây của Bitwarden bị hacker tấn công hoàn toàn vào dữ liệu két sắt của pixelforge studio sẽ không bị giải mã vì nhớ kiến trúc Zero-Knowledge buộc hacker tin những thông tin ảo là sự thật dữ liệu két sắt được mã hóa ngay tại thiết bị của người dùng trước khi gửi lên đám mây.

**Phần 2: Thiết kế Chính sách & Kịch bản Chuyển đổi**

**3.** Thiết kế phương pháp tạo một Master Passphrase đạt chuẩn: Dài tối thiểu 20 ký tự, dễ nhớ đối với con người nhưng bất khả thi đối với các cỗ máy tấn công vét cạn (Brute-Force Attack). Đưa ra 01 ví dụ cụ thể về Passphrase chuẩn.

- Bước 1: thay vì để mật khẩu một chuỗi dễ nhỡ hay thêm 3-4 ký tự độc lập thành những câu vô lý.
- Bước 2: tăng tính ngẫu nhiên cho mật khẩu thêm các kí tự -,_ . 
- Bước 3: Công thức tối ưu cho người Việt:

$$\text{[Từ 1 (Viết hoa)]} + \text{[Ký tự phân tách]} + \text{[Từ 2]} + \text{[Từ 3]} + \text{[Số ngẫu nhiên]} + \text{[Từ 4]}$$ 

**4.** Xây dựng bảng cấu hình chuẩn cho công cụ Generator trong Bitwarden để áp dụng thống nhất cho 40 tài khoản của studio (Quy định độ dài, loại ký tự hoa/thường/số/ký tự đặc biệt).


- Cấu hình  Generator trong Bitwarden là sẽ tạo ngẫu nhiên loại mật khẩu độ dài khoảng 20-24
ký tự có chữ hoa, chữ thường, chữ số, ký tự đặc biệt, tránh ký tự dễ nhầm. 


**5.** Giải thích vì sao tính năng Tự động Điền (Auto-fill) của Bitwarden lại có khả năng chống tấn công Phishing giả mạo tên miền (như `githúb.com` hay `steampowered.xyz`) hiệu quả hơn con người?
  
- Vì Bitwarden kiểm tra từ chữ một với trang web chúng ta add vào chính xác từng hệ thống không bị đánh lừa.
- Với Bitwarden sẽ phát hiện ra tên miền hoàn toàn khác và sẽ không điền mật khẩu vào trang web fake đó.

**6.** Thiết lập quy trình lưu trữ Khóa Cấp cứu (Emergency Kit) để đảm bảo Trưởng nhóm có thể khôi phục quyền truy cập nếu Trưởng phòng Kỹ thuật gặp sự cố đột xuất.
1.  **In và niêm phong:** Tải file PDF Emergency Kit từ Bitwarden, in ra bản cứng, cho vào phong bì dán kín và ký giáp lai.
    
2.  **Lưu trữ phân tán:** Giao bản cứng cho Trưởng nhóm cất vào tủ khóa an toàn tại văn phòng; lưu bản số đã mã hóa vào két sắt số của ban quản lý.
    
3.  **Kích hoạt khẩn cấp (Break-Glass):** Khi Trưởng phòng Kỹ thuật gặp sự cố đột xuất, Trưởng nhóm mở niêm phong bản cứng để lấy thông tin khôi phục quyền quản trị, đảm bảo không gián đoạn hoạt động studio.


-
