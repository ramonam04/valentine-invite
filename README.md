<!DOCTYPE html>
<html lang="ro">
<head>
  <meta charset="UTF-8">
  <title>Andrei 💘</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: linear-gradient(to bottom, #ffd6e8, #fff);
      text-align: center;
      overflow: hidden;
    }

    .page {
      display: none;
      padding: 80px 20px;
      animation: fade 0.7s;
    }

    .page.active {
      display: block;
    }

    h1 {
      color: #e6004c;
      font-size: 45px;
    }

    p {
      font-size: 24px;
      color: #444;
      max-width: 600px;
      margin: auto;
      margin-top: 20px;
    }

    button {
      margin-top: 50px;
      padding: 15px 35px;
      font-size: 20px;
      border: none;
      border-radius: 12px;
      cursor: pointer;
      background: #e6004c;
      color: white;
    }

    .btn2 {
      background: white;
      color: #e6004c;
      border: 2px solid #e6004c;
    }

    @keyframes fade {
      from {opacity: 0;}
      to {opacity: 1;}
    }

    .heart {
      position: absolute;
      font-size: 20px;
      animation: float 6s infinite;
      opacity: 0.6;
    }

    @keyframes float {
      0% {transform: translateY(0);}
      100% {transform: translateY(-800px);}
    }
  </style>
</head>

<body>

  <!-- Pagina 1 -->
  <div class="page active">
    <h1>Salut, Andrei 💘</h1>
    <p>
      Am făcut ceva special pentru tine…  
      un fel de mică “carte” digitală 🥰
    </p>
    <button onclick="nextPage()">Următoarea ➜</button>
  </div>

  <!-- Pagina 2 -->
  <div class="page">
    <h1>Pagina 1 din inimă ❤️</h1>
    <p>
      Nu știu cum faci…  
      dar reușești să-mi aduci liniște și zâmbet în același timp.
    </p>
    <button onclick="nextPage()">Mai departe ➜</button>
  </div>

  <!-- Pagina 3 -->
  <div class="page">
    <h1>Un pic amuzant 😄</h1>
    <p>
      Știi care e problema mea?  
      Că mă gândesc la tine mai des decât la mâncare…  
      și asta e grav 😂
    </p>
    <button onclick="nextPage()">Continuă ➜</button>
  </div>

  <!-- Pagina 4 -->
  <div class="page">
    <h1>Serios acum 🥺</h1>
    <p>
      Ești genul de băiat care face lucrurile mai frumoase  
      doar prin faptul că există.
    </p>
    <button onclick="nextPage()">Încă una ➜</button>
  </div>

  <!-- Pagina 5 FINAL -->
  <div class="page">
    <h1>Andrei… 💘</h1>
    <p>
      Vrei să fii Valentinul meu pe 14 februarie?  
      Promit râsete, îmbrățișări și poate un pupic bonus 😇
    </p>

    <button onclick="alert('YEEES! Abia aștept ❤️')">DA ❤️</button>
    <button class="btn2" id="noBtn">NU 🙄</button>
  </div>

<script>
  let current = 0;
  const pages = document.querySelectorAll(".page");

  function nextPage() {
    pages[current].classList.remove("active");
    current++;
    pages[current].classList.add("active");
  }

  // Butonul NU fuge 😄
  const noBtn = document.getElementById("noBtn");
  noBtn.addEventListener("mouseover", () => {
    noBtn.style.position = "absolute";
    noBtn.style.left = Math.random() * 80 + "%";
    noBtn.style.top = Math.random() * 80 + "%";
  });

  // inimioare animate
  for (let i = 0; i < 20; i++) {
    let heart = document.createElement("div");
    heart.className = "heart";
    heart.innerHTML = "💗";
    heart.style.left = Math.random() * 100 + "%";
    heart.style.top = Math.random() * 100 + "%";
    heart.style.animationDuration = (Math.random() * 3 + 3) + "s";
    document.body.appendChild(heart);
  }
</script>

</body>
</html>