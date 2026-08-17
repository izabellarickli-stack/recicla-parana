<!DOCTYPE html>
<html lang="pt-BR">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <meta name="description"
        content="Recicla Paraná - Tecnologia, sustentabilidade e educação ambiental.">

    <title>♻️ Recicla Paraná</title>

    <style>

        /* =====================================================
           CORES
        ===================================================== */

        :root {
            --verde: #15945f;
            --verde-claro: #dff5e9;
            --verde-hover: #10794d;

            --azul: #062b49;
            --azul-claro: #0c4168;

            --branco: #ffffff;
            --fundo: #f5faf8;

            --texto: #183b33;
            --cinza: #61746e;

            --sombra: 0 10px 35px rgba(6, 43, 73, .10);

            --raio: 22px;
        }


        /* =====================================================
           RESET
        ===================================================== */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: var(--fundo);
            color: var(--texto);

            transition: .3s;
        }

        a {
            text-decoration: none;
        }

        button {
            font-family: inherit;
        }


        /* =====================================================
           BARRA DE NAVEGAÇÃO
        ===================================================== */

        header {
            position: fixed;
            top: 0;
            left: 0;

            width: 100%;

            z-index: 1000;

            background: rgba(6, 43, 73, .95);

            backdrop-filter: blur(12px);

            box-shadow: 0 4px 25px rgba(0, 0, 0, .15);
        }

        .navbar {
            max-width: 1200px;

            margin: auto;

            padding: 16px 25px;

            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            color: white;

            font-size: 22px;

            font-weight: bold;

            display: flex;
            align-items: center;

            gap: 8px;
        }

        .logo span {
            color: #62dca6;
        }

        nav {
            display: flex;

            align-items: center;

            gap: 25px;
        }

        nav a {
            color: white;

            font-size: 14px;

            font-weight: bold;

            transition: .3s;
        }

        nav a:hover {
            color: #62dca6;
        }

        .menu-btn {
            display: none;

            background: none;

            border: none;

            color: white;

            font-size: 27px;

            cursor: pointer;
        }


        /* =====================================================
           BOTÕES
        ===================================================== */

        .btn {
            border: none;

            cursor: pointer;

            display: inline-flex;

            justify-content: center;
            align-items: center;

            gap: 8px;

            padding: 14px 25px;

            border-radius: 50px;

            background: var(--verde);

            color: white;

            font-weight: bold;

            transition: .3s;
        }

        .btn:hover {
            background: var(--verde-hover);

            transform: translateY(-3px);

            box-shadow: 0 10px 25px rgba(21, 148, 95, .3);
        }

        .btn-azul {
            background: var(--azul);
        }

        .btn-azul:hover {
            background: var(--azul-claro);
        }


        /* =====================================================
           HERO
        ===================================================== */

        .hero {
            min-height: 100vh;

            padding: 150px 7% 80px;

            display: flex;

            align-items: center;

            justify-content: center;

            text-align: center;

            background:
                radial-gradient(circle at 10% 20%,
                    rgba(21, 148, 95, .18),
                    transparent 25%),

                radial-gradient(circle at 90% 70%,
                    rgba(6, 43, 73, .15),
                    transparent 25%),

                white;

            overflow: hidden;
        }

        .hero-content {
            max-width: 900px;

            animation: subir 1s ease;
        }

        .selo {
            display: inline-block;

            padding: 9px 18px;

            border-radius: 30px;

            background: var(--verde-claro);

            color: var(--verde);

            font-size: 14px;

            font-weight: bold;

            margin-bottom: 20px;
        }

        .hero h1 {
            color: var(--azul);

            font-family: Georgia, serif;

            font-style: italic;

            font-size: clamp(48px, 10vw, 90px);

            line-height: 1;
        }

        .hero h1 span {
            color: var(--verde);
        }

        .hero h2 {
            margin: 25px 0 15px;

            color: var(--azul);

            font-size: clamp(20px, 3vw, 28px);
        }

        .hero p {
            max-width: 700px;

            margin: auto;

            color: var(--cinza);

            line-height: 1.8;

            font-size: 17px;
        }

        .hero-buttons {
            margin-top: 30px;

            display: flex;

            justify-content: center;

            gap: 15px;

            flex-wrap: wrap;
        }

        .folhas {
            font-size: 55px;

            margin-top: 40px;

            animation: flutuar 3s ease-in-out infinite;
        }


        /* =====================================================
           SEÇÕES
        ===================================================== */

        section {
            padding: 90px 7%;
        }

        .titulo {
            text-align: center;

            color: var(--azul);

            font-family: Georgia, serif;

            font-style: italic;

            font-size: clamp(35px, 5vw, 50px);

            margin-bottom: 15px;
        }

        .titulo span {
            color: var(--verde);
        }

        .subtitulo {
            max-width: 720px;

            margin: 0 auto 50px;

            text-align: center;

            color: var(--cinza);

            line-height: 1.7;
        }


        /* =====================================================
           CARDS
        ===================================================== */

        .cards {
            max-width: 1150px;

            margin: auto;

            display: grid;

            grid-template-columns:
                repeat(auto-fit, minmax(220px, 1fr));

            gap: 25px;
        }

        .card {
            background: white;

            padding: 32px;

            border-radius: var(--raio);

            box-shadow: var(--sombra);

            transition: .35s;

            border: 1px solid rgba(21, 148, 95, .08);
        }

        .card:hover {
            transform: translateY(-9px);

            box-shadow:
                0 18px 45px rgba(6, 43, 73, .15);
        }

        .icone {
            width: 65px;
            height: 65px;

            display: flex;

            align-items: center;
            justify-content: center;

            border-radius: 18px;

            background: var(--verde-claro);

            font-size: 34px;

            margin-bottom: 20px;
        }

        .card h3 {
            color: var(--azul);

            margin-bottom: 12px;
        }

        .card p {
            color: var(--cinza);

            line-height: 1.6;
        }


        /* =====================================================
           COMO FUNCIONA
        ===================================================== */

        #funciona {
            background: var(--verde-claro);
        }

        .passos {
            max-width: 1000px;

            margin: auto;

            display: grid;

            grid-template-columns:
                repeat(auto-fit, minmax(190px, 1fr));

            gap: 25px;
        }

        .passo {
            background: white;

            padding: 30px;

            text-align: center;

            border-radius: var(--raio);

            box-shadow: var(--sombra);
        }

        .numero {
            width: 55px;
            height: 55px;

            margin: 0 auto 20px;

            display: flex;

            justify-content: center;
            align-items: center;

            background: var(--azul);

            color: white;

            border-radius: 50%;

            font-weight: bold;

            font-size: 20px;
        }


        /* =====================================================
           ÁREA DE PONTOS
        ===================================================== */

        #pontos {
            background: var(--azul);
        }

        #pontos .titulo {
            color: white;
        }

        #pontos .subtitulo {
            color: #c9d8df;
        }

        .painel {
            max-width: 650px;

            margin: auto;

            padding: 40px;

            background: white;

            border-radius: 28px;

            text-align: center;

            box-shadow:
                0 20px 60px rgba(0, 0, 0, .25);
        }

        .nivel {
            display: inline-block;

            padding: 7px 15px;

            background: var(--verde-claro);

            color: var(--verde);

            border-radius: 30px;

            font-size: 13px;

            font-weight: bold;
        }

        .pontos {
            color: var(--verde);

            font-size: 65px;

            font-weight: bold;

            margin: 12px;
        }

        .barra {
            width: 100%;

            height: 18px;

            background: #e4ece9;

            border-radius: 30px;

            overflow: hidden;

            margin: 20px 0;
        }

        .progresso {
            width: 0%;

            height: 100%;

            background:
                linear-gradient(
                    90deg,
                    #15945f,
                    #63dca3
                );

            transition: 1s;
        }

        .estatisticas {
            display: grid;

            grid-template-columns:
                repeat(3, 1fr);

            gap: 15px;

            margin-top: 30px;
        }

        .estatistica {
            padding: 18px;

            border-radius: 15px;

            background: #f3f8f6;
        }

        .estatistica strong {
            display: block;

            color: var(--azul);

            font-size: 25px;

            margin-bottom: 5px;
        }

        .estatistica small {
            color: var(--cinza);
        }


        /* =====================================================
           IMPACTO
        ===================================================== */

        .impacto {
            max-width: 1000px;

            margin: auto;

            display: grid;

            grid-template-columns:
                repeat(auto-fit, minmax(220px, 1fr));

            gap: 25px;
        }

        .impacto-box {
            background: white;

            padding: 35px;

            text-align: center;

            border-radius: var(--raio);

            box-shadow: var(--sombra);
        }

        .impacto-box strong {
            display: block;

            color: var(--verde);

            font-size: 45px;

            margin-bottom: 8px;
        }

        .impacto-box p {
            color: var(--cinza);
        }


        /* =====================================================
           QUIZ
        ===================================================== */

        #quiz {
            background: #eef7f3;
        }

        .quiz {
            max-width: 700px;

            margin: auto;

            background: white;

            padding: 35px;

            border-radius: 25px;

            box-shadow: var(--sombra);
        }

        .quiz h3 {
            color: var(--azul);

            margin-bottom: 25px;

            line-height: 1.5;
        }

        .resposta {
            width: 100%;

            padding: 15px;

            margin: 7px 0;

            background: white;

            border: 2px solid #dce8e4;

            border-radius: 13px;

            text-align: left;

            cursor: pointer;

            transition: .3s;
        }

        .resposta:hover {
            border-color: var(--verde);

            background: var(--verde-claro);
        }

        #resultado {
            text-align: center;

            margin-top: 20px;

            font-weight: bold;
        }


        /* =====================================================
           PONTOS DE COLETA
        ===================================================== */

        .localizacao {
            max-width: 900px;

            margin: auto;

            padding: 45px;

            border-radius: 25px;

            background:
                linear-gradient(
                    135deg,
                    var(--azul),
                    var(--azul-claro)
                );

            color: white;

            text-align: center;

            box-shadow: var(--sombra);
        }

        .localizacao h3 {
            font-size: 30px;

            margin-bottom: 15px;
        }

        .localizacao p {
            color: #d4e2e8;

            line-height: 1.7;

            margin-bottom: 25px;
        }


        /* =====================================================
           FOOTER
        ===================================================== */

        footer {
            background: #031c2d;

            color: white;

            padding: 50px 20px;

            text-align: center;
        }

        footer h2 {
            margin-bottom: 10px;
        }

        footer p {
            color: #b9cbc8;

            margin-top: 8px;
        }


        /* =====================================================
           NOTIFICAÇÃO
        ===================================================== */

        .notificacao {
            position: fixed;

            bottom: 25px;
            right: 25px;

            z-index: 2000;

            padding: 17px 23px;

            background: var(--azul);

            color: white;

            border-radius: 15px;

            box-shadow: 0 10px 35px rgba(0, 0, 0, .25);

            transform: translateY(150px);

            transition: .5s;
        }

        .notificacao.mostrar {
            transform: translateY(0);
        }


        /* =====================================================
           ANIMAÇÕES
        ===================================================== */

        @keyframes subir {

            from {
                opacity: 0;

                transform: translateY(30px);
            }

            to {
                opacity: 1;

                transform: translateY(0);
            }

        }

        @keyframes flutuar {

            0%, 100% {
                transform: translateY(0);
            }

            50% {
                transform: translateY(-10px);
            }

        }


        /* =====================================================
           CELULAR
        ===================================================== */

        @media(max-width: 750px) {

            .menu-btn {
                display: block;
            }

            nav {
                display: none;

                position: absolute;

                top: 70px;
                left: 0;

                width: 100%;

                padding: 25px;

                background: var(--azul);

                flex-direction: column;

                text-align: center;
            }

            nav.ativo {
                display: flex;
            }

            .navbar {
                padding: 15px 20px;
            }

            .hero {
                padding-left: 6%;
                padding-right: 6%;
            }

            section {
                padding: 70px 6%;
            }

            .estatisticas {
                grid-template-columns: 1fr;
            }

            .painel {
                padding: 28px 20px;
            }

            .hero-buttons .btn {
                width: 100%;
            }

        }

    </style>
