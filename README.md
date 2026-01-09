# mi_eva-index.html
David
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Buenos días mi eva</title>

<style>
body {
    margin: 0;
    background: linear-gradient(180deg, #1a001f, #2b0033);
    font-family: Arial, sans-serif;
    color: #f6b6d2;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    overflow: hidden;
}

.card {
    background: rgba(255,255,255,0.06);
    border-radius: 22px;
    padding: 25px;
    max-width: 350px;
    text-align: center;
    box-shadow: 0 0 25px rgba(255,182,210,.25);
    z-index: 2;
}

h1 { font-size: 2.2em; }

p {
    font-size: 1.1em;
    line-height: 1.6;
}

.snoopy {
    width: 140px;
    margin: 15px auto;
    animation: float 3s ease-in-out infinite;
}

@keyframes float {
    0% { transform: translateY(0); }
    50% { transform: translateY(-12px); }
    100% { transform: translateY(0); }
}

/* BOTON PLAY */
.play-btn {
    margin-top: 15px;
    background: #f6b6d2;
    border: none;
    color: #2b0033;
    font-size: 1.1em;
    padding: 12px 22px;
    border-radius: 30px;
    cursor: pointer;
    box-shadow: 0 0 15px rgba(246,182,210,.6);
    transition: transform .2s;
}
.play-btn:hover {
    transform: scale(1.05);
}

/* corazones */
.heart {
    position: absolute;
    bottom: -20px;
    font-size: 20px;
    animation: rise 6s linear infinite;
}
@keyframes rise {
    from { transform: translateY(0); opacity: 0; }
    to { transform: translateY(-110vh); opacity: 1; }
}
</style>
</head>

<body>

<div class="heart" style="left:10%">💖</div>
<div class="heart" style="left:30%; animation-delay:1s">💗</div>
<div class="heart" style="left:50%; animation-delay:2s">💞</div>
<div class="heart" style="left:70%; animation-delay:3s">💕</div>
<div class="heart" style="left:90%; animation-delay:4s">💘</div>

<div class="card">
    <h1>Buenos días,<br>mi eva</h1>

    <img class="snoopy"
         src="https://media.giphy.com/media/3oriO0OEd9QIDdllqo/giphy.gif"
         alt="Snoopy">

    <p>
        Que este día esté lleno de la misma dulzura que tú llevas en el alma.
        Eres mi razón para sonreír cada mañana.
    </p>

    <!-- BOTON -->
    <button class="play-btn" onclick="playMusic()">▶ Reproducir Those Eyes</button>

    <!-- YOUTUBE OCULTO -->
    <iframe id="music"
        width="0" height="0"
        src=""
        frameborder="0"
        allow="autoplay; encrypted-media">
    </iframe>
</div>

<script>
function playMusic() {
    document.getElementById("music").src =
    "https://www.youtube.com/embed/3zZ6kFzWiS8?autoplay=1";
}
</script>

</body>
</html>
