<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Will You Be My Valentine? 💘</title>

<style>
    body {
        margin: 0;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        background: linear-gradient(135deg, #ff9a9e, #fad0c4);
        font-family: Arial, sans-serif;
        overflow: hidden;
        text-align: center;
    }

    h1 {
        font-size: 2.5rem;
        color: white;
        margin-bottom: 30px;
    }

    .buttons {
        position: relative;
    }

    button {
        padding: 15px 30px;
        font-size: 18px;
        border: none;
        border-radius: 30px;
        cursor: pointer;
        transition: 0.3s;
        margin: 10px;
    }

    #yesBtn {
        background-color: #ff4d6d;
        color: white;
    }

    #yesBtn:hover {
        background-color: #ff1e4d;
        transform: scale(1.1);
    }

    #noBtn {
        background-color: white;
        color: #ff4d6d;
        position: absolute;
    }

    .message {
        display: none;
        font-size: 2rem;
        color: white;
        margin-top: 20px;
        animation: pop 0.5s ease forwards;
    }

    @keyframes pop {
        from { transform: scale(0); }
        to { transform: scale(1); }
    }

    .sticker {
        font-size: 80px;
        margin-top: 10px;
    }
</style>
</head>

<body>

<h1>Will you be my Valentine? 💖</h1>

<div class="buttons">
    <button id="yesBtn">Yes 💕</button>
    <button id="noBtn">No 😢</button>
</div>

<div class="message" id="loveMessage">
    Of course I am! I'm very cute 🥰  
    <div class="sticker">💖🐻💘</div>
</div>

<script>
    const noBtn = document.getElementById("noBtn");
    const yesBtn = document.getElementById("yesBtn");
    const message = document.getElementById("loveMessage");

    // Make NO button run away
    noBtn.addEventListener("mouseover", function() {
        const x = Math.random() * (window.innerWidth - 100);
        const y = Math.random() * (window.innerHeight - 100);
        noBtn.style.left = x + "px";
        noBtn.style.top = y + "px";
    });

    // When YES is clicked
    yesBtn.addEventListener("click", function() {
        message.style.display = "block";
        yesBtn.style.display = "none";
        noBtn.style.display = "none";
    });
</script>

</body>
</html>
