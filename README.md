<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Painel Admin</title>
  <style>
    body { font-family: Arial; padding: 20px; }
    input, button { padding: 10px; margin: 5px 0; width: 100%; }
  </style>
</head>
<body>
  <h2>Adicionar novo cliente</h2>
  <input type="text" id="telefone" placeholder="Telefone" />
  <input type="text" id="nome" placeholder="Nome" />
  <input type="text" id="link" placeholder="Link" />
  <button onclick="adicionar()">Adicionar</button>
  <div id="msg"></div>

  <script>
    async function adicionar() {
      const telefone = document.getElementById("telefone").value.trim();
      const nome = document.getElementById("nome").value.trim();
      const link = document.getElementById("link").value.trim();

      const res = await fetch("/api/adicionar", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({ telefone, nome, link })
      });

      const texto = await res.text();
      document.getElementById("msg").innerText = texto;
    }
  </script>
</body>
</html>