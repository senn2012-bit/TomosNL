<!DOCTYPE html>
<html lang="nl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Symptomen Community</title>

<style>
body {
    margin: 0;
    font-family: "Segoe UI", Arial, sans-serif;
    background: #f6fbff;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
}

.container {
    background: white;
    padding: 30px;
    border-radius: 14px;
    max-width: 420px;
    width: 90%;
    box-shadow: 0 8px 22px rgba(0,0,0,0.1);
    text-align: center;
}

/* Titel met rustige blauwe tinten */
.title {
    font-size: 34px;
    font-weight: 600;
    letter-spacing: 1px;
}

.light { color: #9ccff2; }
.medium { color: #5faee3; }
.dark { color: #2f7fc1; }

.subtitle {
    margin: 16px 0 24px;
    color: #555;
}

/* Knoppen */
.button {
    display: block;
    margin: 12px 0;
    padding: 14px;
    border-radius: 30px;
    text-decoration: none;
    font-size: 16px;
    font-weight: 600;
    border: none;
    cursor: pointer;
}

.whatsapp {
    background: #25D366;
    color: white;
}

.send {
    background: linear-gradient(135deg, #9ccff2, #5faee3);
    color: white;
}

.button:hover {
    opacity: 0.9;
}

/* Tekstvak */
textarea {
    width: 100%;
    height: 90px;
    border-radius: 10px;
    border: 1px solid #ccc;
    padding: 10px;
    font-size: 14px;
    resize: none;
}
</style>
</head>

<body>

<div class="container">

    <!-- Titel met subtiele kleurwissel -->
    <div class="title">
        <span class="light">S</span>
        <span class="medium">y</span>
        <span class="light">m</span>
        <span class="dark">p</span>
        <span class="medium">t</span>
        <span class="light">o</span>
        <span class="dark">m</span>
        <span class="medium">e</span>
        <span class="light">n</span>
    </div>

    <div class="subtitle">
        Deel je symptomen of ervaringen met de groep
    </div>

    <a class="button whatsapp"
       href="https://chat.whatsapp.com/L0R51a9qGS42AqWWppoXOu"
       target="_blank">
        Join WhatsApp-groep
    </a>

    <form onsubmit="sendToGroup(); return false;">
        <textarea id="symptoms"
        placeholder="Typ hier jouw symptomen of ervaring..."></textarea>

        <button class="button send" type="submit">
            Symptomen insturen
        </button>
    </form>

</div>

<script>
function sendToGroup() {
    const text = document.getElementById("symptoms").value.trim();

    if (!text) {
        alert("Vul eerst iets in 🙂");
        return;
    }

    const message = encodeURIComponent("Symptomen / ervaring:\n\n" + text);

    window.open(
        "https://chat.whatsapp.com/L0R51a9qGS42AqWWppoXOu?text=" + message,
        "_blank"
    );
}
</script>

</body>
</html>

