<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Лендинг с Арканами</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #1a1a2e;
      color: #f3f3f3;
      margin: 0;
      padding: 20px;
      text-align: center;
    }
    .card-container {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-top: 50px;
    }
    .card {
      width: 200px;
      height: 300px;
      cursor: pointer;
      border: 2px solid #f3f3f3;
      border-radius: 10px;
      overflow: hidden;
      transition: transform 0.3s ease;
    }
    .card img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    .card:hover {
      transform: scale(1.1);
    }
    .description {
      display: none;
      margin-top: 20px;
      text-align: left;
      background: #2a2a3e;
      padding: 20px;
      border-radius: 10px;
    }
  </style>
</head>
<body>
  <h1>Светланыны Арканы</h1>
  <p>Познайте силу ваших арканов</p>
  <div class="card-container">
    <div class="card" id="luna">
      <img src="luna.png" alt="Луна">
    </div>
    <div class="card" id="kolesnica">
      <img src="kolesnica.png" alt="Колесница">
    </div>
    <div class="card" id="ierofant">
      <img src="ierofant.png" alt="Иерофант">
    </div>
  </div>

  <div class="description" id="luna-desc">
    <h2>18 Аркан - Луна</h2>
    <p>Это один из ваших главных талантов... (сюда добавьте текст описания).</p>
  </div>
  <div class="description" id="kolesnica-desc">
    <h2>7 Аркан - Колесница</h2>
    <p>Вторая карта указывает на главную провокацию души... (сюда добавьте текст описания).</p>
  </div>
  <div class="description" id="ierofant-desc">
    <h2>5 Аркан - Иерофант</h2>
    <p>Этот аркан показывает то, при каких обстоятельствах мы наполняемся ресурсом... (сюда добавьте текст описания).</p>
  </div>

  <script>
    const cards = document.querySelectorAll('.card');
    const descriptions = document.querySelectorAll('.description');

    cards.forEach(card => {
      card.addEventListener('click', () => {
        const id = card.id + '-desc';
        descriptions.forEach(desc => {
          desc.style.display = desc.id === id ? 'block' : 'none';
        });
      });
    });
  </script>
</body>
</html>
# Tarot-sveta
