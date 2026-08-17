<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Recicla Paraná ♻️</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, sans-serif;
            background: #f3f2df;
            color: #205c43;
        }

        /* MENU */
        header {
            background: #155b40;
            color: white;
            padding: 18px 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .logo {
            font-size: 24px;
            font-weight: bold;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin-left: 25px;
            font-weight: bold;
        }

        nav a:hover {
            color: #d9df9d;
        }

        /* CAPA */
        .hero {
            min-height: 90vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 60px 8%;
            background:
                radial-gradient(circle at 90% 20%, #d7df9b 0 80px, transparent 81px),
                #f3f2df;
        }

        .hero-content {
            max-width: 900px;
            text-align: center;
        }

        .hero h1 {
            font-size: clamp(45px, 8vw, 85px);
            font-family: Georgia, serif;
            font-style: italic;
            margin-bottom: 20px;
            color: #155b40;
        }

        .hero h2 {
            font-size: 26px;
            margin-bottom: 20px;
        }

        .hero p {
            max-width: 650px;
            margin: auto;
            font-size: 18px;
            line-height: 1.7;
            color: #386b55;
        }

        .button {
            display: inline-block;
            margin-top: 30px;
            background: #155b40;
            color: white;
            padding: 15px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            transition: 0.3s;
        }

        .button:hover {
            transform: translateY(-3px);
            background: #0d442f;
        }

        /* SEÇÕES */
        section {
            padding: 80px 8%;
        }

        .section-title {
            text-align: center;
            font-family: Georgia, serif;
            font-style: italic;
            font-size: 45px;
            margin-bottom: 20px;
        }

        .section-subtitle {
            text-align: center;
            max-width: 700px;
            margin: 0 auto 45px;
            line-height: 1.7;
            color: #47745f;
        }

        /* CARDS */
        .cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
            gap: 25px;
            max-width: 1100px;
            margin: auto;
        }

        .card {
            background: #fffef1;
            padding: 30px;
            border-radius: 20px;
            text-align: center;
            box-shadow: 0 8px 25px rgba(32, 92, 67, 0.10);
            transition: 0.3s;
        }

        .card:hover {
            transform: translateY(-8px);
        }

        .card .icon {
            font-size: 45px;
            margin-bottom: 15px;
        }

        .card h3 {
            margin-bottom: 12px;
            font-size: 21px;
        }

        .card p {
            line-height: 1.6;
            color: #557563;
        }

        /* COMO FUNCIONA */
        #funciona {
            background: #dfe7c5;
        }

        .steps {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 25px;
            max-width: 1000px;
            margin: auto;
        }

        .step {
            text-align: center;
            padding: 25px;
        }

        .number {
            width: 60px;
            height: 60px;
            margin: auto auto 20px;
            border-radius: 50%;
            background: #155b40;
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            font-weight: bold;
        }

        .step h3 {
            margin-bottom: 10px;
        }

        .step p {
            line-height: 1.5;
            color: #47745f;
        }

        /* RECOMPENSAS */
        .rewards {
            background: #155b40;
            color: white;
        }

        .rewards .section-subtitle {
            color: #dce8d7;
        }

        .reward-card {
            background: #f3f2df;
            color: #205c43;
        }

        /* IMPACTO */
        .impact {
            text-align: center;
        }

        .impact-box {
            max-width: 900px;
            margin: auto;
            background: #fffef1;
            padding: 45px;
            border-radius: 25px;
            box-shadow: 0 8px 25px rgba(32, 92, 67, 0.10);
        }

        .impact-box p {
            font-size: 19px;
            line-height: 1.8;
        }

        /* INFANTIL */
        #infantil {
            background: #e7eacb;
        }

        /* FOOTER */
        footer {
            background: #0d3f2d;
            color: white;
            text-align: center;
            padding: 40px 20px;
        }

        footer h2 {
            margin-bottom: 10px;
        }

        footer p {
            color: #cbdacb;
            margin-top: 8px;
        }

        /* CELULAR */
        @media (max-width: 700px) {

            header {
                flex-direction: column;
                gap: 15px;
            }

            nav a {
                margin: 0 7px;
                font-size: 13px;
            }

            .hero {
                min-height: 80vh;
            }

            .section-title {
                font-size: 36px;
            }

            section {
                padding: 60px 6%;
            }
        }
    </style>
</head>

<body>

<header>
    <div class="logo">♻️ Recicla Paraná</div>

    <nav>
        <a href="#sobre">Sobre</a>
        <a href="#funciona">Como funciona</a>
        <a href="#recompensas">Recompensas</a>
        <a href="#infantil">Infantil</a>
    </nav>
</header>


<!-- CAPA -->

<section class="hero">

    <div class="hero-content">

        <h1>Recicla Paraná</h1>

        <h2>Recicle hoje. Transforme o amanhã. 🌱</h2>

        <p>
            Uma iniciativa que une tecnologia, sustentabilidade
            e recompensas para tornar a reciclagem mais fácil,
            divertida e acessível para todos.
        </p>

        <a href="#sobre" class="button">
            Conheça o projeto
        </a>

    </div>

