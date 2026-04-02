# Juju-ops636.github.io
!DOCTYPE html>
<html>
<head>
  <title>Jfox gamehub</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      margin: 0;
      font-family: Arial;
      background: linear-gradient(135deg, #000, #111);
      color: white;
      text-align: center;
    }

    h1 {
      margin-top: 20px;
      font-size: 32px;
    }

    .container {
      margin-top: 30px;
    }

    button {
      display: block;
      width: 250px;
      margin: 15px auto;
      padding: 15px;
      font-size: 18px;
      border: none;
      border-radius: 12px;
      background: red;
      color: white;
      cursor: pointer;
      transition: 0.2s;
    }

    button:hover {
      background: darkred;
      transform: scale(1.05);
    }

    iframe {
      width: 100%;
      height: 80vh;
      border: none;
      display: none;
    }
  </style>
</head>

<body>

<h1> Jfox gamehub</h1>

<div class="container">
  <button onclick="openGame()">Open Game App</button>
</div>

<iframe id="gameFrame"></iframe>

<script>
function openGame() {
  document.getElementById("gameFrame").style.display = "block";
  document.getElementById("gameFrame").src = "https://skip.nightly.pw/";
  <a href="https://skip.nightly.pw" target="_blank">
  <button>Play Games (Skip)</button>
</a>
