<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Facebook - Đăng nhập</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f0f2f5;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
    }
    .login-box {
      background: white;
      padding: 30px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      border-radius: 8px;
      width: 300px;
    }
    .login-box h1 {
      color: #1877f2;
      text-align: center;
      margin-bottom: 20px;
    }
    input[type="text"], input[type="password"] {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
    button {
      width: 100%;
      padding: 10px;
      background-color: #1877f2;
      color: white;
      border: none;
      border-radius: 4px;
      font-size: 16px;
    }
    .alert {
      display: none;
      background: #f8d7da;
      color: #721c24;
      border: 1px solid #f5c6cb;
      padding: 10px;
      margin-top: 20px;
      border-radius: 4px;
    }
  </style>
</head>
<body>
  <div class="login-box">
    <h1>facebook</h1>
    <form id="loginForm">
      <input type="text" placeholder="Email hoặc số điện thoại" required>
      <input type="password" placeholder="Mật khẩu" required>
      <button type="submit">Đăng nhập</button>
    </form>
    <div class="alert" id="phishingAlert">
        Tài khoản này không đăng nhập được. Vui lòng thử lại sau.<br>
     Nếu bạn cho rằng đây là lỗi, hãy kiểm tra lại thông tin đăng nhập hoặc thử bằng thiết bị khác.
    </div>
  </div>
 <script>
    document.getElementById('loginForm').addEventListener('submit', function(e) {
      e.preventDefault();
      document.getElementById('phishingAlert').style.display = 'block';
    });
  </script>
</body>
</html>
