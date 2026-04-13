# Sorry-<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>I'm Sorry Seju🥺</title>

<style>
body {
    margin: 0;
    padding: 0;
    text-align: center;
    font-family: 'Segoe UI', sans-serif;
    background: linear-gradient(135deg, #ff758c, #ff7eb3);
    overflow: hidden;
    color: white;
}

h1 {
    margin-top: 80px;
    font-size: 35px;
}

#typing {
    font-size: 20px;
    width: 80%;
    margin: auto;
    min-height: 60px;
}

.btn {
    padding: 12px 25px;
    font-size: 18px;
    border: none;
    border-radius: 10px;
    cursor: pointer;
    margin: 20px;
}

#yes {
    background: #4CAF50;
    color: white;
}

#no {
    background: red;
    color: white;
    position: absolute;
}

.heart {
    position: absolute;
    font-size: 20px;
    animation: fall 3s linear infinite;
}

@keyframes fall {
    0% { transform: translateY(-10px); opacity: 1; }
    100% { transform: translateY(100vh); opacity: 0; }
}
</style>
</head>

<body>

<h1>I'm Really Sorry 😔</h1>
<p id="typing"></p>

<button class="btn" id="yes" onclick="yesClick()">Yes 😊</button>
<button class="btn" id="no" onmouseover="moveButton()">No 😒</button>

<!-- 🎵 Music -->
<audio id="music" autoplay loop>
  <source src="https://www.fesliyanstudios.com/play-mp3/387" type="audio/mpeg">
</audio>

<script>
// ✨ Typing Effect
let text = "Please mujhe maaf kar do... 🥺 Main promise karta hu dobara galti nahi hogi ❤️ ";
let i = 0;

function typing() {
    if (i < text.length) {
        document.getElementById("typing").innerHTML += text.charAt(i);
        i++;
        setTimeout(typing, 50);
    }
}
typing();

// 😂 No Button Bhaagega
function moveButton() {
    let x = Math.random() * window.innerWidth;
    let y = Math.random() * window.innerHeight;
    document.getElementById("no").style.left = x + "px";
    document.getElementById("no").style.top = y + "px";
}

// 💖 Yes Click
function yesClick() {
    document.body.innerHTML = `
        <h1 style='margin-top:100px;'>Thank You ❤️🥺</h1>
        
    `;
    hearts();
}

// ❤️ Hearts Rain
function hearts() {
    setInterval(() => {
        let heart = document.createElement("div");
        heart.classList.add("heart");
        heart.innerHTML = "❤️";
        heart.style.left = Math.random() * 100 + "vw";
        document.body.appendChild(heart);

        setTimeout(() => {
            heart.remove();
        }, 3000);
    }, 200);
}
</script>

</body>
</html>
