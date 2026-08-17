```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Recicla Paraná ♻️</title>

<style>
/* =========================
   RESET
========================= */

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
    background: #ffffff;
    color: #102a43;
    overflow-x: hidden;
}

:root {
    --azul: #082b4c;
    --azul-claro: #0d4778;
    --verde: #19a463;
    --verde-claro: #42c987;
    --branco: #ffffff;
    --cinza: #f4f8fb;
    --texto: #35566d;
    --sombra: 0 15px 40px rgba(8, 43, 76, .10);
}


/* =========================
   HEADER
========================= */

header {
    background: rgba(8, 43, 76, .97);
    backdrop-filter: blur(10px);
    color: white;
    padding: 17px 7%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: sticky;
    top: 0;
    z-index: 1000;
    box-shadow: 0 4px 20px rgba(0,0,0,.12);
}

.logo {
    font-size: 24px;
    font-weight: 800;
    letter-spacing: -.5px;
}

.logo span {
    color: var(--verde-claro);
}

nav {
    display: flex;
    align-items: center;
    gap: 25px;
}

nav a {
    color: white;
    text-decoration: none;
    font-weight: bold;
    font-size: 14px;
    position: relative;
}

nav a::after {
    content: "";
    position: absolute;
    left: 0;
    bottom: -7px;
    width: 0;
    height: 2px;
    background: var(--verde-claro);
    transition: .3s;
}

nav a:hover::after {
    width: 100%;
}

.menu-btn {
    display: none;
    background: none;
    border: none;
    color: white;
    font-size: 28px;
    cursor: pointer;
}


/* =========================
   HERO
========================= */

.hero {
    min-height: 92vh;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 80px 8%;
    position: relative;
    overflow: hidden;
    background:
        radial-gradient(circle at 85% 25%, rgba(25,164,99,.18), transparent 220px),
        radial-gradient(circle at 10% 80%, rgba(13,71,120,.10), transparent 250px),
        #ffffff;
}

.hero::before {
    content: "♻";
    position: absolute;
    right: -40px;
    top: 70px;
    font-size: 300px;
    color: rgba(25,164,99,.055);
    transform: rotate(15deg);
}

.hero-content {
    max-width: 900px;
    text-align: center;
    position: relative;
    z-index: 2;
}

.badge {
    display: inline-block;
    background: #e5f8ef;
    color: var(--verde);
    padding: 9px 18px;
    border-radius: 30px;
    font-weight: bold;
    margin-bottom: 25px;
    animation: aparecer .8s ease;
}

.hero h1 {
    font-size: clamp(48px, 9vw, 90px);
    color: var(--azul);
    font-family: Georgia, serif;
    font-style: italic;
    margin-bottom: 15px;
    animation: subir .8s ease;
}

.hero h1 span {
    color: var(--verde);
}

.hero h2 {
    font-size: clamp(22px, 4vw, 34px);
    margin-bottom: 20px;
    color: var(--azul-claro);
}

.hero p {
    max-width: 700px;
    margin: auto;
    font-size: 18px;
    line-height: 1.8;
    color: var(--texto);
}

.hero-buttons {
    margin-top: 35px;
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
}

.button {
    display: inline-block;
    padding: 15px 30px;
    border-radius: 30px;
    text-decoration: none;
    font-weight: bold;
    transition: .3s;
}

.button-primary {
    background: var(--verde);
    color: white;
    box-shadow: 0 8px 25px rgba(25,164,99,.25);
}

.button-primary:hover {
    transform: translateY(-4px);
    background: #12844f;
}

.button-secondary {
    border: 2px solid var(--azul);
    color: var(--azul);
}

.button-secondary:hover {
    background: var(--azul);
    color: white;
    transform: translateY(-4px);
}


/* =========================
   ESTATÍSTICAS
========================= */

.stats {
    background: var(--azul);
    color: white;
    padding: 45px 8%;
}

.stats-grid {
    max-width: 1100px;
    margin: auto;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 25px;
    text-align: center;
}

.stat strong {
    display: block;
    font-size: 38px;
    color: var(--verde-claro);
    margin-bottom: 8px;
}

.stat span {
    color: #d5e4ef;
}


/* =========================
   SEÇÕES
========================= */

section {
    padding: 90px 8%;
}

.section-title {
    text-align: center;
    color: var(--azul);
    font-family: Georgia, serif;
    font-style: italic;
    font-size: clamp(36px, 5vw, 52px);
    margin-bottom: 18px;
}

.section-subtitle {
    text-align: center;
    max-width: 720px;
    margin: 0 auto 50px;
    line-height: 1.8;
    color: var(--texto);
}


/* =========================
   CARDS
========================= */

.cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 25px;
    max-width: 1150px;
    margin: auto;
}

.card {
    background: white;
    padding: 32px 25px;
    border-radius: 22px;
    text-align: center;
    border: 1px solid #e4edf3;
    box-shadow: var(--sombra);
    transition: .35s;
    position: relative;
    overflow: hidden;
}

.card::before {
    content: "";
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 4px;
    background: linear-gradient(90deg, var(--verde), var(--azul-claro));
}

.card:hover {
    transform: translateY(-10px);
    box-shadow: 0 20px 45px rgba(8,43,76,.16);
}

.icon {
    width: 75px;
    height: 75px;
    margin: 0 auto 20px;
    border-radius: 20px;
    background: #eaf8f1;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 38px;
    transition: .3s;
}

.card:hover .icon {
    transform: scale(1.1) rotate(5deg);
}

.card h3 {
    color: var(--azul);
    margin-bottom: 12px;
    font-size: 21px;
}

.card p {
    color: var(--texto);
    line-height: 1.7;
}


/* =========================
   COMO FUNCIONA
========================= */

#funciona {
    background: var(--cinza);
}

.steps {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    max-width: 1100px;
    margin: auto;
    gap: 20px;
}

.step {
    text-align: center;
    position: relative;
    padding: 20px;
}

.number {
    width: 65px;
    height: 65px;
    margin: auto auto 20px;
    border-radius: 50%;
    background: var(--verde);
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 24px;
    font-weight: bold;
    box-shadow: 0 8px 20px rgba(25,164,99,.25);
}

.step h3 {
    color: var(--azul);
    margin-bottom: 10px;
}

.step p {
    color: var(--texto);
    line-height: 1.6;
}


/* =========================
   RECOMPENSAS
========================= */

.rewards {
    background: var(--azul);
    color: white;
}

.rewards .section-title {
    color: white;
}

.rewards .section-subtitle {
    color: #d5e4ef;
}

.reward-card {
    background: white;
    border: none;
}

.reward-card h3 {
    color: var(--azul);
}


/* =========================
   PONTOS INTERATIVOS
========================= */

.points-area {
    max-width: 850px;
    margin: 55px auto 0;
    padding: 35px;
    background: rgba(255,255,255,.08);
    border: 1px solid rgba(255,255,255,.15);
    border-radius: 25px;
    text-align: center;
}

.points-area h3 {
    font-size: 25px;
    margin-bottom: 15px;
}

.points-number {
    font-size: 55px;
    font-weight: bold;
    color: var(--verde-claro);
    margin: 15px 0;
}

.recycle-btn {
    border: none;
    background: var(--verde);
    color: white;
    padding: 14px 25px;
    border-radius: 30px;
    cursor: pointer;
    font-size: 16px;
    font-weight: bold;
    transition: .3s;
}

.recycle-btn:hover {
    transform: scale(1.05);
    background: #20b973;
}


/* =========================
   INFANTIL
========================= */

#infantil {
    background: #eef9f4;
}

.game-card {
    cursor: pointer;
}

.game-card:hover {
    background: #f8fffc;
}

.game-card .icon {
    background: white;
}


/* =========================
   IMPACTO
========================= */

.impact {
    background: white;
    text-align: center;
}

.impact-box {
    max-width: 950px;
    margin: auto;
    background: var(--cinza);
    padding: 50px;
    border-radius: 28px;
    border-left: 6px solid var(--verde);
    box-shadow: var(--sombra);
}

.impact-box p {
    font-size: 19px;
    line-height: 1.9;
    color: var(--texto);
}


/* =========================
   CTA
========================= */

.cta {
    background: linear-gradient(135deg, var(--verde), #087b50);
    color: white;
    text-align: center;
}

.cta h2 {
    font-size: 42px;
    margin-bottom: 15px;
}

.cta p {
    max-width: 650px;
    margin: 0 auto 25px;
    line-height: 1.7;
}

.cta .button {
    background: white;
    color: var(--azul);
}


/* =========================
   FOOTER
========================= */

footer {
    background: #061d32;
    color: white;
    text-align: center;
    padding: 45px 20px;
}

footer h2 {
    margin-bottom: 10px;
}

footer p {
    color: #b8cad7;
    margin-top: 8px;
}


/* =========================
   BOTÃO TOPO
========================= */

#topButton {
    position: fixed;
    right: 22px;
    bottom: 22px;
    width: 48px;
    height: 48px;
    border-radius: 50%;
    border: none;
    background: var(--verde);
    color: white;
    font-size: 20px;
    cursor: pointer;
    display: none;
    z-index: 999;
    box-shadow: 0 8px 20px rgba(0,0,0,.2);
}


/* =========================
   ANIMAÇÕES
========================= */

.reveal {
    opacity: 0;
    transform: translateY(40px);
    transition: .8s ease;
}

.reveal.active {
    opacity: 1;
    transform: translateY(0);
}

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

@keyframes aparecer {
    from {
        opacity: 0;
        transform: scale(.8);
    }

    to {
        opacity: 1;
        transform: scale(1);
    }
}


/* =========================
   MOBILE
========================= */

@media(max-width: 800px) {

    header {
        padding: 15px 6%;
    }

    .menu-btn {
        display: block;
    }

    nav {
        position: absolute;
        top: 70px;
        left: 0;
        width: 100%;
        background: var(--azul);
        display: none;
        flex-direction: column;
        padding: 25px;
    }

    nav.active {
        display: flex;
    }

    nav a {
        margin: 5px;
    }

    .stats-grid {
        grid-template-columns: repeat(2, 1fr);
    }

    .steps {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media(max-width: 500px) {

    .hero {
        min-height: 85vh;
        padding: 60px 6%;
    }

    section {
        padding: 65px 6%;
    }

    .stats-grid {
        grid-template-columns: 1fr 1fr;
    }

    .steps {
        grid-template-columns: 1fr;
    }

    .impact-box {
        padding: 30px 22px;
    }

    .cta h2 {
        font-size: 32px;
    }
}
</style>
</head>

<body>


<!-- =========================
     MENU
========================= -->

<header>

    <div class="logo">
        ♻️ Recicla <span>Paraná</span>
    </div>

    <button class="menu-btn" onclick="toggleMenu()">☰</button>

    <nav id="menu">
        <a href="#sobre">Sobre</a>
        <a href="#funciona">Como funciona</a>
        <a href="#recompensas">Recompensas</a>
        <a href="#infantil">Infantil</a>
        <a href="#impacto">Impacto</a>
    </nav>

</header>


<!-- =========================
     HERO
========================= -->

<section class="hero">

    <div class="hero-content">

        <div class="badge">
            🌱 Tecnologia + Sustentabilidade
        </div>

        <h1>
            Recicla <span>Paraná</span>
        </h1>

        <h2>
            Recicle hoje. Transforme o amanhã.
        </h2>

        <p>
            Uma plataforma criada para incentivar a reciclagem,
            transformar hábitos e mostrar que pequenas atitudes
            podem gerar grandes mudanças para o nosso planeta.
        </p>

        <div class="hero-buttons">

            <a href="#sobre" class="button button-primary">
                Conheça o projeto
            </a>

            <a href="#funciona" class="button button-secondary">
                Como funciona
            </a>

        </div>

    </div>

</section>


<!-- =========================
     ESTATÍSTICAS
========================= -->

<div class="stats">

    <div class="stats-grid">

        <div class="stat">
            <strong class="counter" data-target="1250">0</strong>
            <span>Reciclagens</span>
        </div>

        <div class="stat">
            <strong class="counter" data-target="850">0</strong>
            <span>Usuários</span>
        </div>

        <div class="stat">
            <strong class="counter" data-target="3200">0</strong>
            <span>Kg reciclados</span>
        </div>

        <div class="stat">
            <strong class="counter" data-target="95">0</strong>
            <span>Desafios concluídos</span>
        </div>

    </div>

</div>


<!-- =========================
     SOBRE
========================= -->

<section id="sobre" class="reveal">

    <h2 class="section-title">
        Por que o Recicla Paraná?
    </h2>

    <p class="section-subtitle">
        O projeto utiliza tecnologia para tornar a reciclagem
        mais simples, divertida e recompensadora.
    </p>

    <div class="cards">

        <div class="card">
            <div class="icon">♻️</div>
            <h3>Reciclagem</h3>
            <p>
                Incentivamos a separação correta dos materiais
                e o descarte consciente.
            </p>
        </div>

        <div class="card">
            <div class="icon">🌱</div>
            <h3>Sustentabilidade</h3>
            <p>
                Criamos hábitos que ajudam a preservar
                o meio ambiente.
            </p>
        </div>

        <div class="card">
            <div class="icon">📱</div>
            <h3>Tecnologia</h3>
            <p>
                O aplicativo facilita o registro das ações
                e acompanha a evolução do usuário.
            </p>
        </div>

        <div class="card">
            <div class="icon">🎁</div>
            <h3>Recompensas</h3>
            <p>
                Cada ação pode gerar pontos e benefícios
                para incentivar a participação.
            </p>
        </div>

    </div>

</section>


<!-- =========================
     FUNCIONAMENTO
========================= -->

<section id="funciona" class="reveal">

    <h2 class="section-title">
        Como funciona?
    </h2>

    <p class="section-subtitle">
        Participar é fácil. Você recicla, registra suas ações
        e acompanha seus pontos.
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
                Informe sua reciclagem pelo aplicativo.
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
                Utilize seus pontos para obter recompensas.
            </p>
        </div>

    </div>

</section>


<!-- =========================
     RECOMPENSAS
========================= -->

<section id="recompensas" class="rewards reveal">

    <h2 class="section-title">
        Recompensas
    </h2>

    <p class="section-subtitle">
        Quanto mais você participa, mais pontos consegue
        acumular.
    </p>

    <div class="cards">

        <div class="card reward-card">
            <div class="icon">💡</div>
            <h3>Descontos</h3>
            <p>
                Benefícios oferecidos por parceiros do projeto.
            </p>
        </div>

        <div class="card reward-card">
            <div class="icon">🎟️</div>
            <h3>Cupons</h3>
            <p>
                Converta seus pontos em cupons especiais.
            </p>
        </div>

        <div class="card reward-card">
            <div class="icon">🏆</div>
            <h3>Desafios</h3>
            <p>
                Complete desafios e ganhe pontos extras.
            </p>
        </div>

    </div>


    <!-- ÁREA INTERATIVA -->

    <div class="points-area">

        <h3>
            🏆 Simulador de pontos
        </h3>

        <p>
            Clique no botão sempre que realizar uma reciclagem.
        </p>

        <div class="points-number" id="points">
            0
        </div>

        <button class="recycle-btn" onclick="addPoints()">
            ♻️ Registrar reciclagem
        </button>

    </div>

</section>


<!-- =========================
     INFANTIL
========================= -->

<section id="infantil" class="reveal">

    <h2 class="section-title">
        Área Infantil 🎮
    </h2>

    <p class="section-subtitle">
        Aprender sobre sustentabilidade também pode ser divertido!
    </p>

    <div class="cards">

        <div class="card game-card"
             onclick="alert('🎮 Em breve: jogo de separação de resíduos!')">

            <div class="icon">🎮</div>

            <h3>
                Jogo da Reciclagem
            </h3>

            <p>
                Separe os resíduos corretamente e acumule pontos.
            </p>

        </div>


        <div class="card game-card"
             onclick="alert('🌎 Missão ambiental iniciada!')">

            <div class="icon">🌎</div>

            <h3>
                Missões ambientais
            </h3>

            <p>
                Complete missões e ajude a cuidar do planeta.
            </p>

        </div>


        <div class="card game-card"
             onclick="alert('🪙 Você ganhou 10 moedas virtuais!')">

            <div class="icon">🪙</div>

            <h3>
                Moedas virtuais
            </h3>

            <p>
                Participe dos jogos e acumule moedas.
            </p>

        </div>

    </div>

</section>


<!-- =========================
     IMPACTO
========================= -->

<section id="impacto" class="impact reveal">

    <h2 class="section-title">
        Nosso impacto
    </h2>

    <div class="impact-box">

        <p>
            O Recicla Paraná busca aumentar a reciclagem,
            reduzir a quantidade de resíduos descartados
            incorretamente e fortalecer a educação ambiental.
            A tecnologia permite acompanhar as ações dos usuários
            e transformar pequenas atitudes em grandes resultados.
        </p>

    </div>

</section>


<!-- =========================
     CTA
========================= -->

<section class="cta">

    <h2>
        Faça parte da mudança 🌎
    </h2>

    <p>
        Cada garrafa, papel, lata ou embalagem reciclada
        representa uma pequena contribuição para um futuro
        mais sustentável.
    </p>

    <a href="#funciona" class="button">
        Começar agora ♻️
    </a>

</section>


<!-- =========================
     FOOTER
========================= -->

<footer>

    <h2>
        ♻️ Recicla Paraná
    </h2>

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


<!-- BOTÃO VOLTAR AO TOPO -->

<button id="topButton" onclick="window.scrollTo(0,0)">
    ↑
</button>


<script>

/* =========================
   MENU MOBILE
========================= */

function toggleMenu() {

    const menu = document.getElementById("menu");

    menu.classList.toggle("active");

}


/* Fecha menu ao clicar */

document.querySelectorAll("nav a").forEach(link => {

    link.addEventListener("click", () => {

        document.getElementById("menu").classList.remove("active");

    });

});


/* =========================
   PONTOS
========================= */

let points = 0;

function addPoints() {

    points += 10;

    document.getElementById("points").textContent = points;

}


/* =========================
   ANIMAÇÃO AO ROLAR
========================= */

const reveals = document.querySelectorAll(".reveal");

function revealOnScroll() {

    reveals.forEach(element => {

        const windowHeight = window.innerHeight;

        const elementTop = element.getBoundingClientRect().top;

        if (elementTop < windowHeight - 100) {

            element.classList.add("active");

        }

    });

}

window.addEventListener("scroll", revealOnScroll);

revealOnScroll();


/* =========================
   CONTADORES
========================= */

const counters = document.querySelectorAll(".counter");

let countersStarted = false;

function startCounters() {

    if (countersStarted) return;

    const stats = document.querySelector(".stats");

    const position = stats.getBoundingClientRect().top;

    if (position < window.innerHeight - 100) {

        countersStarted = true;

        counters.forEach(counter => {

            const target = Number(counter.dataset.target);

            let current = 0;

            const increment = Math.ceil(target / 80);

            const timer = setInterval(() => {

                current += increment;

                if (current >= target) {

                    current = target;

                    clearInterval(timer);

                }

                counter.textContent = current.toLocaleString("pt-BR");

            }, 25);

        });

    }

}

window.addEventListener("scroll", startCounters);


/* =========================
   BOTÃO TOPO
========================= */

const topButton = document.getElementById("topButton");

window.addEventListener("scroll", () => {

    if (window.scrollY > 500) {

        topButton.style.display = "block";

    } else {

        topButton.style.display = "none";

    }

});

</script>

</body>
</html>
```
