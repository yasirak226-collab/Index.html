<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Vivi x Gloo Forever</title>

<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@700&family=Poppins:wght@400;600&display=swap" rel="stylesheet">

<style>
body{
margin:0;
height:100vh;
background:radial-gradient(circle at center,#8a2be2,#240046);
display:flex;
justify-content:center;
align-items:center;
font-family:Poppins;
overflow:hidden;
color:white;
text-align:center;
}

/* Background floating particles */
.particle{
position:absolute;
font-size:22px;
animation:floatUp 6s linear infinite;
opacity:0.7;
}

@keyframes floatUp{
0%{transform:translateY(100vh);opacity:0;}
50%{opacity:1;}
100%{transform:translateY(-10vh);opacity:0;}
}

/* Shake */
@keyframes shake{
0%{transform:translate(0);}
25%{transform:translate(-8px,6px);}
50%{transform:translate(8px,-6px);}
75%{transform:translate(-6px,8px);}
100%{transform:translate(0);}
}
.shake{
animation:shake 0.4s ease;
}

.container{
z-index:2;
}

h1{
font-family:Orbitron;
font-size:2rem;
}

/* Buttons */
button{
padding:14px 35px;
margin:12px;
font-size:1.1rem;
border:none;
border-radius:30px;
cursor:pointer;
transition:.3s;
}

#yesBtn{
background:gold;
color:black;
}

#noBtn{
background:grey;
position:relative;
}

/* Medal */
.medal{
position:absolute;
top:50%;
left:50%;
transform:translate(-50%,-50%) scale(0);
font-family:Orbitron;
font-size:2.8rem;
color:gold;
animation:medalAnim 1.5s ease forwards;
}

@keyframes medalAnim{
0%{transform:translate(-50%,-50%) scale(0);opacity:0;}
50%{transform:translate(-50%,-50%) scale(1.5);opacity:1;}
100%{transform:translate(-50%,-50%) scale(1);opacity:0;}
}

/* Mythic Banner */
.mythic{
position:absolute;
top:30%;
left:50%;
transform:translate(-50%,-50%) scale(0);
font-family:Orbitron;
font-size:2rem;
color:#ff66ff;
animation:mythicAnim 2s forwards;
}

@keyframes mythicAnim{
0%{transform:translate(-50%,-50%) scale(0);}
50%{transform:translate(-50%,-50%) scale(1.3);}
100%{transform:translate(-50%,-50%) scale(1);}
}

/* Footer */
.footer{
position:absolute;
bottom:15px;
width:100%;
50%{transform:translate(10px,-10px);}
75%{transform:translate(-10px,10px);}
100%{transform:translate(0,0);}
}

/* Flash */
.flash{
position:absolute;
width:100%;
height:100%;
background:white;
opacity:0;
animation:flashAnim .5s ease;
}
@keyframes flashAnim{
0%{opacity:1;}
100%{opacity:0;}
}

/* Loading */
.loading{
position:absolute;
width:100%;
height:100%;
background:black;
display:flex;
justify-content:center;
align-items:center;
font-family:Orbitron;
font-size:1.8rem;
z-index:5;
animation:fadeOut 1s ease 2s forwards;
}
@keyframes fadeOut{
to{opacity:0;visibility:hidden;}
}

/* Slime background blobs */
.blob{
position:absolute;
width:150px;
height:150px;
background:rgba(178,102,255,0.4);
border-radius:50%;
filter:blur(30px);
animation:blobMove 8s infinite alternate ease-in-out;
}
@keyframes blobMove{
from{transform:translate(-50px,-50px);}
to{transform:translate(50px,50px);}
}

.container{z-index:2;}

h1{
font-family:Orbitron;
font-size:2rem;
}

/* Buttons */
button{
padding:12px 30px;
margin:10px;
font-size:1.1rem;
border:none;
border-radius:30px;
cursor:pointer;
transition:.3s;
}

#yesBtn{
background:gold;
color:black;
}

#noBtn{
background:grey;
position:relative;
}

