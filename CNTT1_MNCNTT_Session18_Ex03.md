# BÀI TẬP VỀ NHÀ
##   Bài 3 : Xử lý lỗi bố cục giao diện hệ thống theo dõi xe
### Bài Làm
**4. Yêu cầu đầu ra**

**_Phần 1. Phân tích_**

1.   Vẽ lại sơ đồ Box Model hiện tại của phần tử lỗi qua tab **Computed**.
- Sơ đồ Box Model
       ┌────────────────────────────────────────────────────────┐
       │                 MARGIN           
       │   ┌────────────────────────────────────────────────┐   │
       │   │             BORDER          
       │   │   ┌────────────────────────────────────────┐   │   │
       │   │   │         PADDING 
       │   │   │   ┌────────────────────────────────┐   │   │   │
       │   │   │   │     CONTENT 
       │   │   │   └────────────────────────────────┘   │   │   │
       │   │   └────────────────────────────────────────┘   │   │
       │   └────────────────────────────────────────────────┘   │
       └────────────────────────────────────────────────────────┘

    

**_Phần 2. Triển khai_**

1. Đưa ra thông số CSS mới giúp sửa lỗi chồng lấn giao diện.
- Đầu tiên vào f12 và vào phần cần sửa và thêm lệnh PADDING 20px và MARGIN  21px thì sẽ sửa được lỗi chồng lấn giao diện.
    

**_Phần 3. Kiểm thử_**

1.   Giả định thay đổi Margin nhưng phần tử vẫn không di chuyển, hãy kiểm tra xem có thuộc tính nào đang ghi đè ở tầng Browser Engine không?
- Nếu thay đổi Margin mà phần tử vẫn không di chuyển thì kiểm tra và thấy các thẻ inline như `<span>`, `<a>`, `<i>` thì lệnh margin sẽ không hoạt động.

