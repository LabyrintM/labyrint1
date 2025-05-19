<!DOCTYPE html>
<html lang="sv">
<head>
<meta charset="UTF-8" />
<title>Labyrinten</title>
<style>
body {
font-family: Georgia, serif;
max-width: 700px;
margin: auto;
padding: 2em;
line-height: 1.6;
}
img {
max-width: 100%;
}
#intro, #gåta, #instruktioner, #minmicke {
display: none;
}
</style>
</head>
<body>

<!-- Startsida med hjärtbild -->
<div id="start">
<img src="https://i.ibb.co/QJvxx9Z/heart-start.jpg" alt="You’re not too old to start over" />
<p>Skriv kodordet för att öppna nästa steg.</p>
<input type="text" id="kodord" placeholder="Kodord" />
<button onclick="checkKodord()">Öppna</button>
</div>

<!-- Intro + karta + gåta -->
<div id="intro">
<h2>Välkommen, Micke.</h2>
<p>Johanna har byggt något åt dig.<br>
Det är inte ett brev. Inte ett meddelande.<br>
Det är en labyrint.</p>

<p>Ett inre landskap – fullt av era ögonblick, hennes ord, och spår av allt hon burit men inte alltid kunnat säga högt.<br>
Och du är den enda som har nyckeln in.</p>

<p>Du har nu låst upp den första delen.<br>
Du är inne i det första rummet.</p>

<p>Det finns fler –<br>
var och en bär på något hon lämnat till dig:<br>
sanningar, minnen, insikter, riktningar.<br>
Allt det hon bar på, allt det hon önskar att du en dag ska förstå –<br>
men utan krav, utan tidspress.</p>

<p>Det här är hennes sätt att finnas kvar, om du vill hitta henne.<br>
Det är som en skattkarta.</p>

<img src="https://i.ibb.co/5FwRLD6/karta-rum.jpg" alt="Skattkarta" />

<p><strong>Vad skrev du i ett sällskapsspel som Johanna tyckte var så kul att hon sprutade läsk genom näsan?</strong></p>
<input type="text" id="gåtaSvar" placeholder="Skriv svaret..." />
<button onclick="checkGåta()">Skicka</button>
</div>

<!-- Instruktioner -->
<div id="instruktioner">
<p>Det är rätt.<br>
Du har nu låst upp instruktionerna.<br>
Det här är portalen till resten av labyrinten.</p>

<p>Den består av elva rum. Varje rum har ett namn, en ton, ett syfte – och något hon lämnat till dig.<br>
Det är minnen, sanningar, fragment, riktningar.<br>
Allt det du kanske inte kunnat ta in – men som nu finns här, tillgängligt, i din takt.</p>

<p><strong>Här är rummen:</strong></p>
<ol>
<li>Historia</li>
<li>Pippi</li>
<li>Min kompis</li>
<li>Orimligheten</li>
<li>Viggo/Alva</li>
<li>Kärleken</li>
<li>Musikens tidslinje</li>
<li>Min Micke</li>
<li>Framtiden</li>
<li>Möjligheternas rum</li>
<li>Spegling</li>
</ol>

<p>För att låsa upp ett rum behöver du en nyckel.<br>
Du får nyckeln genom att lösa en <strong>gåta</strong>.<br>
När du t.ex. skriver: <strong>Min Micke</strong> – får du en ny gåta.</p>

<input type="text" id="rumsnamn" placeholder="Skriv rumsnamn..." />
<button onclick="visaRum()">Sök rum</button>
</div>

<!-- Min Micke-rummet -->
<div id="minmicke">
<iframe width="100%" height="315" src="https://www.youtube.com/embed/0G383538qzQ" title="YouTube video player" frameborder="0" allowfullscreen></iframe>

<img src="https://i.ibb.co/pRWd6NF/micke-datorn.jpg" alt="Micke flexar vid datorn" />

<p><em>Önskar det fanns tillräckliga ord att beskriva hur fantastisk jag tycker du är.</em></p>
<p>Hur förtjust jag är i alla dina små personligheter som gömmer sig i den manligaste av kroppar.</p>
<p>Att du alltid kommer vara allt annat än fasaden du visar.<br>
Tanten som älskar mint, pojken som garvar åt pruttskämt och framförallt killen som tog revansch på sig själv och ändrade både det yttre som det inre.</p>
<p>Tänk att i det korrekta, det samlade och ordnade så såg jag något helt annat.</p>
</div>

<script>
function checkKodord() {
const kod = document.getElementById('kodord').value.trim().toLowerCase();
if (kod === "mario") {
document.getElementById('start').style.display = "none";
document.getElementById('intro').style.display = "block";
}
}

function checkGåta() {
const svar = document.getElementById('gåtaSvar').value.trim().toLowerCase();
if (svar === "gul bil") {
document.getElementById('intro').style.display = "none";
document.getElementById('instruktioner').style.display = "block";
}
}

function visaRum() {
const rum = document.getElementById('rumsnamn').value.trim().toLowerCase();
if (rum === "min micke") {
document.getElementById('instruktioner').style.display = "none";
document.getElementById('minmicke').style.display = "block";
}
}
</script>

</body>
</html>
Avsnitt för bifogade filer
Förhandsgranska YouTube-videoklipp Black Pumas - Colors (Official Live Session)

