# Bài 7: Wanosoft Git Flow
## Quy trình làm việc chung với git cho nhân viên Wanosoft
---
#### Bài toán chung
* Đã tạo Repository trên github, gitlab, ...
* Branch mặc định của Repository thường là master
* Đã thiết lập quyền cho người có quyền merge
* Developer có quyền truy cập, tạo nhánh mới, push code, tạo pull request
* Branch master, develop phải được bảo vệ để không push trực tiếp từ local lên các branch
---
#### Các nhánh chính
**Có hai nhánh chính luôn ở trạng thái code mới, chính xác và ổn định nhất:**
* `master`
* `develop`

Code trong develop ổn định và sẵn sàng được release thì sẽ được merge với `master`

---
#### Quy trình Git
* **Một tính năng sẽ tương ứng với một branch và có thể có nhiều commit**
1. Dev checkout sang `develop` và update code mới nhất về:
`git checkout develop` 
`git pull origin develop`
2. Tạo nhánh tương ứng với task đã được nhận theo công thức:
`git checkout -b feature/tên_feature`
3. Bắt đầu code
4. Sau khi code xong
* xoá các lệnh `console.log` trong code
* check lỗi lint nếu còn thì fix
5. Bắt đầu lưu các thay đổi:
`git add .`
`git commit -m "feature/tên_feature done"`
6. Push code lên remote:
`git push origin feature/tên_feature`
7. Tạo pull request trên repo
* là hợp nhất nhánh feature/tên_feature vào develop
7.1. Trường hợp bị conflict 
`git checkout develop`: checkout ra nhanh develop
`git pull origin develop`: cập nhật code mới nhất về
`git checkout feature/tên_feature`: chuyển qua checkout nhánh mình làm
`git merge develop`: merge nhánh develop vào và sửa 
`git add .` -> `git commit -m "feature/tên_feature fix conflict"` -> `git push origin feature/tên_feature`: cập nhật lại code mới nhất của nhánh mình lên nhánh mình trên remote sau khi sửa xong
8. gửi link url của pull request cho reviewer để review
8.1. Trường hợp cần sửa lại thì lại check lại tiếp và sửa lặp lại các bước add và commit và push cho đến bước 8
8.2. Trường hợp reviewer đồng ý pull request thì sẽ được merge bở reviewer và xong task 
---
### Nguyên tắc
* Mỗi pull request tương ứng với 1 task
* Một pull request không bị giới hạn commit
* Đặt branch name theo định dạng tên_task/mã_task (feature/23, bug/12, ..)
* Commit message nếu như tổng thể pull request chỉ có 1 commit thì đặt là `tên_task/mã_task mô_tả`
* Pull request title phải đặt giống với title của task được
* Ở phần mô tả pull request thêm link tài liệu của task
* Không được thay đổi code ở nhánh develop và master ở local. Chỉ được pull về từ remote 
---
### Đặt tên nhánh - Các trường hợp
* `feature/tên_task`: task được giao
* `bugfix/tên_task_ngày_tháng_năm`: bug trong quá trình dev
* `hotfix/tên_task_ngày_tháng_năm`: bug trên production