</section>


<!-- SOBRE -->

<section id="sobre">

    <h2 class="section-title">Por que o Recicla Paraná?</h2>

    <p class="section-subtitle">
        Muitas pessoas ainda descartam materiais recicláveis
        de maneira incorreta e não possuem incentivo suficiente
        para transformar a reciclagem em um hábito.
        O Recicla Paraná nasceu para ajudar a mudar essa realidade.
    </p>

    <div class="cards">

        <div class="card">
            <div class="icon">♻️</div>
            <h3>Reciclagem</h3>
            <p>
                Incentivamos o descarte correto e a separação
                dos materiais recicláveis.
            </p>
        </div>

        <div class="card">
            <div class="icon">🌱</div>
            <h3>Sustentabilidade</h3>
            <p>
                Promovemos atitudes que ajudam a preservar
                o meio ambiente.
            </p>
        </div>

        <div class="card">
            <div class="icon">📱</div>
            <h3>Tecnologia</h3>
            <p>
                Utilizamos um aplicativo para tornar a reciclagem
                mais prática e acessível.
            </p>
        </div>

        <div class="card">
            <div class="icon">🎁</div>
            <h3>Recompensas</h3>
            <p>
                Os usuários acumulam pontos e podem receber
                benefícios por suas ações.
            </p>
        </div>

    </div>

</section>


<!-- COMO FUNCIONA -->

<section id="funciona">

    <h2 class="section-title">Como funciona?</h2>

    <p class="section-subtitle">
        Reciclar pode ser simples. Basta seguir alguns passos.
    </p>

    <div class="steps">

        <div class="step">

            <div class="number">1</div>

            <h3>Recicle</h3>

            <p>
                Separe corretamente os materiais recicláveis.
            </p>

        </div>


        <div class="step">

            <div class="number">2</div>

            <h3>Registre</h3>

            <p>
                Registre sua reciclagem pelo aplicativo.
            </p>

        </div>


        <div class="step">

            <div class="number">3</div>

            <h3>Ganhe pontos</h3>

            <p>
                Após a confirmação, você recebe pontos.
            </p>

        </div>


        <div class="step">

            <div class="number">4</div>

            <h3>Troque</h3>

            <p>
                Troque seus pontos por benefícios e recompensas.
            </p>

        </div>

    </div>

</section>


<!-- RECOMPENSAS -->

<section id="recompensas" class="rewards">

    <h2 class="section-title">Recompensas</h2>

    <p class="section-subtitle">
        Quanto mais você recicla, mais pontos acumula.
        Esses pontos podem ser utilizados para obter benefícios
        oferecidos por parceiros do projeto.
    </p>

    <div class="cards">

        <div class="card reward-card">
            <div class="icon">💡</div>
            <h3>Descontos</h3>
            <p>
                Benefícios em serviços parceiros.
            </p>
        </div>

        <div class="card reward-card">
            <div class="icon">🎟️</div>
            <h3>Cupons</h3>
            <p>
                Pontos podem ser convertidos em cupons.
            </p>
        </div>

        <div class="card reward-card">
            <div class="icon">🏆</div>
            <h3>Desafios</h3>
            <p>
                Participe de desafios e conquiste mais pontos.
            </p>
        </div>

    </div>

</section>


<!-- ÁREA INFANTIL -->

<section id="infantil">

    <h2 class="section-title">Área Infantil 🎮</h2>

    <p class="section-subtitle">
        As crianças também fazem parte dessa transformação!
        O aplicativo possui uma área com jogos e atividades
        educativas para ensinar sustentabilidade de maneira
        divertida e interativa.
    </p>

    <div class="cards">

        <div class="card">
            <div class="icon">🎮</div>
            <h3>Jogos educativos</h3>
            <p>
                Aprenda sobre reciclagem brincando.
            </p>
        </div>

        <div class="card">
            <div class="icon">🌎</div>
            <h3>Missões ambientais</h3>
            <p>
                Complete desafios e ajude o planeta.
            </p>
        </div>

        <div class="card">
            <div class="icon">🪙</div>
            <h3>Moedas virtuais</h3>
            <p>
                Ganhe moedas dentro dos jogos.
            </p>
        </div>

    </div>

</section>


<!-- IMPACTO -->

<section class="impact">

    <h2 class="section-title">Nosso impacto</h2>

    <div class="impact-box">

        <p>
            O Recicla Paraná busca aumentar a reciclagem,
            reduzir a poluição e fortalecer a educação ambiental.
            A tecnologia permite acompanhar as ações dos usuários
            e mostrar como pequenas atitudes podem gerar grandes
            mudanças para o meio ambiente.
        </p>

    </div>

</section>


<!-- RODAPÉ -->

<footer>

    <h2>♻️ Recicla Paraná</h2>

    <p>
        Recicle. Participe. Transforme.
    </p>

    <p>
        Projeto desenvolvido para incentivar
        a sustentabilidade através da tecnologia.
    </p>

    <br>

    <p>
        © 2026 Recicla Paraná
    </p>

</footer>

</body>
</html>