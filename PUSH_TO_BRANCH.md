# Hướng Dẫn Đẩy Code Lên Nhánh Khác

## 🎯 Các bước nhanh nhất:

```bash
# Bước 1: Thêm file đã sửa
git add Contact.html assets/contact.css

# Bước 2: Commit
git commit -m "Cải thiện trang Contact: thêm banner, tối ưu UI/UX, form và map"

# Bước 3: Tạo nhánh mới (hoặc chuyển sang nhánh đã có)
git checkout -b feature/contact-update

# Bước 4: Đẩy lên nhánh đó
git push -u origin feature/contact-update
```

## 📋 Tên nhánh gợi ý:

- `feature/contact-improvements`
- `develop`
- `contact-page`
- `hotfix/contact-update`
- `update/contact-form`

## 🔄 Nếu nhánh đã tồn tại trên remote:

```bash
# Lấy nhánh từ remote về
git fetch origin

# Chuyển sang nhánh đó
git checkout feature/contact-update

# Pull code mới nhất (nếu có)
git pull origin feature/contact-update

# Thêm và commit code của bạn
git add .
git commit -m "Cải thiện trang Contact"

# Push lên
git push origin feature/contact-update
```

