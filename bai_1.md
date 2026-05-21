# Bai 1

## Mục đích sử dụng git: 
Sử dụng git để quản lý các version, lịch sử thay đổi của project

---

## Các khái niệm cơ bản:

### Branch: 
Branch là nhánh, chứa các version khác nhau của project, một project có thể có nhiều branch, có thể đặt tên cho chúng

### master: 
master là một branch chính, không được push code trực tiếp lên master, chỉ được merge từ nhánh khác vào, các nhánh khác ban đầu được tạo từ master

### checkout -b tên_nhánh: 
câu lệnh dùng để bắt đầu thực hiện code trên một nhánh nào đó

### push code: 
là đẩy code từ máy tính local lên repo

Các bước push code: git add . -> git commit -m "thông điệp" -> git push code tên_nhánh

### conflict: 
là khi hai nhanh đang cùng push lên master thì xảy ra xung đột do code đang bị đè lên nhau cùng một chỗ

### merge: 
là khi merge code từ nhánh này vào nhánh kia

---

## Đã set up xong name và email 
(ảnh: b1_setupnameandemail.png)

---

## Bài toán 1: được ghi trong ảnh
+ Tạo repo: (ảnh: b1_bt1_1.png)
+ Cài đặt nhánh chính là master: (ảnh: b1_bt1_2.png)
+ ở dưới local tạo 1 branch tên feature_init: (ảnh_b1_bt1_3.png)
+ đẩy code lên branch feature_init: (ảnh: b1_bt1_4.png)
+ kiểm tra: (ảnh: b1_bt1_5.png)

(Thực hành push bằng ssh)