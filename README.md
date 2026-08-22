<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Eternizze Histórias — transforme as flores do seu grande dia em uma lembrança para toda a vida.">
<title>Eternizze Histórias | Buquês Eternizados</title>
<!-- Fontes Oficiais da Identidade Visual -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600;700&family=Parisienne&family=Montserrat:wght@300;400;500;600&display=swap" rel="stylesheet">

<style>
:root {
  /* Paleta Oficial Eternizze História */
  --olive: #999B84;
  --rose-dust: #D7BBBA;
  --rose-light: #EFD9D1;
  --bg-cream: #F4EEED;
  --paper: #FFFFFF;
  --text-dark: #4A4843;
  --text-muted: #736F68;
  --line: #E5DDD9;
}

*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{margin:0;background:var(--bg-cream);color:var(--text-dark);font-family:'Montserrat', sans-serif;line-height:1.6}
a{text-decoration:none;color:inherit}
.container{width:min(1120px,92%);margin:auto}

/* Navegação */
nav{position:sticky;top:0;z-index:20;background:rgba(244,238,237,.95);backdrop-filter:blur(12px);border-bottom:1px solid var(--line)}
.nav-in{height:80px;display:flex;align-items:center;justify-content:space-between}
.logo{font-family:'Cinzel', serif;font-size:24px;letter-spacing:.06em;color:var(--olive);font-weight:700}
.logo span{display:block;font-family:'Parisienne', cursive;font-size:20px;text-transform:lowercase;color:var(--rose-dust);margin-top:-8px;font-weight:normal}
.nav-links{display:flex;gap:28px;font-size:14px;color:var(--text-muted);font-weight:500}
.nav-links a:hover{color:var(--olive)}

