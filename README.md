<!DOCTYPE html>
<html lang="pt">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Rádio Lusa – Brisa Musical</title>
<style>
body {
  font-family: Arial, sans-serif;
  background:#f2f2f2;
  margin:0;
  padding:0;
  display:flex;
  justify-content:center;
  align-items:center;
  height:100vh;
}
.app {
  background:white;
  width:90%;
  max-width:380px;
  border-radius:20px;
  padding:20px;
  box-shadow:0 4px 10px rgba(0,0,0,0.2);
  text-align:center;
}
.logo {
  width:120px;
  border-radius:10px;
}
button {
  background:#d81b1b;
  color:white;
  border:none;
  padding:15px;
  width:100%;
  border-radius:10px;
  font-size:18px;
  cursor:pointer;
  margin-top:15px;
}
button:hover { background:#b01515; }
.info {
  margin-top:15px;
  font-size:14px;
  color:#555;
}
</style>
</head>
<body>

<div class="app">
  <img src="https://i.imgur.com/4ZQZ4ZQ.png" class="logo" alt="Rádio Lusa"/>
  <h2>🎤 Brisa Musical</h2>
  <p>com José Carvalho</p>

  <audio id="player" src="https://sp0.redeaudio.com/8232/stream"></audio>

  <button onclick="togglePlay()">▶️ Tocar Rádio</button>

  <div class="info">
    Rádio Lusa na internet • Stream ao vivo<br/>
    Programa: <strong>Brisa Musical</strong><br/>
    © 16 anos de rádio com coração português ❤️
  </div>
</div>

<script>
let playing = false;
function togglePlay() {
  const p = document.getElementById("player");
  if(!playing) {
    p.play();
    playing = true;
  } else {
    p.pause();
    playing = false;
  }
}
</script>

</body>
</html>
