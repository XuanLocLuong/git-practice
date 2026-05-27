# Bài 9: Git rebase
---
### Định nghĩa: 
là một lệnh dùng để hợp nhất các thay đổi tư nhánh này qua nhánh khác (giống `git merge`) 

### Cú pháp: 
`git rebase tên_nhánh`

### So sánh `git rebase` và `git merge`:
1. *`git rebase`*
1.1. Cú pháp: `git rebase tên_nhánh`
1.2. Không tạo ra merge commit
1.3. Khả năng xử lý xung đột: Có thể cần xử lý xung đột nhiều lần đối với từng commit khi rebase
1.4. Sử dụng khi: Cần lịch sủ commit gọn gàng và tuyến tính; Khi gộp các thay đổi nhỏ hoặc commit không cần thiết

2. *`git merge`*
2.1. Cú pháp: `git merge tên_nhánh`
2.2. Tạo ra merge commit
2.3. Xử lý xung đột một lần duy nhất trong quá trình merge
2.4. Sử dụng khi: Cần giữ nguyên lịch sử phát triển code; Khi làm việc nhóm, cần giữ lịch sử rõ ràng

### Thực hành: 
#### Bài toán: 
Thực hiện sử dụng `git rebase` để hơp nhất nhánh `feature_init` vào trong `feature_test`, khi merge thì bị lỗi
![alt](/image/b9_1.png)

##### Các bước thực hiện
1. Xử lý xung đột tại các file được đánh dấu xung đột như bài 8: 
![alt](/image/b9_2.png)

2. Lưu lại các thay đổi:
![alt](/image/b9_3.png)

3. Tiếp tục quá trình rebase cho đến khi kết thúc bằng `git rebase --continue`:
![alt](/image/b9_4.png)