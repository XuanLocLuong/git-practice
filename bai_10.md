# Bài 10: Git cherry pick
---
### Định nghĩa: 
Dùng để chọn một hoặc một vài commit cụ thể từ nhánh khác để đắp vào nhánh của mình hiện tại, tóm lại nó khác `git rebase` và `git merge` nhưng ở chỗ `git rebase` và `git merge` sẽ lấy toàn bộ lịch sử code của nhánh khác gộp vào còn ở đây chỉ là lấy những thay đổi trong ở trong commit được chỉ định

---
#### Cách sử dụng: 
1. Dùng lệnh `git log --oneline` ở nhánh muốn lấy commit để xem mã commit muốn lấy để đắp vào trong nhánh khác
![alt](/image/b10_1.png)
2. Chuyển về nhánh làm việc: `git checkout tên_nhánh`
3. Thực hiện lệnh `git cherry-pick mã_commit` để đắp vào nhánh hiện tại các thay đổi trong commit đó

---
#### Thực hành: 
##### Bài toán:
Có hai nhánh master và feature_init, sẽ thêm hai commit vào trong feature_init, và sẽ gán commit số 1 vào trong master bằng `git cherry pick`
![alt](/image/b10_2.png)
![alt](/image/b10_3.png)
![alt](/image/b10_4.png)

###### Các bước:
1. `git log --oneline` lấy mã commit cherry pick 1 vừa rồi:
![alt](/image/b10_5.png)
2. checkout qua master và cập nhật mới nhất từ remote:
![alt](/image/b10_6.png)
3. `git cherry-pick mã_commit` để lấy commit cherry pick 1 chèn vào master:
![alt](/image/b10_7.png)