<!DOCTYPE html>
<html lang="en">
<head>

<meta charset="UTF-8">

<meta name="viewport"
      content="width=device-width, initial-scale=1.0,
               maximum-scale=1.0, user-scalable=no">

<meta name="theme-color" content="#c05f82">

<title>The Us Story ❤️</title>

<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>

<style>

:root{
  --rose:#c05f82;
  --deep:#91445f;
  --pink:#ffe8ef;
  --soft:#e8adbd;
  --cream:#fffaf8;
  --paper:rgba(255,253,251,.96);
  --text:#593c45;
  --muted:#80616a;
  --shadow:rgba(90,45,65,.14);
}

*{
  box-sizing:border-box;
}

html{
  scroll-behavior:smooth;
}

body{
  margin:0;
  font-family:Arial,Helvetica,sans-serif;
  color:var(--text);

  background:
    linear-gradient(
      rgba(255,250,248,.88),
      rgba(255,250,248,.94)
    ),
    url("./file_00000000b66082118bbde5d0666da038.png");

  background-size:cover;
  background-position:center;
  background-attachment:fixed;
}

button,
input,
textarea{
  font:inherit;
}

button{
  cursor:pointer;
}

.hidden{
  display:none !important;
}

/* =========================
   HEADER
========================= */

header{
  position:sticky;
  top:0;
  z-index:1000;

  background:rgba(255,250,248,.9);

  backdrop-filter:blur(14px);

  border-bottom:
    1px solid rgba(192,95,130,.12);
}

.nav{
  max-width:1050px;
  margin:auto;

  padding:13px 18px;

  display:flex;
  align-items:center;
  justify-content:space-between;

  gap:10px;
}

.logo{
  color:var(--deep);
  font-size:20px;
  font-weight:900;
}

.nav-buttons{
  display:flex;
  gap:7px;
  flex-wrap:wrap;
  justify-content:flex-end;
}

.nav-buttons button{
  border:0;
  background:var(--pink);
  color:var(--deep);

  padding:8px 12px;

  border-radius:999px;
  font-weight:700;
}

.nav-buttons button:hover{
  background:var(--soft);
}

/* =========================
   HERO
========================= */

.hero{
  max-width:1050px;
  margin:0 auto;

  min-height:75vh;

  padding:60px 20px 40px;

  display:flex;
  align-items:center;
  justify-content:center;

  text-align:center;
}

.hero-card{
  width:min(850px,100%);

  background:var(--paper);

  border-radius:32px;

  padding:42px 24px;

  box-shadow:
    0 20px 60px var(--shadow);

  border:
    1px solid rgba(192,95,130,.12);
}

.teddy{
  font-size:80px;

  animation:
    teddyFloat 2.4s ease-in-out infinite;
}

@keyframes teddyFloat{

  0%,100%{
    transform:
      translateY(0)
      rotate(-2deg);
  }

  50%{
    transform:
      translateY(-12px)
      rotate(2deg);
  }

}

.hero h1{
  margin:12px 0 8px;

  font-size:
    clamp(34px,7vw,64px);

  color:var(--deep);
}

.hero p{
  color:var(--muted);

  font-size:17px;
  line-height:1.7;

  max-width:680px;

  margin:12px auto;
}

/* =========================
   MAIN
========================= */

main{
  max-width:1050px;

  margin:auto;

  padding:
    10px 18px 70px;
}

.card{
  background:var(--paper);

  border-radius:26px;

  padding:25px;

  margin:22px 0;

  box-shadow:
    0 14px 40px var(--shadow);

  border:
    1px solid rgba(192,95,130,.10);
}

.card h2{
  color:var(--deep);
  margin-top:0;
}

/* =========================
   TIMERS
========================= */

.timer-grid{
  display:grid;

  grid-template-columns:
    repeat(3,1fr);

  gap:15px;
}

.timer-card{
  text-align:center;

  background:
    linear-gradient(
      145deg,
      #fff,
      var(--pink)
    );

  border-radius:22px;

  padding:22px 14px;

  box-shadow:
    0 8px 25px var(--shadow);
}

.timer-icon{
  font-size:40px;
}

.timer-title{
  font-weight:800;

  color:var(--deep);

  margin:8px 0;
}

.timer-value{
  font-size:
    clamp(20px,4vw,30px);

  font-weight:900;

  color:var(--rose);

  line-height:1.4;
}

.timer-small{
  font-size:12px;
  color:var(--muted);
  margin-top:7px;
}

@media(max-width:750px){

  .timer-grid{
    grid-template-columns:1fr;
  }

}

/* =========================
   BUTTONS
========================= */

.primary{
  border:0;

  background:var(--rose);
  color:#fff;

  padding:12px 20px;

  border-radius:999px;

  font-weight:800;

  box-shadow:
    0 7px 18px
    rgba(145,68,95,.2);
}

.secondary{
  border:0;

  background:var(--pink);
  color:var(--deep);

  padding:11px 18px;

  border-radius:999px;

  font-weight:800;
}

.primary:active,
.secondary:active{
  transform:scale(.97);
}

/* =========================
   LOGIN
========================= */

.form{
  display:grid;

  gap:12px;

  max-width:520px;

  margin:auto;
}

.form input,
.form textarea{
  width:100%;

  border:
    1px solid
    rgba(192,95,130,.2);

  background:#fff;

  border-radius:15px;

  padding:13px 15px;

  color:var(--text);

  outline:none;
}

.form textarea{
  min-height:110px;
  resize:vertical;
}

.form input:focus,
.form textarea:focus{
  border-color:var(--rose);
}

.auth-status{
  text-align:center;

  margin:10px 0;

  color:var(--muted);

  font-size:14px;
}

/* =========================
   MEMORIES
========================= */

.memory-form{
  display:grid;
  gap:12px;
}

.memory-grid{
  display:grid;

  grid-template-columns:
    repeat(3,1fr);

  gap:16px;

  margin-top:20px;
}

.memory{
  background:#fff;

  border-radius:20px;

  overflow:hidden;

  box-shadow:
    0 7px 20px var(--shadow);
}

