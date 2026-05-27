# Bài 8: Xử lý conflict

#### Bài toán: 
* Hai nhánh master và feature_init có sự khác nhau trong trong một file 
<img src="/image/b8_1.png">
<img src="/image/b8_2.png">
* Merge master vào feature_init sẽ xảy ra lỗi 
<img src="/image/b8_3.png">
* Các bước xử lý
1. Xử lý conflict trên giao diện VS Code: 
1.1. Tìm đến các file có hiện ra các lựa chọn để xử lý conflict ở các hàng đó là:
* Accept Current Change: nếu muốn giữ lại code của nhánh hiện tại
* Accept Incoming Change: nếu muốn lấy câu code từ nhánh master cho vào
* Accept Both Change: nếu muốn giữ lại cả hai đoạn code đó
<img src="/image/b8_3.png">
1.2. Click chọn, VS Code sẽ cập nhật lại đoạn code đó theo lựa chọn
<img src="/image/b8_4.png">
2. Tiếp tục quá trình gộp code trên terminal/git bash: 
2.1. Lưu các thay đổi chỉnh sửa ở nhánh hiện tại (ở đây là feature_init)
<img src="/image/b8_5.png">
2.2. Sau đó sẽ hoàn tất quá trinh merge code ở trên
<img src="/image/b8_6.png">
2.3. Đẩy lại code lên remote của nhánh hiện tại