/* Medal */
.medal{
position:absolute;
top:50%;
left:50%;
transform:translate(-50%,-50%) scale(0);
font-family:Orbitron;
font-size:2.5rem;
color:gold;
animation:medalAnim 1.5s ease forwards;
}
@keyframes medalAnim{
0%{transform:translate(-50%,-50%) scale(0);opacity:0;}
50%{transform:translate(-50%,-50%) scale(1.5);opacity:1;}
100%{transform:translate(-50%,-50%) scale(1);opacity:0;}
}

/* Rank Banner */
.rank{
position:absolute;
top:30%;
left:50%;
transform:translate(-50%,-50%);
font-family:Orbitron;
font-size:2rem;
color:#ffdd00;
opacity:0;
animation:rankAnim 2s ease forwards;
}
@keyframes rankAnim{
0%{opacity:0;transform:translate(-50%,-50%) scale(.5);}
50%{opacity:1;transform:translate(-50%,-50%) scale(1.3);}
100%{opac
    position: relative;
}

.loading-screen {
    position: fixed;
    width: 100%;
    height: 100%;
    background: linear-gradient(45deg, #000 0%, #1a0033 100%);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    z-index: 100;
    animation: fadeOut 0.5s ease-in forwards 2.5s;
}

.loading-text {
    font-family: 'Orbitron', sans-serif;
    font-size: 2.5rem;
    font-weight: 900;
    margin-bottom: 30px;
    background: linear-gradient(90deg, #b266ff, #ff66ff, #b266ff);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    animation: pulse 1.5s ease-in-out infinite;
}

.loading-bar {
    width: 200px;
    height: 4px;
    background: rgba(178, 102, 255, 0.2);
    border-radius: 2px;
    overflow: hidden;
}

.loading-bar-fill {
    height: 100%;
    background: linear-gradient(90deg, #b266ff, #ff66ff);
    animation: loadingFill 2.5s ease-in-out forwards;
}

@keyframes loadingFill {
    0% { width: 0%; }
    100% { width: 100%; }
}

@keyframes pulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.7; transform: scale(1.05); }
}

@keyframes fadeOut {
    to {
        opacity: 0;
        pointer-events: none;
    }
}

.container {
    padding: 40px 20px;
    max-width: 600px;
    z-index: 1;
}

h1 {
    font-family: 'Orbitron', sans-serif;
    font-size: 2.5rem;
    margin-bottom: 20px;
    background: linear-gradient(90deg, #b266ff, #ff66ff, #b266ff);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    text-shadow: 0 0 30px rgba(178, 102, 255, 0.5);
    animation: titlePulse 3s ease-in-out infinite;
    letter-spacing: 2px;
}

@keyframes titlePulse {
    0%, 100% { 
        filter: drop-shadow(0 0 10px rgba(178, 102, 255, 0.6));
    }
    50% { 
        filter: drop-shadow(0 0 20px rgba(255, 102, 255, 0.8));
    }
}

.hero-container {
    display: flex;
    justify-content: center;
    gap: 15px;
    margin: 30px 0;
    flex-wrap: wrap;
}

.hero-img {
    width: 200px;
    height: 200px;
    border-radius: 20px;
    box-shadow: 0 0 30px rgba(178, 102, 255, 0.8), inset 0 0 20px rgba(178, 102, 255, 0.3);
    border: 3px solid rgba(255, 102, 255, 0.6);
    object-fit: cover;
    animation: floatImage 3s ease-in-out infinite;
    transition: transform 0.3s ease;
}

.hero-img:nth-child(1) {
    animation-delay: 0s;
}

.hero-img:nth-child(2) {
    animation-delay: 0.5s;
}

@keyframes floatImage {
    0%, 100% { 
        transform: translateY(0px) scale(1);
        filter: brightness(1);
    }
    50% { 
        transform: translateY(-15px) scale(1.02);
        filter: brightness(1.1);
    }
}

.hero-img:hover {
    transform: scale(1.05);
    box-shadow: 0 0 40px rgba(255, 102, 255, 1), inset 0 0 30px rgba(178, 102, 255, 0.5);
}

.button-container {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-top: 40px;
    flex-wrap: wrap;
}

button {
    padding: 15px 40px;
    font-size: 1.2rem;
    font-weight: 600;
    border: none;
    border-radius: 50px;
    cursor: pointer;
    font-family: 'Poppins', sans-serif;
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
    text-transform: uppercase;
    letter-spacing: 1px;
    box-shadow: 0 0 20px rgba(178, 102, 255, 0.5);
}

button::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: rgba(255, 255, 255, 0.2);
    transition: left 0.5s ease;
    z-index: -1;
}

button:hover::before {
    left: 100%;
}

#yesBtn {
    background: linear-gradient(135deg, #FFD700, #FFA500);
    color: #000;
    box-shadow: 0 0 30px rgba(255, 215, 0, 0.8);
}

#yesBtn:hover {
    transform: scale(1.05);
    box-shadow: 0 0 50px rgba(255, 215, 0, 1);
}

#yesBtn:active {
    transform: scale(0.98);
}