.memory img{
  width:100%;

  height:190px;

  object-fit:cover;

  display:block;
}

.memory-content{
  padding:15px;
}

.memory-content h3{
  margin:0 0 5px;
  color:var(--deep);
}

.memory-date{
  font-size:12px;

  color:var(--rose);

  font-weight:700;

  margin-bottom:8px;
}

.memory-content p{
  color:var(--muted);

  line-height:1.6;

  white-space:pre-wrap;
}

@media(max-width:800px){

  .memory-grid{
    grid-template-columns:
      repeat(2,1fr);
  }

}

@media(max-width:560px){

  .memory-grid{
    grid-template-columns:1fr;
  }

}

/* =========================
   MUSIC
========================= */

.music-box{
  text-align:center;
}

.music-box audio{
  width:100%;
  max-width:600px;
}

/* =========================================================
   LOVE RUN GAME
========================================================= */

.game-intro{
  text-align:center;

  color:var(--muted);

  line-height:1.7;

  margin:
    0 auto 18px;

  max-width:650px;
}

.runner{

  position:relative;

  width:100%;

  height:250px;

  overflow:hidden;

  border-radius:24px;

  background:
    linear-gradient(
      to bottom,
      #fff1f6 0%,
      #ffe4ed 55%,
      #f8cbd9 56%,
      #f1b7ca 100%
    );

  border:
    2px solid
    rgba(192,95,130,.18);

  box-shadow:
    inset
    0 0 30px
    rgba(255,255,255,.45);

  touch-action:none;

  user-select:none;

  -webkit-user-select:none;
}

.runner::before{

  content:"";

  position:absolute;

  width:180px;
  height:180px;

  border-radius:50%;

  background:
    rgba(255,255,255,.35);

  right:-70px;
  top:-80px;

  pointer-events:none;
}

.runner::after{

  content:"";

  position:absolute;

  width:110px;
  height:110px;

  border-radius:50%;

  background:
    rgba(255,255,255,.25);

  left:-35px;
  top:35px;

  pointer-events:none;
}

.runner-cloud{

  position:absolute;

  font-size:35px;

  opacity:.65;

  pointer-events:none;

  z-index:1;
}

.cloud1{

  top:28px;
  left:15%;

  animation:
    cloudMove1 10s linear infinite;
}

.cloud2{

  top:72px;
  left:65%;

  animation:
    cloudMove2 14s linear infinite;
}

@keyframes cloudMove1{

  from{
    transform:translateX(0);
  }

  to{
    transform:translateX(160px);
  }

}

@keyframes cloudMove2{

  from{
    transform:translateX(0);
  }

  to{
    transform:translateX(-180px);
  }

}

/* =========================
   PLAYER
========================= */

.player{

  position:absolute;

  left:55px;

  bottom:43px;

  width:58px;
  height:58px;

  display:flex;

  align-items:center;
  justify-content:center;

  font-size:45px;

  z-index:10;

  filter:
    drop-shadow(
      0 5px 4px
      rgba(80,40,60,.18)
    );

  will-change:
    transform;
}

.player.running{

  animation:
    teddyRun .22s
    infinite alternate;
}

@keyframes teddyRun{

  from{
    transform:translateY(0);
  }

  to{
    transform:translateY(-4px);
  }

}

/* =========================
   OBSTACLE
========================= */

.obstacle{

  position:absolute;

  left:0;

  bottom:40px;

  width:55px;
  height:55px;

  display:flex;

  align-items:center;
  justify-content:center;

  font-size:42px;

  z-index:8;

  will-change:
    left;
}

/* =========================
   HEART
========================= */

.collectible{

  position:absolute;

  left:0;

  bottom:115px;

  width:42px;
  height:42px;

  display:flex;

  align-items:center;
  justify-content:center;

  font-size:32px;

  z-index:9;

  will-change:
    left;

  filter:
    drop-shadow(
      0 5px 7px
      rgba(120,40,70,.18)
    );

  animation:
    heartFloat .8s
    ease-in-out infinite alternate;
}

@keyframes heartFloat{

  from{
    transform:translateY(0);
  }

  to{
    transform:translateY(-9px);
  }

}

/* =========================
   GROUND
========================= */

.game-ground{

  position:absolute;

  left:0;
  right:0;

  bottom:0;

  height:43px;

  background:

    repeating-linear-gradient(
      135deg,
      rgba(255,255,255,.3)
      0px,
      rgba(255,255,255,.3)
      8px,
      transparent 8px,
      transparent 18px
    ),

    #d991aa;

  border-top:
    2px solid
    rgba(145,68,95,.15);

  z-index:5;

  pointer-events:none;
}

/* =========================
   SCORE
========================= */

.game-score{

  display:flex;

  justify-content:center;

  gap:10px;

  flex-wrap:wrap;

  margin:14px 0;
}

.game-score span{

  background:var(--pink);

  color:var(--deep);

  padding:8px 15px;

  border-radius:999px;

  font-weight:700;

  box-shadow:
    0 4px 12px
    var(--shadow);
}

/* =========================
   CONTROLS
========================= */

.game-controls{

  display:flex;

  justify-content:center;

  gap:10px;

  flex-wrap:wrap;
}

.game-control{

  border:0;

  border-radius:999px;

  padding:12px 20px;

  background:var(--rose);

  color:white;

  font-weight:700;

  box-shadow:
    0 6px 16px
    rgba(145,68,95,.2);

  transition:.2s;

  touch-action:manipulation;
}

.game-control:hover{
  transform:translateY(-2px);
}

.game-control:active{
  transform:scale(.96);
}

/* =========================
   GAME MESSAGE
========================= */

.game-message{

  text-align:center;

  margin-top:14px;

  min-height:25px;

  color:var(--muted);

  font-weight:600;
}

/* =========================
   POPUP
========================= */

.game-popup{

  position:absolute;

  left:50%;
  top:45%;

  transform:
    translate(-50%,-50%)
    scale(.7);

  opacity:0;

  pointer-events:none;

  z-index:30;

  background:
    rgba(255,253,251,.96);

  color:var(--deep);

  padding:13px 20px;

  border-radius:999px;

  font-weight:800;

  box-shadow:
    0 10px 30px
    rgba(90,45,65,.22);

  white-space:nowrap;
}

