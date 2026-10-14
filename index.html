<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Список дел</title>
<script src="https://telegram.org/js/telegram-web-app.js"></script>
<style>
  :root {
    --bg: var(--tg-theme-bg-color, #ffffff);
    --text: var(--tg-theme-text-color, #1c1c1e);
    --hint: var(--tg-theme-hint-color, #8e8e93);
    --accent: var(--tg-theme-button-color, #2481cc);
    --accent-text: var(--tg-theme-button-text-color, #ffffff);
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
  form { display: flex; gap: 8px; margin-bottom: 16px; }
  input[type=text] {
    flex: 1; padding: 12px; border: 0; border-radius: 10px;
    background: var(--surface); color: var(--text); font: inherit;
  }
  button.add {
    padding: 0 18px; border: 0; border-radius: 10px;
    background: var(--accent); color: var(--accent-text); font: inherit;
  }
  ul { list-style: none; margin: 0; padding: 0; }
  li {
    display: flex; align-items: center; gap: 12px;
    padding: 12px; margin-bottom: 8px; border-radius: 10px; background: var(--surface);
  }
  li label { flex: 1; word-break: break-word; }
  li.done label { color: var(--hint); text-decoration: line-through; }
  input[type=checkbox] { width: 20px; height: 20px; accent-color: var(--accent); }
  button.del {
    border: 0; background: none; color: var(--hint); font-size: 22px; line-height: 1; padding: 0 4px;
  }
  .empty { color: var(--hint); text-align: center; padding: 32px 0; }
  button:focus-visible, input:focus-visible { outline: 2px solid var(--accent); outline-offset: 2px; }
</style>
</head>
<body>
<main>
  <h1 id="title">Список дел</h1>
  <p class="sub" id="counter"></p>
  <form id="form">
    <input type="text" id="text" placeholder="Что нужно сделать?" maxlength="200" autocomplete="off">
    <button class="add" type="submit">Добавить</button>
  </form>
  <ul id="list"></ul>
  <p class="empty" id="empty">Пока пусто. Добавьте первое дело выше.</p>
</main>
<script>
  const tg = window.Telegram.WebApp;
  tg.ready();
  tg.expand();

  const user = tg.initDataUnsafe && tg.initDataUnsafe.user;
  if (user && user.first_name) {
    document.getElementById('title').textContent = user.first_name + ', ваши дела';
  }

  const KEY = 'todos';
  let todos = [];
  try { todos = JSON.parse(localStorage.getItem(KEY)) || []; } catch (e) { todos = []; }

  function save() {
    try { localStorage.setItem(KEY, JSON.stringify(todos)); } catch (e) {}
  }

  function render() {
    const list = document.getElementById('list');
    list.innerHTML = '';
    todos.forEach((t, i) => {
      const li = document.createElement('li');
      if (t.done) li.className = 'done';

      const cb = document.createElement('input');
      cb.type = 'checkbox';
      cb.checked = t.done;
      cb.id = 't' + i;
      cb.onchange = () => {
        t.done = cb.checked; save(); render();
        if (tg.HapticFeedback) tg.HapticFeedback.selectionChanged();
      };

      const label = document.createElement('label');
      label.htmlFor = cb.id;
      label.textContent = t.text;

      const del = document.createElement('button');
      del.className = 'del';
      del.type = 'button';
      del.setAttribute('aria-label', 'Удалить');
      del.textContent = '×';
      del.onclick = () => { todos.splice(i, 1); save(); render(); };

      li.append(cb, label, del);
      list.appendChild(li);
    });
    const left = todos.filter(t => !t.done).length;
    document.getElementById('counter').textContent =
      todos.length ? 'Осталось: ' + left + ' из ' + todos.length : '';
    document.getElementById('empty').style.display = todos.length ? 'none' : 'block';
  }

  document.getElementById('form').onsubmit = (e) => {
    e.preventDefault();
    const input = document.getElementById('text');
    const text = input.value.trim();
    if (!text) return;
    todos.unshift({ text, done: false });
    input.value = '';
    save(); render();
  };

  render();
</script>
</body>
</html>
