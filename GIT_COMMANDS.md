# Các Lệnh Git Để Đẩy Code Lên Nhánh Khác

## ⚠️ Nếu chưa có Git repository, khởi tạo trước:

```bash
# 1. Khởi tạo Git repository
git init

# 2. Thêm remote repository (thay YOUR_REPO_URL bằng URL thực tế)
git remote add origin YOUR_REPO_URL

# 3. Kiểm tra remote
git remote -v
```

## 🚀 Đẩy code lên nhánh khác (KHÔNG phải main):

### Cách 1: Tạo nhánh mới và push

```bash
# 1. Xem các file đã thay đổi
git status

# 2. Thêm tất cả các file đã thay đổi
git add .

# 3. Commit với message
git commit -m "Cải thiện trang Contact: thêm banner, tối ưu UI/UX, cập nhật form và map"

# 4. Tạo nhánh mới và chuyển sang nhánh đó
git checkout -b feature/contact-improvements

# Hoặc tên nhánh khác:
git checkout -b develop
# hoặc
git checkout -b hotfix/contact-update
# hoặc
git checkout -b contact-page

# 5. Đẩy code lên nhánh mới
git push origin feature/contact-improvements

# Hoặc nếu muốn set upstream ngay:
git push -u origin feature/contact-improvements
```

### Cách 2: Chuyển sang nhánh đã có sẵn

```bash
# 1. Xem tất cả các nhánh
git branch -a

# 2. Chuyển sang nhánh đã có
git checkout develop
# hoặc
git checkout feature/contact

# 3. Thêm và commit code
git add .
git commit -m "Cải thiện trang Contact: thêm banner, tối ưu UI/UX, cập nhật form và map"

# 4. Đẩy lên nhánh đó
git push origin develop
```

### Cách 3: Đẩy code hiện tại lên nhánh khác (không chuyển nhánh)

```bash
# 1. Thêm và commit code
git add .
git commit -m "Cải thiện trang Contact: thêm banner, tối ưu UI/UX, cập nhật form và map"

# 2. Đẩy trực tiếp lên nhánh khác (từ nhánh hiện tại)
git push origin HEAD:feature/contact-improvements
# hoặc
git push origin HEAD:develop
```

## 📝 Các lệnh để commit và push code (tổng quát):

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