#noBtn {
    background: linear-gradient(135deg, #666666, #444444);
    color: white;
    box-shadow: 0 0 20px rgba(100, 100, 100, 0.6);
}

#noBtn:hover {
    background: linear-gradient(135deg, #777777, #555555);
    box-shadow: 0 0 30px rgba(150, 150, 150, 0.8);
}

.medal {
    position: fixed;
    font-family: 'Orbitron', sans-serif;
    font-size: 4rem;
    font-weight: 900;
    color: #FFD700;
    text-shadow: 0 0 20px rgba(255, 215, 0, 0.8);
    animation: medalPop 1.8s cubic-bezier(0.68, -0.55, 0.265, 1.55) forwards;
    pointer-events: none;
    z-index: 50;
}

@keyframes medalPop {
    0% { 
        transform: scale(0) rotate(-180deg);
        opacity: 0;
    }
    50% { 
        transform: scale(1.3) rotate(20deg);
        opacity: 1;
    }
    100% { 
        transform: scale(1) rotate(0deg);
        opacity: 0;
    }
}

.flower {
    position: fixed;
    font-size: 2rem;
    animation: floatUpFlower 4s ease-out forwards;
    pointer-events: none;
    z-index: 30;
    filter: drop-shadow(0 0 5px rgba(255, 105, 180, 0.8));
}

@keyframes floatUpFlower {
    0% { 
        transform: translateY(0) translateX(0) scale(1) rotate(0deg);
        opacity: 1;
    }
    50% {
        transform: translateY(-200px) translateX(50px) scale(1.1) rotate(180deg);
        opacity: 0.8;
    }
    100% { 
        transform: translateY(-500px) translateX(100px) scale(0.5) rotate(360deg);
        opacity: 0;
    }
}

.slime {
    position: fixed;
    font-size: 1.5rem;
    animation: floatUpSlime 4s ease-out forwards;
    pointer-events: none;
    z-index: 30;
    filter: drop-shadow(0 0 8px rgba(178, 102, 255, 0.8));
}

@keyframes floatUpSlime {
    0% { 
        transform: translateY(0) translateX(0) scale(1);
        opacity: 1;
    }
    50% {
        transform: translateY(-250px) translateX(-80px) scale(1.2);
        opacity: 0.9;
    }
    100% { 
        transform: translateY(-600px) translateX(-150px) scale(0.3);
        opacity: 0;
    }
}

.confetti {
    position: fixed;
    width: 10px;
    height: 10px;
    animation: confettiFall 4s ease-in forwards;
    pointer-events: none;
    z-index: 30;
}

@keyframes confettiFall {
    0% {
        transform: translateY(0) translateX(0) rotate(0deg);
        opacity: 1;
    }
    100% {
        transform: translateY(500px) translateX(150px) rotate(720deg);
        opacity: 0;
    }
}

.victory-screen {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: none;
    justify-content: center;
    align-items: center;
    background: rgba(0, 0, 0, 0.8);
    z-index: 200;
    flex-direction: column;
    gap: 20px;
}

.victory-screen.active {
    display: flex;
    animation: victoryFadeIn 0.5s ease-out;
}

@keyframes victoryFadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}

