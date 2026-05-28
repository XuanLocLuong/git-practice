# Bài 11: Git patch
---
### Định nghĩa: 
Patch là một file văn bản (.patch) chứa các thay đổi của những dòng code chưa được commit, có thể áp dụng sau
---
### Cách sử dụng (dựa vào bài toán cụ thể)
#### Bài toán: 
Lưu lại các thay đổi chưa kịp commit vào trong một file .patch, xoá các dòng vừa được thay đổi đó đi và apply lại các thay đổi đó vào file đó
![alt](/image/b11_1.png)
#### Các bước áp dụng:
1. `git status`: xem các file chưa được add và commit
![alt](/image/b11_2.png)
2. `git diff > tên_file_patch.patch`: ném những thay đổi đó vào trong file .patch
![alt](/image/b11_3.png)
![alt](/image/b11_5.png)
3. Xoá các thay đổi đó đi, coi như là mình đang ở máy mới và vẫn chưa có các thay đổi đó (kiểm tra bằng `git status` xem có thay đổi nào không, trong hình ảnh sẽ có file my-patch.patch coi như là chưa tồn tại đi):
![alt](/image/b11_4.png)
4. `git apply tên_file_patch.patch`:cập nhật lại các thay đổi đó vào trong file:
![alt](/image/b11_6.png)