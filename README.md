<!DOCTYPE html>
<html lang="sv">
<head>
<meta charset="UTF-8">
<title>Labyrinten</title>
<style>
body {
font-family: Arial, sans-serif;
background-color: #fff;
margin: 0;
padding: 2rem;
text-align: center;
}
.hidden {
display: none;
}
input[type="text"] {
padding: 0.5rem;
font-size: 1rem;
margin-top: 1rem;
}
button {
padding: 0.5rem 1rem;
font-size: 1rem;
margin-top: 1rem;
cursor: pointer;
}
img {
max-width: 90%;
margin-top: 1rem;
}
audio {
margin-top: 1rem;
}
</style>
</head>
<body>

<!-- Steg 1: Hjärtbild + kodord -->
<div id="step1">
<img src="https://i.imgur.com/6W9XaKP.jpeg" alt="Heart">
<p>Skriv kodordet:</p>
<input type="text" id="kodord">
<button onclick="checkKodord()">Fortsätt</button>
</div>

<!-- Steg 2: Intro + karta + gåta -->
<div id="step2" class="hidden">
<h2>Välkommen, Micke.</h2>
<p>Johanna har byggt något. Det är inte ett brev. Inte ett sista ord. Inte ett försök att ändra något.
Det är något annat. Ett rum för dig.
Ett försök att samla det som funnits, det som fortfarande känns, det som ingen annan någonsin kommer förstå.
Något att gå vilse i – om du vill.</p>
<p>Det är en labyrint.
Den bygger inte på logik, den är byggd på känsla.
Du kan när som helst lämna den. Du kan också gå djupare.
Det finns inget rätt eller fel, bara rum som väntar.</p>
<img src="https://i.imgur.com/LqijQdh.jpeg" alt="Karta">
<p>Vad skrev du i ett sällskapsspel när du tänkte på mig?</p>
<input type="text" id="gåta1">
<button onclick="checkGåta()">Svara</button>
</div>

<!-- Steg 3: Instruktioner -->
<div id="step3" class="hidden">
<h2>Det är rätt.</h2>
<p>Du har nu låst upp instruktionerna.</p>
<p>I det här rummet finns elva portar. Bakom varje port finns något Johanna valt ut för dig.
Varje port är märkt med ett ord – ett rum.
Du kan välja vilket rum du vill, i vilken ordning du vill.
Ibland kommer du få en fråga innan porten öppnas.
Om du svarar rätt, öppnas rummet.
Om du svarar fel… händer ingenting.
Det är ingen tävling.
Du får alltid försöka igen.</p>
<p>Du kan när som helst lämna labyrinten. Men den kommer alltid finnas kvar.</p>
<p>Skriv ett rumsnamn – så ger jag dig en gåta.</p>
<input type="text" id="rumInput">
<button onclick="valjRum()">Fortsätt</button>
</div>

<!-- Steg 4: Rum Min Micke -->
<div id="minMicke" class="hidden">
<p>Gåta: Vilken grej som Johanna serverat tyckte du va godast?</p>
<input type="text" id="svarMicke">
<button onclick="checkMinMicke()">Svara</button>
</div>

<!-- Steg 5: Innehåll Min Micke -->
<div id="mickeInnehåll" class="hidden">
<audio controls autoplay>
<source src="https://open.spotify.com/embed/track/1zi7xx7UVEFkmKfv06H8x0?utm_source=generator" type="audio/mpeg">
Din webbläsare stöder inte ljuduppspelning.
</audio>
<img src="https://i.imgur.com/Nfrw9ms.jpeg" alt="Micke">
<p>Önskar det fanns tillräckliga ord att beskriva hur fantastisk jag tycker du är.</p>
<p>Hur förtjust jag är i alla dina små personligheter som gömmer sig i den manligaste av kroppar.</p>
<p>Att du alltid kommer vara allt annat än fasaden du visar.
Tanten som älskar mint, pojken som garvar åt pruttskämt och framförallt killen som tog revansch på sig själv och ändrade både det yttre som det inre.</p>
<p>Tänk att i det korrekta, det samlade och ordnade så såg jag något helt annat.</p>
<p><em>Fortsättning följer…</em></p>
</div>

<script>
function checkKodord() {
const kod = document.getElementById('kodord').value.toLowerCase();
if (kod === 'mario') {
document.getElementById('step1').classList.add('hidden');
document.getElementById('step2').classList.remove('hidden');
}
}

function checkGåta() {
const svar = document.getElementById('gåta1').value.toLowerCase();
if (svar.includes('gul bil')) {
document.getElementById('step2').classList.add('hidden');
document.getElementById('step3').classList.remove('hidden');
}
}

function valjRum() {
const rum = document.getElementById('rumInput').value.toLowerCase();
if (rum === 'min micke') {
document.getElementById('step3').classList.add('hidden');
document.getElementById('minMicke').classList.remove('hidden');
}
}

function checkMinMicke() {
const svar = document.getElementById('svarMicke').value.toLowerCase();
if (svar.includes('fattiga riddare')) {
document.getElementById('minMicke').classList.add('hidden');
document.getElementById('mickeInnehåll').classList.remove('hidden');
}
}
</script>

</body>
</html>
