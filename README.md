```html
<!DOCTYPE html>
<html lang="pt-br">

<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Recicla Paraná</title>

    <style>

        /* =========================
           RESET
        ========================= */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: #f1f8f5;
            color: #183c63;
        }


        /* =========================
           CABEÇALHO
        ========================= */

        header {
            position: sticky;
            top: 0;
            z-index: 1000;

            background: #ffffff;

            box-shadow: 0 3px 15px rgba(0, 0, 0, 0.10);

            padding: 15px 7%;
        }

        .navbar {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;

            font-size: 24px;
            font-weight: bold;

            color: #159447;
        }

        .logo span {
            color: #1976b8;
        }

        .logo-icon {
            font-size: 35px;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 25px;
        }

        nav a {
            text-decoration: none;
            color: #183c63;
            font-weight: bold;

            transition: 0.3s;
        }

        nav a:hover {
            color: #159447;
        }


        /* =========================
           BOTÃO
        ========================= */

        .btn {
            display: inline-block;

            padding: 13px 22px;

            border-radius: 30px;

            text-decoration: none;

            font-weight: bold;

            border: none;

            cursor: pointer;

            transition: 0.3s;
        }

        .btn-verde {
            background: #159447;
            color: white;
        }

        .btn-verde:hover {
            background: #0d7335;
            transform: translateY(-3px);
        }

        .btn-azul {
            background: #1976b8;
            color: white;
        }

        .btn-azul:hover {
            background: #125a8c;
            transform: translateY(-3px);
        }


        /* =========================
           HERO
        ========================= */

        .hero {
            min-height: 650px;

            display: flex;
            align-items: center;

            padding: 80px 7%;

            background:
                linear-gradient(
                    120deg,
                    rgba(21, 148, 71, 0.95),
                    rgba(25, 118, 184, 0.92)
                );

            color: white;
        }

        .hero-content {
            max-width: 650px;
        }

        .hero h1 {
            font-size: 58px;
            line-height: 1.1;

            margin-bottom: 20px;
        }

        .hero h1 span {
            color: #baffd2;
        }

        .hero p {
            font-size: 20px;
            line-height: 1.7;

            margin-bottom: 30px;

            color: #e9fff1;
        }

        .hero-buttons {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }

        .hero .btn {
            background: white;
            color: #159447;
        }

        .hero .btn:hover {
            background: #eafff1;
        }


        /* =========================
           SEÇÕES
        ========================= */

        section {
            padding: 80px 7%;
        }

        .titulo {
            text-align: center;

            margin-bottom: 50px;
        }

        .titulo h2 {
            font-size: 38px;

            color: #183c63;

            margin-bottom: 12px;
        }

        .titulo h2 span {
            color: #159447;
        }

        .titulo p {
            max-width: 700px;

            margin: auto;

            color: #60758a;

            line-height: 1.6;
        }


        /* =========================
           SOBRE
        ========================= */

        .sobre {
            display: grid;

            grid-template-columns: 1fr 1fr;

            gap: 50px;

            align-items: center;
        }

        .sobre-texto h3 {
            font-size: 30px;

            margin-bottom: 20px;

            color: #159447;
        }

        .sobre-texto p {
            line-height: 1.8;

            color: #536b7d;

            margin-bottom: 15px;
        }

        .sobre-box {
            background: white;

            padding: 35px;

            border-radius: 25px;

            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);

            border-left: 6px solid #159447;
        }

        .sobre-box h3 {
            color: #1976b8;

            margin-bottom: 15px;
        }


        /* =========================
           CARDS
        ========================= */

        .cards {
            display: grid;

            grid-template-columns:
                repeat(3, 1fr);

            gap: 25px;
        }

        .card {
            background: white;

            padding: 30px;

            border-radius: 20px;

            box-shadow:
                0 8px 25px rgba(0, 0, 0, 0.08);

            transition: 0.3s;

            border-top: 5px solid #159447;
        }

        .card:hover {
            transform: translateY(-8px);

            box-shadow:
                0 15px 35px rgba(0, 0, 0, 0.13);
        }

        .card-icon {
            font-size: 45px;

            margin-bottom: 15px;
        }

        .card h3 {
            color: #183c63;

            margin-bottom: 12px;
        }

        .card p {
            color: #65798a;

            line-height: 1.6;
        }


        /* =========================
           PONTOS
        ========================= */

        .pontos {
            background:
                linear-gradient(
                    135deg,
                    #e2f7ea,
                    #e1f1fb
                );
        }

        .pontos-container {
            display: grid;

            grid-template-columns:
                repeat(3, 1fr);

            gap: 25px;
        }

        .ponto-card {
            background: white;

            border-radius: 20px;

            padding: 30px;

            text-align: center;

            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.08);
        }

        .ponto-card .numero {
            font-size: 42px;

            font-weight: bold;

            color: #159447;

            margin-bottom: 10px;
        }

        .ponto-card h3 {
            color: #183c63;

            margin-bottom: 8px;
        }

        .ponto-card p {
            color: #65798a;
        }


        /* =========================
           RECOMPENSAS
        ========================= */

        .recompensas {
            background: #ffffff;
        }

        .recompensa-card {
            background:
                linear-gradient(
                    135deg,
                    #159447,
                    #1976b8
                );

            color: white;

            padding: 35px;

            border-radius: 25px;

            text-align: center;

            box-shadow:
                0 15px 35px rgba(21, 148, 71, 0.25);
        }

        .recompensa-card h3 {
            font-size: 28px;

            margin-bottom: 15px;
        }

        .recompensa-card p {
            line-height: 1.7;

            margin-bottom: 25px;
        }

        .pontos-numero {
            font-size: 50px;

            font-weight: bold;

            color: #c8ffd9;

            margin-bottom: 15px;
        }


        /* =========================
           EDUCAÇÃO
        ========================= */

        .educacao {
            background: #eaf8f0;
        }

        .jogo {
            background: white;

            border-radius: 25px;

            padding: 40px;

            max-width: 850px;

            margin: auto;

            text-align: center;

            box-shadow:
                0 10px 30px rgba(0, 0, 0, 0.08);
        }

        .jogo h3 {
            font-size: 28px;

            color: #1976b8;

            margin-bottom: 15px;
        }

        .jogo p {
            color: #60758a;

            margin-bottom: 25px;

            line-height: 1.6;
        }

        .pergunta {
            font-size: 22px;

            font-weight: bold;

            color: #183c63;

            margin-bottom: 20px;
        }

        .opcoes {
            display: flex;

            justify-content: center;

            gap: 15px;

            flex-wrap: wrap;
        }

        .opcao {
            padding: 12px 25px;

            border-radius: 25px;

            border: 2px solid #159447;

            background: white;

            color: #159447;

            cursor: pointer;

            font-weight: bold;

            transition: 0.3s;
        }

        .opcao:hover {
            background: #159447;

            color: white;
        }

        #resultado {
            margin-top: 20px;

            font-weight: bold;

            font-size: 18px;
        }


        /* =========================
           IMPACTO
        ========================= */

        .impacto {
            background:
                linear-gradient(
                    120deg,
                    #183c63,
                    #1976b8
                );

            color: white;
        }

        .impacto .titulo h2 {
            color: white;
        }

        .impacto .titulo p {
            color: #d9ecfa;
        }

        .impacto-cards {
            display: grid;

            grid-template-columns:
                repeat(3, 1fr);

            gap: 25px;
        }

        .impacto-card {
            background: rgba(255, 255, 255, 0.12);

            padding: 35px;

            border-radius: 20px;

            text-align: center;

            border: 1px solid rgba(255,255,255,0.15);
        }

        .impacto-card strong {
            display: block;

            font-size: 42px;

            color: #8dffb3;

            margin-bottom: 10px;
        }

        .impacto-card span {
            color: #e1f2ff;
        }


        /* =========================
           FOOTER
        ========================= */

        footer {
            background: #102d49;

            color: white;

            padding: 50px 7%;
        }

        .footer-content {
            display: grid;

            grid-template-columns:
                2fr 1fr 1fr;

            gap: 40px;
        }

        footer h3 {
            margin-bottom: 15px;

            color: #72e99a;
        }

        footer p {
            color: #c8d7e4;

            line-height: 1.7;
        }

        footer ul {
            list-style: none;
        }

        footer li {
            margin-bottom: 10px;

            color: #c8d7e4;
        }

        .copyright {
            text-align: center;

            border-top: 1px solid rgba(255,255,255,0.1);

            margin-top: 40px;

            padding-top: 25px;

            color: #9db1c1;
        }


        /* =========================
           RESPONSIVIDADE
        ========================= */

        @media (max-width: 850px) {

            nav ul {
                display: none;
            }

            .hero h1 {
                font-size: 42px;
            }

            .sobre {
                grid-template-columns: 1fr;
            }

            .cards,
            .pontos-container,
            .impacto-cards {
                grid-template-columns: 1fr;
            }

            .footer-content {
                grid-template-columns: 1fr;
            }

        }


        @media (max-width: 500px) {

            section {
                padding: 60px 5%;
            }

            .hero {
                padding: 70px 5%;
            }

            .hero h1 {
                font-size: 35px;
            }

            .hero p {
                font-size: 17px;
            }

            .titulo h2 {
                font-size: 30px;
            }

        }

    </style>

</head>


<body>


    <!-- =========================
         MENU
    ========================= -->

    <header>

        <div class="navbar">

            <div class="logo">

                <div class="logo-icon">
                    ♻️
                </div>

                Recicla <span>Paraná</span>

            </div>


            <nav>

                <ul>

                    <li>
                        <a href="#inicio">Início</a>
                    </li>

                    <li>
                        <a href="#sobre">Projeto</a>
                    </li>

                    <li>
                        <a href="#recompensas">Recompensas</a>
                    </li>

                    <li>
                        <a href="#educacao">Educação</a>
                    </li>

                    <li>
                        <a href="#impacto">Impacto</a>
                    </li>

                </ul>

            </nav>

            <a href="#registrar" class="btn btn-verde">
                Reciclar ♻️
            </a>

        </div>

    </header>


    <!-- =========================
         HERO
    ========================= -->

    <section class="hero" id="inicio">

        <div class="hero-content">

            <h1>
                Recicle hoje.
                <span>Transforme o amanhã.</span>
            </h1>

            <p>
                O Recicla Paraná conecta tecnologia,
                sustentabilidade e recompensas para
                transformar a reciclagem em um hábito
                simples, divertido e valorizado.
            </p>

            <div class="hero-buttons">

                <a href="#registrar" class="btn">
                    📸 Registrar reciclagem
                </a>

                <a href="#sobre" class="btn">
                    Conheça o projeto
                </a>

            </div>

        </div>

    </section>


    <!-- =========================
         SOBRE
    ========================= -->

    <section id="sobre">

        <div class="titulo">

            <h2>
                Sobre o <span>Recicla Paraná</span>
            </h2>

            <p>
                Uma solução tecnológica para incentivar
                a reciclagem e fortalecer a consciência
                ambiental no Paraná.
            </p>

        </div>


        <div class="sobre">

            <div class="sobre-texto">

                <h3>
                    🌱 Tecnologia a favor do planeta
                </h3>

                <p>
                    O Recicla Paraná nasceu para combater
                    problemas comuns relacionados ao descarte
                    incorreto de resíduos e à falta de
                    incentivo para a reciclagem.
                </p>

                <p>
                    Através do aplicativo, os usuários podem
                    registrar materiais reciclados utilizando
                    fotos, QR Codes ou comprovantes.
                </p>

                <p>
                    Após a confirmação, os usuários recebem
                    pontos que podem ser trocados por
                    benefícios e recompensas.
                </p>

            </div>


            <div class="sobre-box">

                <h3>
                    ♻️ Nossa missão
                </h3>

                <p>
                    Tornar a reciclagem mais simples,
                    acessível e motivadora, contribuindo
                    para um Paraná mais limpo, sustentável
                    e consciente.
                </p>

            </div>

        </div>

    </section>


    <!-- =========================
         COMO FUNCIONA
    ========================= -->

    <section>

        <div class="titulo">

            <h2>
                Como <span>funciona?</span>
            </h2>

            <p>
                Reciclar com o Recicla Paraná é fácil.
            </p>

        </div>


        <div class="cards">


            <div class="card">

                <div class="card-icon">
                    📸
                </div>

                <h3>
                    1. Registre
                </h3>

                <p>
                    Tire uma foto do material reciclado,
                    utilize um QR Code ou envie um
                    comprovante.
                </p>

            </div>


            <div class="card">

                <div class="card-icon">
                    ⭐
                </div>

                <h3>
                    2. Ganhe pontos
                </h3>

                <p>
                    Após a confirmação, você recebe pontos
                    por suas ações sustentáveis.
                </p>

            </div>


            <div class="card">

                <div class="card-icon">
                    🎁
                </div>

                <h3>
                    3. Troque
                </h3>

                <p>
                    Utilize seus pontos para conseguir
                    descontos, benefícios e recompensas.
                </p>

            </div>


        </div>

    </section>


    <!-- =========================
         REGISTRAR
    ========================= -->

    <section id="registrar" class="pontos">

        <div class="titulo">

            <h2>
                Faça sua parte. <span>Recicle!</span>
            </h2>

            <p>
                Registre sua reciclagem e acompanhe
                sua contribuição para o meio ambiente.
            </p>

        </div>


        <div class="pontos-container">

            <div class="ponto-card">

                <div class="numero">
                    📸
                </div>

                <h3>
                    Foto
                </h3>

                <p>
                    Registre o material reciclado
                    através de uma foto.
                </p>

            </div>


            <div class="ponto-card">

                <div class="numero">
                    QR
                </div>

                <h3>
                    QR Code
                </h3>

                <p>
                    Escaneie o código disponível
                    no ponto de coleta.
                </p>

            </div>


            <div class="ponto-card">

                <div class="numero">
                    📄
                </div>

                <h3>
                    Comprovante
                </h3>

                <p>
                    Envie seu comprovante para
                    confirmar a reciclagem.
                </p>

            </div>

        </div>

    </section>


    <!-- =========================
         RECOMPENSAS
    ========================= -->

    <section id="recompensas" class="recompensas">

        <div class="titulo">

            <h2>
                Recicle e <span>ganhe!</span>
            </h2>

            <p>
                Suas atitudes sustentáveis podem gerar
                benefícios.
            </p>

        </div>


        <div class="recompensa-card">

            <div class="pontos-numero">
                ⭐ 1.250 pontos
            </div>

            <h3>
                Você está fazendo a diferença!
            </h3>

            <p>
                Seus pontos podem ser trocados por
                descontos, produtos e benefícios oferecidos
                pelas empresas parceiras.
            </p>

            <button class="btn" onclick="mostrarRecompensa()">
                Ver recompensas 🎁
            </button>

            <p id="mensagemRecompensa"></p>

        </div>

    </section>


    <!-- =========================
         EDUCAÇÃO
    ========================= -->

    <section id="educacao" class="educacao">

        <div class="titulo">

            <h2>
                Aprender também pode ser <span>divertido!</span>
            </h2>

            <p>
                Jogos e desafios para ensinar sustentabilidade
                para crianças e famílias.
            </p>

        </div>


        <div class="jogo">

            <h3>
                🎮 Desafio da Reciclagem
            </h3>

            <p>
                Teste seus conhecimentos sobre reciclagem!
            </p>

            <div class="pergunta">

                Onde devemos colocar uma garrafa PET?

            </div>


            <div class="opcoes">

                <button
                    class="opcao"
                    onclick="responder(false)">
                    🗑️ Lixo comum
                </button>

                <button
                    class="opcao"
                    onclick="responder(true)">
                    ♻️ Reciclável
                </button>

                <button
                    class="opcao"
                    onclick="responder(false)">
                    🍂 Orgânico
                </button>

            </div>


            <div id="resultado"></div>

        </div>

    </section>


    <!-- =========================
         IMPACTO
    ========================= -->

    <section id="impacto" class="impacto">

        <div class="titulo">

            <h2>
                Nosso <span>impacto</span>
            </h2>

            <p>
                Cada pessoa pode contribuir para um futuro
                mais sustentável.
            </p>

        </div>


        <div class="impacto-cards">


            <div class="impacto-card">

                <strong>
                    12.540
                </strong>

                <span>
                    Kg de resíduos reciclados
                </span>

            </div>


            <div class="impacto-card">

                <strong>
                    3.280
                </strong>

                <span>
                    Usuários participantes
                </span>

            </div>


            <div class="impacto-card">

                <strong>
                    48
                </strong>

                <span>
                    Pontos de coleta
                </span>

            </div>


        </div>

    </section>


    <!-- =========================
         FOOTER
    ========================= -->

    <footer>

        <div class="footer-content">


            <div>

                <h3>
                    ♻️ Recicla Paraná
                </h3>

                <p>
                    Tecnologia, educação e sustentabilidade
                    trabalhando juntos por um Paraná melhor.
                </p>

            </div>


            <div>

                <h3>
                    Navegação
                </h3>

                <ul>

                    <li>Início</li>

                    <li>Projeto</li>

                    <li>Recompensas</li>

                    <li>Educação</li>

                </ul>

            </div>


            <div>

                <h3>
                    Siga essa ideia
                </h3>

                <p>
                    🌱 Recicle<br>
                    ♻️ Reutilize<br>
                    💚 Preserve
                </p>

            </div>


        </div>


        <div class="copyright">

            © 2026 Recicla Paraná —
            Todos os direitos reservados.

        </div>

    </footer>


    <!-- =========================
         JAVASCRIPT
    ========================= -->

    <script>

        function responder(correta) {

            const resultado =
                document.getElementById("resultado");

            if (correta) {

                resultado.innerHTML =
                    "🎉 Parabéns! Você acertou! A garrafa PET deve ser destinada à reciclagem.";

                resultado.style.color = "#159447";

            } else {

                resultado.innerHTML =
                    "❌ Quase! Tente novamente. A garrafa PET é um material reciclável.";

                resultado.style.color = "#d9534f";

            }

        }


        function mostrarRecompensa() {

            const mensagem =
                document.getElementById("mensagemRecompensa");

            mensagem.innerHTML =
                "🎁 Em breve você poderá trocar seus pontos por descontos e benefícios!";

            mensagem.style.marginTop = "20px";

        }

    </script>


</body>

</html>
```
