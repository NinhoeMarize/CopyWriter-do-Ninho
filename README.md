
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>João Paulo - Copywriter Cristão</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #000;
      color: white;
    }

    header {
      background-image: url('https://images.unsplash.com/photo-1521737604893-d14cc237f11d');
      background-size: cover;
      background-position: center;
      color: white;
      padding: 60px 20px;
      text-align: center;
      border-bottom: 3px solid #003366;
      border-radius: 0 0 15px 15px;
    }

    nav ul {
      list-style: none;
      padding: 0;
    }

    nav ul li {
      display: inline;
      margin: 0 15px;
    }

    nav ul li a {
      color: #66b2ff;
      text-decoration: none;
      font-weight: bold;
    }

    section {
      padding: 40px;
      text-align: center;
    }

    .work-item {
      background-color: #111;
      padding: 20px;
      margin: 10px auto;
      width: 80%;
      border: 2px solid #003366;
      border-radius: 15px;
      box-shadow: 0 0 10px #003366;
    }

    form input, form textarea {
      display: block;
      width: 80%;
      margin: 10px auto;
      padding: 10px;
      border-radius: 10px;
      border: 1px solid #003366;
      background-color: #222;
      color: white;
    }

    form button, .btn-social {
      background-color: #003366;
      color: white;
      padding: 10px 20px;
      margin: 5px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
    }

    .btn-social:hover {
      background-color: #0055aa;
    }

    .social-links {
      margin-top: 20px;
    }

    .modal {
      display: none;
      position: fixed;
      z-index: 999;
      padding-top: 100px;
      left: 0; top: 0;
      width: 100%; height: 100%;
      overflow: auto;
      background-color: rgba(0,0,0,0.8);
    }

    .modal-content {
      background-color: #111;
      margin: auto;
      padding: 20px;
      border: 2px solid #003366;
      width: 80%;
      max-width: 500px;
      border-radius: 15px;
      text-align: center;
    }

    .close {
      color: white;
      float: right;
      font-size: 28px;
      font-weight: bold;
      cursor: pointer;
    }

    footer {
      background-color: #111;
      color: white;
      text-align: center;
      padding: 20px;
      border-top: 3px solid #003366;
      border-radius: 15px 15px 0 0;
    }
  </style>
</head>
<body>

  <header>
    <h1>João Paulo - Artilheiro do Amor de Jesus</h1>
    <nav>
      <ul>
        <li><a href="#about">Sobre</a></li>
        <li><a href="#works">Trabalhos</a></li>
        <li><a href="#contact">Contato</a></li>
      </ul>
    </nav>
  </header>

  <section id="about">
    <h2>Sobre Mim</h2>
    <p>Copywriter com propósito! Escrevo com fé, foco e criatividade para conectar mensagens que tocam o coração.</p>
    <a href="seu-portifolio.pdf" download class="btn-social">📄 Baixar Portfólio PDF</a>
  </section>

  <section id="works">
    <h2>Meus Trabalhos</h2>
    <div class="work-item">✍️ Projeto 1 - Texto para campanha solidária</div>
    <div class="work-item">💬 Projeto 2 - Roteiro para vídeo de testemunho</div>
    <div class="work-item">📢 Projeto 3 - Anúncio para ONG cristã</div>
  </section>

  <section id="contact">
    <h2>Contato</h2>
    <p>Quer trabalhar comigo? Envie uma mensagem ou me chame nas redes sociais!</p>
    <form id="contactForm">
      <input type="text" placeholder="Seu nome" required />
      <input type="email" placeholder="Seu e-mail" required />
      <textarea placeholder="Sua mensagem" required></textarea>
      <button type="submit">Enviar</button>
    </form>
    <div class="social-links">
      <a href="https://instagram.com/seuusuario" target="_blank" class="btn-social">📸 Instagram</a>
      <a href="https://linkedin.com/in/seuperfil" target="_blank" class="btn-social">💼 LinkedIn</a>
      <button class="btn-social" onclick="openModal()">💖 Faça uma doação via Pix</button>
    </div>
  </section>

  <div id="pixModal" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal()">&times;</span>
      <h3>Faça sua doação via Pix 🙏</h3>
      <p><strong>Chave Pix (celular):</strong></p>
      <p style="font-size: 20px; font-weight: bold;">(81) 9 8657-3209</p>
      <p><input type="checkbox" id="autorizacaoPix"> Autorizo o débito em minha conta para esta doação.</p>
    </div>
  </div>

  <footer>
    <p>© 2025 João Paulo - Todos os direitos reservados. Com fé e criatividade, a Palavra ganha vida!</p>
  </footer>

  <script>
    document.querySelector("#contactForm").addEventListener("submit", function(event) {
      event.preventDefault();
      alert("Mensagem enviada com sucesso! 🙏");
    });

    function openModal() {
      document.getElementById("pixModal").style.display = "block";
    }

    function closeModal() {
      document.getElementById("pixModal").style.display = "none";
    }

    window.onclick = function(event) {
      const modal = document.getElementById("pixModal");
      if (event.target === modal) {
        closeModal();
      }
    };
  </script>

</body>
</html>