.game-popup.show{

  animation:
    popupMessage 1s
    ease forwards;
}

@keyframes popupMessage{

  0%{

    opacity:0;

    transform:
      translate(-50%,-50%)
      scale(.7);
  }

  20%{

    opacity:1;

    transform:
      translate(-50%,-50%)
      scale(1.08);
  }

  70%{

    opacity:1;

    transform:
      translate(-50%,-50%)
      scale(1);
  }

  100%{

    opacity:0;

    transform:
      translate(-50%,-75%)
      scale(.95);
  }

}

/* =========================
   GAME OVER
========================= */

.game-over{

  position:absolute;

  inset:0;

  display:flex;

  align-items:center;

  justify-content:center;

  flex-direction:column;

  background:
    rgba(89,60,69,.28);

  backdrop-filter:
    blur(3px);

  z-index:25;

  opacity:0;

  pointer-events:none;

  transition:.25s;
}

.game-over.show{

  opacity:1;

  pointer-events:auto;
}

.game-over-box{

  background:
    rgba(255,253,251,.97);

  padding:22px;

  border-radius:22px;

  text-align:center;

  box-shadow:
    0 12px 35px
    rgba(90,45,65,.25);

  max-width:90%;
}

.game-over-box h3{

  margin:
    0 0 8px;

  color:var(--deep);
}

.game-over-box p{

  margin:
    5px 0 15px;

  color:var(--muted);
}

/* =========================
   BIRTHDAY
========================= */

#birthdayOverlay{

  position:fixed;

  inset:0;

  display:flex;

  align-items:center;

  justify-content:center;

  background:
    radial-gradient(
      circle,
      rgba(255,255,255,.95),
      rgba(255,225,235,.96)
    );

  z-index:99999;

  opacity:0;

  visibility:hidden;

  transition:.4s;
}

#birthdayOverlay.show{

  opacity:1;

  visibility:visible;
}

.birthday-box{

  position:relative;

  width:min(560px,90%);

  text-align:center;

  background:
    rgba(255,253,251,.97);

  border-radius:30px;

  padding:32px 20px;

  box-shadow:
    0 20px 70px
    rgba(90,45,65,.25);

  animation:
    birthdayBox .8s ease;
}

@keyframes birthdayBox{

  from{

    transform:
      scale(.5)
      rotate(-5deg);

    opacity:0;
  }

  to{

    transform:
      scale(1)
      rotate(0);

    opacity:1;
  }

}

.birthday-title{

  color:var(--deep);

  font-size:
    clamp(34px,8vw,58px);

  margin:0;

  animation:
    birthdayText 1s
    infinite alternate;
}

@keyframes birthdayText{

  from{
    transform:scale(1);
  }

  to{
    transform:scale(1.04);
  }

}

.birthday-subtitle{

  color:var(--muted);

  line-height:1.6;
}

.cake{

  font-size:100px;

  margin:15px 0;

  animation:
    cakeBounce 1s
    ease-in-out infinite alternate;
}

@keyframes cakeBounce{

  from{
    transform:translateY(0);
  }

  to{
    transform:translateY(-8px);
  }

}

.close-birthday{

  border:0;

  background:var(--rose);

  color:white;

  padding:12px 24px;

  border-radius:999px;

  font-weight:800;
}

.birthday-particle{

  position:fixed;

  pointer-events:none;

  z-index:100000;

  font-size:25px;

  animation:
    birthdayParticle 3s
    ease-out forwards;
}

@keyframes birthdayParticle{

  0%{

    transform:
      translateY(0)
      scale(.5)
      rotate(0);

    opacity:0;
  }

  15%{
    opacity:1;
  }

  100%{

    transform:
      translateY(-100vh)
      scale(1.4)
      rotate(360deg);

    opacity:0;
  }

}

/* =========================
   FOOTER
========================= */

footer{

  text-align:center;

  padding:
    25px 18px 45px;

  color:var(--muted);
}

footer span{
  color:var(--rose);
}

/* =========================
   MOBILE
========================= */

@media(max-width:600px){

  .nav{
    align-items:flex-start;
  }

  .logo{
    font-size:16px;
  }

  .nav-buttons button{

    font-size:11px;

    padding:
      7px 9px;
  }

  .hero{

    min-height:65vh;

    padding-top:35px;
  }

  .hero-card{

    padding:
      30px 18px;
  }

  .teddy{
    font-size:65px;
  }

  .card{

    padding:
      19px 15px;
  }

  .runner{

    height:225px;

    border-radius:20px;
  }

  .player{

    left:30px;

    bottom:43px;
  }

  .game-control{

    padding:
      11px 17px;
  }

}

/* =========================
   LOADING
========================= */

.loading{

  text-align:center;

  color:var(--muted);

  padding:20px;
}

.empty{

  text-align:center;

  color:var(--muted);

  padding:20px;
}

</style>
</head>

<body>

<!-- =========================================================
     NAVIGATION
========================================================= -->

<header>

  <div class="nav">

    <div class="logo">
      The Us Story ❤️
    </div>

    <div class="nav-buttons">

      <button onclick="scrollToSection('timers')">
        ⏳ Timers
      </button>

      <button onclick="scrollToSection('memories')">
        📸 Memories
      </button>

      <button onclick="scrollToSection('game')">
        🎮 Game
      </button>

      <button onclick="scrollToSection('music')">
        🎵 Music
      </button>

    </div>

  </div>

</header>


<!-- =========================================================
     HERO
========================================================= -->

<section class="hero">

  <div class="hero-card">

    <div class="teddy">
      🧸
    </div>

    <h1>
      The Us Story ❤️
    </h1>

    <p>
      A little corner for the memories,
      moments, birthdays, and everything
      worth remembering.
    </p>

    <button
      class="primary"
      onclick="scrollToSection('timers')">

      ✨ Start the Story

    </button>

  </div>

