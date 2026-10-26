# BillSplit - Ứng dụng chia tiền nhóm

Ứng dụng web tĩnh hỗ trợ quản lý chi tiêu nhóm, tự động tính toán số tiền mỗi thành viên cần trả/nhận và tối ưu hóa số lượng giao dịch chuyển khoản.

## 🚀 Các cách chạy dự án ở Local

### Cách 1: Sử dụng npm & Live Server (Khuyên dùng - Hỗ trợ tự động tải lại khi sửa code)
1. Cài đặt các gói phụ thuộc (nếu chưa):
   ```bash
   npm install
   ```
2. Khởi chạy server:
   ```bash
   npm start
   # hoặc
   npm run dev
   ```
   Ứng dụng sẽ tự động mở trên trình duyệt tại địa chỉ `http://127.0.0.1:5500`.

---

### Cách 2: Sử dụng Python
Nếu máy tính đã cài đặt Python:
```bash
python -m http.server 5500
```
Sau đó mở trình duyệt và truy cập: `http://localhost:5500`

---

### Cách 3: Mở trực tiếp không cần server
Do đây là ứng dụng web tĩnh thuần (Vanilla HTML/CSS/JavaScript), bạn có thể click đúp chuột trực tiếp vào file `index.html` để mở trong trình duyệt.

---

## 🛠️ Công nghệ sử dụng
- **HTML5 / CSS3 / JavaScript (ES6+)**
- **Bootstrap 5**: Giao diện và layout responsive.
- **SweetAlert2**: Thông báo và hộp thoại xác nhận.
- **LocalStorage**: Tự động lưu trữ danh sách thành viên và các khoản chi tiêu ngay trên trình duyệt mà không cần backend/database.

## ✨ Tính năng chính
- Quản lý danh sách thành viên nhóm (thêm, sửa tên, xóa, khôi phục mặc định).
- Thêm / sửa / xóa các khoản chi tiêu linh hoạt:
  - Chia đều cho tất cả hoặc một nhóm thành viên được chọn.
  - Chia tùy biến (nhập số tiền cụ thể của từng người).
- Bảng tổng kết chi tiết: đã trả, đã tiêu, và số tiền chênh lệch (dương: được nhận lại, âm: phải trả thêm).
- Thuật toán tự động ghép cặp thanh toán nợ tối ưu nhất (giảm thiểu tối đa số lần chuyển khoản giữa các thành viên).
