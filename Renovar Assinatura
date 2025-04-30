<!DOCTYPE html>
<html>
<head>
  <title>Gerador de Link por Telefone</title>
</head>
<body>
  <h2>Digite seu telefone:</h2>
  <input type="text" id="telefone" placeholder="Digite o telefone">
  <button onclick="mostrarLink()">Ver link</button>

  <p id="resultado"></p>

  <script>
    function mostrarLink() {
      const telefone = document.getElementById("telefone").value;
      const resultado = document.getElementById("resultado");

      // Substitua pelos números e links desejados
      const links = {
        "12996437435": "https://link1.com",
        "11999999999": "https://link2.com",
        "21988888888": "https://link3.com"
      };

      if (links[telefone]) {
        resultado.innerHTML = `<a href="${links[telefone]}" target="_blank">Clique aqui para acessar</a>`;
      } else {
        resultado.innerHTML = "Telefone não encontrado.";
      }
    }
  </script>
</body>
</html>