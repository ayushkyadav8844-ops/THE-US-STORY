<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
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

*{box-sizing:border-box}

html{scroll-behavior:smooth}

body{
margin:0;
min-height:100vh;
font-family:Georgia,"Times New Roman",serif;
color:var(--text);
overflow-x:hidden;
background:
linear-gradient(rgba(255,241,246,.78),rgba(255,248,243,.9)),
url("./file_0000000b66082118bbde5d0666da038.png");
background-size:cover;
background-position:center;
background-attachment:fixed;
}

body:before{
content:"";
position:fixed;
inset:0;
pointer-events:none;
z-index:0;
background:
radial-gradient(circle at 10% 15%,rgba(255,255,255,.65),transparent 25%),
radial-gradient(circle at 90% 30%,rgba(255,210,225,.35),transparent 28%),
radial-gradient(circle at 50% 90%,rgba(255,230,215,.35),transparent 30%);
}

.decorations{
position:fixed;
inset:0;
pointer-events:none;
overflow:hidden;
z-index:1;
}

.float{
position:absolute;
bottom:-50px;
opacity:0;
animation:floatUp 11s linear infinite;
font-size:25px;
}

.float:nth-child(1){left:7%}
.float:nth-child(2){left:22%;animation-delay:3s}
.float:nth-child(3){left:43%;animation-delay:6s}
.float:nth-child(4){left:68%;animation-delay:2s}
.float:nth-child(5){left:90%;animation-delay:5s}

@keyframes floatUp{
0%{transform:translateY(0) rotate(0) scale(.6);opacity:0}
12%{opacity:.6}
50%{transform:translateY(-55vh) translateX(25px) rotate(18deg) scale(1);opacity:.4}
100%{transform:translateY(-115vh) translateX(-25px) rotate(-18deg) scale(1.15);opacity:0}
}

.sparkle{
position:absolute;
color:rgba(192,95,130,.5);
animation:sparkle 3s ease-in-out infinite;
}
.s1{top:14%;left:9%}
.s2{top:31%;right:8%;animation-delay:.8s}
.s3{top:61%;left:6%;animation-delay:1.5s}
.s4{top:79%;right:9%;animation-delay:2s}

@keyframes sparkle{
0%,100%{transform:scale(.5);opacity:.2}
50%{transform:scale(1.5) rotate(35deg);opacity:.9}
}

.container{
position:relative;
z-index:5;
width:92%;
max-width:850px;
margin:auto;
padding:20px 0 80px;
}

header{text-align:center;padding:25px 8px 10px}

.teddies{
display:flex;
justify-content:center;
align-items:flex-end;
gap:12px;
height:155px;
}

.teddy{
position:relative;
width:100px;
height:135px;
animation:teddyFloat 3s ease-in-out infinite;
filter:drop-shadow(0 9px 8px rgba(80,40,30,.13));
}

.teddy:nth-child(2){animation-delay:.4s}

