# For-eabi-bucuk-and-paniesh
<html lang="ms">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Eabi Bucuk & Paniesh</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to bottom, #fefefe, #f0f0ff);
      text-align: center;
      margin: 0;
      padding: 0;
      overflow-x: hidden;
    }

   header {
      background-color: #6c5ce7;
      color: white;
      padding: 20px;
      animation: fadeDown 1s ease-in-out;
    }

   .character {
      margin: 40px auto;
      max-width: 300px;
      opacity: 0;
      transform: translateY(50px);
      animation: slideUp 1s ease-out forwards;
    }
    .character:nth-child(2) {
      animation-delay: 0.5s;
    }

   .character:nth-child(3) {
      animation-delay: 1s;
    }
    .character img {
      border-radius: 50%;
      width: 100%;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
      transition: transform 0.3s;
    }
    .character img:hover {
      transform: scale(1.05);
    }
    h2 {
      color: #2d3436;
    }
    p {
      color: #636e72;
    }
    @keyframes slideUp {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

   @keyframes fadeDown {
      from {
        opacity: 0;
        transform: translateY(-30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
   }
    iframe {
      margin-top: 20px;
      border: none;
      width: 80%;
      max-width: 560px;
      height: 315px;
   }
  </style>
</head>
<body>
  <header>
    <h1>Selamat Datang ke Dunia Eabi Bucuk & Paniesh</h1>
  </header>

  <div class="character">
    <img src="eabi.jpg" alt="Eabi Bucuk">
    <h2>Eabi Bucuk</h2>
    <p>Si comel bertopeng dengan senyuman yang menawan!</p>
  </div>

  <div class="character">
    <img src="paniesh.jpg" alt="Paniesh">
    <h2>Paniesh</h2>
    <p>Kucing putih gebu dengan gaya penuh pesona!</p>
  </div>
 
  <iframe src="https://www.youtube.com/embed/0lMO0lSJ9lk?si=ZGGS8_TuPxlV1Hgw" 
          title="YouTube video player" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
          allowfullscreen>
  
