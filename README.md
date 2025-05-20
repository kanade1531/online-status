<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>明日方舟账号状态</title>
  <style>
    body {
      font-family: sans-serif;
      text-align: center;
      margin-top: 50px;
    }
    .status {
      font-size: 24px;
      padding: 20px;
      border: 2px solid #333;
      display: inline-block;
      border-radius: 10px;
      margin-bottom: 20px;
    }
    .online {
      color: green;
    }
    .offline {
      color: red;
    }
    button {
      padding: 10px 20px;
      font-size: 16px;
      border-radius: 8px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h1>明日方舟账号状态</h1>
  <div id="status" class="status offline">🔴 当前：账号未使用</div>
  <p id="time">更新时间：-</p>
  <button onclick="toggleStatus()">切换状态</button>

  <script>
    function toggleStatus() {
      const statusEl = document.getElementById('status');
      const timeEl = document.getElementById('time');
      const now = new Date().toLocaleString();

      if (statusEl.classList.contains('offline')) {
        statusEl.classList.remove('offline');
        statusEl.classList.add('online');
        statusEl.textContent = '🟢 当前：小明 正在使用账号';
      } else {
        statusEl.classList.remove('online');
        statusEl.classList.add('offline');
        statusEl.textContent = '🔴 当前：账号未使用';
      }

      timeEl.textContent = '更新时间：' + now;
    }
  </script>
</body>
</html>