</head>


<body>


<!-- =====================================================
     MENU
===================================================== -->

<header>

    <div class="navbar">

        <a href="#" class="logo">
            ♻️ Recicla <span>Paraná</span>
        </a>

        <button
            class="menu-btn"
            onclick="abrirMenu()">

            ☰

        </button>

        <nav id="menu">

            <a href="#sobre">Sobre</a>

            <a href="#funciona">Como funciona</a>

            <a href="#pontos">Meu impacto</a>

            <a href="#coleta">Coleta</a>

            <a href="#quiz">Quiz</a>

        </nav>

    </div>

</header>


<!-- =====================================================
     HERO
===================================================== -->

<section class="hero">

    <div class="hero-content">

        <div class="selo">
            🌱 Projeto sustentável
        </div>

        <h1>
            Recicla <span>Paraná</span>
        </h1>

        <h2>
            ♻️ Recicle hoje. Transforme o amanhã.
        </h2>

        <p>
            Uma plataforma que utiliza a tecnologia para
            incentivar a reciclagem, promover a educação
            ambiental e transformar boas atitudes em
            benefícios.
        </p>

        <div class="hero-buttons">

            <a
                href="#funciona"
                class="btn">

                🚀 Conhecer o projeto

            </a>

            <a
                href="#pontos"
                class="btn btn-azul">

                ⭐ Ver meus pontos

            </a>

        </div>

        <div class="folhas">
            🌿 ♻️ 🌿
        </div>

    </div>

