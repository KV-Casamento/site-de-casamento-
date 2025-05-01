<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Vinícius & Karolyne - Casamento</title>
  <style>
    body {
      font-family: 'Georgia', serif;
      margin: 0;
      padding: 0;
      background: #fffefc;
      color: #5c4b36;
    }
    header {
      background: #fffaf5;
      text-align: center;
      padding: 2rem 1rem;
      border-bottom: 1px solid #e0d3c2;
    }
    header h1 {
      font-size: 2.5rem;
      color: #a87c4f;
      margin-bottom: 0.5rem;
    }
    header p {
      font-size: 1.2rem;
      margin: 0.2rem 0;
    }
    .detalhes {
      margin-top: 1rem;
      font-size: 1.1rem;
    }
    main {
      padding: 2rem;
      max-width: 800px;
      margin: 0 auto;
    }
    h2 {
      color: #a87c4f;
      text-align: center;
      margin-bottom: 1rem;
    }
    .presente {
      border: 1px solid #e6ddd2;
      border-radius: 10px;
      padding: 1rem;
      margin-bottom: 1rem;
      display: flex;
      background: #fff;
      align-items: center;
    }
    .presente img {
      width: 120px;
      height: 120px;
      object-fit: cover;
      border-radius: 8px;
      margin-right: 1rem;
    }
    .presente-info {
      flex: 1;
    }
    .btn {
      background-color: #c59b6d;
      color: white;
      padding: 0.5rem 1rem;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      text-decoration: none;
    }
    .btn:hover {
      background-color: #a87c4f;
    }
    .pix-info {
      background: #fdf4ef;
      padding: 2rem;
      margin-top: 2rem;
      border-radius: 10px;
      display: none;
    }
    .pix-info.active {
      display: block;
    }
    .qr-code {
      width: 180px;
      margin-top: 1rem;
    }
  </style>
</head>
<body>
  <header>
    <h1>Vinícius & Karolyne</h1>
    <p>Convidam você para celebrar a união do nosso amor</p>
    <div class="detalhes">
      <p><strong>19 de julho de 2025 – 09:30h</strong></p>
      <p>Capela São Francisco de Assis | Araguaína - TO</p>
      <p>A festa será em uma chácara a 6 km de Araguaína</p>
      <p><em>(Endereço será informado próximo à data)</em></p>
    </div>
  </header>

  <main>
    <h2>Lista de Presentes 🎁</h2>

    <div class="presente">
      <img src="https://via.placeholder.com/120" alt="Liquidificador Oster" />
      <div class="presente-info">
        <h3>Liquidificador Oster</h3>
        <p>R$ 250</p>
        <button class="btn" onclick="mostrarPix('Liquidificador Oster', 'R$ 250')">Presentear</button>
      </div>
    </div>

    <div class="presente">
      <img src="https://via.placeholder.com/120" alt="Jantar Romântico" />
      <div class="presente-info">
        <h3>Jantar Romântico</h3>
        <p>R$ 180</p>
        <button class="btn" onclick="mostrarPix('Jantar Romântico', 'R$ 180')">Presentear</button>
      </div>
    </div>

    <div class="pix-info" id="pixBox">
      <h3 id="pixTitle"></h3>
      <p><strong>Valor:</strong> <span id="pixValor"></span></p>
      <p><strong>Chave PIX:</strong> <span id="chavePix">seuemail@exemplo.com</span></p>
      <button class="btn" onclick="copiarPix()">Copiar chave PIX</button>
      <p>Ou escaneie o QR Code abaixo:</p>
      <img class="qr-code" src="https://via.placeholder.com/180" alt="QR Code PIX" />
    </div>
  </main>

  <script>
    function mostrarPix(titulo, valor) {
      document.getElementById('pixBox').classList.add('active');
      document.getElementById('pixTitle').innerText = `Você escolheu: ${titulo}`;
      document.getElementById('pixValor').innerText = valor;
    }

    function copiarPix() {
      const chave = document.getElementById('chavePix').innerText;
      navigator.clipboard.writeText(chave);
      alert('Chave PIX copiada!');
    }
  </script>
</body>
</html>
