<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contador Regressivo</title>
    <script>
        // Defina a data alvo para o contador (exemplo: 31 de dezembro de 2024)
        const targetDate = new Date("Dec 31, 2024 23:59:59").getTime();
function updateCountdown() {
            const now = new Date().getTime();
const distance = targetDate - now;
const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);
document.getElementById("countdown").innerHTML = `${days}d ${hours}h ${minutes}m ${seconds}s`;

   if (distance < 0)              clearInterval(updateInterval) document.getElementById("countdown").innerHTML = "EXPIRADO";
            }
const updateInterval = setInterval(updateCountdown, 1000);
    </script>
</head>
<body>
    <h1>Contador Regressivo</h1>
    <p id="countdown"></p>
</body>
</html>
