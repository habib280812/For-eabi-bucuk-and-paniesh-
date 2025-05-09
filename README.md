# For-eabi-bucuk-and-paniesh
<!DOCTYPE html>
<html lang="ms">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Memuji Eabi Bucuk & Paniesh Wangi</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to right, #ff99cc, #ffccff);
      margin: 0;
      padding: 0;
      overflow-x: hidden;
      text-align: center;
    }
    header {
      background-color: #ff3399;
      color: white;
      padding: 40px;
      font-size: 2.5em;
      text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
      animation: headerAnimation 2s ease-in-out forwards;
    }
    @keyframes headerAnimation {
      from {
        opacity: 0;
        transform: translateY(-50px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
    .container {
      padding: 20px;
      margin: 0 auto;
      width: 80%;
      max-width: 1000px;
    }
    .character {
      display: inline-block;
      margin: 30px;
      text-align: center;
      opacity: 0;
      transform: translateY(50px);
      animation: characterAnimation 1.5s ease-out forwards;
    }
    .character:nth-child(2) {
      animation-delay: 1s;
    }
    .character:nth-child(3) {
      animation-delay: 2s;
    }
    .character img {
      border-radius: 50%;
      width: 250px;
      height: 250px;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
      transition: transform 0.3s ease;
    }
    .character img:hover {
      transform: scale(1.1);
    }
    h2 {
      font-size: 2em;
      color: #ff66b3;
      margin-top: 20px;
      animation: textAnimation 1.5s ease-in-out forwards;
    }
    p {
      font-size: 1.2em;
      color: #ff80bf;
      animation: textAnimation 2s ease-in-out forwards;
    }
    .praise {
      font-size: 2.2em;
      color: #ff4d94;
      font-weight: bold;
      animation: praiseAnimation 3s ease-out infinite;
    }
    @keyframes characterAnimation {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
    @keyframes textAnimation {
      0% {
        color: #ff66b3;
      }
      50% {
        color: #ff4d94;
      }
      100% {
        color: #ff66b3;
      }
    }
    @keyframes praiseAnimation {
      0% {
        transform: scale(1);
        opacity: 0;
      }
      50% {
        transform: scale(1.3);
        opacity: 1;
      }
      100% {
        transform: scale(1);
        opacity: 0;
      }
    }
    iframe {
      margin-top: 20px;
      width: 80%;
      height: 400px;
      border: none;
    }

  </style>
</head>
<body>

  <header>
    <h1>Memuji Eabi Bucuk & Paniesh Wangi!</h1>
  </header>

  <div class="container">
    <div class="character">
      <img src="eabi.jpg" alt="Eabi Bucuk">
      <h2>Eabi Bucuk</h2>
      <p>Si comel dengan topeng penuh misteri!</p>
      <div class="praise">Eabi, kamu adalah bintang yang bersinar terang!</div>
    </div>
    <div class="character">
      <img src="paniesh.jpg" alt="Paniesh Wangi">
      <h2>Paniesh Wangi</h2>
      <p>Kucing putih gebu yang penuh dengan pesona!</p>
      <div class="praise">Paniesh, kecantikanmu tiada tandingan!</div>
    </div>
  </div>

  <!-- Menyematkan video YouTube -->
  <iframe src="https://www.youtube.com/embed/0lMO0lSJ9lk?si=ZGGS8_TuPxlV1Hgw" 
          title="YouTube video player" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
          allowfullscreen>
  </iframe>

</body>
</html>
