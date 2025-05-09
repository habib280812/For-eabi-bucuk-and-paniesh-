# For-eabi-bucuk-and-paniesh
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Puji-Pujian Eabi & Paniesh</title>
  <style>
    body {
      margin: 0;
      background: linear-gradient(135deg, #ffe6f7, #ffe);
      font-family: 'Comic Sans MS', cursive;
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      flex-direction: column;
    }

    .carousel {
      width: 90vw;
      max-width: 600px;
      height: 220px;
      background: #fff0f8;
      border-radius: 30px;
      box-shadow: 0 0 20px rgba(255,192,203,0.5);
      display: flex;
      overflow: hidden;
      position: relative;
    }

    .slide {
      min-width: 100%;
      height: 100%;
      transition: transform 0.8s ease;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 1.8rem;
      color: #ff69b4;
      padding: 20px;
      box-sizing: border-box;
      text-align: center;
    }

    .controls {
      margin-top: 20px;
    }

    .btn {
      background-color: #ffc0cb;
      border: none;
      padding: 10px 20px;
      border-radius: 25px;
      color: white;
      font-weight: bold;
      cursor: pointer;
      margin: 0 10px;
      transition: 0.3s ease;
    }

    .btn:hover {
      background-color: #ff69b4;
    }

    .sparkle {
      position: absolute;
      width: 10px;
      height: 10px;
      background: gold;
      border-radius: 50%;
      animation: sparkle 4s infinite;
    }

    @keyframes sparkle {
      from { transform: translateY(0); opacity: 1; }
      to { transform: translateY(-150px); opacity: 0; }
    }
  </style>
</head>
<body>

  <div class="carousel" id="carousel">
    <div class="slide">Eabi bucuk sangat comel macam gula kapas dan cool!</div>
    <div class="slide">Paniesh wangi macam bunga sakura musim bunga walaupun introvert!</div>
    <div class="slide">Mereka berdua macam anime couple paling sweet!</div>
  </div>

  <div class="controls">
    <button class="btn" onclick="prev()">←</button>
    <button class="btn" onclick="next()">→</button>
  </div>

  <!-- Sparkles -->
  <div class="sparkle" style="left: 20%; bottom: 0; animation-delay: 0s;"></div>
  <div class="sparkle" style="left: 50%; bottom: 0; animation-delay: 1s;"></div>
  <div class="sparkle" style="left: 80%; bottom: 0; animation-delay: 2s;"></div>

  <script>
    const carousel = document.getElementById("carousel");
    const slides = document.querySelectorAll(".slide");
    let index = 0;

    function showSlide(i) {
      carousel.style.transform = `translateX(-${i * 100}%)`;
    }

    function next() {
      index = (index + 1) % slides.length;
      showSlide(index);
    }

    function prev() {
      index = (index - 1 + slides.length) % slides.length;
      showSlide(index);
    }

    setInterval(next, 7000); // Auto slide
  </script>
</body>
</html>