.head{
position:absolute;
left:12px;
top:8px;
width:76px;
height:70px;
border-radius:48%;
background:linear-gradient(145deg,#dfa174,#ae694b);
z-index:3;
}

.girl .head{background:linear-gradient(145deg,#e5a08f,#b97065)}

.ear{
position:absolute;
top:-7px;
width:30px;
height:30px;
border-radius:50%;
background:#bd7651;
z-index:-1;
}

.girl .ear{background:#c98277}
.ear.left{left:0}
.ear.right{right:0}

.ear:after{
content:"";
position:absolute;
inset:6px;
border-radius:50%;
background:#f1b7a2;
}

.eye{
position:absolute;
top:28px;
width:7px;
height:8px;
border-radius:50%;
background:#493036;
}

.eye.left{left:20px}
.eye.right{right:20px}

.eye:after{
content:"";
position:absolute;
width:2px;
height:2px;
top:1px;
left:1px;
border-radius:50%;
background:white;
}

.cheek{
position:absolute;
top:42px;
width:11px;
height:7px;
border-radius:50%;
background:#ed999d;
opacity:.7;
}

.cheek.left{left:10px}
.cheek.right{right:10px}

.muzzle{
position:absolute;
left:23px;
top:37px;
width:30px;
height:23px;
border-radius:50%;
background:#f0c4a8;
}

.nose{
position:absolute;
left:10px;
top:5px;
width:10px;
height:7px;
border-radius:50%;
background:#553037;
}

.mouth{
position:absolute;
left:12px;
top:11px;
width:6px;
height:5px;
border-bottom:2px solid #553037;
border-radius:50%;
}

.body{
position:absolute;
left:21px;
top:73px;
width:58px;
height:50px;
border-radius:48% 48% 40% 40%;
background:linear-gradient(145deg,#dfa174,#ae694b);
}

.girl .body{background:linear-gradient(145deg,#e5a08f,#b97065)}

.belly{
position:absolute;
left:15px;
top:9px;
width:28px;
height:26px;
border-radius:50%;
background:#edc09e;
}

.arm{
position:absolute;
top:77px;
width:20px;
height:38px;
border-radius:50%;
background:#c17a55;
z-index:4;
}

.girl .arm{background:#c67c72}
.arm.left{left:5px;transform:rotate(27deg)}
.arm.right{right:5px;transform:rotate(-27deg)}

.leg{
position:absolute;
top:108px;
width:24px;
height:19px;
border-radius:50%;
background:#ad684b;
}

.leg.left{left:19px}
.leg.right{right:19px}

.heart{
position:absolute;
left:37px;
top:71px;
z-index:8;
font-size:27px;
animation:heartBounce 1.5s ease-in-out infinite;
}

.bow{
position:absolute;
right:-4px;
top:-5px;
z-index:20;
font-size:27px;
animation:bowWiggle 2s ease-in-out infinite;
}

@keyframes teddyFloat{
0%,100%{transform:translateY(0) rotate(-2deg)}
50%{transform:translateY(-10px) rotate(2deg)}
}

@keyframes heartBounce{
0%,100%{transform:scale(1) rotate(-3deg)}
50%{transform:scale(1.2) rotate(4deg)}
}

@keyframes bowWiggle{
0%,100%{transform:rotate(10deg)}
50%{transform:rotate(-8deg) scale(1.06)}
}

.header-heart{
font-size:39px;
animation:heartbeat 1.5s ease-in-out infinite;
}

@keyframes heartbeat{
0%,100%{transform:scale(1)}
50%{transform:scale(1.18)}
}

h1{
margin:10px 0;
color:var(--deep);
font-size:clamp(40px,9vw,72px);
line-height:1;
text-shadow:0 4px 15px rgba(145,76,101,.13);
}

.subtitle{
color:var(--muted);
font-size:20px;
line-height:1.6;
}

.divider{
display:flex;
justify-content:center;
align-items:center;
gap:12px;
margin:22px auto;
}

.divider:before,.divider:after{
content:"";
width:70px;
height:1px;
background:linear-gradient(to right,transparent,var(--soft));
}

.divider:after{
background:linear-gradient(to left,transparent,var(--soft));
}

.counter{
position:relative;
text-align:center;
margin:25px 0 35px;
padding:32px 20px;
overflow:hidden;
background:rgba(255,252,250,.95);
border:1px solid rgba(160,91,111,.18);
border-radius:32px;
box-shadow:0 18px 50px var(--shadow);
backdrop-filter:blur(9px);
}

.counter:before{
content:"";
position:absolute;
inset:8px;
border:1px dashed rgba(192,95,130,.3);
border-radius:25px;
pointer-events:none;
}

.counter-heart{
font-size:40px;
animation:heartbeat 1.5s infinite;
}

.counter-title{
margin-top:5px;
color:var(--deep);
font-size:25px;
font-weight:bold;
}

.counter-date{
margin:8px 0 20px;
color:var(--muted);
font-size:15px;
}

.counter-grid{
display:grid;
grid-template-columns:repeat(4,1fr);
gap:10px;
max-width:620px;
margin:auto;
}

.counter-box{
padding:15px 5px;
border-radius:19px;
background:linear-gradient(145deg,#fff7fa,#fffdfb);
border:1px solid rgba(192,95,130,.14);
box-shadow:0 7px 18px rgba(90,50,60,.07);
}

.number{
color:var(--deep);
font-size:clamp(22px,5vw,36px);
font-weight:bold;
}

.label{
margin-top:4px;
color:#a27682;
font-size:11px;
text-transform:uppercase;
letter-spacing:.8px;
}

.card,.music{
position:relative;
margin:30px 0;
padding:30px;
background:var(--paper);
border:1px solid rgba(160,91,111,.18);
border-radius:30px;
box-shadow:0 18px 50px var(--shadow);
backdrop-filter:blur(8px);
}

.card:before,.music:before{
content:"";
position:absolute;
inset:8px;
border:1px dashed rgba(182,107,131,.28);
border-radius:23px;
pointer-events:none;
}

.card h2{
position:relative;
margin-top:0;
color:var(--deep);
font-size:30px;
}

.card p{
position:relative;
font-size:19px;
line-height:1.7;
}

#login{
max-width:450px;
margin:25px auto 40px;
text-align:center;
}

.login-title{
color:var(--deep);
font-size:29px;
font-weight:bold;
}

.login-subtitle{
margin:10px 0 25px;
color:var(--muted);
font-size:17px;
}

label{
display:block;
margin:10px 0 6px;
font-size:17px;
}

input,textarea{
width:100%;
padding:14px;
margin:7px 0 14px;
border:1px solid #d6aeba;
border-radius:16px;
background:rgba(255,255,255,.95);
color:var(--text);
font-family:inherit;
font-size:17px;
outline:none;
}

textarea{
min-height:150px;
resize:vertical;
}

input[type=file]{padding:11px}

button{
font-family:inherit;
}

.primary{
border:none;
border-radius:30px;
padding:14px 24px;
background:linear-gradient(135deg,#c7678a,#ae5577);
color:white;
font-size:17px;
cursor:pointer;
box-shadow:0 9px 24px rgba(150,70,100,.2);
}

.primary:disabled{
opacity:.6;
cursor:not-allowed;
}

#loginButton{width:100%}

.logout{
padding:8px 15px;
border:1px solid #c88ca0;
border-radius:20px;
background:rgba(255,255,255,.8);
color:var(--deep);
cursor:pointer;
}

.status{
min-height:25px;
margin-top:14px;
text-align:center;
font-size:16px;
line-height:1.5;
}

.success{color:#5d8a65}
.error{color:#b04b5b}

#diary{display:none}

.diary-top{
display:flex;
justify-content:space-between;
align-items:center;
gap:15px;
margin-bottom:20px;
}

.welcome{
color:var(--deep);
font-size:17px;
overflow-wrap:anywhere;
}

.music{text-align:center;overflow:visible}

.music-icon{
display:inline-block;
font-size:45px;
}

.music.playing .music-icon{
animation:musicPulse 1.2s infinite;
}

@keyframes musicPulse{
0%,100%{transform:scale(1)}
50%{transform:scale(1.2) rotate(5deg)}
}

.music-title{
color:var(--deep);
font-size:30px;
font-weight:bold;
}

.music-subtitle{
margin:8px 0 18px;
color:var(--muted);
font-size:17px;
font-style:italic;
}

#song{
display:block;
width:100%;
max-width:500px;
margin:10px auto 18px;
}

.music-status{
min-height:24px;
margin-top:12px;
color:#8a6872;
font-size:15px;
}

.memory{
position:relative;
margin:26px 0;
padding:25px;
border:1px solid rgba(160,91,111,.15);
border-radius:23px;
background:linear-gradient(145deg,#fffdfb,#fff7f4);
box-shadow:0 13px 32px rgba(90,50,60,.09);
}

.memory h3{
margin-top:0;
padding-right:35px;
color:var(--deep);
font-size:26px;
}

.memory-date{
display:inline-block;
margin-bottom:12px;
padding:5px 11px;
border-radius:16px;
background:#fff0f4;
color:#a27682;
font-size:14px;
}

.memory p{
font-size:17px;
line-height:1.65;
white-space:pre-wrap;
overflow-wrap:anywhere;
}

.memory img{
display:block;
width:100%;
max-height:520px;
object-fit:cover;
margin-top:16px;
padding:9px 9px 28px;
border-radius:6px;
background:white;
box-shadow:0 8px 20px rgba(50,30,35,.14);
}

.loading,.empty{
padding:35px 15px;
text-align:center;
color:#98737d;
line-height:1.7;
}

.loading-bears,.empty-bear{
font-size:38px;
}

.sticker{
position:fixed;
right:14px;
bottom:14px;
z-index:20;
width:72px;
height:72px;
border-radius:50%;
display:flex;
justify-content:center;
align-items:center;
background:rgba(255,255,255,.92);
border:3px solid white;
box-shadow:0 8px 25px rgba(90,40,60,.18);
animation:stickerFloat 3s infinite;
pointer-events:none;
}

.sticker:before{content:"🧸";font-size:40px}
.sticker:after{
content:"💕";
position:absolute;
top:-12px;
right:-5px;
font-size:20px;
}

@keyframes stickerFloat{
0%,100%{transform:translateY(0) rotate(-4deg)}
50%{transform:translateY(-8px) rotate(4deg)}
}

.runner{
position:relative;
width:100%;
height:230px;
margin:20px 0;
overflow:hidden;
border-radius:22px;
background:linear-gradient(to bottom,#fff2f7 0%,#fff9f7 72%,#f7d9e3 72%,#f7d9e3 74%,#fff9f7 74%);
border:1px solid #edc3d0;
}

.runner-cloud{
position:absolute;
font-size:30px;
opacity:.5;
animation:cloudMove 14s linear infinite;
}

.cloud1{top:25px;left:100%}
.cloud2{top:65px;left:130%;animation-delay:6s}

@keyframes cloudMove{
from{transform:translateX(0)}
to{transform:translateX(-650px)}
}

.player{
position:absolute;
left:55px;
bottom:55px;
width:42px;
height:48px;
font-size:39px;
z-index:5;
}

.obstacle{
position:absolute;
bottom:52px;
right:-60px;
font-size:38px;
z-index:4;
}

.game-ground{
position:absolute;
bottom:0;
left:0;
right:0;
height:54px;
border-top:3px solid #d69aaf;
}

.game-score{
display:flex;
justify-content:space-between;
margin:12px 4px;
color:var(--deep);
font-weight:bold;
}

.game-controls{
display:flex;
justify-content:center;
gap:10px;
margin-top:12px;
}

.game-control{
min-width:130px;
padding:13px 18px;
border:none;
border-radius:25px;
background:var(--rose);
color:white;
font-size:16px;
cursor:pointer;
touch-action:manipulation;
}

.game-message{
min-height:25px;
text-align:center;
color:var(--muted);
margin-top:10px;
}

footer{
margin-top:55px;
padding-bottom:20px;
text-align:center;
color:#86636d;
font-size:16px;
}

.footer-bears{
font-size:35px;
margin-bottom:8px;
}

@media(max-width:600px){
.container{width:94%;padding-top:12px}
.card,.music,.counter{padding:24px 19px;border-radius:24px}
h1{font-size:43px}
.subtitle{font-size:18px}
.teddies{transform:scale(.82);margin-bottom:-8px}
.counter-grid{gap:6px}
.counter-box{padding:12px 3px}
.number{font-size:22px}
.label{font-size:9px}
.diary-top{flex-direction:column;align-items:flex-start}
.logout{align-self:flex-end}
.sticker{width:60px;height:60px;right:8px;bottom:8px}
.sticker:before{font-size:32px}
.runner{height:210px}
.player{left:30px}
.game-control{width:100%;min-width:0}
.game-controls{gap:8px}
}
</style>
</head>

<body>

<div class="decorations">
<div class="float">💕</div>
<div class="float">💗</div>
<div class="float">💖</div>
<div class="float">❤️</div>
<div class="float">✨</div>

<div class="sparkle s1">✦</div>
<div class="sparkle s2">✧</div>
<div class="sparkle s3">✦</div>
<div class="sparkle s4">✧</div>
</div>

<div class="container">

<header>

<div class="teddies">

<div class="teddy">
<div class="head">
<div class="ear left"></div>
<div class="ear right"></div>
<div class="eye left"></div>
<div class="eye right"></div>
<div class="cheek left"></div>
<div class="cheek right"></div>
<div class="muzzle">
<div class="nose"></div>
<div class="mouth"></div>
</div>
</div>

<div class="body"><div class="belly"></div></div>
<div class="arm left"></div>
<div class="arm right"></div>
<div class="leg left"></div>
<div class="leg right"></div>
<div class="heart">❤️</div>
</div>

<div class="teddy girl">
<div class="bow">🎀</div>
<div class="head">
<div class="ear left"></div>
<div class="ear right"></div>
<div class="eye left"></div>
<div class="eye right"></div>
<div class="cheek left"></div>
<div class="cheek right"></div>
<div class="muzzle">
<div class="nose"></div>
<div class="mouth"></div>
</div>
</div>

<div class="body"><div class="belly"></div></div>
<div class="arm left"></div>
<div class="arm right"></div>
<div class="leg left"></div>
<div class="leg right"></div>
<div class="heart">💗</div>
</div>

</div>

<div class="header-heart">❤️</div>

<h1>The Us Story</h1>

<div class="divider"><span>♡</span></div>

<p class="subtitle">
A tiny corner of the internet<br>
that belongs only to our story. 🧸❤️
</p>

</header>

<div class="counter">

<div class="counter-heart">❤️</div>

<div class="counter-title">Our Story So Far</div>

<div class="counter-date">
Since 11 January 2022 · every second counts · forever ♾️
</div>

<div class="counter-grid">

<div class="counter-box">
<div id="days" class="number">0</div>
<div class="label">Days</div>
</div>

<div class="counter-box">
<div id="hours" class="number">00</div>
<div class="label">Hours</div>
</div>

<div class="counter-box">
<div id="minutes" class="number">00</div>
<div class="label">Minutes</div>
</div>

<div class="counter-box">
<div id="seconds" class="number">00</div>
<div class="label">Seconds</div>
</div>

</div>
</div>

<div id="login" class="card">

<div class="login-title">🔐 Our Private Diary</div>

<div class="login-subtitle">
Just us, our memories, and a little piece of forever. ❤️
</div>

<label>Email</label>
<input id="email" type="email" placeholder="Enter your email">

<label>Password</label>
<input id="password" type="password" placeholder="Enter your password">

<button id="loginButton" class="primary" type="button">
Enter Our Diary ❤️
</button>

<div id="loginStatus" class="status"></div>

</div>

<div id="diary">

<div class="diary-top">
<div id="welcome" class="welcome">Welcome back ❤️</div>
<button id="logout" class="logout">Logout</button>
</div>

<div id="music" class="music">

<div class="music-icon">🎵</div>

<div class="music-title">Our Song ❤️</div>

<div class="music-subtitle">
A little soundtrack for our little world...
</div>

<audio id="song" preload="metadata" controls playsinline>
<source src="./vidssave.com%20Osho%20Jain%20_%20Tu%20Aisa%20Kaise%20Hai_%20%E2%80%93%20%23OshoJain%20720P.mp3" type="audio/mpeg">
Your browser does not support audio.
</audio>

<button id="musicButton" class="primary">
▶ Play Our Song
</button>

<div id="musicStatus" class="music-status">
Our song ❤️
</div>

</div>

<div class="card">

<h2>🌷 To Us</h2>

<p>
Some moments are too beautiful to disappear into a phone gallery.
<br><br>
So this little place exists for us — for the photos, the silly moments,
the milestones, the conversations, and all those tiny things that somehow
became huge parts of our story.
<br><br>
One day we'll look back at this place and realize just how much life we lived together. ❤️
</p>

</div>

<div class="card">

<h2>✨ Save A Little Moment</h2>

<label>Memory title</label>
<input id="title" type="text" placeholder="Our first date...">

<label>Date</label>
<input id="date" type="date">

<label>What happened?</label>
<textarea id="message" placeholder="Write everything you want us to remember..."></textarea>

<label>Add a photo 📷</label>
<input id="photo" type="file" accept="image/*">

<button id="save" class="primary">
🧸 Save This Little Moment ♡
</button>

<div id="status" class="status"></div>

</div>

<div class="card">

<h2>📖 Our Memory Wall</h2>

<p style="color:#80616a;margin-top:-5px;margin-bottom:25px;">
Little pieces of us, kept safe in one place. ♡
</p>

<div id="memories">
<div class="loading">
<div class="loading-bears">🧸 💕 🧸</div>
<br>
Bringing our memories...
</div>
</div>

</div>

<div class="card">

<h2>💌 Missing Me? Let's Look Back Together</h2>

<p>
Feeling a little lonely?
Come play our tiny endless-runner.
Jump over the little obstacles and see how long you can keep our story going. 🧸❤️
</p>

<div class="runner" id="runner">

<div class="runner-cloud cloud1">☁️</div>
<div class="runner-cloud cloud2">☁️</div>

<div id="player" class="player">🧸</div>
<div id="obstacle" class="obstacle">🌷</div>

<div class="game-ground"></div>

</div>

<div class="game-score">
<span>Score: <span id="score">0</span></span>
<span>Best: <span id="best">0</span></span>
</div>

<div class="game-controls">
<button id="startGame" class="game-control">🧸 Start</button>
<button id="jumpButton" class="game-control">☝️ Jump</button>
</div>

<div id="gameMessage" class="game-message">
Tap Start, then tap Jump whenever you need to. ❤️
</div>

</div>

</div>

<div class="sticker"></div>

<footer>

<div class="footer-bears">🧸 ♡ 🧸</div>

The Us Story.<br>
A thousand little moments.<br>
One beautiful story. ❤️

</footer>

</div>

<script>

/* ================================
   SUPABASE
================================ */

const SUPABASE_URL =
"https://rxtiefedshmfbfejtetk.supabase.co";

const SUPABASE_KEY =
"sb_publishable_S59gIZua305x2r3BZ1BYKQ_Us1zmr3f";

const TABLE = "memories";

const supabaseClient =
window.supabase.createClient(
SUPABASE_URL,
SUPABASE_KEY
);


/* ================================
   COUNTER
================================ */

const relationshipStart =
new Date("2022-01-11T00:00:00");

function updateCounter(){

const now = new Date();

let difference =
now.getTime() -
relationshipStart.getTime();

if(difference < 0) difference = 0;

const totalSeconds =
Math.floor(difference / 1000);

const days =
Math.floor(totalSeconds / 86400);

const hours =
Math.floor((totalSeconds % 86400) / 3600);

const minutes =
Math.floor((totalSeconds % 3600) / 60);

const seconds =
totalSeconds % 60;

document.getElementById("days").textContent =
days.toLocaleString();

document.getElementById("hours").textContent =
String(hours).padStart(2,"0");

document.getElementById("minutes").textContent =
String(minutes).padStart(2,"0");

document.getElementById("seconds").textContent =
String(seconds).padStart(2,"0");
}

updateCounter();
setInterval(updateCounter,1000);


/* ================================
   ELEMENTS
================================ */

const login =
document.getElementById("login");

const diary =
document.getElementById("diary");

const loginButton =
document.getElementById("loginButton");

const logoutButton =
document.getElementById("logout");

const loginStatus =
document.getElementById("loginStatus");

const welcome =
document.getElementById("welcome");

const saveButton =
document.getElementById("save");

const status =
document.getElementById("status");

const memoriesContainer =
document.getElementById("memories");


/* ================================
   LOGIN DISPLAY
================================ */

function showLogin(){

login.style.display = "block";
diary.style.display = "none";

}

function showDiary(user){

login.style.display = "none";
diary.style.display = "block";

if(user && user.email){
welcome.textContent =
"Welcome back ❤️ " + user.email;
}

loadMemories();

}


/* ================================
   LOGIN
================================ */

async function doLogin(){

const email =
document.getElementById("email").value.trim();

const password =
document.getElementById("password").value;

if(!email || !password){

loginStatus.className = "status error";
loginStatus.textContent =
"Please enter both email and password ❤️";

return;
}

loginButton.disabled = true;
loginButton.textContent =
"Opening our diary... ❤️";

try{

const {data,error} =
await supabaseClient.auth.signInWithPassword({
email,
password
});

if(error) throw error;

if(!data || !data.session || !data.user){
throw new Error("Login session could not be created.");
}

loginStatus.textContent = "";
showDiary(data.user);

}catch(error){

console.error(error);

loginStatus.className = "status error";

loginStatus.textContent =
error.message ||
"Couldn't log in. Please check your details.";

}finally{

loginButton.disabled = false;

loginButton.textContent =
"Enter Our Diary ❤️";

}

}


/* ================================
   LOGOUT
================================ */

async function doLogout(){

await supabaseClient.auth.signOut();

showLogin();

loginStatus.className = "status";
loginStatus.textContent = "Logged out ❤️";

}


/* ================================
   AUTH
================================ */

supabaseClient.auth.onAuthStateChange(
function(event,session){

if(session && session.user){
showDiary(session.user);
}else{
showLogin();
}

});


async function checkSession(){

try{

const {data,error} =
await supabaseClient.auth.getSession();

if(error) throw error;

if(data.session && data.session.user){
showDiary(data.session.user);
}else{
showLogin();
}

}catch(error){

console.error(error);
showLogin();

}

}

checkSession();


/* ================================
   ESCAPE HTML
================================ */

function escapeHTML(value){

if(value === null || value === undefined)
return "";

return String(value)
.replace(/&/g,"&amp;")
.replace(/</g,"&lt;")
.replace(/>/g,"&gt;")
.replace(/"/g,"&quot;")
.replace(/'/g,"&#039;");

}


/* ================================
   IMAGE COMPRESSION
================================ */

function compressImage(file){

return new Promise(function(resolve,reject){

const reader = new FileReader();

reader.onload = function(event){

const image = new Image();

image.onload = function(){

const MAX = 1600;

let width = image.width;
let height = image.height;

if(width > MAX || height > MAX){

if(width > height){

height = Math.round(height * MAX / width);
width = MAX;

}else{

width = Math.round(width * MAX / height);
height = MAX;

}

}

const canvas =
document.createElement("canvas");

canvas.width = width;
canvas.height = height;

const ctx =
canvas.getContext("2d");

ctx.drawImage(
image,
0,
0,
width,
height
);

resolve(
canvas.toDataURL("image/jpeg",.82)
);

};

image.onerror = function(){
reject(new Error("This image could not be processed."));
};

image.src = event.target.result;

};

reader.onerror = function(){
reject(new Error("Could not read the photo."));
};

reader.readAsDataURL(file);

});

}


/* ================================
   LOAD MEMORIES
================================ */

async function loadMemories(){

memoriesContainer.innerHTML = `
<div class="loading">
<div class="loading-bears">🧸 💕 🧸</div>
<br>
Bringing our memories...
</div>
`;

try{

const {data:userData,error:userError} =
await supabaseClient.auth.getUser();

if(userError) throw userError;

const user = userData.user;

if(!user){

memoriesContainer.innerHTML =
`<div class="empty">Please log in to see our memories. ❤️</div>`;

return;

}

const {data,error} =
await supabaseClient
.from(TABLE)
.select("id,user_id,title,date,message,image,created_at")
.eq("user_id",user.id)
.order("created_at",{ascending:false});

if(error) throw error;

displayMemories(data || []);

}catch(error){

console.error(error);

memoriesContainer.innerHTML = `
<div class="empty">
<div class="empty-bear">🧸💔</div>
<strong>Our memory wall couldn't load.</strong>
<br><br>
${escapeHTML(error.message || "Unknown error.")}
</div>
`;

}

}


/* ================================
   DISPLAY MEMORIES
================================ */

function displayMemories(memories){

if(!memories.length){

memoriesContainer.innerHTML = `
<div class="empty">
<div class="empty-bear">🧸💕</div>
No memories yet...
<br>
Let's save our first little moment. ❤️
</div>
`;

return;

}

memoriesContainer.innerHTML = "";

memories.forEach(function(memory){

const article =
document.createElement("article");

article.className = "memory";

let dateHTML = "";

if(memory.date){

const d =
new Date(memory.date + "T00:00:00");

dateHTML = `
<div class="memory-date">
${escapeHTML(
d.toLocaleDateString(undefined,{
day:"numeric",
month:"long",
year:"numeric"
})
)}
</div>
`;

}

let imageHTML = "";

if(memory.image){

imageHTML = `
<img
src="${escapeHTML(memory.image)}"
alt="Our memory"
loading="lazy">
`;

}

article.innerHTML = `
<h3>${escapeHTML(memory.title)}</h3>
${dateHTML}
<p>${escapeHTML(memory.message)}</p>
${imageHTML}
`;

memoriesContainer.appendChild(article);

});

}


/* ================================
   SAVE MEMORY
================================ */

async function saveMemory(){

const title =
document.getElementById("title").value.trim();

const date =
document.getElementById("date").value;

const message =
document.getElementById("message").value.trim();

const photoInput =
document.getElementById("photo");

if(!title || !message){

status.className = "status error";
status.textContent =
"Please add a title and message ❤️";

return;

}

saveButton.disabled = true;

saveButton.textContent =
"Saving our little moment... 🧸";

try{

const {data:userData,error:userError} =
await supabaseClient.auth.getUser();

if(userError) throw userError;

const user = userData.user;

if(!user){
throw new Error(
"Your login session has expired. Please log in again."
);
}

let image = null;

if(photoInput.files.length > 0){

const file = photoInput.files[0];

if(!file.type.startsWith("image/")){
throw new Error("Please choose an image file.");
}

if(file.size > 15 * 1024 * 1024){
throw new Error(
"That photo is over 15 MB. Please choose a smaller photo."
);
}

status.className = "status";
status.textContent =
"Making the photo diary-friendly... 📷";

image = await compressImage(file);

}

const {error} =
await supabaseClient
.from(TABLE)
.insert({
user_id:user.id,
title:title,
date:date || null,
message:message,
image:image
});

if(error) throw error;

status.className = "status success";

status.textContent =
"Our little moment is safely saved forever. ❤️";

document.getElementById("title").value = "";
document.getElementById("date").value = "";
document.getElementById("message").value = "";
photoInput.value = "";

celebration();

await loadMemories();

}catch(error){

console.error(error);

status.className = "status error";

status.textContent =
error.message ||
"Couldn't save this memory.";

}finally{

saveButton.disabled = false;

saveButton.textContent =
"🧸 Save This Little Moment ♡";

}

}


/* ================================
   CELEBRATION
================================ */

function celebration(){

const symbols =
["❤️","💕","💗","💖","✨","🧸"];

for(let i=0;i<15;i++){

const element =
document.createElement("div");

element.style.position = "fixed";
element.style.zIndex = "100";
element.style.pointerEvents = "none";
element.style.fontSize = "25px";

element.textContent =
symbols[Math.floor(Math.random()*symbols.length)];

element.style.left = "50%";
element.style.top = "50%";

element.style.transform =
`translate(${Math.random()*340-170}px,
${Math.random()*340-240}px)`;

document.body.appendChild(element);

setTimeout(function(){
element.remove();
},1500);

}

}


/* ================================
   MUSIC
================================ */

const song =
document.getElementById("song");

const music =
document.getElementById("music");

const musicButton =
document.getElementById("musicButton");

const musicStatus =
document.getElementById("musicStatus");

musicButton.addEventListener(
"click",
async function(){

if(song.paused){

try{

await song.play();

}catch(error){

musicStatus.textContent =
"Couldn't play the song. Check the song filename. ❤️";

}

}else{

song.pause();

}

});


song.addEventListener("play",function(){

music.classList.add("playing");

musicButton.textContent =
"⏸ Pause Our Song";

musicStatus.textContent =
"Playing our song ❤️";

});


song.addEventListener("pause",function(){

music.classList.remove("playing");

if(!song.ended){

musicButton.textContent =
"▶ Play Our Song";

musicStatus.textContent =
"Paused ❤️";

}

});


song.addEventListener("ended",function(){

music.classList.remove("playing");

musicButton.textContent =
"▶ Play Our Song";

musicStatus.textContent =
"Our song ❤️";

});


/* ================================
   GAME
================================ */

const runner =
document.getElementById("runner");

const player =
document.getElementById("player");

const obstacle =
document.getElementById("obstacle");

const scoreElement =
document.getElementById("score");

const bestElement =
document.getElementById("best");

const startGameButton =
document.getElementById("startGame");

const jumpButton =
document.getElementById("jumpButton");

const gameMessage =
document.getElementById("gameMessage");

let gameRunning = false;
let jumping = false;
let velocityY = 0;
let playerY = 0;
let obstacleX = -70;
let score = 0;
let gameSpeed = 6;
let animationFrame = null;
let lastTime = 0;

let best =
Number(localStorage.getItem("theUsStoryBest") || 0);

bestElement.textContent = best;


function jump(){

if(!gameRunning || jumping) return;

jumping = true;
velocityY = 14;

}


function startGame(){

if(gameRunning) return;

gameRunning = true;
jumping = false;
velocityY = 0;
playerY = 0;

obstacleX =
runner.clientWidth + 40;

score = 0;
gameSpeed = 6;

scoreElement.textContent = "0";

gameMessage.textContent =
"Keep going! 🧸❤️";

startGameButton.textContent =
"🔄 Restart";

lastTime = performance.now();

cancelAnimationFrame(animationFrame);

animationFrame =
requestAnimationFrame(gameLoop);

}


function gameOver(){

gameRunning = false;

cancelAnimationFrame(animationFrame);

if(score > best){

best = score;

localStorage.setItem(
"theUsStoryBest",
best
);

bestElement.textContent = best;

gameMessage.textContent =
"NEW BEST! 🧸💗 You made our story longer!";

}else{

gameMessage.textContent =
"Aww, you bumped into a flower. 🌷 Try again? ❤️";

}

startGameButton.textContent =
"🧸 Play Again";

}


function gameLoop(time){

if(!gameRunning) return;

const delta =
Math.min((time-lastTime)/16.67,2);

lastTime = time;


if(jumping){

velocityY -= .75 * delta;

playerY += velocityY * delta;

if(playerY <= 0){

playerY = 0;
velocityY = 0;
jumping = false;

}

}

player.style.transform =
`translateY(${-playerY}px)`;


obstacleX -= gameSpeed * delta;

if(obstacleX < -70){

obstacleX =
runner.clientWidth + 20;

score++;

scoreElement.textContent = score;

gameSpeed =
Math.min(12,6+score*.12);

}

obstacle.style.transform =
`translateX(${obstacleX}px)`;


const playerRect =
player.getBoundingClientRect();

const obstacleRect =
obstacle.getBoundingClientRect();

const padding = 8;

const collision =
playerRect.left + padding <
obstacleRect.right - padding &&

playerRect.right - padding >
obstacleRect.left + padding &&

playerRect.top + padding <
obstacleRect.bottom - padding &&

playerRect.bottom - padding >
obstacleRect.top + padding;

if(collision){

gameOver();
return;

}

animationFrame =
requestAnimationFrame(gameLoop);

}


startGameButton.addEventListener(
"click",
startGame
);

jumpButton.addEventListener(
"pointerdown",
function(event){

event.preventDefault();
jump();

});


runner.addEventListener(
"pointerdown",
function(event){

if(gameRunning){

event.preventDefault();
jump();

}

});


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

});


/* ================================
   BUTTONS
================================ */

loginButton.addEventListener(
"click",
doLogin
);

logoutButton.addEventListener(
"click",
doLogout
);

saveButton.addEventListener(
"click",
saveMemory
);


document.getElementById("password")
.addEventListener(
"keydown",
function(event){

if(event.key === "Enter"){
doLogin();
}

});


document.getElementById("email")
.addEventListener(
"keydown",
function(event){

if(event.key === "Enter"){

document.getElementById("password").focus();

}

});

</script>

</body>
</html>
