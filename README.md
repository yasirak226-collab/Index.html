<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Gloo Forever?</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&family=Orbitron:wght@700&display=swap" rel="stylesheet">

<style>
body {
    margin: 0;
    height: 100vh;
    background: radial-gradient(circle at center, #5a189a, #240046);
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: 'Poppins', sans-serif;
    overflow: hidden;
    text-align: center;
    color: white;
}

.container {
    padding: 20px;
}

h1 {
    font-family: 'Orbitron', sans-serif;
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
