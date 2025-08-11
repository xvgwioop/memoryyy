<html lang="en">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login | Kantamxs</title>
  <<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'Comic Sans MS', cursive, sans-serif;
    background: url('https://i.postimg.cc/ZKppQytj/20250806-180912.jpg') no-repeat center center fixed;
    background-size: cover;
    height: 100vh;
    display: flex;
    justify-content: center; /* จัดกลางแนวนอน */
    align-items: center;     /* จัดกลางแนวตั้ง */
  }

  .center-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;
    max-width: 500px;
  }

  .login-box {
    background: rgba(255, 240, 245, 0.6);
    backdrop-filter: blur(8px);
    -webkit-backdrop-filter: blur(8px);
    padding: 30px;
    border-radius: 20px;
    text-align: center;
    width: 100%;
    box-shadow: 0 0 20px rgba(0,0,0,0.1);
  }

  h2 {
    color: #ff69b4;
    margin-bottom: 20px;
  }

  input[type="text"],
  input[type="password"] {
    padding: 17px;
    margin: 15px 0;
    width: 100%;
    border: 2px solid #ffb6c1;
    border-radius: 10px;
    font-size: 16px;
    outline: none;
  }

  button {
    padding: 15px 25px;
    background-color: #ff69b4;
    color: white;
    border: none;
    border-radius: 10px;
    cursor: pointer;
    font-size: 16px;
  }

  .hidden { display: none; }

  .image-container img {
    max-width: 100%;
    border-radius: 15px;
    margin-top: 20px;
    box-shadow: 0 0 15px rgba(0,0,0,0.2);
  }

  /* กล่องแจ้งเตือน */
  #errorBox {
    position: fixed;
    top: 50%; left: 50%;
    transform: translate(-50%, -50%);
    background: white;
    padding: 20px 30px;
    border-radius: 15px;
    box-shadow: 0 0 20px rgba(0,0,0,0.3);
    text-align: center;
    z-index: 9999;
  }

  #errorBox p {
    margin-bottom: 15px;
    color: #ff69b4;
    font-weight: bold;
  }

  #errorBox button {
    padding: 10px 20px;
    background: #ff69b4;
    color: white;
    border: none;
    border-radius: 10px;
    cursor: pointer;
  }
</style>
 </head>
 <body id="pageBody">
  <div class="center-container">
    <!-- กล่องล็อกอิน -->
    <div class="login-box" id="loginForm">
      <h2>Memory na Jzn 💖</h2>
      <input type="text" id="username" placeholder="Username na hubb">
      <input type="password" id="password" placeholder="Password (dd,mm)">
      <button type="button" onclick="login()">Login</button>
    </div>

    <!-- กล่องแสดงรูป -->
    <div class="login-box hidden" id="imageBox">
      <h2>Hi na hub JuneNae~ Kantamxs! 🌸</h2>
      <div class="image-container">
        <img src="https://i.postimg.cc/7ZJMV3h5/IMG-20241106-193518-819.jpg" alt="My Image">
      </div>
    </div>
  </div>

  <!-- กล่องแจ้งเตือน -->
  <div id="errorBox" class="hidden">
    <p>❌ Username หรือ Password ไม่ถูกต้อง</p>
    <button onclick="closeError()">ตกลง</button>
  </div>
</body>
  <script>
    function login() {
      const username = document.getElementById('username').value.trim();
      const password = document.getElementById('password').value.trim();

      if (username.toLowerCase() === 'kantamxs' && password === '2606') {
        document.getElementById('loginForm').classList.add('hidden');
        document.getElementById('imageBox').classList.remove('hidden');
        document.getElementById('pageBody').style.backgroundImage =
          "url('https://i.postimg.cc/ZR3vQCC6/8b57589a-f721-4045-a41f-cdce91ef30e5.jpg')";
        document.getElementById('pageBody').style.backgroundRepeat = "no-repeat";
        document.getElementById('pageBody').style.backgroundSize = "cover";
        document.getElementById('pageBody').style.backgroundPosition = "center";
      } else {
        document.getElementById('errorBox').classList.remove('hidden');
      }
    }

    function closeError() {
      document.getElementById('errorBox').classList.add('hidden');
    }
  </script>
 </body>
</html>
