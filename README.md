# Invitaci-n-de-San-Valent-n-
Invitación 
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>San Valentín 💘</title>
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
        text-align: center;
    }

    h1 {
        color: white;
        font-size: 2em;
    }

    .buttons {
        margin-top: 20px;
        position: relative;
    }

    button {
        padding: 15px 30px;
        font-size: 18px;
        border: none;
        border-radius: 10px;
        cursor: pointer;
        margin: 10px;
        transition: 0.3s;
    }

    #yesBtn {
        background-color: #ff4d6d;
        color: white;
    }

    #noBtn {
        background-color: white;
        color: #ff4d6d;
        position: absolute;
    }

    #invitation {
        display: none;
        margin-top: 30px;
        font-size: 22px;
        color: white;
        background-color: rgba(0,0,0,0.3);
        padding: 20px;
        border-radius: 15px;
    }
</style>
</head>
<body>

<h1>¿Quieres ser mi cita de San Valentín? 💖</h1>

<div class="buttons">
    <button id="yesBtn">Sí 💘</button>
    <button id="noBtn">No 😢</button>
</div>

<div id="invitation">
    💌 ¡Perfecto!  
    <br><br>
    Te invito a una cita el  
    <br>
    ❤️ 14 de febrero a las 17:00 horas ❤️
</div>

<script>
    const yesBtn = document.getElementById("yesBtn");
    const noBtn = document.getElementById("noBtn");
    const invitation = document.getElementById("invitation");

    let size = 1;

    noBtn.addEventListener("mouseover", function() {
        size += 0.2;
        yesBtn.style.transform = `scale(${size})`;

        // Mover botón NO a posición aleatoria
        const x = Math.random() * (window.innerWidth - 100);
        const y = Math.random() * (window.innerHeight - 100);
        noBtn.style.left = x + "px";
        noBtn.style.top = y + "px";
    });

    yesBtn.addEventListener("click", function() {
        document.querySelector(".buttons").style.display = "none";
        invitation.style.display = "block";
    });
</script>

</body>
</html>
