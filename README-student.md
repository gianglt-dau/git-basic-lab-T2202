# Git Basic Lab — Student Guide

## Mục tiêu
Sau bài lab này, bạn sẽ:
- khởi tạo Git repository
- theo dõi thay đổi bằng `git status`
- lưu thay đổi bằng `git add` và `git commit`
- tạo branch
- merge branch về `main`

## Cấu trúc dự án
```text
git-basic-lab/
├── README.md
├── index.html
├── css/
│   └── style.css
└── js/
    └── app.js
```

## Bước 1: Kiểm tra cấu trúc source
Mở thư mục dự án và kiểm tra các file có sẵn:
- `index.html`
- `css/style.css`
- `js/app.js`

## Bước 2: Khởi tạo Git repository
Chạy:
```bash
git init
git status
```

Kết quả mong đợi:
- thư mục hiện tại trở thành Git repository
- các file đang ở trạng thái `untracked`

## Bước 3: Cấu hình Git user
Chạy:
```bash
git config user.name "Your Name"
git config user.email "your@email.com"
```

Kiểm tra:
```bash
git config --list
```

## Bước 4: Tạo commit đầu tiên
Chạy:
```bash
git add .
git commit -m "Initial commit: add starter website"
```

Kiểm tra lịch sử:
```bash
git log --oneline
```

## Bước 5: Cập nhật nội dung trang
Mở `index.html` và thay dòng:
```html
<p id="message">Hello Git</p>
```

thành:
```html
<p id="message">Hello Git Basic Lab</p>
```

Kiểm tra thay đổi:
```bash
git status
git diff
```

Commit thay đổi:
```bash
git add index.html
git commit -m "Update welcome message"
```

## Bước 6: Tạo branch mới
Chạy:
```bash
git switch -c feature/change-style
```

Kiểm tra branch hiện tại:
```bash
git branch
```

## Bước 7: Chỉnh giao diện trên branch mới
Mở file `css/style.css` và cập nhật thành:
```css
body {
  font-family: Arial, sans-serif;
  margin: 40px;
  background-color: #f5f5f5;
  color: #222;
}

h1 {
  margin-bottom: 12px;
}
```

Commit thay đổi:
```bash
git add css/style.css
git commit -m "Improve page style"
```

## Bước 8: Merge branch vào `main`
Chạy:
```bash
git switch main
git merge feature/change-style
```

## Bước 9: Xem lịch sử commit
Chạy:
```bash
git log --oneline --graph --all
```

## Yêu cầu nộp bài
Nộp các nội dung sau:
1. ảnh chụp `git log --oneline --graph --all`
2. ảnh chụp `git status`
3. source code cuối cùng
4. danh sách lệnh Git đã chạy

## Câu hỏi tự kiểm tra
1. `git add` dùng để làm gì?
2. `git commit` dùng để làm gì?
3. Khi nào nên tạo branch?
4. `git diff` cho biết điều gì?

## Gợi ý nếu gặp lỗi
- Dùng `git status` để xem Git đang hiểu trạng thái repo ra sao
- Dùng `git branch` để kiểm tra branch hiện tại
- Đọc kỹ thông báo lỗi trước khi chạy lệnh tiếp theo
