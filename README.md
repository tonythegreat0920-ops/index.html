# index.html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Cosmic Button</title>

<style>
body {
    margin: 0;
    height: 100vh;
    background: radial-gradient(circle at center, #0f0f1f, #000);
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    font-family: monospace;
    color: #00ffcc;
    overflow: hidden;
}

h1 {
    font-size: 3rem;
    letter-spacing: 3px;
}

button {
    padding: 15px 30px;
    font-size: 1.2rem;
    background: #00ffcc;
    border: none;
    cursor: pointer;
    margin-top: 20px;
    transition: 0.3s;
}

button:hover {
    background: #00ccaa;
    transform: scale(1.1);
}

#message {
    margin-top: 30px;
    font-size: 1.3rem;
}
</style>
</head>

<body>

<h1>☄ COSMIC BUTTON</h1>
<button onclick="explode()">Press Me</button>
<div id="message">Awaiting interaction...</div>

<script>
function explode() {
    const messages = [
        "You just bent space-time.",
        "Reality.exe has stopped responding.",
        "The void noticed you.",
        "A parallel universe just spawned.",
        "You unlocked Developer Mode.",
        "Gravity has resigned."
    ];

    const randomMessage = messages[Math.floor(Math.random() * messages.length)];
    document.getElementById("message").textContent = randomMessage;

    // random background color shift
    document.body.style.background =
        `radial-gradient(circle at center, 
        hsl(${Math.random() * 360}, 80%, 20%), 
        #000)`;
}
</script>

</body>
</html>
