```html
<!DOCTYPE html>
<html lang="pt-BR">

<head>

    <meta charset="UTF-8">

    <meta name="viewport"
          content="width=device-width, initial-scale=1.0">

    <meta name="description"
          content="Recicla Paraná - Recicle, participe e transforme o futuro.">

    <meta name="theme-color"
          content="#071c33">

    <title>Recicla Paraná ♻️</title>


    <style>

        /* ==================================================
           CORES
        ================================================== */

        :root {

            --azul: #071c33;
            --azul2: #0c3559;
            --verde: #16a765;
            --verde2: #35d58a;

            --branco: #ffffff;
            --fundo: #f5f9fb;

            --texto: #50677a;

            --borda: #dfe9ef;

            --sombra:
                0 15px 40px rgba(7, 28, 51, .10);
        }


        /* ==================================================
           RESET
        ================================================== */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }


        html {
            scroll-behavior: smooth;
        }


        body {

            font-family:
                Arial,
                Helvetica,
                sans-serif;

            background: var(--branco);

            color: var(--azul);

            overflow-x: hidden;
        }


        /* ==================================================
           SCROLLBAR
        ================================================== */

        ::-webkit-scrollbar {
            width: 9px;
        }

        ::-webkit-scrollbar-track {
            background: #edf2f5;
        }

        ::-webkit-scrollbar-thumb {

            background: var(--verde);

            border-radius: 20px;
        }


        /* ==================================================
           HEADER
        ================================================== */

        header {

            position: sticky;

            top: 0;

            z-index: 1000;

            height: 75px;

            display: flex;

            align-items: center;

            justify-content: space-between;

            padding: 0 7%;

            background:
                rgba(7, 28, 51, .97);

            box-shadow:
                0 5px 25px
                rgba(0, 0, 0, .12);
        }


        .logo {

            color: white;

            font-size: 22px;

            font-weight: 900;
        }


        .logo span {

            color: var(--verde2);
        }


        nav {

            display: flex;

            align-items: center;

            gap: 28px;
        }


        nav a {

            position: relative;

            color: white;

            text-decoration: none;

            font-size: 14px;

            font-weight: bold;

            transition: .3s;
        }


        nav a:hover {

            color: var(--verde2);
        }


        nav a::after {

            content: "";

            position: absolute;

            left: 0;

            bottom: -7px;

            width: 0;

            height: 2px;

            background: var(--verde2);

            transition: .3s;
        }


        nav a:hover::after {

            width: 100%;
        }


        .menu {

            display: none;

            border: none;

            background: transparent;

            color: white;

            font-size: 28px;

            cursor: pointer;
        }


        /* ==================================================
           HERO
        ================================================== */

        .hero {

            min-height:
                calc(100vh - 75px);

            display: flex;

            align-items: center;

            padding: 70px 8%;

            position: relative;

            overflow: hidden;

            background:

                radial-gradient(
                    circle at 90% 20%,
                    rgba(22,167,101,.17),
                    transparent 250px
                ),

                radial-gradient(
                    circle at 5% 85%,
                    rgba(7,28,51,.07),
                    transparent 250px
                ),

                white;
        }


        .hero::after {

            content: "♻";

            position: absolute;

            right: -60px;

            top: 50px;

            font-size: 350px;

            color:
                rgba(22,167,101,.04);

            transform:
                rotate(15deg);

            pointer-events: none;
        }


        .hero-content {

            max-width: 850px;

            position: relative;

            z-index: 2;
        }


        .tag {

            display: inline-block;

            padding: 9px 17px;

            margin-bottom: 25px;

            border-radius: 30px;

            background: #e6f8ef;

            color: var(--verde);

            font-size: 13px;

            font-weight: bold;
        }


        .hero h1 {

            font-family: Georgia, serif;

            font-size:
                clamp(52px, 9vw, 95px);

            line-height: .95;

            color: var(--azul);

            margin-bottom: 25px;
        }


        .hero h1 span {

            color: var(--verde);
        }


        .hero h2 {

            color: var(--azul2);

            font-size:
                clamp(23px, 4vw, 35px);

            margin-bottom: 20px;

            line-height: 1.3;
        }


        .hero p {

            max-width: 680px;

            color: var(--texto);

            font-size: 18px;

            line-height: 1.8;
        }


        .buttons {

            display: flex;

            flex-wrap: wrap;

            gap: 15px;

            margin-top: 35px;
        }


        .button {

            display: inline-flex;

            align-items: center;

            justify-content: center;

            padding: 15px 28px;

            border-radius: 30px;

            text-decoration: none;

            font-weight: bold;

            transition: .3s;
        }


        .primary {

            background: var(--verde);

            color: white;

            box-shadow:
                0 10px 25px
                rgba(22,167,101,.25);
        }


        .primary:hover {

            transform:
                translateY(-4px);

            background: #108b55;
        }


        .secondary {

            color: var(--azul);

            border:
                2px solid
                var(--azul);
        }


        .secondary:hover {

            background: var(--azul);

            color: white;

            transform:
                translateY(-4px);
        }


        /* ==================================================
           ESTATÍSTICAS
        ================================================== */

        .stats {

            background: var(--azul);

            color: white;

            padding: 42px 8%;
        }


        .stats-grid {

            max-width: 1150px;

            margin: auto;

            display: grid;

            grid-template-columns:
                repeat(4, 1fr);

            gap: 20px;

            text-align: center;
        }


        .stat strong {

            display: block;

            color: var(--verde2);

            font-size: 38px;

            margin-bottom: 7px;
        }


        .stat span {

            color: #c8d7e2;

            font-size: 14px;
        }


        /* ==================================================
           SEÇÕES
        ================================================== */

        section {

            padding: 95px 8%;
        }


        .section-header {

            max-width: 750px;

            margin:
                0 auto 50px;

            text-align: center;
        }


        .section-tag {

            display: inline-block;

            padding: 7px 14px;

            margin-bottom: 15px;

            border-radius: 20px;

            background: #e6f8ef;

            color: var(--verde);

            font-size: 12px;

            font-weight: bold;

            text-transform: uppercase;

            letter-spacing: 1px;
        }


        .section-title {

            font-family: Georgia, serif;

            font-style: italic;

            font-size:
                clamp(35px, 5vw, 52px);

            color: var(--azul);

            margin-bottom: 15px;
        }


        .section-description {

            color: var(--texto);

            line-height: 1.8;
        }


        /* ==================================================
           CARDS
        ================================================== */

        .cards {

            max-width: 1150px;

            margin: auto;

            display: grid;

            grid-template-columns:
                repeat(
                    auto-fit,
                    minmax(220px, 1fr)
                );

            gap: 25px;
        }


        .card {

            position: relative;

            padding: 32px 25px;

            background: white;

            border:
                1px solid
                var(--borda);

            border-radius: 22px;

            text-align: center;

            box-shadow: var(--sombra);

            transition: .35s;

            overflow: hidden;
        }


        .card::before {

            content: "";

            position: absolute;

            top: 0;

            left: 0;

            width: 100%;

            height: 4px;

            background:
                linear-gradient(
                    90deg,
                    var(--verde),
                    var(--azul2)
                );
        }


        .card:hover {

            transform:
                translateY(-10px);

            box-shadow:
                0 25px 50px
                rgba(7,28,51,.16);
        }


        .icon {

            width: 75px;

            height: 75px;

            margin:
                0 auto 20px;

            display: flex;

            align-items: center;

            justify-content: center;

            border-radius: 20px;

            background: #eaf8f2;

            font-size: 38px;

            transition: .3s;
        }


        .card:hover .icon {

            transform:
                scale(1.1)
                rotate(5deg);
        }


        .card h3 {

            color: var(--azul);

            margin-bottom: 12px;

            font-size: 20px;
        }


        .card p {

            color: var(--texto);

            line-height: 1.7;

            font-size: 14px;
        }


        /* ==================================================
           FUNCIONAMENTO
        ================================================== */

        #funciona {

            background: var(--fundo);
        }


        .steps {

            max-width: 1100px;

            margin: auto;

            display: grid;

            grid-template-columns:
                repeat(4, 1fr);

            gap: 20px;
        }


        .step {

            text-align: center;

            padding: 20px;
        }


        .number {

            width: 65px;

            height: 65px;

            margin:
                0 auto 20px;

            display: flex;

            align-items: center;

            justify-content: center;

            border-radius: 50%;

            background: var(--verde);

            color: white;

            font-size: 23px;

            font-weight: bold;

            box-shadow:
                0 8px 20px
                rgba(22,167,101,.25);
        }


        .step h3 {

            color: var(--azul);

            margin-bottom: 10px;
        }


        .step p {

            color: var(--texto);

            line-height: 1.6;

            font-size: 14px;
        }


        /* ==================================================
           RECOMPENSAS
        ================================================== */

        #recompensas {

            background: var(--azul);

            color: white;
        }


        #recompensas
        .section-title {

            color: white;
        }


        #recompensas
        .section-description {

            color: #c7d7e3;
        }


        /* ==================================================
           PONTOS
        ================================================== */

        .points-box {

            max-width: 800px;

            margin:
                50px auto 0;

            padding: 35px;

            text-align: center;

            border-radius: 25px;

            background:
                rgba(255,255,255,.08);

            border:
                1px solid
                rgba(255,255,255,.14);
        }


        .points-box h3 {

            font-size: 24px;

            margin-bottom: 10px;
        }


        .points-box p {

            color: #c7d7e3;

            font-size: 14px;
        }


        .points {

            color: var(--verde2);

            font-size: 60px;

            font-weight: 900;

            margin: 15px 0;
        }


        .points-button {

            border: none;

            padding: 14px 25px;

            border-radius: 30px;

            background: var(--verde);

            color: white;

            font-weight: bold;

            cursor: pointer;

            transition: .3s;
        }


        .points-button:hover {

            transform:
                scale(1.05);

            background: #20b973;
        }


        /* ==================================================
           INFANTIL
        ================================================== */

        #infantil {

            background: #eef9f4;
        }


        .game-card {

            cursor: pointer;
        }


        /* ==================================================
           IMPACTO
        ================================================== */

        .impact {

            text-align: center;
        }


        .impact-box {

            max-width: 950px;

            margin: auto;

            padding: 50px;

            background: var(--fundo);

            border-radius: 25px;

            border-left:
                6px solid
                var(--verde);

            box-shadow: var(--sombra);
        }


        .impact-box p {

            color: var(--texto);

            font-size: 18px;

            line-height: 1.9;
        }


        /* ==================================================
           CTA
        ================================================== */

        .cta {

            text-align: center;

            color: white;

            background:
                linear-gradient(
                    135deg,
                    var(--verde),
                    #087c50
                );
        }


        .cta h2 {

            font-size:
                clamp(30px, 5vw, 45px);

            margin-bottom: 15px;
        }


        .cta p {

            max-width: 650px;

            margin:
                0 auto 25px;

            line-height: 1.7;
        }


        .cta .button {

            background: white;

            color: var(--azul);
        }


        /* ==================================================
           FOOTER
        ================================================== */

        footer {

            background: #041524;

            color: white;

            text-align: center;

            padding: 45px 20px;
        }


        footer p {

            color: #aebfcd;

            margin-top: 8px;

            font-size: 14px;
        }


        /* ==================================================
           NOTIFICAÇÃO
        ================================================== */

        #notification {

            position: fixed;

            left: 50%;

            bottom: 25px;

            transform:
                translate(-50%, 120px);

            background: var(--verde);

            color: white;

            padding: 14px 22px;

            border-radius: 30px;

            font-weight: bold;

            box-shadow:
                0 10px 30px
                rgba(0,0,0,.2);

            z-index: 3000;

            transition: .4s;
        }


        #notification.show {

            transform:
                translate(-50%, 0);
        }


        /* ==================================================
           TOPO
        ================================================== */

        #top {

            position: fixed;

            right: 20px;

            bottom: 20px;

            width: 48px;

            height: 48px;

            border: none;

            border-radius: 50%;

            background: var(--verde);

            color: white;

            font-size: 20px;

            cursor: pointer;

            display: none;

            z-index: 2000;
        }


        /* ==================================================
           ANIMAÇÕES
        ================================================== */

        .reveal {

            opacity: 0;

            transform:
                translateY(35px);

            transition:
                .8s ease;
        }


        .reveal.active {

            opacity: 1;

            transform:
                translateY(0);
        }


        /* ==================================================
           MOBILE
        ================================================== */

        @media(max-width: 800px) {

            header {

                padding: 0 6%;
            }


            .menu {

                display: block;
            }


            nav {

                position: absolute;

                top: 75px;

                left: 0;

                width: 100%;

                display: none;

                flex-direction: column;

                padding: 25px;

                background: var(--azul);
            }


            nav.active {

                display: flex;
            }


            .stats-grid {

                grid-template-columns:
                    repeat(2, 1fr);
            }


            .steps {

                grid-template-columns:
                    repeat(2, 1fr);
            }
        }


        @media(max-width: 500px) {

            section {

                padding: 70px 6%;
            }


            .hero {

                padding: 60px 6%;
            }


            .buttons {

                flex-direction: column;
            }


            .button {

                width: 100%;
            }


            .steps {

                grid-template-columns: 1fr;
            }


            .impact-box {

                padding: 30px 20px;
            }


            .points-box {

                padding: 30px 20px;
            }

        }

    </style>

</head>


<body>


<!-- ==================================================
     MENU
================================================== -->

<header>

    <div class="logo">

        ♻️ Recicla
        <span>Paraná</span>

    </div>


    <button
        class="menu"
        onclick="abrirMenu()"
        aria-label="Abrir menu">

        ☰

    </button>


    <nav id="nav">

        <a href="#sobre">
            Sobre
        </a>

        <a href="#funciona">
            Como funciona
        </a>

        <a href="#recompensas">
            Recompensas
        </a>

        <a href="#infantil">
            Infantil
        </a>

        <a href="#impacto">
            Impacto
        </a>

    </nav>

</header>


<!-- ==================================================
     HERO
================================================== -->

<section class="hero">

    <div class="hero-content">

        <div class="tag">

            🌱 Tecnologia + Sustentabilidade

        </div>


        <h1>

            Recicla
            <span>Paraná</span>

        </h1>


        <h2>

            Recicle hoje.
            <br>
            Transforme o amanhã.

        </h2>


        <p>

            Uma iniciativa que une tecnologia,
            sustentabilidade e educação ambiental
            para transformar a reciclagem em um
            hábito simples, acessível e divertido.

        </p>


        <div class="buttons">

            <a
                href="#sobre"
                class="button primary">

                Conheça o projeto →

            </a>


            <a
                href="#funciona"
                class="button secondary">

                Como funciona

            </a>

        </div>

    </div>

</section>


<!-- ==================================================
     ESTATÍSTICAS
================================================== -->

<div class="stats">

    <div class="stats-grid">

        <div class="stat">

            <strong
                class="contador"
                data-numero="1250">

                0

            </strong>

            <span>
                Reciclagens
            </span>

        </div>


        <div class="stat">

            <strong
                class="contador"
                data-numero="850">

                0

            </strong>

            <span>
                Usuários
            </span>

        </div>


        <div class="stat">

            <strong
                class="contador"
                data-numero="3200">

                0

            </strong>

            <span>
                Kg reciclados
            </span>

        </div>


        <div class="stat">

            <strong
                class="contador"
                data-numero="95">

                0

            </strong>

            <span>
                Desafios
            </span>

        </div>

    </div>

</div>


<!-- ==================================================
     SOBRE
================================================== -->

<section
    id="sobre"
    class="reveal">

    <div class="section-header">

        <div class="section-tag">
            Nosso propósito
        </div>


        <h2 class="section-title">

            Por que o Recicla Paraná?

        </h2>


        <p class="section-description">

            O projeto utiliza tecnologia para
            incentivar atitudes sustentáveis e
            aproximar as pessoas da reciclagem.

        </p>

    </div>


    <div class="cards">


        <div class="card">

            <div class="icon">
                ♻️
            </div>

            <h3>
                Reciclagem
            </h3>

            <p>

                Incentivamos a separação correta
                e o descarte consciente.

            </p>

        </div>


        <div class="card">

            <div class="icon">
                🌱
            </div>

            <h3>
                Sustentabilidade
            </h3>

            <p>

                Promovemos atitudes que ajudam
                a preservar o meio ambiente.

            </p>

        </div>


        <div class="card">

            <div class="icon">
                📱
            </div>

            <h3>
                Tecnologia
            </h3>

            <p>

                Acompanhe suas ações através
                de uma experiência digital.

            </p>

        </div>


        <div class="card">

            <div class="icon">
                🎁
            </div>

            <h3>
                Recompensas
            </h3>

            <p>

                Acumule pontos participando
                das ações de reciclagem.

            </p>

        </div>

    </div>

</section>


<!-- ==================================================
     COMO FUNCIONA
================================================== -->

<section
    id="funciona"
    class="reveal">

    <div class="section-header">

        <div class="section-tag">
            Passo a passo
        </div>


        <h2 class="section-title">

            Como funciona?

        </h2>


        <p class="section-description">

            Quatro passos simples para
            transformar uma atitude em impacto.

        </p>

    </div>


    <div class="steps">


        <div class="step">

            <div class="number">
                1
            </div>

            <h3>
                Recicle
            </h3>

            <p>
                Separe os materiais recicláveis.
            </p>

        </div>


        <div class="step">

            <div class="number">
                2
            </div>

            <h3>
                Registre
            </h3>

            <p>
                Registre sua ação no projeto.
            </p>

        </div>


        <div class="step">

            <div class="number">
                3
            </div>

            <h3>
                Ganhe pontos
            </h3>

            <p>
                Receba pontos pela participação.
            </p>

        </div>


        <div class="step">

            <div class="number">
                4
            </div>

            <h3>
                Troque
            </h3>

            <p>
                Utilize seus pontos em recompensas.
            </p>

        </div>

    </div>

</section>


<!-- ==================================================
     RECOMPENSAS
================================================== -->

<section
    id="recompensas"
    class="reveal">

    <div class="section-header">

        <div class="section-tag">
            Gamificação
        </div>


        <h2 class="section-title">

            Recicle e conquiste

        </h2>


        <p class="section-description">

            Transforme suas ações sustentáveis
            em pontos e conquistas.

        </p>

    </div>


    <div class="cards">


        <div class="card">

            <div class="icon">
                🎟️
            </div>

            <h3>
                Cupons
            </h3>

            <p>
                Troque pontos por benefícios.
            </p>

        </div>


        <div class="card">

            <div class="icon">
                🏆
            </div>

            <h3>
                Desafios
            </h3>

            <p>
                Complete desafios ambientais.
            </p>

        </div>


        <div class="card">

            <div class="icon">
                ⭐
            </div>

            <h3>
                Ranking
            </h3>

            <p>
                Acompanhe sua evolução.
            </p>

        </div>

    </div>


    <!-- PONTOS -->

    <div class="points-box">

        <h3>
            ♻️ Seu saldo
        </h3>

        <p>
            Registre uma reciclagem para ganhar pontos.
        </p>


        <div
            id="points"
            class="points">

            0

        </div>


        <button
            class="points-button"
            onclick="reciclar()">

            + Registrar reciclagem

        </button>

    </div>

</section>


<!-- ==================================================
     INFANTIL
================================================== -->

<section
    id="infantil"
    class="reveal">

    <div class="section-header">

        <div class="section-tag">
            Diversão
        </div>


        <h2 class="section-title">

            Área Infantil 🎮

        </h2>


        <p class="section-description">

            Aprender sobre sustentabilidade
            também pode ser divertido.

        </p>

    </div>


    <div class="cards">


        <div
            class="card"
            onclick="mensagem('🎮 Jogo da reciclagem em breve!')">

            <div class="icon">
                🎮
            </div>

            <h3>
                Jogos educativos
            </h3>

            <p>
                Aprenda reciclagem brincando.
            </p>

        </div>


        <div
            class="card"
            onclick="mensagem('🌎 Missão ambiental desbloqueada!')">

            <div class="icon">
                🌎
            </div>

            <h3>
                Missões
            </h3>

            <p>
                Complete desafios ambientais.
            </p>

        </div>


        <div
            class="card"
            onclick="mensagem('🪙 Você ganhou uma moeda virtual!')">

            <div class="icon">
                🪙
            </div>

            <h3>
                Moedas
            </h3>

            <p>
                Ganhe moedas participando.
            </p>

        </div>

    </div>

</section>


<!-- ==================================================
     IMPACTO
================================================== -->

<section
    id="impacto"
    class="impact reveal">

    <div class="section-header">

        <div class="section-tag">
            Nosso impacto
        </div>


        <h2 class="section-title">

            Pequenas ações.
            <br>
            Grandes mudanças.

        </h2>

    </div>


    <div class="impact-box">

        <p>

            O Recicla Paraná busca aumentar a
            reciclagem, reduzir a poluição e
            fortalecer a educação ambiental.
            A tecnologia ajuda a acompanhar as
            ações dos usuários e mostrar como
            pequenas atitudes podem gerar
            grandes mudanças.

        </p>

    </div>

</section>


<!-- ==================================================
     CTA
================================================== -->

<section class="cta">

    <h2>
        Faça parte da mudança 🌎
    </h2>


    <p>

        Comece com uma pequena atitude.
        Recicle, participe e incentive
        outras pessoas.

    </p>


    <a
        href="#recompensas"
        class="button">

        Começar agora ♻️

    </a>

</section>


<!-- ==================================================
     FOOTER
================================================== -->

<footer>

    <h2>
        ♻️ Recicla Paraná
    </h2>


    <p>
        Recicle. Participe. Transforme.
    </p>


    <p>
        Projeto de sustentabilidade e tecnologia.
    </p>


    <br>


    <p>
        © 2026 Recicla Paraná
    </p>

</footer>


<!-- ==================================================
     NOTIFICAÇÃO
================================================== -->

<div
    id="notification">

</div>


<!-- ==================================================
     BOTÃO TOPO
================================================== -->

<button
    id="top"
    onclick="topo()"
    aria-label="Voltar ao topo">

    ↑

</button>


<script>


    /* ==============================================
       MENU
    ============================================== */

    function abrirMenu() {

        document
            .getElementById("nav")
            .classList
            .toggle("active");

    }


    document
        .querySelectorAll("nav a")
        .forEach(link => {

            link.addEventListener(
                "click",
                () => {

                    document
                        .getElementById("nav")
                        .classList
                        .remove("active");

                }
            );

        });


    /* ==============================================
       PONTOS
    ============================================== */

    let pontos =
        Number(
            localStorage.getItem(
                "recicla-parana-pontos"
            )
        ) || 0;


    function atualizarPontos() {

        document
            .getElementById("points")
            .textContent =
            pontos.toLocaleString("pt-BR");

    }


    function reciclar() {

        pontos += 10;


        localStorage.setItem(
            "recicla-parana-pontos",
            pontos
        );


        atualizarPontos();


        mensagem(
            "♻️ Reciclagem registrada! +10 pontos"
        );

    }


    atualizarPontos();


    /* ==============================================
       NOTIFICAÇÃO
    ============================================== */

    let tempoNotificacao;


    function mensagem(texto) {

        const box =
            document.getElementById(
                "notification"
            );


        box.textContent = texto;


        box.classList.add("show");


        clearTimeout(
            tempoNotificacao
        );


        tempoNotificacao =
            setTimeout(
                () => {

                    box.classList.remove(
                        "show"
                    );

                },
                2500
            );

    }


    /* ==============================================
       ANIMAÇÃO
    ============================================== */

    const elementos =
        document.querySelectorAll(
            ".reveal"
        );


    function animar() {

        elementos.forEach(
            elemento => {

                const posicao =
                    elemento
                        .getBoundingClientRect()
                        .top;


                if (
                    posicao <
                    window.innerHeight - 100
                ) {

                    elemento
                        .classList
                        .add("active");

                }

            }
        );

    }


    window.addEventListener(
        "scroll",
        animar
    );


    animar();


    /* ==============================================
       CONTADORES
    ============================================== */

    const contadores =
        document.querySelectorAll(
            ".contador"
        );


    let iniciouContadores = false;


    function iniciarContadores() {

        if (
            iniciouContadores
        ) {
            return;
        }


        const stats =
            document
                .querySelector(".stats")
                .getBoundingClientRect()
                .top;


        if (
            stats <
            window.innerHeight - 100
        ) {

            iniciouContadores = true;


            contadores.forEach(
                contador => {

                    const alvo =
                        Number(
                            contador
                                .dataset
                                .numero
                        );


                    let atual = 0;


                    const incremento =
                        Math.max(
                            1,
                            Math.ceil(
                                alvo / 80
                            )
                        );


                    const intervalo =
                        setInterval(
                            () => {

                                atual +=
                                    incremento;


                                if (
                                    atual >=
                                    alvo
                                ) {

                                    atual = alvo;

                                    clearInterval(
                                        intervalo
                                    );

                                }


                                contador.textContent =
                                    atual.toLocaleString(
                                        "pt-BR"
                                    );

                            },
                            25
                        );

                }
            );

        }

    }


    window.addEventListener(
        "scroll",
        iniciarContadores
    );


    iniciarContadores();


    /* ==============================================
       BOTÃO TOPO
    ============================================== */

    const botaoTopo =
        document.getElementById("top");


    window.addEventListener(
        "scroll",
        () => {

            if (
                window.scrollY > 500
            ) {

                botaoTopo.style.display =
                    "block";

            } else {

                botaoTopo.style.display =
                    "none";

            }

        }
    );


    function topo() {

        window.scrollTo({

            top: 0,

            behavior: "smooth"

        });

    }

</script>

</body>

</html>
```