</section>


<main>

<!-- =========================================================
     TIMERS
========================================================= -->

<section
  id="timers"
  class="card">

  <h2>
    ⏳ Three Little Timers
  </h2>

  <div class="timer-grid">

    <div class="timer-card">

      <div class="timer-icon">
        ❤️
      </div>

      <div class="timer-title">
        Together Since
      </div>

      <div
        id="relationshipTimer"
        class="timer-value">

        Loading...

      </div>

      <div class="timer-small">
        11 January 2022
      </div>

    </div>


    <div class="timer-card">

      <div class="timer-icon">
        🎂
      </div>

      <div class="timer-title">
        His Birthday
      </div>

      <div
        id="hisBirthdayTimer"
        class="timer-value">

        Loading...

      </div>

      <div class="timer-small">
        14 February
      </div>

    </div>


    <div class="timer-card">

      <div class="timer-icon">
        🎂
      </div>

      <div class="timer-title">
        Her Birthday
      </div>

      <div
        id="herBirthdayTimer"
        class="timer-value">

        Loading...

      </div>

      <div class="timer-small">
        2 September
      </div>

    </div>

  </div>

</section>


<!-- =========================================================
     LOGIN
========================================================= -->

<section
  id="loginSection"
  class="card">

  <h2>
    🔐 Private Memory Wall
  </h2>

  <p
    style="
      text-align:center;
      color:var(--muted)
    ">

    Login to save and view private memories.

  </p>

  <div class="form">

    <input
      id="email"
      type="email"
      placeholder="Email">

    <input
      id="password"
      type="password"
      placeholder="Password">

    <button
      id="loginButton"
      class="primary"
      type="button">

      🔐 Login

    </button>

    <button
      id="logoutButton"
      class="secondary hidden"
      type="button">

      Logout

    </button>

  </div>

  <div
    id="authStatus"
    class="auth-status">

    Not logged in.

  </div>

</section>


<!-- =========================================================
     MEMORIES
========================================================= -->

<section
  id="memories"
  class="card hidden">

  <h2>
    📸 Memory Wall
  </h2>

  <p style="color:var(--muted)">
    Save little moments here.
  </p>

  <div class="memory-form">

    <input
      id="memoryTitle"
      type="text"
      placeholder="Memory title">

    <input
      id="memoryDate"
      type="date">

    <textarea
      id="memoryMessage"
      placeholder="Write something about this memory..."></textarea>

    <input
      id="memoryImage"
      type="file"
      accept="image/*">

    <button
      id="saveMemory"
      class="primary"
      type="button">

      💾 Save Memory

    </button>

  </div>

  <div
    id="memoryStatus"
    class="auth-status">
  </div>

  <div
    id="memoryGrid"
    class="memory-grid">

    <div class="loading">
      Loading memories...
    </div>

  </div>

</section>


<!-- =========================================================
     LOVE RUN GAME
========================================================= -->

<section
  id="game"
  class="card">

  <h2>
    🎮 Love Run
  </h2>

  <p class="game-intro">

    Help the little teddy keep running
    through the story. 🧸

    Jump over flowers,
    collect hearts,
    and beat the best score. ❤️

  </p>


  <div
    class="runner"
    id="runner">

    <div class="runner-cloud cloud1">
      ☁️
    </div>

    <div class="runner-cloud cloud2">
      ☁️
    </div>


    <div
      id="player"
      class="player">

      🧸

    </div>


    <div
      id="obstacle"
      class="obstacle">

      🌷

    </div>


    <div
      id="collectible"
      class="collectible">

      ❤️

    </div>


    <div
      id="gamePopup"
      class="game-popup">
    </div>


    <div
      id="gameOver"
      class="game-over">

      <div class="game-over-box">

        <h3 id="gameOverTitle">
          Game Over 💕
        </h3>

        <p id="gameOverText">
          The teddy bumped into a flower.
        </p>

        <button
          id="gameRestartInside"
          class="game-control"
          type="button">

          🔄 Play Again

        </button>

      </div>

    </div>


    <div class="game-ground"></div>

  </div>


  <div class="game-score">

    <span>
      Score:
      <span id="score">0</span>
    </span>

    <span>
      ❤️ Hearts:
      <span id="heartScore">0</span>
    </span>

    <span>
      Best:
      <span id="best">0</span>
    </span>

  </div>


  <div class="game-controls">

    <button
      id="startGame"
      class="game-control"
      type="button">

      🧸 Start

    </button>

    <button
      id="jumpButton"
      class="game-control"
      type="button">

      ☝️ Jump

    </button>

  </div>


  <div
    id="gameMessage"
    class="game-message">

    Tap Start to begin.
    Then tap the screen or Jump to jump! ❤️

  </div>

</section>


<!-- =========================================================
     MUSIC
========================================================= -->

<section
  id="music"
  class="card music-box">

  <h2>
    🎵 Our Music
  </h2>

  <p style="color:var(--muted)">
    Press play to start the music.
  </p>

  <audio
    id="musicPlayer"
    controls
    preload="metadata">

    <source
      src="./vidssave.com%20Osho%20Jain%20_%20Tu%20Aisa%20Kaise%20Hai_%20_%20%23OshoJain%20720P.mp3"
      type="audio/mpeg">

    Your browser does not support audio.

  </audio>

</section>

</main>


<!-- =========================================================
     BIRTHDAY OVERLAY
========================================================= -->

<div
  id="birthdayOverlay">

  <div class="birthday-box">

    <h1
      id="birthdayTitle"
      class="birthday-title">

      🎉 HAPPY BIRTHDAY! 🎉

    </h1>

    <div class="cake">
      🎂
    </div>

    <p
      id="birthdaySubtitle"
      class="birthday-subtitle">

      Wishing a beautiful birthday
      filled with happiness, smiles,
      and wonderful memories. ❤️

    </p>

    <button
      id="closeBirthday"
      class="close-birthday">

      ❤️ Close

    </button>

  </div>

</div>


<footer>

  Made with <span>❤️</span>
  • The Us Story

</footer>


<script>

