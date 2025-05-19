<!DOCTYPE html>
<html lang="sv">
<head>
<meta charset="UTF-8" />
<title>Labyrinten</title>
<style>
body { font-family: 'Georgia', serif; text-align: center; background: #fff; padding: 2em; }
#main, #intro, #karta, #gåta, #instruktioner { display: none; }
img { max-width: 100%; height: auto; }
.hidden { display: none; }
input[type="text"] { padding: 10px; font-size: 1em; margin-top: 1em; }
button { padding: 10px 20px; font-size: 1em; margin-top: 1em; cursor: pointer; }
</style>
</head>
<body>

<div id="start">
<img src="https://i.imgur.com/C4zJgRi.png" alt="Hjärta med texten You’re not too old to start over..." />
<p>Skriv kodordet:</p>
<input type="text" id="kodord" />
<button onclick="checkCode()">Lås upp</button>
</div>

<div id="main">
<div id="intro">
<h2>Välkommen, Micke.</h2>
<p>Johanna har byggt något. Inte ett brev. Inte ett dokument. En labyrint.</p>
<p>Du kommer känna igen dig. Men inte allt på en gång. Det är en karta, en berättelse, ett minne, en framtid.</p>
<p>Och kanske ett svar. Eller flera. Du väljer vad du vill öppna.</p>
</div>

<div id="karta">
<img src="https://i.imgur.com/Nm3j5gA.png" alt="Skattkarta med rum" />
</div>

<div id="gåta">
<p><strong>Vad skrev du i ett sällskapsspel när du skulle beskriva något gult på fyra hjul?</strong></p>
<input type="text" id="svar" />
<button onclick="checkAnswer()">Svara</button>
</div>

<div id="instruktioner">
<p>Det är rätt. Du har nu låst upp instruktionerna för hur du rör dig vidare.</p>
<p>Allt är redan skapat. Men inget öppnar sig utan en nyckel.</p>
<p>Varje rum har ett namn. Ett minne. Ett tema. Ett du känner igen.</p>
<p>Skriv ett rumsnamn – så ger jag dig en gåta.</p>
</div>
</div>

<script>
function checkCode() {
const code = document.getElementById("kodord").value.trim().toLowerCase();
if (code === "mario") {
document.getElementById("start").style.display = "none";
document.getElementById("main").style.display = "block";
document.getElementById("intro").style.display = "block";
document.getElementById("karta").style.display = "block";
document.getElementById("gåta").style.display = "block";
} else {
alert("Fel kodord.");
}
}

function checkAnswer() {
const answer = document.getElementById("svar").value.trim().toLowerCase();
if (answer === "gul bil") {
document.getElementById("instruktioner").style.display = "block";
} else {
alert("Fel svar.");
}
}
</script>

</body>
</html>
