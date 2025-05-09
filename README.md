# For-eabi-bucuk-and-paniesh
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Kucing Comel Pujian</title>
  <style>
    body {
      margin: 0;
      font-family: 'Comic Sans MS', cursive;
      background: linear-gradient(to bottom right, #fff0f5, #ffe4e1);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
      flex-direction: column;
    }

    .slider {
      width: 320px;
      height: 360px;
      overflow: hidden;
      border-radius: 30px;
      box-shadow: 0 0 25px rgba(255,182,193,0.5);
      background-color: #fff0fa;
      position: relative;
    }

    .slides {
      display: flex;
      width: 100%;
      height: 100%;
      transition: transform 0.6s ease-in-out;
    }

    .slide {
      min-width: 100%;
      box-sizing: border-box;
      padding: 20px;
      text-align: center;
    }

    .slide img {
      width: 150px;
      height: 150px;
      object-fit: contain;
      border-radius: 20px;
      margin-bottom: 15px;
    }

    .text {
      font-size: 1.2rem;
      background-color: #ffe6f7;
      padding: 15px;
      border-radius: 20px;
      color: #ff69b4;
      box-shadow: 0 0 10px rgba(255,105,180,0.2);
      animation: fadeIn 1s ease;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: scale(0.95); }
      to { opacity: 1; transform: scale(1); }
    }

    .controls {
      margin-top: 20px;
    }

    .btn {
      background: #ffb6c1;
      border: none;
      padding: 10px 20px;
      border-radius: 25px;
      color: white;
      font-weight: bold;
      cursor: pointer;
      margin: 0 10px;
    }

    .btn:hover {
      background: #ff69b4;
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
      to { transform: translateY(-120px); opacity: 0; }
    }
  </style>
</head>
<body>

  <div class="slider">
    <div class="slides" id="slides">
      <div class="slide">
        <img src="https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif" alt="Cat 1">
        <div class="text">Eabi bucuk, you're purr-fect!</div>
      </div>
      <div class="slide">
        <img src="https://media.giphy.com/media/v6aOjy0Qo1fIA/giphy.gif" alt="Cat 2">
        <div class="text">So fluffy and lovely, macam Paniesh!</div>
      </div>
      <div class="slide">
        <img src="https://media.giphy.com/media/13borq7Zo2kulO/giphy.gif" alt="Cat 3">
        <div class="text">Cutest kitty in town! Sama macam kamu!</div>
      </div>
    </div>
  </div>

  <div class="controls">
    <button class="btn" onclick="prevSlide()">←</button>
    <button class="btn" onclick="nextSlide()">→</button>
  </div>

  <!-- Sparkles -->
  <div class="sparkle" style="left: 20%; bottom: 0;"></div>
  <div class="sparkle" style="left: 50%; bottom: 0; animation-delay: 1s;"></div>
  <div class="sparkle" style="left: 80%; bottom: 0; animation-delay: 2s;"></div>

  <script>
    const slides = document.getElementById('slides');
    const totalSlides = document.querySelectorAll('.slide').length;
    let index = 0;

    function updateSlide() {
      slides.style.transform = `translateX(-${index * 100}%)`;
    }

    function nextSlide() {
      index = (index + 1) % totalSlides;
      updateSlide();
    }

    function prevSlide() {
      index = (index - 1 + totalSlides) % totalSlides;
      updateSlide();
    }

    setInterval(nextSlide, 6000); // Auto slide
  </script>
</body>
</html>