/* =========================================================
   SUPABASE
========================================================= */

const SUPABASE_URL =
  "https://rxtiefedshmfbfejtetk.supabase.co";

const SUPABASE_KEY =
  "sb_publishable_S59gIZua305x2r3BZ1BYKQ_Us1zmr3f";

const TABLE =
  "memories";

const supabaseClient =
  window.supabase.createClient(
    SUPABASE_URL,
    SUPABASE_KEY
  );


/* =========================================================
   GENERAL
========================================================= */

function scrollToSection(id){

  const element =
    document.getElementById(id);

  if(element){

    element.scrollIntoView({
      behavior:"smooth",
      block:"start"
    });

  }

}


/* =========================================================
   TIMERS
========================================================= */

const relationshipStart =
  new Date(
    "2022-01-11T00:00:00"
  );


function pad(number){

  return String(number)
    .padStart(2,"0");

}


function getTimeDifference(target){

  const now =
    new Date();

  let difference =
    target - now;

  if(difference < 0){
    difference = 0;
  }

  const totalSeconds =
    Math.floor(
      difference / 1000
    );

  const days =
    Math.floor(
      totalSeconds / 86400
    );

  const hours =
    Math.floor(
      (totalSeconds % 86400) / 3600
    );

  const minutes =
    Math.floor(
      (totalSeconds % 3600) / 60
    );

  const seconds =
    totalSeconds % 60;

  return {
    days,
    hours,
    minutes,
    seconds
  };

}


function birthdayTarget(
  month,
  day
){

  const now =
    new Date();

  let year =
    now.getFullYear();

  let target =
    new Date(
      year,
      month - 1,
      day,
      0,
      0,
      0
    );

  if(target <= now){

    target =
      new Date(
        year + 1,
        month - 1,
        day,
        0,
        0,
        0
      );

  }

  return target;

}


function updateRelationshipTimer(){

  const now =
    new Date();

  let difference =
    now - relationshipStart;

  if(difference < 0){
    difference = 0;
  }

  const totalSeconds =
    Math.floor(
      difference / 1000
    );

  const days =
    Math.floor(
      totalSeconds / 86400
    );

  const hours =
    Math.floor(
      (totalSeconds % 86400) / 3600
    );

  const minutes =
    Math.floor(
      (totalSeconds % 3600) / 60
    );

  const seconds =
    totalSeconds % 60;

  document.getElementById(
    "relationshipTimer"
  ).textContent =
    days +
    "d " +
    pad(hours) +
    "h " +
    pad(minutes) +
    "m " +
    pad(seconds) +
    "s";

}


function updateBirthdayTimer(
  elementId,
  month,
  day
){

  const target =
    birthdayTarget(
      month,
      day
    );

  const time =
    getTimeDifference(target);

  document.getElementById(
    elementId
  ).textContent =
    time.days +
    "d " +
    pad(time.hours) +
    "h " +
    pad(time.minutes) +
    "m " +
    pad(time.seconds) +
    "s";

}


function updateAllTimers(){

  updateRelationshipTimer();

  updateBirthdayTimer(
    "hisBirthdayTimer",
    2,
    14
  );

  updateBirthdayTimer(
    "herBirthdayTimer",
    9,
    2
  );

}

updateAllTimers();

setInterval(
  updateAllTimers,
  1000
);


/* =========================================================
   BIRTHDAY CELEBRATION
========================================================= */

const birthdayOverlay =
  document.getElementById(
    "birthdayOverlay"
  );

const birthdayTitle =
  document.getElementById(
    "birthdayTitle"
  );

const birthdaySubtitle =
  document.getElementById(
    "birthdaySubtitle"
  );

const closeBirthday =
  document.getElementById(
    "closeBirthday"
  );


function createBirthdayParticles(){

  const symbols = [
    "❤️",
    "💕",
    "💗",
    "💖",
    "✨",
    "🎉",
    "🎈",
    "🎂",
    "🌷",
    "🧸"
  ];

  for(let i = 0; i < 70; i++){

    const particle =
      document.createElement("div");

    particle.className =
      "birthday-particle";

    particle.textContent =
      symbols[
        Math.floor(
          Math.random() *
          symbols.length
        )
      ];

    particle.style.left =
      Math.random() * 100 +
      "vw";

    particle.style.top =
      (70 + Math.random() * 30) +
      "vh";

    particle.style.animationDelay =
      Math.random() * 1.5 +
      "s";

    particle.style.fontSize =
      (18 + Math.random() * 25) +
      "px";

    document.body.appendChild(
      particle
    );

    setTimeout(
      () => particle.remove(),
      4500
    );

  }

}


function isBirthdayToday(
  month,
  day
){

  const now =
    new Date();

  return (
    now.getMonth() + 1 === month &&
    now.getDate() === day
  );

}


function showBirthdayCelebration(
  type
){

  if(type === "her"){

    birthdayTitle.textContent =
      "🎉 HAPPY BIRTHDAY! 🎉";

    birthdaySubtitle.textContent =
      "Wishing a beautiful birthday " +
      "filled with happiness, smiles, " +
      "and wonderful memories. ❤️";

  }else{

    birthdayTitle.textContent =
      "🎉 HAPPY BIRTHDAY! 🎉";

    birthdaySubtitle.textContent =
      "Wishing you a fantastic birthday " +
      "filled with happiness and great memories! ❤️";

  }

  birthdayOverlay.classList.add(
    "show"
  );

  createBirthdayParticles();

}


function checkBirthday(){

  const todayKey =
    new Date()
      .toISOString()
      .slice(0,10);

  const alreadyShown =
    localStorage.getItem(
      "birthdayShown"
    );

  if(alreadyShown === todayKey){
    return;
  }

  if(isBirthdayToday(9,2)){

    localStorage.setItem(
      "birthdayShown",
      todayKey
    );

    setTimeout(
      () =>
        showBirthdayCelebration("her"),
      1000
    );

    return;
  }

  if(isBirthdayToday(2,14)){

    localStorage.setItem(
      "birthdayShown",
      todayKey
    );

    setTimeout(
      () =>
        showBirthdayCelebration("his"),
      1000
    );

  }

}