.victory-text {
    font-family: 'Orbitron', sans-serif;
    font-size: 3rem;
    font-weight: 900;
    background: linear-gradient(90deg, #FFD700, #FF1493, #FFD700);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    text-shadow: 0 0 50px rgba(255, 215, 0, 0.8);
    animation: victoryPulse 0.6s ease-out;
}

@keyframes victoryPulse {
    0% { transform: scale(0.5); }
    100% { transform: scale(1); }
}

@keyframes spin {
    0% { transform: rotate(0deg) scale(1); }
    50% { transform: rotate(180deg) scale(1.1); }
    100% { transform: rotate(360deg) scale(1); }
}

@media (max-width: 600px) {
    h1 {
        font-size: 2rem;
    }
    
    .hero-img {
        width: 150px;
        height: 150px;
    }
    
    button {
        padding: 12px 30px;
        font-size: 1rem;
    }
}
</style>
</head>

<body>

<div class="loading-screen" id="loading">
    <div class="loading-text">MATCH FOUND…</div>
    <div style="margin: 20px 0; font-size: 3rem;">💜</div>
    <div class="loading-text" style="font-size: 1.5rem; margin-top: 20px;">Loading Gloo</div>
    <div class="loading-bar" style="margin-top: 30px;">
        <div class="loading-bar-fill"></div>
    </div>
</div>

<div class="victory-screen" id="victoryScreen">
    <div class="victory-text">GLOO FOREVER! 💜</div>
    <div style="font-size: 5rem; animation: spin 2s linear infinite;">
        💜
    </div>
</div>

<div class="container">
    <h1 id="mainText">Vivi… can I be your Gloo forever? 💜</h1>

    <div class="hero-container">
        <img class="hero-img" id="gif1" src="https://media.giphy.com/media/l0MYt5jPR6QX5pnqM/giphy.gif" alt="Gloo">
        <img class="hero-img" id="gif2" src="https://media.giphy.com/media/l0MYt5jPR6QX5pnqM/giphy.gif" alt="Gloo Celebration">
    </div>

    <div class="button-container">
        <button id="yesBtn">YES 🏆</button>
        <button id="noBtn">NO 😢</button>
    </div>
</div>

<script>
const noBtn = document.getElementById("noBtn");
const yesBtn = document.getElementById("yesBtn");
const mainText = document.getElementById("mainText");
const loading = document.getElementById("loading");
const victoryScreen = document.getElementById("victoryScreen");
const gif1 = document.getElementById("gif1");
const gif2 = document.getElementById("gif2");

setTimeout(() => {
    loading.style.opacity = "0";
    setTimeout(() => loading.remove(), 500);
}, 2500);

const noMessages = [
    "Vivi don't split from me 🥺",
    "Gloo sticks forever 😭",
    "You can't escape the slime 💜",
    "We are permanently attached 😏",
    "Final chance… little flower 🌸",
    "Are we not Gloo? 🥹"
];

let messageIndex = 0;
let yesScale = 1;
let clickCount = 0;

function moveButton() {
    const maxX = window.innerWidth - noBtn.offsetWidth - 20;
    const maxY = window.innerHeight - noBtn.offsetHeight - 20;

    noBtn.style.position = "absolute";
    noBtn.style.left = Math.floor(Math.random() * maxX) + "px";
    noBtn.style.top = Math.floor(Math.random() * maxY) + "px";

    if (messageIndex < noMessages.length) {
        mainText.textContent = noMessages[messageIndex];
        messageIndex++;
    }

    yesScale += 0.2;
    yesBtn.style.transform = `scale(${yesScale})`;
    
    clickCount++;
}

noBtn.addEventListener("mouseover", moveButton);
noBtn.addEventListener("touchstart", moveButton);

yesBtn.addEventListener("click", () => {
    mainText.textContent = "Vivi 💜 You're officially stuck with your Gloo forever!";
    
    gif1.src = "https://media.giphy.com/media/111ebonMs90YLu/giphy.gif";
    gif2.src = "https://media.giphy.com/media/111ebonMs90YLu/giphy.gif";

    noBtn.style.display = "none";
    yesBtn.style.display = "none";

    setTimeout(() => {
        victoryScreen.classList.add("active");
    }, 500);

    showMedal("SAVAGE");
    setTimeout(() => showMedal("LEGENDARY"), 800);
    setTimeout(() => showMedal("MVP"), 1600);

    setTimeout(() => createFlowers(), 200);
    setTimeout(() => createSlime(), 400);
    setTimeout(() => createConfetti(), 600);
});

function showMedal(text) {
    const medal = document.createElement("div");
    medal.className = "medal";
    medal.innerText = text;
    medal.style.top = window.innerHeight / 2 + "px";
    medal.style.left = window.innerWidth / 2 + "px";
    document.body.appendChild(medal);

    setTimeout(() => medal.remove(), 1800);
}

function createFlowers() {
    for (let i = 0; i < 40; i++) {
        const flower = document.createElement("div");
        flower.className = "flower";
        flower.innerHTML = "🌸";
        flower.style.left = Math.random() * window.innerWidth + "px";
        flower.style.top = window.innerHeight + "px";
        flower.style.fontSize = (Math.random() * 25 + 20) + "px";
        flower.style.animationDelay = (Math.random() * 0.5) + "s";
        document.body.appendChild(flower);

        setTimeout(() => flower.remove(), 4000);
    }
}

function createSlime() {
    for (let i = 0; i < 40; i++) {
        const slime = document.createElement("div");
        slime.className = "slime";
        slime.innerHTML = "💜";
        slime.style.left = Math.random() * window.innerWidth + "px";
        slime.style.top = window.innerHeight + "px";
        slime.style.fontSize = (Math.random() * 25 + 20) + "px";
        slime.style.animationDelay = (Math.random() * 0.5) + "s";
        document.body.appendChild(slime);

        setTimeout(() => slime.remove(), 4000);
    }
}

function createConfetti() {
    const colors = ["#FFD700", "#FF1493", "#b266ff", "#FF69B4"];
    
    for (let i = 0; i < 50; i++) {
        const confetti = document.createElement("div");
        confetti.className = "confetti";
        confetti.style.left = Math.random() * window.innerWidth + "px";
        confetti.style.top = 0 + "px";
        confetti.style.background = colors[Math.floor(Math.random() * colors.length)];
        confetti.style.animationDelay = (Math.random() * 0.5) + "s";
        document.body.appendChild(confetti);

        setTimeout(() => confetti.remove(), 4500);
    }
}
</script>

</body>
</html>justify-content:center;
align-items:center;
font-family:Orbitron;
font-size:1.8rem;
z-index:5;
animation:fadeOut 1s ease 2s forwards;
}

