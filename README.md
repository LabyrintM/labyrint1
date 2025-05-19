<!DOCTYPE html>
<html lang="sv">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Labyrinten</title>
<style>
body {
font-family: Arial, sans-serif;
margin: 20px;
background-color: #fff;
color: #333;
}
#codeInput {
width: 250px;
padding: 10px;
font-size: 16px;
}
button {
padding: 10px 15px;
font-size: 16px;
margin-left: 10px;
cursor: pointer;
}
#responseText {
margin-top: 20px;
font-weight: bold;
}
#introImage, #mapImage {
max-width: 100%;
margin-top: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0,0,0,0.1);
}
#instructions {
margin-top: 20px;
white-space: pre-wrap;
background-color: #f9f9f9;
padding: 15px;
border-radius: 6px;
border: 1px solid #ddd;
}
</style>
</head>
<body>
<h1>Välkommen, Micke.</h1>
<p>Det här är inte ett brev. Det är något jag har byggt.</p>
<p>En labyrint. En skattkarta. Ett fält för det du minns.</p>
<p>Du börjar här. Skriv in kodordet.</p>

<form onsubmit="checkCode(event)">
<input type="text" id="codeInput" placeholder="Skriv kodordet här" autocomplete="off" />
<button type="submit">Öppna</button>
</form>

<p id="responseText"></p>

<img id="introImage" src="https://i.imgur.com/oV6Zm4P.jpeg" alt="Introbild med hjärta" style="display:none" />
<img id="mapImage" src="https://i.imgur.com/zpFG3fB.jpg" alt="Skattkarta Labyrinten" style="display:none" />

<div id="instructions" style="display:none"></div>

<script>
const correctCode = "Mario";
const mapImage = document.getElementById("mapImage");
const introImage = document.getElementById("introImage");
const responseText = document.getElementById("responseText");
const instructions = document.getElementById("instructions");

const instructionText = `Det är rätt. Du har nu låst upp instruktionerna för Labyrinten.

Kartan ovan visar alla rum. Skriv ett rumsnamn – så ger jag dig en gåta.`;

function checkCode(event) {
event.preventDefault();
const userInput = document.getElementById("codeInput").value.trim();

if(userInput.toLowerCase() === correctCode.toLowerCase()) {
responseText.textContent = "Rätt! Välkommen in.";
introImage.style.display = "block";
mapImage.style.display = "block";
instructions.style.display = "block";
instructions.textContent = instructionText;
} else {
responseText.textContent = "Fel kodord, försök igen.";
introImage.style.display = "none";
mapImage.style.display = "none";
instructions.style.display = "none";
}
}
</script>
</body>
</html>