checkBirthday();


closeBirthday.addEventListener(
  "click",
  function(){

    birthdayOverlay.classList.remove(
      "show"
    );

  }
);


/* =========================================================
   AUTH
========================================================= */

const emailInput =
  document.getElementById("email");

const passwordInput =
  document.getElementById("password");

const loginButton =
  document.getElementById("loginButton");

const logoutButton =
  document.getElementById("logoutButton");

const authStatus =
  document.getElementById("authStatus");

const memoriesSection =
  document.getElementById("memories");


loginButton.addEventListener(
  "click",
  async function(){

    const email =
      emailInput.value.trim();

    const password =
      passwordInput.value;

    if(!email || !password){

      authStatus.textContent =
        "Please enter email and password.";

      return;
    }

    loginButton.disabled =
      true;

    authStatus.textContent =
      "Logging in...";

    try{

      const {
        data,
        error
      } =
        await supabaseClient.auth
          .signInWithPassword({
            email,
            password
          });

      if(error){

        authStatus.textContent =
          error.message;

        return;
      }

      if(data.user){

        authStatus.textContent =
          "Logged in successfully ❤️";

      }

    }catch(error){

      console.error(error);

      authStatus.textContent =
        "Login failed. Please try again.";

    }finally{

      loginButton.disabled =
        false;

    }

  }
);


logoutButton.addEventListener(
  "click",
  async function(){

    await supabaseClient.auth.signOut();

  }
);


async function updateAuthUI(){

  try{

    const {
      data
    } =
      await supabaseClient.auth
        .getSession();

    const session =
      data.session;

    if(session){

      authStatus.textContent =
        "Logged in as " +
        (session.user.email || "user") +
        " ❤️";

      loginButton.classList.add(
        "hidden"
      );

      emailInput.classList.add(
        "hidden"
      );

      passwordInput.classList.add(
        "hidden"
      );

      logoutButton.classList.remove(
        "hidden"
      );

      memoriesSection.classList.remove(
        "hidden"
      );

      loadMemories();

    }else{

      authStatus.textContent =
        "Not logged in.";

      loginButton.classList.remove(
        "hidden"
      );

      emailInput.classList.remove(
        "hidden"
      );

      passwordInput.classList.remove(
        "hidden"
      );

      logoutButton.classList.add(
        "hidden"
      );

      memoriesSection.classList.add(
        "hidden"
      );

    }

  }catch(error){

    console.error(
      "Auth error:",
      error
    );

  }

}


supabaseClient.auth.onAuthStateChange(
  function(){

    updateAuthUI();

  }
);

updateAuthUI();


/* =========================================================
   IMAGE COMPRESSION
========================================================= */

async function compressImage(file){

  return new Promise(
    function(resolve,reject){

      const reader =
        new FileReader();

      reader.onload =
        function(event){

          const image =
            new Image();

          image.onload =
            function(){

              const maxSize =
                1600;

              let width =
                image.width;

              let height =
                image.height;

              if(width > maxSize){

                height =
                  Math.round(
                    height *
                    maxSize /
                    width
                  );

                width =
                  maxSize;

              }

              if(height > maxSize){

                width =
                  Math.round(
                    width *
                    maxSize /
                    height
                  );

                height =
                  maxSize;

              }

              const canvas =
                document.createElement(
                  "canvas"
                );

              canvas.width =
                width;

              canvas.height =
                height;

              const context =
                canvas.getContext(
                  "2d"
                );

              context.drawImage(
                image,
                0,
                0,
                width,
                height
              );

              resolve(
                canvas.toDataURL(
                  "image/jpeg",
                  .82
                )
              );

            };

          image.onerror =
            reject;

          image.src =
            event.target.result;

        };

      reader.onerror =
        reject;

      reader.readAsDataURL(file);

    }
  );

}


/* =========================================================
   SAVE MEMORY
========================================================= */

const saveMemory =
  document.getElementById(
    "saveMemory"
  );

const memoryStatus =
  document.getElementById(
    "memoryStatus"
  );


saveMemory.addEventListener(
  "click",
  async function(){

    const {
      data
    } =
      await supabaseClient.auth
        .getUser();

    const user =
      data.user;

    if(!user){

      memoryStatus.textContent =
        "Please login first.";

      return;
    }

    const title =
      document.getElementById(
        "memoryTitle"
      ).value.trim();

    const date =
      document.getElementById(
        "memoryDate"
      ).value;

    const message =
      document.getElementById(
        "memoryMessage"
      ).value.trim();

    const imageFile =
      document.getElementById(
        "memoryImage"
      ).files[0];

    if(!title && !message && !imageFile){

      memoryStatus.textContent =
        "Add something to the memory.";

      return;
    }

    saveMemory.disabled =
      true;

    memoryStatus.textContent =
      "Saving memory...";

    let image =
      null;

    try{

      if(imageFile){

        image =
          await compressImage(
            imageFile
          );

      }

      const {
        error
      } =
        await supabaseClient
          .from(TABLE)
          .insert({

            user_id:user.id,

            title:
              title ||
              "Untitled Memory",

            date:
              date ||
              null,

            message:
              message ||
              "",

            image:image

          });

      if(error){

        console.error(error);

        memoryStatus.textContent =
          error.message;

        return;
      }

      memoryStatus.textContent =
        "Memory saved ❤️";

      document.getElementById(
        "memoryTitle"
      ).value = "";

      document.getElementById(
        "memoryDate"
      ).value = "";

      document.getElementById(
        "memoryMessage"
      ).value = "";

      document.getElementById(
        "memoryImage"
      ).value = "";

      await loadMemories();

    }catch(error){

      console.error(error);

      memoryStatus.textContent =
        "Could not save memory.";

    }finally{

      saveMemory.disabled =
        false;

    }

  }
);


/* =========================================================
   LOAD MEMORIES
========================================================= */

