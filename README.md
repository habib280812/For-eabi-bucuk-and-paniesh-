# For-eabi-bucuk-and-paniesh
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Eabi & Paniesh Cute Slideshow</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to bottom right, #ffe6f7, #fff0f5);
      font-family: 'Comic Sans MS', cursive;
      overflow: hidden;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
    }

    .slider-container {
      position: relative;
      width: 90vw;
      max-width: 600px;
      height: 250px;
      overflow: hidden;
      border-radius: 30px;
      box-shadow: 0 0 20px rgba(255, 192, 203, 0.6);
      background-color: #fff;
      padding: 20px;
    }

    .slide {
      position: absolute;
      width: 100%;
      height: 100%;
      opacity: 0;
      transform: scale(0.9);
      transition: opacity 1s ease, transform 1s ease;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      font-size: 1.8rem;
      color: #ff69b4;
    }

    .slide.active {
      opacity: 1;
      transform: scale(1);
    }

    .bubble {
      background-color: #fff0fa;
      border-radius: 25px;
      padding: 20px;
      box-shadow: 0 5px 15px rgba(255,105,180,0.2);
      max-width: 90%;
      animation: pop 1s ease-in-out;
    }

    @keyframes pop {
      0% { transform: scale(0.8); opacity: 0; }
      100% { transform: scale(1); opacity: 1; }
    }

    .controls {
      margin-top: 15px;
    }

    .btn {
      background-color: #ffb6c1;
      border: none;
      padding: 10px 20px;
      margin: 0 10px;
      border-radius: 25px;
      font-size: 1rem;
      cursor: pointer;
      color: white;
      box-shadow: 0 2px 5px rgba(0,0,0,0.2);
      transition: background-color 0.3s ease;
    }

    .btn:hover {
      background-color: #ff69b4;
    }

    .sparkle {
      position: absolute;
      width: 8px;
      height: 8px;
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

  <div class="slider-container">
    <div class="slide active">
      <div class="bubble">Eabi bucuk sangat comel macam mochi!</div>
    </div>
    <div class="slide">
      <div class="bubble">Paniesh wangi macam bunga sakura yang baru kembang!</div>
    </div>
    <div class="slide">
      <div class="bubble">Eabi & Paniesh, combo cute meletops!</div>
    </div>
  </div>

  <div class="controls">
    <button class="btn" onclick="prevSlide()">← Sebelumnya</button>
    <button class="btn" onclick="nextSlide()">Seterusnya →</button>
  </div>

  <audio autoplay loop>
    <source src="audio/aku-budak-girl.mp3" type="audio/mpeg">
    Lagu tidak dapat dimainkan.
  </audio>

  <!-- Simple sparkles -->
  <div class="sparkle" style="left: 20%; top: 90%; animation-delay: 0s;"></div>
  <div class="sparkle" style="left: 50%; top: 95%; animation-delay: 1s;"></div>
  <div class="sparkle" style="left: 80%; top: 92%; animation-delay: 2s;"></div>

  <script>
    let slides = document.querySelectorAll('.slide');
    let current = 0;

    function showSlide(index) {
      slides.forEach((slide, i) => {
        slide.classList.toggle('active', i === index);
      });
    }

    function nextSlide() {
      current = (current + 1) % slides.length;
      showSlide(current);
    }

    function prevSlide() {
      current = (current - 1 + slides.length) % slides.length;
      showSlide(current);
    }

    setInterval(nextSlide, 8000); // Auto slide every 8s
  </script>
</body>
</html>
