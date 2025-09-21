<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <title>WorldStudios</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #0f1724;
      color: #fff;
      text-align: center;
      margin: 0;
      padding: 0;
    }
    header {
      background: #7c3aed;
      padding: 20px;
      font-size: 32px;
      font-weight: bold;
    }
    main {
      margin-top: 40px;
    }
    textarea, input {
      width: 80%;
      max-width: 500px;
      margin: 10px 0;
      padding: 10px;
      border-radius: 8px;
      border: none;
    }
    button {
      padding: 12px 20px;
      background: #7c3aed;
      border: none;
      border-radius: 8px;
      color: #fff;
      font-weight: bold;
      cursor: pointer;
    }
    button:hover {
      background: #5b21b6;
    }
  </style>
</head>
<body>
  <header>WorldStudios</header>
  <main>
    <h2>Bize Ulaşın</h2>
    <input type="text" id="name" placeholder="Adınız"><br>
    <textarea id="message" placeholder="Mesajınızı yazın..."></textarea><br>
    <button onclick="sendMail()">Gönder</button>
  </main>

  <script>
    function sendMail() {
      const name = document.getElementById('name').value;
      const message = document.getElementById('message').value;
      if (!message) {
        alert('Lütfen mesaj yazın!');
        return;
      }
      const subject = encodeURIComponent('WorldStudios İletişim');
      const body = encodeURIComponent((name ? name + ' yazdı:\n\n' : '') + message);
      window.location.href = `mailto:kaos06898@gmail.com?subject=${subject}&body=${body}`;
    }
  </script>
</body>
</html>
