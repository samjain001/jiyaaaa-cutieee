<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Jiya 💖</title>

<style>
body {
    font-family: Arial, sans-serif;
    background: pink;
    text-align: center;
    overflow: hidden;
}

.card {
    margin-top: 80px;
}

h1 {
    color: #b30059;
}

.yes {
    padding: 15px 30px;
    font-size: 18px;
    border-radius: 10px;
    border: none;
    background: red;
    color: white;
    cursor: pointer;
}

.no {
    padding: 12px 25px;
    font-size: 16px;
    border-radius: 10px;
    border: none;
    background: gray;
    color: white;
    cursor: pointer;
    position: absolute;
    transition: all 0.3s ease;
}

#cat {
    width: 140px;
    position: absolute;
    left: 50%;
    top: 150px;
    transform: translateX(-50%);
    transition: all 0.3s ease;
    animation: bounce 2s infinite;
}

.page {
    display: none;
}

.page.active {
    display: block;
}

.gifts {
    display: none;
    justify-content: center;
    gap: 20px;
    margin-top: 30px;
    flex-wrap: wrap;
}

.gift {
    background: white;
    padding: 20px;
    border-radius: 15px;
    width: 220px;
}

@keyframes bounce {
    0%, 100% { transform: translate(-50%, 0); }
    50% { transform: translate(-50%, -15px); }
}
</style>

<script>
function runAway() {
    const noBtn = document.getElementById("noBtn");
    const cat = document.getElementById("cat");

    const x = Math.random() * 70 + "vw";
    const y = Math.random() * 60 + "vh";

    noBtn.style.left = x;
    noBtn.style.top = y;

    cat.style.left = x;
    cat.style.top = y;
}

function showPage2() {
    document.getElementById("page1").classList.remove("active");
    document.getElementById("page2").classList.add("active");
}

function openGifts() {
    document.getElementById("giftsBox").style.display = "flex";
}
</script>
</head>

<body>

<!-- PAGE 1 -->
<div id="page1" class="page active">
    <div class="card">
        <h1>💖 Jiya, will you be my Valentine? 💖</h1>

        <img src="cat.gif" id="cat">

        <br><br>
        <button class="yes" onclick="showPage2()">Yes 💕</button>
        <button class="no" id="noBtn" onmouseover="runAway()" onclick="runAway()">No 😜</button>
    </div>
</div>

<!-- PAGE 2 -->
<div id="page2" class="page">
    <h1>🎁 Jiya’s Valentine Gifts 🎁</h1>

    <img src="cat.gif" style="width:120px">

    <br><br>
    <button class="yes" onclick="openGifts()">Open Your Gifts 🎁</button>

    <div class="gifts" id="giftsBox">

        <div class="gift">
            💌
            <h3>Love Letter</h3>
            <p>
                Dear Jiya,<br><br>
                You make my world brighter and my heart happier.
                I choose you — today and always ❤️
            </p>
        </div>

        <div class="gift">
            🧇
            <h3>Waffles Treat</h3>
            <p>
                A cozy waffles date with extra chocolate and love 😋
            </p>
        </div>

        <div class="gift">
            📸
            <h3>Our Photos</h3>
            <img src="photos/photo1.jpg" width="180"><br><br>
            <img src="photos/photo2.jpg" width="180">
        </div>

    </div>
</div>

</body>
</html>
