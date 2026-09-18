<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pizzaria Sabor & Massa</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      background: #fff8ef;
      color: #2b2b2b;
    }

    header {
      background: #b51f1f;
      color: white;
      padding: 25px;
      text-align: center;
    }

    header h1 {
      font-size: 32px;
    }

    header p {
      margin-top: 8px;
    }

    .banner {
      background: #ffca28;
      padding: 35px 20px;
      text-align: center;
    }

    .banner h2 {
      font-size: 30px;
      color: #7b1600;
    }

    .banner p {
      margin-top: 10px;
      font-size: 18px;
    }

    .container {
      max-width: 1000px;
      margin: 30px auto;
      padding: 0 20px;
    }

    .container h2 {
      text-align: center;
      margin-bottom: 25px;
      color: #b51f1f;
    }

    .cardapio {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
      gap: 20px;
    }

    .pizza {
      background: white;
      border-radius: 15px;
      padding: 20px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.12);
      text-align: center;
    }

    .pizza .emoji {
      font-size: 65px;
    }

    .pizza h3 {
      margin: 10px 0;
      color: #b51f1f;
    }

    .pizza p {
      color: #666;
      min-height: 45px;
    }

    .preco {
      display: block;
      font-size: 21px;
      font-weight: bold;
      margin: 15px 0;
    }

    button {
      border: none;
      background: #b51f1f;
      color: white;
      padding: 12px 20px;
      border-radius: 8px;
      cursor: pointer;
      font-size: 16px;
    }

    button:hover {
      background: #8d1515;
    }

    #carrinho {
      background: white;
      margin-top: 35px;
      padding: 25px;
      border-radius: 15px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.12);
    }

    #listaCarrinho {
      margin: 15px 0;
    }

    .item {
      display: flex;
      justify-content: space-between;
      padding: 10px 0;
      border-bottom: 1px solid #ddd;
    }

    .total {
      font-size: 22px;
      font-weight: bold;
      margin: 20px 0;
    }

    .whatsapp {
      background: #25d366;
      width: 100%;
    }

    .whatsapp:hover {
      background: #1da851;
    }

    footer {
      margin-top: 40px;
      background: #2b2b2b;
      color: white;
      text-align: center;
      padding: 25px;
    }
  </style>
</head>

<body>

  <header>
    <h1>🍕 Pizzaria Sabor & Massa</h1>
    <p>A melhor pizza da cidade!</p>
  </header>

  <section class="banner">
    <h2>🔥 Promoção de Hoje!</h2>
    <p>Na compra de 2 pizzas, ganhe um refrigerante!</p>
  </section>

  <main class="container">

    <h2>🍕 Nosso Cardápio</h2>

    <section class="cardapio">

      <div class="pizza">
        <div class="emoji">🍕</div>
        <h3>Calabresa</h3>
        <p>Calabresa, cebola, queijo e molho de tomate.</p>
        <span class="preco">R$ 39,90</span>
        <button onclick="adicionar('Pizza de Calabresa', 39.90)">
          Adicionar
        </button>
      </div>

      <div class="pizza">
        <div class="emoji">🍕</div>
        <h3>Frango com Catupiry</h3>
        <p>Frango desfiado, catupiry, queijo e molho.</p>
        <span class="preco">R$ 44,90</span>
        <button onclick="adicionar('Frango com Catupiry', 44.90)">
          Adicionar
        </button>
      </div>

      <div class="pizza">
        <div class="emoji">🍕</div>
        <h3>Portuguesa</h3>
        <p>Presunto, ovos, cebola, ervilha, queijo e azeitona.</p>
        <span class="preco">R$ 42,90</span>
        <button onclick="adicionar('Pizza Portuguesa', 42.90)">
          Adicionar
        </button>
      </div>

      <div class="pizza">
        <div class="emoji">🍕</div>
        <h3>4 Queijos</h3>
        <p>Mussarela, parmesão, provolone e catupiry.</p>
        <span class="preco">R$ 46,90</span>
        <button onclick="adicionar('Pizza 4 Queijos', 46.90)">
          Adicionar
        </button>
      </div>

      <div class="pizza">
        <div class="emoji">🍕</div>
        <h3>Chocolate</h3>
        <p>Chocolate cremoso e granulado.</p>
        <span class="preco">R$ 41,90</span>
        <button onclick="adicionar('Pizza de Chocolate', 41.90)">
          Adicionar
        </button>
      </div>

      <div class="pizza">
        <div class="emoji">🥤</div>
        <h3>Refrigerante</h3>
        <p>Refrigerante 2 litros.</p>
        <span class="preco">R$ 10,00</span>
        <button onclick="adicionar('Refrigerante 2L', 10)">
          Adicionar
        </button>
      </div>

    </section>

    <section id="carrinho">
      <h2>🛒 Seu Pedido</h2>

      <div id="listaCarrinho">
        Seu carrinho está vazio.
      </div>

      <div class="total">
        Total: R$ <span id="total">0,00</span>
      </div>

      <button class="whatsapp" onclick="finalizarPedido()">
        📲 Finalizar pedido pelo WhatsApp
      </button>
    </section>

  </main>

  <footer>
    <p>🍕 Pizzaria Sabor & Massa</p>
    <p>Aberto todos os dias • 18h às 23h</p>
  </footer>

  <script>
    let carrinho = [];
    let total = 0;

    function adicionar(nome, preco) {
      carrinho.push({
        nome: nome,
        preco: preco
      });

      total += preco;

      atualizarCarrinho();
    }

    function atualizarCarrinho() {
      const lista = document.getElementById("listaCarrinho");

      if (carrinho.length === 0) {
        lista.innerHTML = "Seu carrinho está vazio.";
        return;
      }

      lista.innerHTML = "";

      carrinho.forEach((item, index) => {
        lista.innerHTML += `
          <div class="item">
            <span>${item.nome}</span>
            <span>
              R$ ${item.preco.toFixed(2).replace(".", ",")}
              <button onclick="remover(${index})">❌</button>
            </span>
          </div>
        `;
      });

      document.getElementById("total").innerText =
        total.toFixed(2).replace(".", ",");
    }

    function remover(index) {
      total -= carrinho[index].preco;
      carrinho.splice(index, 1);

      atualizarCarrinho();
    }

    function finalizarPedido() {
      if (carrinho.length === 0) {
        alert("Adicione alguma coisa ao carrinho!");
        return;
      }

      let mensagem = "🍕 *NOVO PEDIDO*%0A%0A";

      carrinho.forEach(item => {
        mensagem += `• ${item.nome} - R$ ${item.preco.toFixed(2).replace(".", ",")}%0A`;
      });

      mensagem += `%0A💰 *Total: R$ ${total.toFixed(2).replace(".", ",")}*`;

      // TROQUE PELO NÚMERO DA PIZZARIA
      const telefone = "5521999999999";

      window.open(
        `https://wa.me/${telefone}?text=${mensagem}`,
        "_blank"
      );
    }
  </script>

</body>
</html>