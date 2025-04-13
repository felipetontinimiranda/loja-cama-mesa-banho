<body>
  <header>
    <h1>Loja Cama, Mesa e Banho</h1>
    <nav>
      <a href="#">Início</a>
      <a href="#produtos">Produtos</a>
      <a href="#carrinho">Carrinho</a>
    </nav>
  </header>

  <main>
    <section id="produtos">
      <div class="produto">
        <img src="https://via.placeholder.com/200" alt="Toalha de Banho Luxo">
        <h2>Toalha de Banho Luxo</h2>
        <p>Toalha 100% algodão, super macia e absorvente.</p>
        <p class="preco">R$ 39,90</p>
        <button onclick="adicionarAoCarrinho('Toalha de Banho Luxo', 39.90)">Comprar</button>
      </div>

      <div class="produto">
        <img src="https://via.placeholder.com/200" alt="Jogo de Cama Queen">
        <h2>Jogo de Cama Queen</h2>
        <p>Conjunto 4 peças 200 fios. Toque macio e elegante.</p>
        <p class="preco">R$ 149,90</p>
        <button onclick="adicionarAoCarrinho('Jogo de Cama Queen', 149.90)">Comprar</button>
      </div>

      <div class="produto">
        <img src="https://via.placeholder.com/200" alt="Jogo de Toalhas">
        <h2>Kit Toalhas</h2>
        <p>Conjunto 5 peças com cores sortidas.</p>
        <p class="preco">R$ 79,90</p>
        <button onclick="adicionarAoCarrinho('Kit Toalhas', 79.90)">Comprar</button>
      </div>
    </section>

    <section id="carrinho">
      <h2>Carrinho de Compras</h2>
      <ul id="lista-carrinho"></ul>
      <p>Total: R$ <span id="total">0.00</span></p>
      <a href="checkout.html"><button>Finalizar Compra</button></a>
    </section>
  </main>

  <script>
    let carrinho = [];
    function adicionarAoCarrinho(produto, preco) {
      carrinho.push({ produto, preco });
      atualizarCarrinho();
    }

    function atualizarCarrinho() {
      const lista = document.getElementById('lista-carrinho');
      lista.innerHTML = '';
      let total = 0;
      carrinho.forEach(item => {
        const li = document.createElement('li');
        li.textContent = `${item.produto} - R$ ${item.preco.toFixed(2)}`;
        lista.appendChild(li);
        total += item.preco;
      });
      document.getElementById('total').textContent = total.toFixed(2);
    }
  </script>
</body>
