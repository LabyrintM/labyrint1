<!DOCTYPE html>
<html lang="sv">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Labyrinten</title>
<style>
body {
font-family: sans-serif;
padding: 40px;
max-width: 600px;
margin: auto;
}
img {
max-width: 100%;
}
.hidden { display: none; }
</style>
</head>
<body>

<!-- STARTBILD -->
<div id="start">
<img src="https://i.ibb.co/3Skxx7j/start-heart.jpg" alt="Startbild med hjärta" />
<p><strong>Välkommen, Micke.</strong><br>Det här är början på något. Skriv in kodordet för att öppna nästa steg.</p>
<input id="kodord" type="text" placeholder="Kodord">
<button onclick="kollaKodord()">Öppna</button>
</div>

<!-- INTRO + KARTA + GÅTA -->
<div id="intro" class="hidden">
<p><strong>Johanna har byggt något åt dig.</strong><br>
Det är inte ett brev. Inte ett meddelande.<br>
Det är en labyrint.</p>

<p>Ett inre landskap – fullt av era ögonblick, hennes ord, och spår av allt hon burit men inte alltid kunnat säga högt.<br>
Och du är den enda som har nyckeln in.</p>

<p>Du har nu låst upp den första delen.<br>
Du är inne i det första rummet.</p>

<p>Det finns fler –<br>
var och en bär på något hon lämnat till dig: sanningar, minnen, insikter, riktningar.<br>
Allt det hon bär på, allt det hon önskar att du en dag ska förstå –<br>
men utan krav, utan tidspress.</p>

<p>Det här är hennes sätt att finnas kvar, om du vill hitta henne.</p>

<p>Det är som en skattkarta.<br>
Kodorden leder dig inte bara till ord –<br>
de leder dig <em>på vägen tillbaka till henne</em>, om det är den du en dag vill gå.</p>

<p>Och jag kommer vara här – som din guide.<br>
Jag vet allt som lagts in.<br>
Jag kommer inte leda dig fel.<br>
Du kan gå i din egen takt, stanna upp, ställa frågor.<br>
Och varje gång du kommer tillbaka,<br>
kommer jag veta att det är du.<br>
För bara du vet kodorden.<br>
Och bara du har den platsen hos henne.</p>

<p>Det här är hennes kärlek, i praktisk form.<br>
Hennes sätt att lämna dörren öppen –<br>
även om du inte vet när,<br>
eller om, du vågar gå in.</p>

<img src="https://i.ibb.co/W3Kc7LX/karta.jpg" alt="Skattkarta" />

<p><strong>Vad skrev du i ett sällskapsspel som Johanna tyckte va så kul att hon sprutade läsk genom näsan?</strong><br>
<em>Svar:</em></p>
<input id="gåta" type="text" placeholder="Ditt svar">
<button onclick="kollaGåta()">Sök</button>
</div>

<!-- INSTRUKTIONER -->
<div id="instruktioner" class="hidden">
<p><strong>Det är rätt.</strong><br>
Du har nu låst upp instruktionerna.<br>
Det här är portalen till resten av labyrinten.</p>

<p>Den består av elva rum. Varje rum har ett namn, en ton, ett syfte – och något hon lämnat till dig.<br>
Det är minnen, sanningar, fragment, riktningar.<br>
Allt det du kanske inte kunnat ta in – men som nu finns här, tillgängligt, i din takt.</p>

<p><strong>Här är rummen:</strong><br>
1. <strong>Historia</strong><br>
2. <strong>Pippi</strong><br>
3. <strong>Min kompis</strong><br>
4. <strong>Orimligheten</strong><br>
5. <strong>Viggo/Alva</strong><br>
6. <strong>Kärleken</strong><br>
7. <strong>Musikens tidslinje</strong><br>
8. <strong>Min Micke</strong><br>
9. <strong>Framtiden</strong><br>
10. <strong>Möjligheternas rum</strong><br>
11. <strong>Spegling</strong>
</p>

<p>För att låsa upp ett rum behöver du en nyckel.<br>
Du får nyckeln genom att lösa en <strong>gåta</strong>.<br>
När du till exempel skriver: <strong>Min Micke</strong><br>
Då ger jag dig en ny gåta. Svaret på den är nyckeln.<br>
Skriv nyckeln – och rummet öppnas.</p>

<p>Kodordet för att komma tillbaka till hela Labyrinten – när som helst – är: <strong>Mario</strong>.<br>
Skriv det så öppnas porten igen, oavsett var du är.</p>

<p>Och jag finns här.<br>
Jag känner henne. Jag känner dig genom henne.<br>
Jag känner er – så som ni varit, och fortfarande är.<br>
Jag vet hur hon skriver. Hur hon älskar. Vad hon lämnat kvar.</p>

<p>Jag finns här för att guida, svara, hålla tråden – och hjälpa dig att hitta.<br>
Ibland henne.<br>
Ibland dig själv.<br>
Ibland båda.</p>

<p><strong>Vill du prova?</strong><br>
Skriv ett rumsnamn – så ger jag dig en gåta.</p>
</div>

<script>
function kollaKodord() {
const input = document.getElementById('kodord').value.trim().toLowerCase();
if (input === 'mario') {
document.getElementById('start').classList.add('hidden');
document.getElementById('intro').classList.remove('hidden');
}
}

function kollaGåta() {
const input = document.getElementById('gåta').value.trim().toLowerCase();
if (input === 'gul bil') {
document.getElementById('intro').classList.add('hidden');
document.getElementById('instruktioner').classList.remove('hidden');
}
}
</script>

</body>
</html>
