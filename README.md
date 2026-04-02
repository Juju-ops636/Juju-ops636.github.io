<!DOCTYPE html>
<html>
<head>
  <title>My Game Hub</title>
  <style>
    body {
      margin: 0;
      font-family: Arial;
      background: #111;
      color: white;
      text-align: center;
    }

    header {
      background: red;
      padding: 20px;
      font-size: 28px;
      font-weight: bold;
    }

    .games {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 20px;
      padding: 20px;
    }

    .card {
      background: #222;
      padding: 20px;
      border-radius: 15px;
      transition: 0.2s;
    }

    .card:hover {
      transform: scale(1.05);
      background: #333;
    }

    button {
      margin-top: 10px;
      padding: 10px 20px;
      border: none;
      border-radius: 10px;
      background: red;
      color: white;
      cursor: pointer;
    }

    iframe {
      width: 100%;
      height: 500px;
      border: none;
      margin-top: 20px;
    }
  </style>
</head>

<body>

<header>🎮 My Game Hub</header>

<div class="games">

  <!-- Skip Game -->
  <div class="card">
    <h2>Skip Games</h2>
    <p>Play unblocked games</p>
    <button onclick="openSkip()">Play</button>
  </div>

  <!-- Example Other Game -->
  <div class="card">
    <h2>Mini Game</h2>
    <p>Coming soon</p>
    <button onclick="alert('Add your own games here!')">Play</button>
  </div>

</div>

<script>
function openSkip() {
  // Opens skip in a new tab (most reliable)
  window.open("https://skip.nightly.pw", "_blank");
