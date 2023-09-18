# Tito.github
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>My pagina de prueba</title>
  <link rel="stylesheet" type="text/css" href="joya.css">
</head>
<body>
  <h1>El logo de firefox</h1>
  <img src="imagenes/firefox-icon.jpg" alt="un gran zorro de fuego que rodea la Tierra ">
  <p>mi sitio web seria para explicarles sobre algo a las personas o hacer un blog de un tema en especifico.</p>
  <p>El tema puede ser dependiendo sobre lo que quiera escribir.</p>
  <p>El bloque que haria tendria un orden masomenos asi:</p>
  <ul>
    <li>introducion al tema</li>
    <li>Los subtemas</li>
    <li>Una resumen de todo lo que escribi arriba</li>
  </ul>
  <a href="https://www.google.com/url?sa=i&url=https%3A%2F%2Fen.wikipedia.org%2Fwiki%2FFirefox&psig=AOvVaw1wT9MBjPn8YcjNfgjQ_QGd&ust=1695075214332000&source=images&cd=vfe&opi=89978449&ved=0CBAQjRxqFwoTCKjKh7LVsoEDFQAAAAAdAAAAABAE">descripcion de motzilla</a>
  <button>cambiar de usuario</button>
  <script src="scripts/main.js"></script>
</body>
</html>
// CSS:
body{
  width: 600px;
  margin: 0 auto;
  background-color: #ff9500;
  padding: 0 20px 20px 20px;
  border: 5px solid black;
  text-align: center;
}

h1 {
  margin: 0;
  padding: 20px 0;
  color: #00539f;
  text-shadow: 3px 3px 2px black;

}

p,
li,
a {
  font-size: 14px;
  line-height: 2;
  letter-spacing: 1px;
}

img {
  display: block;
  margin: 0 auto;
}
//Java scrip:

let myImage = document.querySelector('img');

myImage.onclick = function() {
  let mySrc = myImage.getAttribute('src');
  if(mySrc === 'imagenes/firefox-icon.png') {
    myImage.setAttribute ('src','imagenes/firefox2.png');
  } else {
    myImage.setAttribute ('src','imagenes/firefox-icon.png');
  }
}

// Personalized welcome message code

let myButton = document.querySelector('button');
let myHeading = document.querySelector('h1');

function setUserName() {
  let myName = prompt('Porfavor escriba su nombre.');
  if(!myName) {
    setUserName();
  } else {
    localStorage.setItem('name', myName);
    myHeading.innerHTML = 'Mozilla es genial, ' + myName;
  }
}

if(!localStorage.getItem('name')) {
  setUserName();
} else {
  let storedName = localStorage.getItem('nombre');
  myHeading.innerHTML = 'Mozilla es genial, ' + storedName;
}

myButton.onclick = function() {
  setUserName();
}
