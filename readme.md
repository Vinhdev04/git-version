# Làm việc với git
@author: @Vinhdev04 
---
## 📜 Xem lịch sử commit
- **git log**: Xem chi tiết toàn bộ lịch sử commit
- 👉 Hiển thị đầy đủ: commit ID, author, ngày, message
```
    git log
```
![git log](image/readme/1776630848775.png)
---
- **git log --oneline**: Xem nhanh, mỗi commit 1 dòng
- 👉 Dễ đọc, gọn nhẹ
```
    git log --oneline 
```
![git log --oneline ](image/readme/1776630912952.png)
---
- **git log --oneline --graph**: Hiển thị dạng cây (branch)
- 👉 Giúp thấy rõ nhánh, merge, HEAD
```
    git log --oneline --graph --decorate --all 
```
![git log --oneline --graph*](image/readme/1776630976521.png)
---
- **git log -p**: Xem chi tiết thay đổi code trong từng commit
- 👉 Hiển thị diff (code thay đổi)
```
    git log -p
```
![git log -p](image/readme/1776631029709.png)
---
- **git log file_name**: Xem lịch sử của 1 file
```
    git log file_name
```
![git log file_name](image/readme/1776631066811.png)
---
- **git log --author=author_name**: Lọc commit theo người tạo
```
    git log --author=author_name
```
![git log --author=author_name](image/readme/1776631099030.png)
---
- **git log --since=date**: Lọc theo thời gian
```
    git log --since=date
```
![git log --since=date](image/readme/1776631174841.png)
---
- **git commit --amend**: Sửa commit gần nhất
- 👉 Dùng khi:
    + sửa message
    + thêm/bớt file đã commit
- ⚠️ Commit sẽ bị đổi ID (hash)
```
    git commit --amend
```
![git commit --amend](image/readme/1776631302955.png)
![git commit --amend](image/readme/1776631316452.png)
---
**git push origin add_header  -f**: Ghi đè lịch sử trên remote
- 👉 Dùng khi đã --amend hoặc rebase
- ⚠️ Cẩn thận:
    + Có thể ghi đè commit của người khác
- ✅ Khuyến nghị dùng an toàn hơn: `git push --force-with-lease`

```
    git push origin add_header  -f
```
![git push origin add_header  -f ](image/readme/1776631446272.png)
---
**git diff**: git diff là lệnh dùng để `so sánh sự khác nhau (diff) giữa các phiên bản file trong Git.`
- 👉 Nói đơn giản: nó cho bạn biết bạn đã thay đổi gì trong code.
```
    git diff
```
- 👉 Hiển thị thay đổi giữa working directory và staging area
![git diff](image/readme/1776631936425.png)
-   🧠 Cách hoạt động
    -   So sánh giữa:
        -   file hiện tại (working directory)
        -   với phiên bản đã được lưu trong Git (commit hoặc staging)
**git diff**→ xem thay đổi chưa add
**git diff --staged** → xem thay đổi đã add
**git diff commit1 commit2** → so sánh 2 commit
---