</section>


<!-- =====================================================
     SOBRE
===================================================== -->

<section id="sobre">

    <h2 class="titulo">
        Por que <span>Recicla Paraná?</span>
    </h2>

    <p class="subtitulo">

        O descarte incorreto de resíduos ainda faz parte
        do dia a dia de muitas pessoas. O projeto busca
        tornar a reciclagem mais simples, acessível e
        motivadora.

    </p>


    <div class="cards">


        <div class="card">

            <div class="icone">
                ♻️
            </div>

            <h3>
                Reciclagem
            </h3>

            <p>
                Incentivamos a separação e o descarte
                correto dos materiais recicláveis.
            </p>

        </div>


        <div class="card">

            <div class="icone">
                📱
            </div>

            <h3>
                Tecnologia
            </h3>

            <p>
                Utilizamos um aplicativo para registrar
                e acompanhar as ações sustentáveis.
            </p>

        </div>


        <div class="card">

            <div class="icone">
                🏆
            </div>

            <h3>
                Recompensas
            </h3>

            <p>
                As pessoas acumulam pontos através
                de suas atitudes sustentáveis.
            </p>

        </div>


        <div class="card">

            <div class="icone">
                🌎
            </div>

            <h3>
                Impacto ambiental
            </h3>

            <p>
                Acompanhe como pequenas atitudes podem
                contribuir para um ambiente melhor.
            </p>

        </div>

    </div>

