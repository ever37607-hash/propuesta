<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>💍 Sorpresa 💍</title>
<style>
    body {
        margin: 0;
        overflow: hidden;
        background: black;
        color: white;
        font-family: Arial, sans-serif;
    }
    .frase {
        position: absolute;
        white-space: nowrap;
        font-size: 24px;
        animation: caer linear;
    }
    @keyframes caer {
        0% { transform: translateY(-50px); opacity: 1; }
        100% { transform: translateY(110vh); opacity: 0; }
    }
</style>
</head>
<body>

<script>
const frase = "¿Quieres casarte conmigo?";
function crearFrase() {
    const elem = document.createElement("div");
    elem.className = "frase";
    elem.textContent = frase;

    elem.style.left = Math.random() * 100 + "vw";
    elem.style.fontSize = (20 + Math.random() * 10) + "px";
    elem.style.animationDuration = (3 + Math.random() * 3) + "s";

    document.body.appendChild(elem);

    setTimeout(() => {
        elem.remove();
    }, 6000);
}

setInterval(crearFrase, 300);
</script>

</body>
</html>
