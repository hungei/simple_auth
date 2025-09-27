# Simple Authentication Demo

Dự án demo các phương thức xác thực trong Node.js Express, bao gồm Basic Authentication và Cookie-based Authentication.

## Cấu trúc dự án

- `basic_auth.js` - Demo Basic Authentication
- `cookie_auth.js` - Demo Cookie-based Authentication với MongoDB
- `package.json` - Dependencies và scripts
- `img/` - Thư mục chứa hình ảnh demo

## Cài đặt

```bash
npm install
```

## Chạy ứng dụng

### Basic Authentication Demo
```bash
node basic_auth.js
```
Server sẽ chạy tại: http://localhost:3000

### Cookie Authentication Demo
```bash
node cookie_auth.js
```
**Lưu ý:** Cần có MongoDB chạy tại localhost:27017

## API Endpoints

### Basic Auth (basic_auth.js)
- `GET /` - Public route
- `GET /public` - Public route
- `GET /secure` - Protected route (cần Basic Auth)
  - Username: `admin`
  - Password: `12345`

### Cookie Auth (cookie_auth.js)
- `POST /login` - Đăng nhập và tạo cookie
- `GET /profile` - Protected route (cần cookie hợp lệ)
- `POST /logout` - Đăng xuất và xóa cookie

## Test với Postman

### 1. Public Route
![Public route](./img/image1.png)

### 2. Secure Route với Basic Auth
![Secure route Basic Auth](./img/image2.png)

### 3. Login với Cookie Auth
![Cookie Auth Login](./img/image3.png)

### 4. Protected Route với Cookie
![Protected Route Cookie](./img/image4.png)

### 5. Logout
![Logout](./img/image5.png)

## Thông tin xác thực

### Basic Auth
- Username: `admin`
- Password: `12345`

### Cookie Auth
- Username: `admin`
- Password: `12345`
- Role: `adsys`