async function loadMemories(){

  const memoryGrid =
    document.getElementById(
      "memoryGrid"
    );

  memoryGrid.innerHTML =
    '<div class="loading">Loading memories...</div>';

  try{

    const {
      data:userData
    } =
      await supabaseClient.auth
        .getUser();

    const user =
      userData.user;

    if(!user){

      memoryGrid.innerHTML =
        '<div class="empty">Login to see memories.</div>';

      return;
    }

    const {
      data,
      error
    } =
      await supabaseClient
        .from(TABLE)
        .select(
          "id,user_id,title,date,message,image,created_at"
        )
        .eq(
          "user_id",
          user.id
        )
        .order(
          "created_at",
          {
            ascending:false
          }
        );

    if(error){

      console.error(error);

      memoryGrid.innerHTML =
        '<div class="empty">Could not load memories.</div>';

      return;
    }

    if(!data || data.length === 0){

      memoryGrid.innerHTML =
        '<div class="empty">' +
        'No memories yet. Add the first one ❤️' +
        '</div>';

      return;
    }

    memoryGrid.innerHTML =
      "";

    data.forEach(
      function(memory){

        const card =
          document.createElement(
            "article"
          );

        card.className =
          "memory";

        if(memory.image){

          const image =
            document.createElement(
              "img"
            );

          image.src =
            memory.image;

          image.alt =
            memory.title ||
            "Memory";

          card.appendChild(
            image
          );

        }

        const content =
          document.createElement(
            "div"
          );

        content.className =
          "memory-content";

        const title =
          document.createElement(
            "h3"
          );

        title.textContent =
          memory.title ||
          "Untitled Memory";

        const date =
          document.createElement(
            "div"
          );

        date.className =
          "memory-date";

        if(memory.date){

          date.textContent =
            memory.date;

        }else{

          date.textContent =
            memory.created_at
              ? new Date(
                  memory.created_at
                ).toLocaleDateString()
              : "";

        }

        const message =
          document.createElement(
            "p"
          );

        message.textContent =
          memory.message ||
          "";

        content.appendChild(
          title
        );

        content.appendChild(
          date
        );

        content.appendChild(
          message
        );

        card.appendChild(
          content
        );

        memoryGrid.appendChild(
          card
        );

      }
    );

  }catch(error){

    console.error(error);

    memoryGrid.innerHTML =
      '<div class="empty">Could not load memories.</div>';

  }

}


/* =========================================================
   LOVE RUN GAME
   FIXED VERSION
========================================================= */

const runner =
  document.getElementById(
    "runner"
  );

const player =
  document.getElementById(
    "player"
  );

const obstacle =
  document.getElementById(
    "obstacle"
  );

const collectible =
  document.getElementById(
    "collectible"
  );

const scoreElement =
  document.getElementById(
    "score"
  );

const heartScoreElement =
  document.getElementById(
    "heartScore"
  );

const bestElement =
  document.getElementById(
    "best"
  );

const startGameButton =
  document.getElementById(
    "startGame"
  );

const jumpButton =
  document.getElementById(
    "jumpButton"
  );

const gameMessage =
  document.getElementById(
    "gameMessage"
  );

const gamePopup =
  document.getElementById(
    "gamePopup"
  );

const gameOver =
  document.getElementById(
    "gameOver"
  );

const gameOverTitle =
  document.getElementById(
    "gameOverTitle"
  );

const gameOverText =
  document.getElementById(
    "gameOverText"
  );

const gameRestartInside =
  document.getElementById(
    "gameRestartInside"
  );


let gameRunning =
  false;

let jumping =
  false;

let velocityY =
  0;

let playerY =
  0;

let obstacleX =
  0;

let heartX =
  0;

let score =
  0;

let heartScore =
  0;

let gameSpeed =
  5.5;

let animationFrame =
  null;

let lastTime =
  0;

let obstacleCycle =
  0;

let heartCycle =
  0;

let best =
  Number(
    localStorage.getItem(
      "theUsStoryBest"
    ) || 0
  );


bestElement.textContent =
  best;


/* =========================================================
   RESET GAME OBJECTS
========================================================= */

function resetGameObjects(){

  const width =
    runner.clientWidth;

  obstacleX =
    width + 100;

  heartX =
    width + 300;

  obstacle.style.left =
    obstacleX + "px";

  collectible.style.left =
    heartX + "px";

  playerY =
    0;

  player.style.transform =
    "translateY(0px)";

}


/* =========================================================
   JUMP
========================================================= */

function jump(){

  if(!gameRunning){
    return;
  }

  if(jumping){
    return;
  }

  jumping =
    true;

  velocityY =
    14;

}


/* =========================================================
   START GAME
========================================================= */

function startGame(){

  cancelAnimationFrame(
    animationFrame
  );

  gameRunning =
    true;

  jumping =
    false;

  velocityY =
    0;

  playerY =
    0;

  score =
    0;

  heartScore =
    0;

  gameSpeed =
    5.5;

  obstacleCycle =
    0;

  heartCycle =
    0;

  scoreElement.textContent =
    "0";

  heartScoreElement.textContent =
    "0";

  player.style.transform =
    "translateY(0px)";

  player.classList.add(
    "running"
  );

  gameOver.classList.remove(
    "show"
  );

  gamePopup.classList.remove(
    "show"
  );

  collectible.style.display =
    "flex";

  resetGameObjects();

  gameMessage.textContent =
    "Run! Jump over 🌷 and collect ❤️";

  startGameButton.textContent =
    "🔄 Restart";

  lastTime =
    performance.now();

  animationFrame =
    requestAnimationFrame(
      gameLoop
    );

}


/* =========================================================
   POPUP
========================================================= */

function showPopup(text){

  gamePopup.textContent =
    text;

  gamePopup.classList.remove(
    "show"
  );

  void gamePopup.offsetWidth;

  gamePopup.classList.add(
    "show"
  );

}


/* =========================================================
   GAME OVER
========================================================= */

