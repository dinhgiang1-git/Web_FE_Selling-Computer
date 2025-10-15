```markdown
# Web_FE_Selling-Computer

Frontend cho dự án website bán máy tính / linh kiện — giao diện, chức năng giỏ hàng và đặt hàng, quản lý tài khoản người dùng.

---

## Tổng quan

Web_FE_Selling-Computer là phần frontend (ứng dụng SPA) xây dựng bằng Vue 3 và Vite. Mục tiêu của dự án là cung cấp giao diện thân thiện cho người dùng để:
- Duyệt và tìm kiếm sản phẩm (laptop, linh kiện, phụ kiện).
- Xem chi tiết sản phẩm, thông số kỹ thuật.
- Thêm / xóa sản phẩm trong giỏ hàng và thực hiện đặt hàng.
- Quản lý thông tin người dùng (đăng nhập/đăng ký, cập nhật địa chỉ).

Frontend hiện tương tác với API backend trên `http://localhost:3000/api` (xem trong các helper: `FE_HTTT/src/helpers/*.js`).

---

## Tính năng chính
- Hiển thị danh sách sản phẩm và trang chi tiết sản phẩm.
- Tìm kiếm / lọc sản phẩm theo thuộc tính.
- Giỏ hàng: thêm/xóa, cập nhật số lượng.
- Đặt hàng: gửi đơn hàng và cập nhật trạng thái (ví dụ: Payment component).
- Quản lý tài khoản: lưu token JWT vào localStorage, lấy thông tin user từ API.
- Responsive UI (thiết kế hoạt động trên desktop/mobile).
- Component hóa với Header, Footer, SlideBarMenu, ProductDetail, Payment, UserDetail, v.v.

---

## Công nghệ sử dụng
- Frontend: Vue 3 (Composition API)
- Build tool: Vite
- State management: Pinia
- Router: Vue Router
- HTTP client: Axios
- Hỗ trợ: dayjs, jwt-decode
- CSS: SCSS / Sass

Thông tin từ `FE_HTTT/package.json`:
- node engine: ^20.19.0 || >=22.12.0
- script tiêu chuẩn: `dev`, `build`, `preview`

---

## Yêu cầu
- Node.js (phiên bản theo package.json: Node 20+ hoặc 22.12+)
- npm hoặc pnpm/yarn
- Backend API chạy tại `http://localhost:3000/api` (hoặc cấu hình lại biến môi trường tương ứng)

---

## Cài đặt & chạy (frontend)
1. Clone repository:
   ```bash
   git clone https://github.com/dinhgiang1-git/Web_FE_Selling-Computer.git
   ```

2. Vào thư mục frontend và cài dependencies:
   ```bash
   cd Web_FE_HTTT/FE_HTTT || cd Web_FE_Selling-Computer/FE_HTTT
   npm install
   ```

3. (Tùy chọn) Thiết lập biến môi trường:
   - Tạo file `.env` hoặc `.env.local` trong `FE_HTTT` nếu muốn override API base URL:
     ```
     VITE_API_BASE_URL=http://localhost:3000/api
     ```

4. Chạy ứng dụng trong môi trường phát triển:
   ```bash
   npm run dev
   ```
   Mở trình duyệt theo URL được Vite cung cấp (mặc định http://localhost:5173).

5. Build để deploy:
   ```bash
   npm run build
   npm run preview
   ```

---

## Demo (Hình ảnh giao diện)

Dưới đây là chỗ dành cho ảnh demo

- Trang chủ
  ![Trang chủ](/FE_HTTT/assets/demo/home.png)

- Trang danh sách sản phẩm
  ![Danh sách sản phẩm](/FE_HTTT/assets/demo/products-list.png)

- Trang chi tiết sản phẩm
  ![Chi tiết sản phẩm](/FE_HTTT/assets/demo/product-detail.png)

- Giỏ hàng & Thanh toán
  ![Giỏ hàng](/FE_HTTT/assets/demo/cart.png)

## Cấu trúc thư mục chính (tổng quan)
- FE_HTTT/
  - src/
    - components/        # Các component UI (Header, Footer, ProductDetail, Payment, ...)
    - layouts/           # AppLayout.vue
    - views/             # Các view/route (Dashboard, trang sản phẩm, v.v.)
    - helpers/           # Hàm gọi API: user.js, order.js, ...
    - assets/            # Hình ảnh, icon, ...
    - styles/            # SCSS chung
  - package.json
- index.js               # file root (placeholder)
- README.md

---

## Liên hệ
- Email: dinhgiang1.edu@gmail.com  
- GitHub: https://github.com/dinhgiang1-git

---
```