@keyframes fadeOut{
to{opacity:0;visibility:hidden;}
}

.container{padding:20px;z-index:2;}

h1{
font-family:Orbitron;
font-size:2rem;
}

/* Slime blobs */
.blob{
position:absolute;
width:120px;
height:120px;
background:rgba(178,102,255,0.4);
border-radius:50%;
filter:blur(20px);
animation:blobMove 8s infinite alternate ease-in-out;
}

@keyframes blobMove{
from{transform:translate(-50px,-50px);}
to{transform:translate(50px,50px);}
}

button{
padding:12px 30px;
margin:10px;
font-size:1.1rem;
border:none;
border-radius:30px;
cursor:pointer;
transition:.3s;
}

#yesBtn{
background:gold;
color:black;
}

#noBtn{
background:grey;
position:relative;
}

/* Medal */
.medal{
position:absolute;
top:50%;
left:50%;
transform:translate(-50%,-50%) scale(0);
font-family:Orbitron;
font-size:2.5rem;
color:gold;
animation:medalAnim 1.5s ease forwards;
}

@keyframes medalAnim{
0%{transform:translate(-50%,-50%) scale(0);opacity:0;}
50%{transform:translate(-50%,-50%) scale(1.5);opacity:1;}
100%{transform:tran
}

.hero-img {
    width:260px;
    border-radius:15px;
    margin:10px;
    box-shadow:0 0 20px #b266ff;
}

button {
    padding:12px 30px;
    margin:10px;
    font-size:1.1rem;
    border:none;
    border-radius:30px;
    cursor:pointer;
    transition:.3s;
}

#yesBtn {
    background:gold;
    color:black;
}

#noBtn {
    background:grey;
    position:relative;
}

.medal {
    position:absolute;
    font-family:Orbitron;
    font-size:2.5rem;
    color:gold;
    animation:pop 1.5s ease forwards;
}

