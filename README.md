#<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BressedStory</title>
    <style>
        body {
            font-family: 'Arial, sans-serif';
            margin: 0;
            padding: 0;
            background-color: #f8f0fc;
        }
        header {
            background: linear-gradient(90deg, rgba(0,0,0,0.5) 0%, rgba(255,105,180,0.5) 100%);
            color: white;
            padding: 20px;
            text-align: center;
            font-size: 2em;
        }
        nav {
            display: flex;
            justify-content: center;
            background-color: #ff70a6;
        }
        nav a {
            color: white;
            text-decoration: none;
            padding: 14px 20px;
        }
        nav a:hover {
            background-color: #ff9cee;
        }
        .container {
            padding: 20px;
        }
        .product {
            border: 1px solid #ff70a6;
            border-radius: 10px;
            padding: 10px;
            margin: 10px 0;
            text-align: center;
        }
        .product img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
            cursor: pointer;
        }
        .product button {
            background-color: #ff70a6;
            color: white;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
            border-radius: 5px;
        }
        .product button:hover {
            background-color: #ff9cee;
        }
        footer {
            background-color: #ff9cee;
            color: white;
            text-align: center;
            padding: 10px;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
        .lightbox {
            display: none;
            position: fixed;
            z-index: 999;
            padding-top: 60px;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0,0,0,0.9);
        }
        .lightbox-content {
            margin: auto;
            display: block;
            width: 80%;
            max-width: 700px;
        }
        .lightbox-caption {
            margin: auto;
            display: block;
            width: 80%;
            max-width: 700px;
            text-align: center;
            color: #ccc;
            padding: 10px 0;
            height: 150px;
        }
        .lightbox-close {
            position: absolute;
            top: 15px;
            right: 35px;
            color: #f1f1f1;
            font-size: 40px;
            font-weight: bold;
            transition: 0.3s;
        }
        .lightbox-close:hover,
        .lightbox-close:focus {
            color: #bbb;
            text-decoration: none;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <header>
        <h1>BressedStory</h1>
        <p>Roupas e Acessórios</p>
    </header>
    <nav>
        <a href="#home">Home</a>
        <a href="#sobre">Sobre</a>
        <a href="#produtos">Produtos</a>
        <a href="#contato">Contato</a>
    </nav>
    <div class="container">
        <section id="home">
            <h2>Bem-vindo à BressedStory</h2>
            <p>Explore nossa coleção de roupas e acessórios feitos especialmente para você!</p>
        </section>
        <section id="sobre">
            <h2>Sobre Nós</h2>
            <p>A BressedStory nasceu da paixão por moda e estilo. Nossos produtos são selecionados com cuidado para trazer o melhor da moda feminina para você.</p>
        </section>
        <section id="produtos">
            <h2>Nossos Produtos</h2>
            <div class="product">
                <img src="https://via.placeholder.com/300" alt="Saia Longa Verde" onclick="openLightbox(this)">
                <h3>Saia Longa Verde</h3>
                <p>Descrição da Saia Longa Verde</p>
                <button>Comprar</button>
            </div>
            <div class="product">
                <img src="https://via.placeholder.com/300" alt="Produto 2" onclick="openLightbox(this)">
                <h3>Produto 2</h3>
                <p>Descrição do Produto 2</p>
                <button>Comprar</button>
            </div>
            <!-- Adicione mais produtos conforme necessário -->
        </section>
        <section id="contato">
            <h2>Contato</h2>
            <p>Entre em contato conosco através do telefone: (11) 98704-7617</p>
            <p>ou através do email: blessedstoreeofc@gmail.com</p>
        </section>
    </div>
    <footer>
        <p>&copy; Descubra a Blessed Storee Ofc desde 2023 e encontre o estilo que é a sua cara. Explore nossa coleção exclusiva de moda feminina e apaixone-se pelo que vestir.</p>
        <p>MOÇA LINDA Ltda. - Rua Hélcio da Silva 90, São Paulo, SP 02854-060</p>
        <p>Telefone: (11) 98704-7617</p>
    </footer>

    <!-- Lightbox -->
    <div id="lightbox" class="lightbox">
        <span class="lightbox-close" onclick="closeLightbox()">&times;</span>
        <img class="lightbox-content" id="lightbox-img">
        <div class="lightbox-caption" id="lightbox-caption"></div>
    </div>

    <script>
        function openLightbox(element) {
            document.getElementById('lightbox').style.display = 'block';
            document.getElementById('lightbox-img').src = element.src;
            document.getElementById('lightbox-caption').innerHTML = element.alt;
        }

        function closeLightbox() {
            document.getElementById('lightbox').style.display = 'none';
        }

        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
 Blessedstoreeofc
