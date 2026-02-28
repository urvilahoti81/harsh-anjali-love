# harsh-anjali-love
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Only Anjali 💖</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600&family=Poppins:wght@300;400&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box}

body{
  min-height:100vh;
  background: radial-gradient(circle at top,#2b1055,#12001f);
  font-family:'Poppins',sans-serif;
  color:#fff;
  display:flex;
  align-items:center;
  justify-content:center;
  overflow:hidden;
}

/* LOCK SCREEN */
.lock{
  text-align:center;
  padding:40px 25px;
  width:90%;
  max-width:360px;
  background:rgba(255,255,255,0.08);
  backdrop-filter:blur(12px);
  border-radius:26px;
  box-shadow:0 0 40px rgba(255,105,180,0.35);
  animation:fadeIn 1.2s ease;
}

.lock h1{
  font-family:'Playfair Display',serif;
  color:#ffd1e8;
  margin-bottom:10px;
}

.lock p{
  font-size:0.9rem;
  color:#f4cfe1;
  margin-bottom:20px;
}

input{
  width:100%;
  padding:12px;
  border:none;
  border-radius:14px;
  outline:none;
  text-align:center;
  font-size:1rem;
}

button{
  margin-top:15px;
  width:100%;
  padding:12px;
  border:none;
  border-radius:14px;
  background:#ff5fa2;
  color:#fff;
  font-size:1rem;
  cursor:pointer;
}

.error{
  margin-top:10px;
  font-size:0.8rem;
  color:#ffb3c7;
  display:none;
}

/* LETTER */
.letter{
  display:none;
  width:90%;
  max-width:380px;
  background:rgba(255,255,255,0.12);
  backdrop-filter:blur(14px);
  border-radius:26px;
  padding:45px 30px;
  text-align:center;
  animation:open 1.2s ease forwards;
}

.letter h2{
  font-family:'Playfair Display',serif;
  font-size:2rem;
  color:#ffd6ec;
}

.names{
  color:#ffb3d9;
  margin-bottom:15px;
}

.heart{
  font-size:3rem;
  margin:20px 0;
  animation:pulse 1.5s infinite;
}

.message{
  font-size:0.95rem;
  line-height:1.8;
  color:#fff0f7;
}

.signature{
  margin-top:20px;
  font-size:0.85rem;
  color:#eec3d8;
}

/* Floating Hearts */
.floating{
  position:absolute;
  bottom:-40px;
  font-size:18px;
  color:rgba(255,182,193,0.45);
  animation:floatUp 7s linear infinite;
}

/* Animations */
@keyframes pulse{
  0%{transform:scale(1)}
  50%{transform:scale(1.2)}
  100%{transform:scale(1)}
}
@keyframes floatUp{
  0%{transform:translateY(0);opacity:0}
  20%{opacity:1}
  100%{transform:translateY(-110vh);opacity:0}
}
@keyframes fadeIn{
  from{opacity:0;transform:translateY(20px)}
  to{opacity:1;transform:translateY(0)}
}
@keyframes open{
  from{opacity:0;transform:scale(0.9)}
  to{opacity:1;transform:scale(1)}
}
</style>
</head>

<body>

<!-- LOCK -->
<div class="lock" id="lock">
  <h1>🔒 Locked</h1>
  <p>Only <b>Anjali</b> can open this</p>
  <input type="text" id="key" placeholder="Enter your name ❤️">
  <button onclick="unlock()">Unlock</button>
  <div class="error" id="error">Wrong key… but cute try 😌</div>
</div>

<!-- LETTER -->
<div class="letter" id="letter">
  <h2>Happy One Month 💍</h2>
  <div class="names">Harsh ❤️ Anjali</div>

  <div class="heart">❤️</div>

  <div class="message">
    On <b>06/02/2026</b>,  
    we promised forever — and somehow,  
    one month later, it already feels timeless.<br><br>

    Every smile, every argument, every silence  
    feels warmer because it’s with you.<br><br>

    This page unlocks with your name  
    because my life unlocked the same day you said yes.
  </div>

  <div class="signature">
    — Forever yours, Harsh 💖
  </div>
</div>

<!-- MUSIC -->
<audio id="music" loop>
  <source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_8bfc1a52e6.mp3" type="audio/mpeg">
</audio>

<!-- FLOATING HEARTS -->
<span class="floating" style="left:10%;animation-delay:0s">❤</span>
<span class="floating" style="left:30%;animation-delay:2s">❤</span>
<span class="floating" style="left:50%;animation-delay:4s">❤</span>
<span class="floating" style="left:70%;animation-delay:1s">❤</span>
<span class="floating" style="left:90%;animation-delay:3s">❤</span>

<script>
function unlock(){
  const key=document.getElementById("key").value.trim().toLowerCase();
  if(key==="anjali"){
    document.getElementById("lock").style.display="none";
    document.getElementById("letter").style.display="block";
    document.getElementById("music").play();
  } else {
    document.getElementById("error").style.display="block";
  }
}
</script>

</body>
</html>