/* Hero Section */
.hero{padding:72px 0 90px}
.hero-grid{display:grid;grid-template-columns:1fr 1fr;gap:58px;align-items:center}
.eyebrow{font-family:'Cinzel', serif;font-size:13px;text-transform:uppercase;letter-spacing:.2em;color:var(--olive);font-weight:600}
h1{font-family:'Cinzel', serif;font-weight:400;font-size:clamp(38px,5vw,62px);line-height:1.15;margin:18px 0 22px;color:var(--text-dark)}
h1 em{font-family:'Parisienne', cursive;color:var(--olive);font-style:normal;font-weight:normal;display:inline-block;padding-left:5px}
.lead{font-size:16px;color:var(--text-muted);max-width:540px;font-weight:300}
.btn{display:inline-flex;align-items:center;justify-content:center;padding:14px 28px;border-radius:50px;font-weight:600;font-size:13px;letter-spacing:.05em;text-transform:uppercase;margin:10px 8px 0 0;transition:all .3s ease}
.btn-primary{background:var(--olive);color:white;border:1px solid var(--olive)}
.btn-primary:hover{background:#888A75;border-color:#888A75}
.btn-outline{background:transparent;border:1px solid var(--olive);color:var(--olive)}
.btn-outline:hover{background:var(--rose-light)}

.hero-photo{position:relative}
.hero-photo img{width:100%;height:580px;object-fit:cover;border-radius:12px;box-shadow:0 20px 40px rgba(153,155,132,.18)}
.hero-photo:after{content:"";position:absolute;right:-15px;bottom:-15px;width:120px;height:120px;border:2px solid var(--rose-dust);border-radius:12px;z-index:-1}

/* Seções */
.section{padding:90px 0}
.section.alt{background:var(--paper)}
.section-head{text-align:center;max-width:680px;margin:0 auto 48px}
.section-head h2{font-family:'Cinzel', serif;font-weight:400;font-size:38px;margin:12px 0;color:var(--text-dark)}
.section-head p{color:var(--text-muted);font-weight:300}

/* Cards */
.cards{display:grid;grid-template-columns:repeat(3,1fr);gap:24px}
.card{background:var(--bg-cream);border:1px solid var(--line);padding:36px 28px;border-radius:12px;transition:transform .3s ease}
.card:hover{transform:translateY(-5px)}
.num{font-family:'Cinzel', serif;font-size:32px;color:var(--rose-dust);font-weight:700}
.card h3{font-family:'Cinzel', serif;font-weight:600;font-size:20px;margin:14px 0 10px;color:var(--olive)}
.card p{color:var(--text-muted);font-size:14px;font-weight:300}

/* Galeria */
.gallery{display:grid;grid-template-columns:1fr 1fr;gap:28px}
.gallery figure{margin:0;background:white;border:1px solid var(--line);padding:12px;border-radius:12px;box-shadow:0 10px 30px rgba(0,0,0,.03)}
.gallery img{width:100%;height:520px;object-fit:cover;display:block;border-radius:8px}
.gallery figcaption{padding:16px 8px 6px;font-family:'Parisienne', cursive;font-size:24px;color:var(--olive);text-align:center}

/* Depoimento / Citação */
.quote{max-width:820px;margin:auto;text-align:center}
.quote blockquote{font-family:'Cinzel', serif;font-size:28px;line-height:1.4;margin:0;color:var(--text-dark);font-weight:400}
.quote p{font-family:'Parisienne', cursive;font-size:30px;color:var(--rose-dust);margin-top:18px}

/* CTA */
.cta{background:var(--olive);color:white;padding:85px 0;text-align:center}
.cta h2{font-family:'Cinzel', serif;font-weight:400;font-size:40px;margin:0 0 16px}
.cta p{color:var(--bg-cream);max-width:620px;margin:0 auto 28px;font-weight:300}
.cta .btn-primary{background:var(--rose-dust);border-color:var(--rose-dust);color:white}
.cta .btn-primary:hover{background:#c8abaa;border-color:#c8abaa}

/* Rodapé */
footer{padding:32px 0;color:var(--text-muted);font-size:13px;background:var(--bg-cream);border-top:1px solid var(--line)}
.footer-in{display:flex;justify-content:space-between;gap:20px;flex-wrap:wrap;font-weight:300}

@media(max-width:800px){
 .nav-links{display:none}.hero{padding:48px 0 65px}.hero-grid{grid-template-columns:1fr;gap:35px}
 .hero-photo img{height:420px}.cards,.gallery{grid-template-columns:1fr}.gallery img{height:420px}
 .section{padding:68px 0}.section-head h2{font-size:30px}.quote blockquote{font-size:22px}
}
</style>
</head>
<body>
<nav>
  <div class="container nav-in">
    <a class="logo" href="#">ETERNIZZE<span>história</span></a>
    <div class="nav-links">
      <a href="#como-funciona">Como funciona</a>
      <a href="#galeria">Galeria</a>
      <a href="#sobre">Sobre</a>
      <a href="#contato">Contato</a>
    </div>
  </div>
</nav>

<header class="hero">
  <div class="container hero-grid">
    <div>
      <div class="eyebrow">Flores que viram memória</div>
      <h1>Seu amor merece ser guardado <em>para sempre.</em></h1>
      <p class="lead">Transformamos o seu buquê em uma peça única, delicada e cheia de significado — para você reviver a emoção do grande dia sempre que olhar para ela.</p>
      <div>
        <a class="btn btn-primary" href="#contato">Quero eternizar meu buquê</a>
        <a class="btn btn-outline" href="#galeria">Ver trabalhos</a>
      </div>
    </div>
    <div class="hero-photo">
      <img src="images/buque-01.jpeg" alt="Buquê de flores eternizado em moldura">
    </div>
  </div>
</header>

<section class="section alt" id="como-funciona">
  <div class="container">
    <div class="section-head">
      <div class="eyebrow">Do buquê à lembrança</div>
      <h2>Como funciona</h2>
      <p>Cada peça é preparada com cuidado para preservar a beleza e a história das suas flores.</p>
    </div>
    <div class="cards">
      <article class="card"><div class="num">01</div><h3>Você entrega as flores</h3><p>Recebemos seu buquê e conversamos sobre o estilo e os detalhes que você deseja guardar.</p></article>
      <article class="card"><div class="num">02</div><h3>As flores são eternizadas</h3><p>As flores passam pelo processo de preservação e são cuidadosamente preparadas para a composição.</p></article>
      <article class="card"><div class="num">03</div><h3>Nasce sua história</h3><p>A composição é montada em uma moldura personalizada, criando uma lembrança feita especialmente para você.</p></article>
    </div>
  </div>
</section>

<section class="section" id="galeria">
  <div class="container">
    <div class="section-head">
      <div class="eyebrow">Algumas histórias</div>
      <h2>Trabalhos que falam por si</h2>
      <p>Detalhes, flores, nomes e datas que transformam uma lembrança em algo que pode ser admirado por muitos anos.</p>
    </div>
    <div class="gallery">
      <figure>
        <img src="images/buque-01.jpeg" alt="Moldura Eternizze Histórias com rosas amarelas e flores delicadas">
        <figcaption>Uma composição delicada para guardar uma história especial.</figcaption>
      </figure>
      <figure>
        <img src="images/buque-02.jpeg" alt="Moldura com buquê branco preservado, nomes e data do casamento">
        <figcaption>Buquê, nomes e a data do grande dia reunidos em uma única peça.</figcaption>
      </figure>
    </div>
  </div>
</section>

<section class="section alt" id="sobre">
  <div class="container quote">
    <div class="eyebrow">Eternizze História</div>
    <blockquote>“Algumas flores duram dias. A história que elas representam pode durar para sempre.”</blockquote>
    <p>Uma lembrança feita para voltar no tempo sem precisar dizer uma palavra.</p>
  </div>
</section>

<section class="cta" id="contato">
  <div class="container">
    <div class="eyebrow" style="color:var(--rose-light)">Vamos criar a sua?</div>
    <h2>Seu buquê pode virar uma história para toda a vida.</h2>
    <p>Fale conosco para consultar disponibilidade, valores e as opções de personalização da sua eternização.</p>
    <a class="btn btn-primary" href="https://wa.me/?text=Olá!%20Quero%20saber%20mais%20sobre%20a%20eternização%20do%20meu%20buquê." target="_blank" rel="noopener">Falar pelo WhatsApp</a>
    <a class="btn" style="color:white; border: 1px solid white;" href="https://www.instagram.com/eternizze_historia/" target="_blank" rel="noopener">Instagram @eternizze_historia</a>
  </div>
</section>

<footer>
  <div class="container footer-in">
    <div>© 2026 Eternizze História</div>
    <div>Buquês eternizados • Memórias que permanecem</div>
  </div>
</footer>
</body>
</html>
