<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Выбор персонажа</title>
<script src="https://telegram.org/js/telegram-web-app.js"></script>
<style>
  :root {
    --bg: var(--tg-theme-bg-color, #ffffff);
    --text: var(--tg-theme-text-color, #1c1c1e);
    --hint: var(--tg-theme-hint-color, #8e8e93);
    --accent: var(--tg-theme-button-color, #2481cc);
    --surface: var(--tg-theme-secondary-bg-color, #f2f2f7);
  }
  * { box-sizing: border-box; }
  body {
    margin: 0; padding: 16px 16px 32px;
    background: var(--bg); color: var(--text);
    font: 16px/1.4 -apple-system, "Segoe UI", Roboto, sans-serif;
  }
  main { max-width: 520px; margin: 0 auto; }
  h1 { font-size: 22px; margin: 4px 0 2px; }
  .sub { color: var(--hint); margin: 0 0 16px; }
  .grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
  .card {
    border: 2px solid transparent; border-radius: 14px; padding: 16px 12px;
    background: var(--surface); color: var(--text); font: inherit;
    text-align: center; cursor: pointer;
  }
  .card:active { transform: scale(0.97); }
  .card.picked { border-color: var(--accent); }
  .emoji { font-size: 40px; line-height: 1.1; }
  .name { font-weight: 600; margin-top: 8px; }
  .desc { color: var(--hint); font-size: 13px; margin-top: 2px; }
  .warn { color: var(--hint); text-align: center; margin-top: 16px; display: none; }
  button:focus-visible { outline: 2px solid var(--accent); outline-offset: 2px; }
</style>
</head>
<body>
<main>
  <h1>Выберите персонажа</h1>
  <p class="sub">Нажмите на карточку, и бот станет этим персонажем.</p>
  <div class="grid" id="grid"></div>
  <p class="warn" id="warn">Откройте это приложение из бота в Telegram.</p>
</main>
<script>
  const tg = window.Telegram.WebApp;
  tg.ready();
  tg.expand();

  // id должны совпадать с ключами CHARACTERS в bot.py
  const CHARACTERS = [
    { id: 'helper',   emoji: '🤝', name: 'Добрый помощник',    desc: 'Поможет с чем угодно' },
    { id: 'teacher',  emoji: '🎓', name: 'Учитель',            desc: 'Объяснит просто' },
    { id: 'sherlock', emoji: '🔍', name: 'Шерлок Холмс',       desc: 'Делает выводы из мелочей' },
    { id: 'pirate',   emoji: '🏴‍☠️', name: 'Пират',              desc: 'Морские словечки' },
    { id: 'cat',      emoji: '🐱', name: 'Мудрый кот',         desc: 'Спокойный и с юмором' },
    { id: 'friend',   emoji: '😏', name: 'Саркастичный друг',  desc: 'Подкалывает по-доброму' }
  ];

  const grid = document.getElementById('grid');
  CHARACTERS.forEach(c => {
    const b = document.createElement('button');
    b.type = 'button';
    b.className = 'card';
    b.innerHTML = '<div class="emoji">' + c.emoji + '</div>' +
                  '<div class="name">' + c.name + '</div>' +
                  '<div class="desc">' + c.desc + '</div>';
    b.onclick = () => {
      document.querySelectorAll('.card').forEach(x => x.classList.remove('picked'));
      b.classList.add('picked');
      if (tg.HapticFeedback) tg.HapticFeedback.impactOccurred('light');
      if (!tg.initData) {
        document.getElementById('warn').style.display = 'block';
        return;
      }
      tg.sendData(JSON.stringify({ character: c.id }));
    };
    grid.appendChild(b);
  });
</script>
</body>
</html>
