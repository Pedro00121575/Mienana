# Mienana
Para usted 
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Mi hermosa</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to bottom, #ffafcc, #ffc8dd);
      overflow: hidden;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: sans-serif;
    }

    h1 {
      color: white;
      font-size: 3rem;
      text-shadow: 2px 2px 5px #c9184a;
    }

    .heart {
      width: 50px;
      height: 50px;
      position: absolute;
      background-color: red;
      transform: rotate(-45deg);
      animation: float 5s linear infinite;
    }

    .heart::before,
    .heart::after {
      content: "";
      width: 50px;
      height: 50px;
      position: absolute;
      background-color: red;
      border-radius: 50%;
    }

    .heart::before {
      top: -25px;
      left: 0;
    }

    .heart::after {
      left: 25px;
      top: 0;
    }

    @keyframes float {
      0% {
        transform: rotate(-45deg) translateY(0);
        opacity: 1;
      }
      100% {
        transform: rotate(-45deg) translateY(-100vh);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <h1>¡Muchos corazones para ti! ❤️</h1>

  <!-- Corazones flotantes -->
  <script>
    function crearCorazon() {
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = (Math.random() * 3 + 3) + 's';
      document.body.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 5000);
    }

    setInterval(crearCorazon, 300);
  </script>
</body>
</html>
