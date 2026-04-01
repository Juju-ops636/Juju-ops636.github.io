# Juju-ops636.github.io
<canvas id="game" width="400" height="400" style="background:black"></canvas>
<script>
  const canvas = document.getElementById("game");
  const ctx = canvas.getContext("2d");
  let x = 200, y = 200, dx = 20, dy = 0;

  function draw() {
    ctx.clearRect(0, 0, 400, 400); // Clear screen
    x += dx; y += dy; // Move
    
    if (x < 0 || x >= 400 || y < 0 || y >= 400) { alert("Game Over!"); location.reload(); }
    
    ctx.fillStyle = "lime";
    ctx.fillRect(x, y, 18, 18); // Draw Player
    setTimeout(draw, 100);
  }

  window.onkeydown = (e) => {
    if (e.key === "ArrowUp") { dx = 0; dy = -20; }
    if (e.key === "ArrowDown") { dx = 0; dy = 20; }
    if (e.key === "ArrowLeft") { dx = -20; dy = 0; }
    if (e.key === "ArrowRight") { dx = 20; dy = 0; }
  };
  draw();
</script>