</section>


<!-- =====================================================
     COMO FUNCIONA
===================================================== -->

<section id="funciona">

    <h2 class="titulo">
        Como <span>funciona?</span>
    </h2>

    <p class="subtitulo">

        O processo foi pensado para ser simples,
        rápido e fácil de entender.

    </p>


    <div class="passos">


        <div class="passo">

            <div class="numero">
                1
            </div>

            <h3>
                ♻️ Recicle
            </h3>

            <p>
                Separe corretamente seus materiais.
            </p>

        </div>


        <div class="passo">

            <div class="numero">
                2
            </div>

            <h3>
                📸 Registre
            </h3>

            <p>
                Registre a reciclagem no aplicativo.
            </p>

        </div>


        <div class="passo">

            <div class="numero">
                3
            </div>

            <h3>
                ⭐ Ganhe pontos
            </h3>

            <p>
                Cada ação gera pontos.
            </p>

        </div>


        <div class="passo">

            <div class="numero">
                4
            </div>

            <h3>
                🎁 Troque
            </h3>

            <p>
                Utilize seus pontos em benefícios.
            </p>

        </div>

    </div>

</section>


<!-- =====================================================
     MEU IMPACTO
===================================================== -->

<section id="pontos">

    <h2 class="titulo">
        Meu <span>impacto</span> 🌱
    </h2>

    <p class="subtitulo">

        Registre suas reciclagens e veja sua evolução.

    </p>


    <div class="painel">

        <div
            class="nivel"
            id="nivel">

            🌱 Nível 1 — Iniciante

        </div>


        <div
            class="pontos"
            id="pontos">

            0

        </div>

        <p>
            pontos acumulados
        </p>


        <div class="barra">

            <div
                class="progresso"
                id="progresso">

            </div>

        </div>


        <p id="mensagem">
            Comece sua jornada sustentável!
        </p>


        <br>


        <button
            class="btn"
            onclick="registrarReciclagem()">

            ♻️ Registrar reciclagem

        </button>


        <div class="estatisticas">


            <div class="estatistica">

                <strong id="reciclagens">
                    0
                </strong>

                <small>
                    Reciclagens
                </small>

            </div>


            <div class="estatistica">

                <strong id="acoes">
                    0
                </strong>

                <small>
                    Ações
                </small>

            </div>


            <div class="estatistica">

                <strong id="nivelNumero">
                    1
                </strong>

                <small>
                    Nível
                </small>

            </div>


        </div>

    </div>

