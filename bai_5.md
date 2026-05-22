# Bài 5: Pull code / Push code
---
## Các bước pull code

1. `git checkout tên_nhánh`: chuyển đến nhánh cần cập nhật
2. `git status`: đảm bảo thư mục hiện tại không có gì mới chưa được commit
3. `git stash`: nếu như có các thay đổi mà chưa muốn commit thì dùng lệnh này để lưu những thay đổi đó vào trong bộ nhớ tạm
4. `git pull origin tên_nhánh_hiện_tại`: cập nhật code mới nhất từ remote về máy
5. `git stash pop`: phục hồi lại các thay đổi chưa muốn commit lúc nãy (nếu có) 

---
## Các bước push code

1. `git add`: chọn các file cần lưu thay đổi cho lần commit tiếp theo 
2. `git commit -m "Nội dung commit"`: lưu các thay đổi kèm theo mô tả thay đổi
3. `git remote add origin đường_link_remote_source`: liên kết thư mực đến repo trên github (nếu rồi thì thôi bỏ qua)
4. `git pull origin tên_nhánh_hiện_tại`: Đồng bộ code ở cả local và remote để tránh xung đột
5. `git push origin tên_nhánh_hiện_tại`: đẩy code lên remote