function endGame(){

  if(!gameRunning){
    return;
  }

  gameRunning =
    false;

  cancelAnimationFrame(
    animationFrame
  );

  player.classList.remove(
    "running"
  );

  if(score > best){

    best =
      score;

    localStorage.setItem(
      "theUsStoryBest",
      String(best)
    );

    bestElement.textContent =
      best;

    gameOverTitle.textContent =
      "NEW BEST! 🎉";

    gameOverText.textContent =
      "Amazing! Score: " +
      score +
      " • Hearts: " +
      heartScore +
      " ❤️";

  }else{

    gameOverTitle.textContent =
      "Game Over 💕";

    gameOverText.textContent =
      "Score: " +
      score +
      " • Hearts: " +
      heartScore +
      " ❤️";

  }

  gameMessage.textContent =
    "The teddy bumped into a flower. Try again! 🌷";

  gameOver.classList.add(
    "show"
  );

  startGameButton.textContent =
    "🧸 Play Again";

}


/* =========================================================
   COLLISION
========================================================= */

function isColliding(
  a,
  b,
  padding
){

  return (

    a.left + padding <
    b.right - padding

    &&

    a.right - padding >
    b.left + padding

    &&

    a.top + padding <
    b.bottom - padding

    &&

    a.bottom - padding >
    b.top + padding

  );

}


/* =========================================================
   GAME LOOP
========================================================= */

function gameLoop(time){

  if(!gameRunning){
    return;
  }


  let delta =
    (time - lastTime) / 16.67;

  delta =
    Math.min(
      Math.max(delta,.5),
      2
    );

  lastTime =
    time;


  /* =========================
     JUMP PHYSICS
  ========================= */

  if(jumping){

    velocityY -=
      .72 * delta;

    playerY +=
      velocityY * delta;

    if(playerY <= 0){

      playerY =
        0;

      velocityY =
        0;

      jumping =
        false;

    }

  }


  player.style.transform =
    "translateY(" +
    (-playerY) +
    "px)";


  /* =========================
     OBSTACLE MOVEMENT
  ========================= */

  obstacleX -=
    gameSpeed * delta;


  if(
    obstacleX <
    -70
  ){

    score++;

    scoreElement.textContent =
      score;

    gameSpeed =
      Math.min(
        11,
        5.5 +
        score * .12
      );

    obstacleCycle++;

    const width =
      runner.clientWidth;

    obstacleX =
      width +
      100 +
      Math.random() * 180;

    /* Every few obstacles
       change heart position */

    heartX =
      width +
      250 +
      Math.random() * 350;

    collectible.style.display =
      "flex";

    /* Milestones */

    if(score === 5){

      showPopup(
        "🌷 5 Points!"
      );

    }

    if(score === 10){

      showPopup(
        "✨ 10 Points!"
      );

    }

    if(score === 25){

      showPopup(
        "💗 25 Points!"
      );

    }

    if(score === 50){

      showPopup(
        "🎉 50 Points!"
      );

    }

  }


  obstacle.style.left =
    obstacleX + "px";


  /* =========================
     HEART MOVEMENT
  ========================= */

  heartX -=
    gameSpeed * delta;


  if(
    heartX <
    -60
  ){

    heartCycle++;

    heartX =
      runner.clientWidth +
      250 +
      Math.random() * 350;

  }


  collectible.style.left =
    heartX + "px";


  /* =========================
     PLAYER RECT
  ========================= */

  const playerRect =
    player.getBoundingClientRect();


  /* =========================
     FLOWER COLLISION
  ========================= */

  const obstacleRect =
    obstacle.getBoundingClientRect();


  if(
    isColliding(
      playerRect,
      obstacleRect,
      10
    )
  ){

    endGame();

    return;

  }


  /* =========================
     HEART COLLECTION
  ========================= */

  const heartRect =
    collectible.getBoundingClientRect();


  if(
    collectible.style.display !== "none" &&
    isColliding(
      playerRect,
      heartRect,
      7
    )
  ){

    heartScore++;

    heartScoreElement.textContent =
      heartScore;

    showPopup(
      "❤️ +1 Heart!"
    );

    collectible.style.display =
      "none";

    heartX =
      runner.clientWidth +
      400 +
      Math.random() * 300;

  }


  /* =========================
     CONTINUE
  ========================= */

  animationFrame =
    requestAnimationFrame(
      gameLoop
    );

}


/* =========================================================
   START BUTTON
========================================================= */

startGameButton.addEventListener(
  "click",
  function(){

    startGame();

  }
);


/* =========================================================
   GAME OVER RESTART BUTTON
========================================================= */

gameRestartInside.addEventListener(
  "click",
  function(event){

    event.stopPropagation();

    startGame();

  }
);


/* =========================================================
   JUMP BUTTON
========================================================= */

jumpButton.addEventListener(
  "pointerdown",
  function(event){

    event.preventDefault();

    event.stopPropagation();

    if(!gameRunning){

      startGame();

    }else{

      jump();

    }

  }
);


/* =========================================================
   GAME AREA TOUCH
========================================================= */

runner.addEventListener(
  "pointerdown",
  function(event){

    if(
      event.target.closest(
        ".game-over-box"
      )
    ){

      return;

    }

    event.preventDefault();

    if(!gameRunning){

      startGame();

    }else{

      jump();

    }

  }
);


/* =========================================================
   KEYBOARD
========================================================= */

document.addEventListener(
  "keydown",
  function(event){

    if(
      event.code === "Space" ||
      event.code === "ArrowUp"
    ){

      event.preventDefault();

      if(!gameRunning){

        startGame();

      }else{

        jump();

      }

    }

  }
);


/* =========================================================
   INITIAL GAME STATE
========================================================= */

collectible.style.display =
  "none";

gameOver.classList.remove(
  "show"
);

resetGameObjects();


/* =========================================================
   MEMORY DATE DEFAULT
========================================================= */

const memoryDateInput =
  document.getElementById(
    "memoryDate"
  );

if(memoryDateInput){

  const now =
    new Date();

  const year =
    now.getFullYear();

  const month =
    String(
      now.getMonth() + 1
    ).padStart(2,"0");

  const day =
    String(
      now.getDate()
    ).padStart(2,"0");

  memoryDateInput.value =
    year +
    "-" +
    month +
    "-" +
    day;

}

</script>

</body>
</html>
