# Love[valentine.html](https://github.com/user-attachments/files/25050347/valentine.html)
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Will You Be My Valentine?</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      font-family: 'Arial', sans-serif;
    }

    .card {
      background: white;
      padding: 40px;
      border-radius: 20px;
      text-align: center;
      box-shadow: 0 10px 25px rgba(0,0,0,0.2);
    }

    h1 {
      color: #e63946;
      margin-bottom: 20px;
    }

    button {
      padding: 12px 25px;
      font-size: 18px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      margin: 10px;
    }

    #yes {
      background-color: #ff4d6d;
      color: white;
    }

    #no {
      background-color: #adb5bd;
      color: white;
      position: absolute;
    }
  </style>
</head>
<body>

  <div class="card">
    <h1>Will you be my Valentine? 💖</h1>
    <button id="yes" onclick="yesClicked()">Yes 💕</button>
    <button id="no" onmouseover="moveNo()">No 😢</button>
  </div>

  <script>
    function yesClicked() {
      document.body.innerHTML = `
        <div style="
          height:100vh;
          display:flex;
          justify-content:center;
          align-items:center;
          background:linear-gradient(135deg,#ff9a9e,#fad0c4);
          font-family:Arial;
        ">
          <h1 style="color:#e63946;">
            Yay! I knew it 😍💘
          </h1>
        </div>
      `;
    }

    function moveNo() {
      const noBtn = document.getElementById("no");
      const x = Math.random() * (window.innerWidth - 100);
      const y = Math.random() * (window.innerHeight - 50);
      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    }
  </script>

</body>
</html>