@keyframes pop {
    0% {transform:scale(.3);opacity:0;}
    50% {transform:scale(1.4);opacity
    font-size: 2rem;
}

img {
    width: 260px;
    margin: 20px 0;
    border-radius: 15px;
}

button {
    padding: 12px 30px;
    margin: 10px;
    font-size: 1.1rem;
    border: none;
    border-radius: 30px;
    cursor: pointer;
    transition: 0.3s ease;
}

#yesBtn {
    background: gold;
    color: black;
}

#noBtn {
    background: grey;
    position: relative;
}

.medal {
    position: absolute;
    font-family: 'Orbitron', sans-serif;
    font-size: 2rem;
    color: gold;
    animation: medalPop 1.5s ease forwards;
}

@keyframes medalPop {
    0% { transform: scale(0.3); opacity: 0; }
    50% { transform: scale(1.3); opacity: 1; }
    100% { transform: scale(1); opacity: 0; }
}

.flower {
    position: absolute;
    font-size: 24px;
    animation: floatUp 4s linear forwards;
}

@keyframes floatUp {
    0% { transform: translateY(0); opacity: 1; }
    100% { transform: translateY(-400px); opacity: 0; }
}
</style>
</head>

<body>

<div class="container">
    <h1 id="mainText">Vivi… can I be your Gloo forever? 💜</h1>

    <!-- Replace with MLBB Gloo GIF -->
    <img id="gif" src="https://media.giphy.com/media/l0MYt5jPR6QX5pnqM/giphy.gif">

    <div>
        <button id="yesBtn">YES 🏆</button>
        <button id="noBtn">NO 😢</button>
    </div>
</div>

<script>
const noBtn = document.getElementById("noBtn");
const yesBtn = document.getElementById("yesBtn");
const gif = document.getElementById("gif");
const mainText = document.getElementById("mainText");

const noMessages = [
    "Vivi don’t split from me 🥺",
    "Gloo sticks forever 😭",
    "You can’t escape the slime 💜",
    "We are permanently attached 😏",
    "Final chance… little flower 🌸",
    "Are we not Gloo? 🥹"
];

let messageIndex = 0;
let yesScale = 1;

function moveButton() {
    const maxX = window.innerWidth - noBtn.offsetWidth - 20;
    const maxY = window.innerHeight - noBtn.offsetHeight - 20;

    const randomX = Math.floor(Math.random() * maxX);
    const randomY = Math.floor(Math.random() * maxY);

    noBtn.style.position = "absolute";
    noBtn.style.left = randomX + "px";
    noBtn.style.top = randomY + "px";

    if (messageIndex < noMessages.length) {
        mainText.textContent = noMessages[messageIndex];
        messageIndex++;
    }

    yesScale += 0.25;
    yesBtn.style.transform = `scale(${yesScale})`;
}

noBtn.addEventListener("mouseover", moveButton);
noBtn.addEventListener("touchstart", moveButton);

yesBtn.addEventListener("click", () => {

    mainText.textContent = "Vivi 💜 You’re officially stuck with your Gloo forever!";

    gif.src = "https://media.giphy.com/media/111ebonMs90YLu/giphy.gif";

    noBtn.style.display = "none";
    yesBtn.style.display = "none";

    showMedal("SAVAGE");
    setTimeout(() => showMedal("LEGENDARY"), 1500);
    setTimeout(() => showMedal("MVP"), 3000);

    createFlowers();
});

function showMedal(text) {
    const medal = document.createElement("div");
    medal.className = "medal";
    medal.innerText = text;
    medal.style.top = "40%";
    medal.style.left = "50%";
    medal.style.transform = "translate(-50%, -50%)";
    document.body.appendChild(medal);

    setTimeout(() => medal.remove(), 1500);
}

function createFlowers() {
    for (let i = 0; i < 40; i++) {
        const flower = document.createElement("div");
        flower.className = "flower";
        flower.innerHTML = "🌸";
        flower.style.left = Math.random() * window.innerWidth + "px";
        flower.style.top = Math.random() * window.innerHeight + "px";
        document.body.appendChild(flower);

        setTimeout(() => flower.remove(), 4000);
    }
}
</script>

</body>
</html>
