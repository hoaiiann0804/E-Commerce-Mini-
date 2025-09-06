# 🛍️ Website Bán Hàng Mini

[![React](https://img.shields.io/badge/React-18.2.0-61DAFB?logo=react&logoColor=white)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0.2-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Node.js](https://img.shields.io/badge/Node.js-18.x-339933?logo=node.js&logoColor=white)](https://nodejs.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15.x-4169E1?logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Project Status](https://img.shields.io/badge/status-active_development-yellowgreen)](https://github.com/hoaiiann0804/WebsiteBanHangMini)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 🌟 Giới thiệu

**Website Bán Hàng Mini** là một ứng dụng thương mại điện tử full-stack, tích hợp chatbot AI (Gemini) và thanh toán Stripe, mang đến trải nghiệm mua sắm trực tuyến mượt mà, an toàn và responsive.

**Vai trò của tôi**:
- Phát triển toàn bộ frontend (React, TypeScript, Zustand) và backend (Node.js, Express, PostgreSQL).
- Tích hợp Stripe cho thanh toán và Gemini AI cho chatbot.
- Tối ưu hiệu suất với lazy loading, database indexing, và API caching.

## 🎯 Tính năng chính

### Phía người dùng
- 🔐 **Xác thực**: Đăng ký/đăng nhập với JWT, hỗ trợ vai trò khách hàng và admin.
- 🔍 **Quản lý sản phẩm**: Tìm kiếm, lọc sản phẩm theo danh mục, giá, và thuộc tính.
- 🛒 **Giỏ hàng**: Thêm/xóa sản phẩm, tính toán tổng tiền.
- 💳 **Thanh toán**: Tích hợp Stripe với webhook để xử lý giao dịch an toàn.
- 📱 **Responsive**: Giao diện tương thích mọi thiết bị, hỗ trợ đa ngôn ngữ (i18n).
- 🤖 **Chatbot AI**: Hỗ trợ khách hàng với Gemini AI, có chế độ fallback khi API không khả dụng.

### Phía quản trị
- 📊 **Dashboard**: Thống kê doanh thu và phân tích dữ liệu.
- 📦 **Quản lý sản phẩm**: CRUD sản phẩm, danh mục, và thuộc tính.
- 📝 **Quản lý đơn hàng**: Theo dõi và cập nhật trạng thái đơn hàng.
- 👥 **Quản lý người dùng**: Phân quyền admin và khách hàng.

## 🚀 Công nghệ sử dụng

- **Frontend**: React 18.2.0, TypeScript 5.0.2, Zustand, Tailwind CSS, Vite
- **Backend**: Node.js 18.x, Express, PostgreSQL 15.x, Sequelize
- **Dịch vụ bên ngoài**: Stripe (thanh toán), Gemini AI (chatbot)
- **Khác**: JWT, i18n, lazy loading, database indexing, RESTful API

## 📸 Hình ảnh demo

![Trang chủ](https://github.com/hoaiiann0804/WebsiteBanHangMini/raw/main/screenshots/homepage.png)
*Trang chủ với danh sách sản phẩm và thanh tìm kiếm*

![Chi tiết sản phẩm](https://github.com/hoaiiann0804/WebsiteBanHangMini/raw/main/screenshots/product-detail.png)
*Thông tin sản phẩm, variants, và đánh giá*

![Giỏ hàng](https://github.com/hoaiiann0804/WebsiteBanHangMini/raw/main/screenshots/cart.png)
*Quản lý sản phẩm trong giỏ hàng*

![Thanh toán](https://github.com/hoaiiann0804/WebsiteBanHangMini/raw/main/screenshots/payment.png)
*Thanh toán an toàn với Stripe*

![Admin Dashboard](https://github.com/hoaiiann0804/WebsiteBanHangMini/raw/main/screenshots/admin-home.png)
*Dashboard quản trị với thống kê doanh thu*

![Chatbot AI](https://github.com/hoaiiann0804/WebsiteBanHangMini/raw/main/screenshots/chatbot.png)
*Tương tác với Gemini AI*

## 🛠️ Cài đặt và chạy local

### Yêu cầu
- Node.js >= 18.x
- PostgreSQL >= 15.x
- Yarn hoặc npm
- API keys: [Stripe](https://stripe.com), [Gemini AI](https://ai.google.dev)

### Các bước cài đặt

1. **Clone repository**
   ```bash
   git clone https://github.com/hoaiiann0804/WebsiteBanHangMini.git
   cd WebsiteBanHangMini

Cài đặt dependencies
bash# Frontend
cd frontend
yarn install

# Backend
cd ../backend
yarn install

Cấu hình môi trường

Copy frontend/.env.example và backend/.env.example thành .env.
Cập nhật biến môi trường trong backend/.env:
envDB_URL=postgres://user:password@localhost:5432/ecommerce
STRIPE_KEY=your_stripe_key
GEMINI_API_KEY=your_gemini_api_key
JWT_SECRET=your_jwt_secret



Khởi tạo database
bash# Tạo database
psql -U postgres -c "CREATE DATABASE ecommerce;"

# Chạy migrations
cd backend
yarn migrate

# (Tùy chọn) Seed dữ liệu
yarn seed

Khởi động ứng dụng
bash# Backend
cd backend
yarn start

# Frontend
cd ../frontend
yarn dev

Truy cập

Website: http://localhost:3000
Admin dashboard: http://localhost:3000/admin
Tài khoản thử nghiệm:

Khách hàng: user@example.com / password123
Admin: admin@example.com / admin123





Lưu ý

Đảm bảo PostgreSQL chạy trên localhost:5432 hoặc cập nhật DB_URL.
Nếu thiếu API keys, ứng dụng chạy ở chế độ demo (thanh toán giả lập, chatbot fallback).
Để kiểm tra webhook Stripe trên local, sử dụng ngrok:
bashngrok http 3000


🔍 Kết quả đạt được

Tải trang dưới 2 giây nhờ lazy loading và API caching.
Chatbot AI trả lời trong <1 giây, cải thiện trải nghiệm người dùng.
Giao dịch thanh toán an toàn với Stripe và webhook.
Database tối ưu với indexing, giảm thời gian truy vấn.

📚 Bài học rút ra

Thành thạo tích hợp API bên thứ ba (Stripe, Gemini AI) và thiết kế RESTful API.
Học cách tối ưu hiệu suất với lazy loading, database indexing, và caching.
Giải quyết thách thức đa ngôn ngữ (i18n) với lazy loading translations.
Nâng cao kỹ năng debug trong môi trường full-stack.

📂 Cấu trúc dự án
textWebsiteBanHangMini/
├── frontend/                     # Giao diện người dùng và quản trị
│   ├── src/
│   │   ├── components/         # Component dùng chung
│   │   ├── pages/              # Các trang (trang chủ, sản phẩm, giỏ hàng, v.v.)
│   │   ├── features/           # Tính năng chính (auth, cart, payment)
│   │   └── assets/             # Hình ảnh, fonts
│   └── public/                 # Tài nguyên tĩnh
├── backend/                     # Backend Node.js
│   ├── src/
│   │   ├── controllers/        # API controllers
│   │   ├── models/             # Sequelize models
│   │   ├── routes/             # API routes
│   │   ├── services/           # Business logic
│   │   └── migrations/         # Database migrations
│   └── .env                    # Cấu hình môi trường
├── screenshots/                 # Ảnh chụp màn hình
└── README.md                   # Tài liệu dự án
🚀 Triển khai

Lưu ý: Triển khai hiện cần API keys hợp lệ cho Stripe và Gemini AI.

Triển khai Backend

Deploy trên Render hoặc Heroku.
Cấu hình PostgreSQL trên dịch vụ như Neon.
Cập nhật DB_URL và các biến môi trường trong dashboard của dịch vụ.

Triển khai Frontend

Build production:
bashcd frontend
yarn build

Deploy thư mục dist lên Vercel hoặc Netlify.

🤝 Đóng góp
Chúng tôi hoan nghênh mọi đóng góp! Để tham gia:

Fork repository này.
Tạo branch mới: git checkout -b feature/your-feature.
Commit thay đổi: git commit -m "feat: mô tả thay đổi".
Push branch: git push origin feature/your-feature.
Tạo Pull Request với mô tả chi tiết.

Xem CONTRIBUTING.md để biết thêm chi tiết.
📄 Giấy phép
Dự án được cấp phép theo MIT License.
📞 Liên hệ

Tên: Nguyễn Hoài An
GitHub: github.com/hoaiiann0804
Email: hoaiiann0804@gmail.com
Portfolio: your-portfolio.com (nếu có)