</section>


<!-- =====================================================
     IMPACTO DO PROJETO
===================================================== -->

<section>

    <h2 class="titulo">
        Impacto do <span>projeto</span>
    </h2>

    <p class="subtitulo">

        Nosso objetivo é transformar pequenas ações
        em grandes resultados.

    </p>


    <div class="impacto">


        <div class="impacto-box">

            <strong>
                ♻️
            </strong>

            <p>
                Aumentar a reciclagem
            </p>

        </div>


        <div class="impacto-box">

            <strong>
                🌱
            </strong>

            <p>
                Incentivar a educação ambiental
            </p>

        </div>


        <div class="impacto-box">

            <strong>
                📱
            </strong>

            <p>
                Usar tecnologia para gerar impacto
            </p>

        </div>


        <div class="impacto-box">

            <strong>
                🤝
            </strong>

            <p>
                Envolver a comunidade
            </p>

        </div>

    </div>

</section>


<!-- =====================================================
     PONTOS DE COLETA
===================================================== -->

<section id="coleta">

    <h2 class="titulo">
        Pontos de <span>coleta</span> 📍
    </h2>

    <p class="subtitulo">

        Encontre locais adequados para entregar
        seus materiais recicláveis.

    </p>


    <div class="localizacao">

        <h3>
            📍 Encontre um ponto próximo
        </h3>

        <p>

            No aplicativo, o usuário poderá visualizar
            pontos de coleta disponíveis e encontrar o
            local mais próximo para realizar o descarte.

        </p>

        <button
            class="btn"
            onclick="mostrarAviso()">

            🔎 Procurar ponto de coleta

        </button>

    </div>

</section>


<!-- =====================================================
     QUIZ
===================================================== -->

<section id="quiz">

    <h2 class="titulo">
        Quiz da <span>Reciclagem</span> 🧠
    </h2>

    <p class="subtitulo">

        Teste seus conhecimentos sobre sustentabilidade!

    </p>


    <div class="quiz">

        <h3>
            Qual desses materiais é reciclável?
        </h3>


        <button
            class="resposta"
            onclick="responder(false)">

            🍌 Restos de comida

        </button>


        <button
            class="resposta"
            onclick="responder(true)">

            🥤 Garrafa PET

        </button>


        <button
            class="resposta"
            onclick="responder(false)">

            🧻 Papel higiênico usado

        </button>


        <button
            class="resposta"
            onclick="responder(false)">

            🗑️ Resíduo contaminado

        </button>


        <div id="resultado"></div>

    </div>

</section>


<!-- =====================================================
     RODAPÉ
