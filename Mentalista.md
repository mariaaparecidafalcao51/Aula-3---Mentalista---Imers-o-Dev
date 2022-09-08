# Aula-3---Mentalista---Imers-o-Dev

Tentar adivinhar qual é o número que o programa (computador) escolheu; acertou ou errou.


HTML5

<html>

<head>
  <title>
    Imersão Dev - Aula 03
  </title>
</head>

<body>
  <div class="container">
    <h1 class="page-title">
      Mentalista
    </h1>
    <img src="https://www.alura.com.br/assets/img/imersoes/dev-2021/logo-imersao-mentalista.svg" class="page-logo" alt=""><br>
    <p class="page-subtitle">
      Digite um número de 0 a 10
    </p>
    <input type="number" id="valor" /><br>
    <button type="submit" onclick="Chutar()">Chutar</button>
    <h2 class="resultado" id="resultado"></h2>
  </div>
  <a href="https://alura.com.br/" target="_blank">
    <img src="https://www.alura.com.br/assets/img/home/alura-logo.svg" alt="" class="alura-logo">
  </a>
  <script src="app.js"></script>
</body>

</html>


CSS3

body {
  font-family: "Roboto Mono", monospace;
  min-height: 600px;
  background-image: url("https://www.alura.com.br/assets/img/imersoes/dev-2021/dia-03-mentalista.png");
  background-color: #000000;
  background-size: cover;
  background-position: center bottom;
  background-repeat: no-repeat;
}

.container {
  text-align: center;
  padding: 20px;
  height: 100vh;
}

.page-title {
  color: #ffffff;
  margin: 0 0 5px;
}

.page-subtitle {
  color: #ffffff;
  margin-top: 16px;
}

.page-logo {
  width: 200px;
}

.alura-logo {
  width: 40px;
  position: absolute;
  top: 10px;
  right: 10px;
}

@media (max-height: 500px) {
  body {
    min-height: 800px;
  }
}

input {
  margin: 4px;
  padding: 6px;
  border-radius: 5px;
}

button {
  margin-top: 12px;
  padding: 4px 8px;
  border-radius: 10px;
  background: #ffffff;
}

.resultado {
  color: #ffffff;
  text-align: center;
  margin-top: 16px;
}



JAVASCRIPT

var numeroSecreto = parseInt(Math.random() * 11);

function Chutar() {
  var elementoResultado = document.getElementById("resultado");
  var chute = parseInt(document.getElementById("valor").value);
  console.log(chute);
  if (chute == numeroSecreto) {
    elementoResultado.innerHTML = "Você acertou";
  } else if (chute > 10 || chute < 0) {
    elementoResultado.innerHTML = "Você deve digitar um número de 0 a 10";
  } else {
    elementoResultado.innerHTML = "Errou";
  }
}

