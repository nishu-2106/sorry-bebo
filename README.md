# sorry-bebo
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>I'm Sorry Diptuuu 💖</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <style>
        body {
            margin: 0;
            height: 100vh;
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(to bottom right, #ffafbd, #ffc3a0);
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            overflow: hidden;
        }

        .card {
            background: rgba(255, 255, 255, 0.95);
            padding: 30px;
            border-radius: 25px;
            width: 90%;
            max-width: 420px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
            animation: pop 1s ease;
        }

        h1 {
            color: #ff4d6d;
            margin-bottom: 10px;
        }

        #typing {
            font-size: 17px;
            color: #444;
            min-height: 130px;
        }

        .btn {
            margin-top: 20px;
            padding: 12px 25px;
            background: #ff4d6d;
            color: white;
            border: none;
            border-radius: 30px;
            font-size: 16px;
            cursor: pointer;
            transition: 0.3s;
        }

        .btn:hover {
            background: #e63956;
        }

        .heart {
            position: absolute;
            color: #ff4d6d;
            font-size: 18px;
            animation: float 6s linear infinite;
        }

        @keyframes float {
            0% { transform: translateY(100vh); opacity: 1; }
            100% { transform: translateY(-10vh); opacity: 0; }
        }

        @keyframes pop {
            from { transform: scale(0.7); opacity: 0; }
            to { transform: scale(1); opacity: 1; }
        }
    </style>
</head>
<body>

    <!-- Romantic Music -->
    <audio autoplay loop>
        <source src="https://files.catbox.moe/0tq8w1.mp3" type="audio/mp3">
    </audio>

    <div class="card">
        <h1>I'm Sorry Diptuuu 🥺💗</h1>
        <p id="typing"></p>

        <button class="btn" onclick="alert('Thank you for forgiving me 💕 You mean the world to me, Diptuuu 🥰')">
            Forgive me? 🥺
        </button>
    </div>

    <script>
        const text = "I know I hurt you, and I'm really really sorry 🥺💔\n\nYou are too precious to lose, Diptuuu 💖\nEvery smile of yours matters to me.\n\nPlease forgive me and hold my hand again 🤍";
        let i = 0;
        const speed = 45;

        function typeEffect() {
            if (i < text.length) {
                document.getElementById("typing").innerHTML += text.charAt(i) === "\n" ? "<br>" : text.charAt(i);
                i++;
                setTimeout(typeEffect, speed);
            }
        }
        typeEffect();

        function createHeart() {
            const heart = document.createElement("div");
            heart.className = "heart";
            heart.innerHTML = "❤";
            heart.style.left = Math.random() * 100 + "vw";
            heart.style.animationDuration = Math.random() * 3 + 4 + "s";
            document.body.appendChild(heart);

            setTimeout(() => heart.remove(), 6000);
        }

        setInterval(createHeart, 300);
    </script>

</body>
</html>