===================================================== -->

<footer>

    <h2>
        ♻️ Recicla Paraná
    </h2>

    <p>
        Recicle. Participe. Transforme.
    </p>

    <p>
        Tecnologia a favor de um futuro sustentável.
    </p>

    <br>

    <p>
        © 2026 Recicla Paraná
    </p>

</footer>


<!-- NOTIFICAÇÃO -->

<div
    class="notificacao"
    id="notificacao">

    ♻️ Ação registrada! +10 pontos!

</div>


<!-- =====================================================
     JAVASCRIPT
===================================================== -->

<script>

    /* =====================================================
       MENU MOBILE
    ===================================================== */

    function abrirMenu() {

        const menu =
            document.getElementById("menu");

        menu.classList.toggle("ativo");

    }


    /* =====================================================
       SISTEMA DE PONTOS
    ===================================================== */

    let pontos =
        Number(localStorage.getItem("pontos")) || 0;

    let reciclagens =
        Number(localStorage.getItem("reciclagens")) || 0;


    function atualizarPainel() {

        document.getElementById("pontos")
            .innerText = pontos;


        document.getElementById("reciclagens")
            .innerText = reciclagens;


        document.getElementById("acoes")
            .innerText = reciclagens;


        /* NÍVEIS */

        let nivel = 1;

        if (pontos >= 100) nivel = 2;

        if (pontos >= 250) nivel = 3;

        if (pontos >= 500) nivel = 4;

        if (pontos >= 1000) nivel = 5;


        document.getElementById("nivelNumero")
            .innerText = nivel;


        const nomes = {

            1: "🌱 Nível 1 — Iniciante",

            2: "🌿 Nível 2 — Protetor",

            3: "🌳 Nível 3 — Guardião",

            4: "🌎 Nível 4 — Defensor",

            5: "🏆 Nível 5 — Embaixador"

        };


        document.getElementById("nivel")
            .innerText = nomes[nivel];


        /* BARRA */

        let progresso =
            (pontos % 100);

        if (pontos > 0 && progresso === 0) {
            progresso = 100;
        }


        document.getElementById("progresso")
            .style.width =
            progresso + "%";


        /* MENSAGEM */

        if (pontos === 0) {

            document.getElementById("mensagem")
                .innerText =
                "Comece sua jornada sustentável!";

        }

        else if (pontos < 100) {

            document.getElementById("mensagem")
                .innerText =
                "Você está começando muito bem! 🌱";

        }

        else if (pontos < 500) {

            document.getElementById("mensagem")
                .innerText =
                "Continue assim! Você está fazendo a diferença. 🌿";

        }

        else {

            document.getElementById("mensagem")
                .innerText =
                "Você é um verdadeiro defensor do meio ambiente! 🌎";

        }

    }


    function registrarReciclagem() {

        pontos += 10;

        reciclagens++;


        localStorage.setItem(
            "pontos",
            pontos
        );


        localStorage.setItem(
            "reciclagens",
            reciclagens
        );


        atualizarPainel();

        mostrarNotificacao();

    }


    /* =====================================================
       NOTIFICAÇÃO
    ===================================================== */

    function mostrarNotificacao() {

        const notificacao =
            document.getElementById("notificacao");

        notificacao.classList.add("mostrar");


        setTimeout(() => {

            notificacao.classList.remove("mostrar");

        }, 2500);

    }


    function mostrarAviso() {

        alert(
            "📍 Essa função poderá mostrar os pontos de coleta próximos ao usuário."
        );

    }


    /* =====================================================
       QUIZ
    ===================================================== */

    function responder(correta) {

        const resultado =
            document.getElementById("resultado");


        if (correta) {

            resultado.innerHTML =
                "🎉 Parabéns! Você acertou!";

            resultado.style.color =
                "#15945f";

        }

        else {

            resultado.innerHTML =
                "💡 Quase! Tente novamente.";

            resultado.style.color =
                "#c43b3b";

        }

    }


    /* =====================================================
       INICIAR
    ===================================================== */

    atualizarPainel();

</script>

</body>

</html>