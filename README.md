<!DOCTYPE html>
<html>
<head>
  <title>Game Hub</title>
  <style>
    body {
      margin: 0;
      font-family: Arial;
      background: #0f0f0f;
      color: white;
    }

    header {
      background: #1a1a1a;
      padding: 15px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    header h1 {
      margin: 0;
      color: red;
    }

    #search {
      padding: 8px;
      border-radius: 8px;
      border: none;
      outline: none;
    }

    .games {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
      gap: 20px;
      padding: 20px;
    }

    .card {
      background: #1c1c1c;
      border-radius: 15px;
      padding: 15px;
      text-align: center;
      transition: 0.2s;
    }

    .card:hover {
      transform: scale(1.05);
      background: #2a2a2a;
    }

    .card img {
      width: 100%;
      border-radius: 10px;
    }

    button {
      margin-top: 10px;
      padding: 8px 15px;
      border: none;
      border-radius: 8px;
      background: red;
      color: white;
      cursor: pointer;
    }

    #player {
      width: 100%;
      height: 500px;
      border: none;
      display: none;
    }
  </style>
</head>

<body>

<header>
  <h1>🎮 Game Hub</h1>
  <input type="text" id="search" placeholder="Search games..." onkeyup="searchGames()">
</header>

<iframe id="player"></iframe>

<div class="games" id="gameList">

  <!-- Game 1 -->
  <div class="card" data-name="skip games">
    <img src="https://via.placeholder.com/200x120">
    <h3>Skip Games</h3>
    <button onclick="openGame('https://skip.nightly.pw')">Play</button>
  </div>

  <!-- Game 2 -->
  <div class="card" data-name="slope">
    <img src="https://via.placeholder.com/200x120">
    <h3>Slope</h3>
    <button onclick="openGame('https://ubg100.github.io/slope/')">Play</button>
  </div>

  <!-- Game 3 -->
  <div class="card" data-name="run 3">
    <img src="https://via.placeholder.com/200x120">
    <h3>Run 3</h3>
    <button onclick="openGame('https://ubg100.github.io/run-3/')">Play</button>
  </div>

</div>

<script>
function openGame(url) {
  let player = document.getElementById("player");
  player.style.display = "block";
  player.src = url;
  window.scrollTo(0, 0);
}

function searchGames() {
  let input = document.getElementById("search").value.toLowerCase();
  let games = document.querySelectorAll(".card");

  games.forEach(game => {
    let name = game.getAttribute("data-name");
    if (name.includes(input)) {
      game.style.display = "block";
    } else {
      game.style.display = "none";
function openGame(url) {
  const iframeAllowed = url.includes("ubg100.github.io"); // Only these games
  let player = document.getElementById("player");

  if (iframeAllowed) {
    player.style.display = "block";
    player.src = url;
    window.scrollTo(0, 0);
  } else {
    window.open(url, "_blank");
  }
}
<!DOCTYPE html>
<html>
<head>
  <title>Game Hub</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #0f0f0f;
      color: white;
    }

    header {
      background: #1a1a1a;
      padding: 15px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    header h1 {
      margin: 0;
      color: red;
    }

    #search {
      padding: 8px;
      border-radius: 8px;
      border: none;
      outline: none;
    }

    .games {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
      gap: 20px;
      padding: 20px;
    }

    .card {
      background: #1c1c1c;
      border-radius: 15px;
      padding: 15px;
      text-align: center;
      transition: 0.2s;
    }

    .card:hover {
      transform: scale(1.05);
      background: #2a2a2a;
    }

    .card img {
      width: 100%;
      border-radius: 10px;
    }

    button {
      margin-top: 10px;
      padding: 8px 15px;
      border: none;
      border-radius: 8px;
      background: red;
      color: white;
      cursor: pointer;
    }

    #player {
      width: 100%;
      height: 500px;
      border: none;
      display: none;
      margin-top: 20px;
    }
  </style>
</head>

<body>

<header>
  <h1>🎮 Game Hub</h1>
  <input type="text" id="search" placeholder="Search games..." onkeyup="searchGames()">
</header>

<iframe id="player"></iframe>

<div class="games" id="gameList">

  <!-- Game 1: Skip Games (opens in new tab) -->
  <div class="card" data-name="skip games">
    <img src="https://via.placeholder.com/200x120">
    <h3>Skip Games</h3>
    <button onclick="openGame('https://skip.nightly.pw', false)">Play</button>
  </div>

  <!-- Game 2: Slope (iframe allowed) -->
  <div class="card" data-name="slope">
    <img src="https://via.placeholder.com/200x120">
    <h3>Slope</h3>
    <button onclick="openGame('https://ubg100.github.io/slope/', true)">Play</button>
  </div>

  <!-- Game 3: Run 3 (iframe allowed) -->
  <div class="card" data-name="run 3">
    <img src="https://via.placeholder.com/200x120">
    <h3>Run 3</h3>
    <button onclick="openGame('https://ubg100.github.io/run-3/', true)">Play</button>
  </div>

</div>

<script>
function openGame(url, useIframe) {
  const player = document.getElementById("player");

  if (useIframe) {
    player.style.display = "block";
    player.src = url;
    window.scrollTo({ top: 0, behavior: "smooth" });
  } else {
    window.open(url, "_blank");
  }
}

function searchGames() {
  const input = document.getElementById("search").value.toLowerCase();
  const games = document.querySelectorAll(".card");

  games.forEach(game => {
    const name = game.getAttribute("data-name");
    game.style.display = name.includes(input) ? "block" : "none";
  });
}
</script>

</body>
</html>
