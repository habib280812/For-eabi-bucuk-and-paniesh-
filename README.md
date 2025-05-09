# For-eabi-bucuk-and-paniesh
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Eabi Bucuk & Paniesh Wangi</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(135deg, #ffd6e0, #ffe4f0);
      font-family: 'Comic Sans MS', cursive, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
    }
    .container {
      text-align: center;
      animation: popIn 1.5s ease-in-out;
    }
    .text {
      font-size: 2.5rem;
      color: #ff69b4;
      text-shadow: 2px 2px #fff;
      margin: 10px 0;
      animation: floatText 3s infinite ease-in-out;
    }
    @keyframes popIn {
      from {
        transform: scale(0);
        opacity: 0;
      }
      to {
        transform: scale(1);
        opacity: 1;
      }
    }
    @keyframes floatText {
      0%, 100% {
        transform: translateY(0);
      }
      50% {
        transform: translateY(-10px);
      }
    }
    .sparkles {
      position: absolute;
      width: 100%;
      height: 100%;
      pointer-events: none;
      overflow: hidden;
    }
    .sparkle {
      position: absolute;
      width: 10px;
      height: 10px;
      background: gold;
      border-radius: 50%;
      animation: sparkleMove 4s infinite;
      opacity: 0.7;
    }
    @keyframes sparkleMove {
      from {
        transform: translateY(0) scale(1);
        opacity: 1;
      }
      to {
        transform: translateY(-200px) scale(0.5);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="text">Eabi bucuk sangat comel!</div>
    <div class="text">Paniesh wangi macam bunga ros!</div>
    <div class="text">Memuji sampai cair!</div>
  </div>
  <div class="sparkles">
    <div class="sparkle" style="left: 20%; animation-delay: 0s;"></div>
    <div class="sparkle" style="left: 50%; animation-delay: 1s;"></div>
    <div class="sparkle" style="left: 80%; animation-delay: 2s;"></div>
  </div>

  <audio autoplay loop>
    <source src="https://open.spotify.com/track/2w0N1WsZ62BK9qgCFBKNoK?si=4ybTzaYRQwCQqqeOYTeb5Q&context=spotify%3Atrack%3A2w0N1WsZ62BK9qgCFBKNoK" type="audio/mpeg">
    Browser anda tidak menyokong audio.
  </audio>
</body>
</html>
