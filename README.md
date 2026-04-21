# Foryouu
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Love Letter</title>

<style>
    body {
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        background: linear-gradient(135deg, #ff758c, #ff7eb3);
        font-family: Arial, sans-serif;
    }

    .envelope {
        width: 300px;
        height: 200px;
        background: #ff4d6d;
        position: relative;
        cursor: pointer;
        border-radius: 10px;
        transition: 0.5s;
    }

    .flap {
        position: absolute;
        width: 100%;
        height: 100%;
        background: #ff3355;
        clip-path: polygon(0 0, 100% 0, 50% 60%);
        transition: 0.5s;
        transform-origin: top;
    }

    .letter {
        position: absolute;
        width: 90%;
        height: 90%;
        background: white;
        top: 5%;
        left: 5%;
        border-radius: 10px;
        padding: 20px;
        text-align: center;
        transform: translateY(100%);
        transition: 0.5s;
    }

    .letter h2 {
        color: #ff4d6d;
    }

    .open .flap {
        transform: rotateX(180deg);
    }

    .open .letter {
        transform: translateY(0);
    }
</style>

</head>
<body>

<div class="envelope" onclick="openLetter(this)">
    <div class="flap"></div>
    <div class="letter">
        <h2>💖 My Love</h2>
        <p>
            I just want to tell you...<br><br>
            You mean everything to me ❤️<br>
            No matter what happens,<br>
            I will always choose you.
        </p>
    </div>
</div>

<script>
function openLetter(el) {
    el.classList.toggle("open");
}
</script>

</body>
</html>
