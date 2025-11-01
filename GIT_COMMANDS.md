# Các Lệnh Git Để Đẩy Code Lên Repository

## Nếu chưa có Git repository, khởi tạo trước:

```bash
# 1. Khởi tạo Git repository
git init

# 2. Thêm remote repository (thay YOUR_REPO_URL bằng URL thực tế)
git remote add origin YOUR_REPO_URL

# 3. Kiểm tra remote
git remote -v
```

## Các lệnh để commit và push code:

```bash
# 1. Xem các file đã thay đổi
git status

# 2. Thêm tất cả các file đã thay đổi vào staging area
git add .

# Hoặc thêm từng file cụ thể:
git add Contact.html
git add assets/contact.css

# 3. Commit với message mô tả
git commit -m "Cải thiện trang Contact: thêm banner, tối ưu UI/UX, cập nhật form và map"

# 4. Kiểm tra branch hiện tại
git branch

# 5. Tạo branch mới (nếu cần)
git checkout -b feature/improve-contact-page

# Hoặc chuyển sang branch đã có
git checkout main
# hoặc
git checkout master

# 6. Đẩy code lên remote repository
git push origin main

# Hoặc nếu branch là master:
git push origin master

# Hoặc nếu đang ở branch mới:
git push origin feature/improve-contact-page
```

## Lệnh đầy đủ (từng bước):

```bash
# Bước 1: Xem trạng thái
git status

# Bước 2: Thêm file
git add Contact.html assets/contact.css

# Bước 3: Commit
git commit -m "Update: Cải thiện trang Contact với banner, form optimization và UI enhancements"

# Bước 4: Push lên GitHub/GitLab
git push origin main
```

## Nếu gặp lỗi khi push:

```bash
# Lấy code mới nhất từ remote trước
git pull origin main --rebase

# Sau đó push lại
git push origin main
```

## Nếu remote repository chưa tồn tại:

1. Tạo repository mới trên GitHub/GitLab
2. Copy URL repository
3. Chạy lệnh:
```bash
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

