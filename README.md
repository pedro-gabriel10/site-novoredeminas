<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rede Minas Net - Internet Rápida e Estável de Verdade</title>
    <!-- Google Fonts: Inter -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">
    <!-- Font Awesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary: #0A192F; /* Azul Marinho */
            --primary-light: #112B4A;
            --secondary: #FF6B00; /* Laranja */
            --secondary-hover: #E56000;
            --white: #FFFFFF;
            --light-bg: #F8F9FA;
            --text-dark: #333333;
            --text-light: #E0E0E0;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--light-bg);
            color: var(--text-dark);
            overflow-x: hidden;
        }

        /* Animações de Scroll */
        .hidden {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }
        .show {
            opacity: 1;
            transform: translateY(0);
        }

        /* Tipografia Comum */
        h1, h2, h3 {
            color: var(--primary);
        }
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 1rem;
            font-weight: 800;
        }
        .section-subtitle {
            text-align: center;
            font-size: 1.1rem;
            color: #666;
            margin-bottom: 3rem;
        }
        
        section {
            padding: 80px 20px;
        }

        /* Botões */
        .btn {
            display: inline-block;
            background-color: var(--secondary);
            color: var(--white);
            padding: 16px 32px;
            border-radius: 8px;
            font-size: 1.1rem;
            font-weight: 700;
            text-decoration: none;
            text-align: center;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(255, 107, 0, 0.3);
            border: none;
            cursor: pointer;
        }
        .btn:hover {
            background-color: var(--secondary-hover);
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(255, 107, 0, 0.4);
            color: var(--white);
        }

        /* Header */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background-color: rgba(10, 25, 47, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 15px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        .logo img {
            height: 50px;
            object-fit: contain;
        }
        nav ul {
            list-style: none;
            display: flex;
            gap: 20px;
        }
        nav a {
            color: var(--white);
            text-decoration: none;
            font-weight: 600;
            font-size: 0.95rem;
            transition: color 0.3s;
        }
        nav a:hover {
            color: var(--secondary);
        }

        /* Mobile Menu Toggle */
        .menu-toggle {
            display: none;
            color: var(--white);
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-light) 100%);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 120px 20px 60px;
            position: relative;
            overflow: hidden;
        }
        /* Efeito de grade/tecnologia no fundo */
        .hero::before {
            content: '';
            position: absolute;
            top: 0; left: 0; width: 100%; height: 100%;
            background-image: 
                linear-gradient(rgba(255, 255, 255, 0.03) 1px, transparent 1px),
                linear-gradient(90deg, rgba(255, 255, 255, 0.03) 1px, transparent 1px);
            background-size: 30px 30px;
            pointer-events: none;
        }
        .hero-content {
            max-width: 800px;
            z-index: 1;
        }
        .hero h1 {
            color: var(--white);
            font-size: 3.5rem;
            font-weight: 800;
            line-height: 1.2;
            margin-bottom: 20px;
        }
        .hero p {
            color: var(--text-light);
            font-size: 1.2rem;
            margin-bottom: 10px;
        }
        .hero .gatilhos {
            margin-top: 30px;
            margin-bottom: 40px;
            display: flex;
            flex-direction: column;
            gap: 10px;
            color: var(--white);
            font-weight: 600;
        }
        .hero .gatilhos span i {
            color: var(--secondary);
            margin-right: 8px;
        }

        /* Benefits & Diferenciais */
        .grid-4 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            max-width: 1200px;
            margin: 0 auto;
        }
        .card-icon {
            background: var(--white);
            padding: 40px 20px;
            border-radius: 12px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
            transition: transform 0.3s, box-shadow 0.3s;
            border-bottom: 4px solid transparent;
        }
        .card-icon:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.1);
            border-bottom: 4px solid var(--secondary);
        }
        .card-icon i {
            font-size: 3rem;
            color: var(--secondary);
            margin-bottom: 20px;
        }
        .card-icon h3 {
            font-size: 1.3rem;
            margin-bottom: 15px;
        }

        /* Cobertura */
        .cobertura {
            background-color: var(--primary);
            color: var(--white);
        }
        .cobertura .section-title {
            color: var(--white);
        }
        .cobertura .section-subtitle {
            color: var(--text-light);
        }
        .cidades-grid {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            max-width: 900px;
            margin: 0 auto;
        }
        .cidade-tag {
            background: rgba(255,255,255,0.1);
            padding: 15px 30px;
            border-radius: 50px;
            font-weight: 600;
            font-size: 1.1rem;
            display: flex;
            align-items: center;
            gap: 10px;
            border: 1px solid rgba(255,255,255,0.2);
        }
        .cidade-tag i {
            color: var(--secondary);
        }

        /* Planos */
        .planos-grid {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
            max-width: 1200px;
            margin: 0 auto;
        }
        .plano-card {
            background: var(--white);
            border-radius: 16px;
            padding: 40px 30px;
            text-align: center;
            width: 300px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
            position: relative;
            transition: transform 0.3s;
            display: flex;
            flex-direction: column;
            border: 1px solid #eaeaea;
        }
        .plano-card:hover {
            transform: scale(1.02);
        }
        .plano-destaque {
            border: 2px solid var(--secondary);
            transform: scale(1.05);
            box-shadow: 0 15px 40px rgba(255, 107, 0, 0.15);
        }
        .plano-destaque:hover {
            transform: scale(1.07);
        }
        .badge-destaque {
            position: absolute;
            top: -15px;
            left: 50%;
            transform: translateX(-50%);
            background: var(--secondary);
            color: var(--white);
            padding: 5px 20px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        .plano-mega {
            font-size: 3rem;
            font-weight: 800;
            color: var(--primary);
            margin-bottom: 5px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 5px;
        }
        .plano-mega span {
            font-size: 1.2rem;
            font-weight: 600;
            color: #666;
        }
        .plano-desc {
            color: #555;
            margin: 20px 0;
            font-size: 0.95rem;
            flex-grow: 1;
        }
        .plano-card .btn {
            padding: 12px 20px;
            font-size: 0.95rem;
            width: 100%;
        }

        /* Como Funciona */
        .passos-grid {
            display: flex;
            justify-content: center;
            align-items: flex-start;
            gap: 40px;
            max-width: 1000px;
            margin: 0 auto;
            flex-wrap: wrap;
        }
        .passo {
            text-align: center;
            width: 250px;
            position: relative;
        }
        .passo-numero {
            width: 60px;
            height: 60px;
            background: var(--primary);
            color: var(--white);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            font-weight: 800;
            margin: 0 auto 20px;
            position: relative;
            z-index: 2;
            border: 4px solid var(--white);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        .passo h3 {
            font-size: 1.2rem;
            margin-bottom: 10px;
        }
        .passo p {
            font-size: 0.95rem;
            color: #666;
        }

        /* Prova Social */
        .depoimentos-grid {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            max-width: 1200px;
            margin: 0 auto;
        }
        .depoimento-card {
            background: var(--white);
            padding: 30px;
            border-radius: 12px;
            width: 350px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.05);
            position: relative;
        }
        .depoimento-card i.fa-quote-left {
            color: rgba(255, 107, 0, 0.2);
            font-size: 3rem;
            position: absolute;
            top: 20px;
            left: 20px;
        }
        .depoimento-texto {
            font-style: italic;
            color: #555;
            margin-bottom: 20px;
            position: relative;
            z-index: 1;
            padding-top: 20px;
        }
        .depoimento-autor {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        .autor-avatar {
            width: 50px;
            height: 50px;
            background: var(--primary-light);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-weight: bold;
        }
        .autor-info h4 {
            color: var(--primary);
            font-size: 1rem;
        }
        .autor-info span {
            font-size: 0.85rem;
            color: #888;
        }

        /* Final CTA */
        .final-cta {
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-light) 100%);
            text-align: center;
            color: var(--white);
        }
        .final-cta h2 {
            color: var(--white);
            font-size: 3rem;
            margin-bottom: 20px;
        }
        .final-cta p {
            font-size: 1.2rem;
            color: var(--text-light);
            margin-bottom: 40px;
        }

        /* Footer */
        footer {
            background: #050d18;
            color: var(--text-light);
            padding: 60px 20px 20px;
            text-align: center;
        }
        .footer-logo img {
            height: 60px;
            margin-bottom: 20px;
            filter: brightness(0) invert(1); /* Deixa a logo branca caso seja escura */
        }
        .footer-info {
            margin-bottom: 30px;
        }
        .footer-copy {
            border-top: 1px solid rgba(255,255,255,0.1);
            padding-top: 20px;
            font-size: 0.9rem;
        }

        /* Floating WhatsApp */
        .whatsapp-float {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background-color: #25d366;
            color: white;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 35px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.3);
            z-index: 1000;
            transition: transform 0.3s ease;
            text-decoration: none;
        }
        .whatsapp-float:hover {
            transform: scale(1.1);
            color: white;
        }
        .pulse {
            animation: pulse-animation 2s infinite;
        }
        @keyframes pulse-animation {
            0% { box-shadow: 0 0 0 0 rgba(37, 211, 102, 0.7); }
            70% { box-shadow: 0 0 0 15px rgba(37, 211, 102, 0); }
            100% { box-shadow: 0 0 0 0 rgba(37, 211, 102, 0); }
        }

        /* Responsividade */
        @media (max-width: 992px) {
            .plano-destaque {
                transform: scale(1);
            }
            .plano-destaque:hover {
                transform: scale(1.02);
            }
        }
        
        @media (max-width: 768px) {
            .hero h1 { font-size: 2.5rem; }
            .section-title { font-size: 2rem; }
            nav ul {
                display: none;
                flex-direction: column;
                position: absolute;
                top: 70px;
                left: 0;
                width: 100%;
                background: rgba(10, 25, 47, 0.98);
                padding: 20px;
                text-align: center;
            }
            nav ul.active { display: flex; }
            .menu-toggle { display: block; }
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <div class="logo">
            <!-- A imagem da logo fornecida será carregada aqui -->
            <img src="logosemfundo.png" alt="Rede Minas Net Logo">
        </div>
        <nav>
            <div class="menu-toggle" id="mobile-menu"><i class="fas fa-bars"></i></div>
            <ul id="nav-list">
                <li><a href="#beneficios">Benefícios</a></li>
                <li><a href="#cobertura">Cobertura</a></li>
                <li><a href="#planos">Planos</a></li>
                <li><a href="#como-funciona">Como Funciona</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="inicio">
        <div class="hero-content hidden">
            <h1>Internet rápida e estável de verdade</h1>
            <p>Conexão confiável para sua casa ou empresa, sem dor de cabeça.</p>
            
            <div class="gatilhos">
                <span><i class="fas fa-check-circle"></i> Consulte disponibilidade para sua rua</span>
                <span><i class="fas fa-bolt"></i> Atendimento rápido via WhatsApp</span>
            </div>
            
            <a href="https://wa.me/5535998252502?text=Olá,%20gostaria%20de%20consultar%20a%20disponibilidade%20de%20internet%20para%20minha%20rua!" class="btn" target="_blank">
                <i class="fab fa-whatsapp"></i> Falar no WhatsApp
            </a>
        </div>
    </section>

    <!-- Benefícios -->
    <section id="beneficios" class="light-bg">
        <h2 class="section-title hidden">Por que escolher a Rede Minas Net?</h2>
        <p class="section-subtitle hidden">A tecnologia que você precisa com o respeito que você merece.</p>
        
        <div class="grid-4 hidden">
            <div class="card-icon">
                <i class="fas fa-network-wired"></i>
                <h3>Fibra Óptica</h3>
                <p>Tecnologia de ponta ponta a ponta para garantir a melhor transmissão de dados.</p>
            </div>
            <div class="card-icon">
                <i class="fas fa-tachometer-alt"></i>
                <h3>Alta Velocidade</h3>
                <p>Velocidade real entregue, ideal para streaming, jogos e home office.</p>
            </div>
            <div class="card-icon">
                <i class="fas fa-shield-alt"></i>
                <h3>Estabilidade</h3>
                <p>Conexão contínua sem quedas ou interrupções nos momentos em que você mais precisa.</p>
            </div>
            <div class="card-icon">
                <i class="fas fa-headset"></i>
                <h3>Atendimento Rápido</h3>
                <p>Suporte ágil e humanizado diretamente pelo WhatsApp.</p>
            </div>
        </div>
    </section>

    <!-- Diferenciais -->
    <section id="diferenciais">
        <h2 class="section-title hidden">Nossos Diferenciais</h2>
        <p class="section-subtitle hidden">Muito além de apenas uma conexão de internet.</p>
        
        <div class="grid-4 hidden">
            <div class="card-icon">
                <i class="fas fa-user-friends"></i>
                <h3>Atendimento Humanizado</h3>
                <p>Fale com pessoas reais, não com robôs. Entendemos e resolvemos seu problema.</p>
            </div>
            <div class="card-icon">
                <i class="fas fa-map-marker-alt"></i>
                <h3>Empresa Regional</h3>
                <p>Conhecemos a região e estamos perto de você para qualquer eventualidade.</p>
            </div>
            <div class="card-icon">
                <i class="fas fa-anchor"></i>
                <h3>Foco em Estabilidade</h3>
                <p>Nossa rede é projetada para manter você conectado o tempo todo.</p>
            </div>
            <div class="card-icon">
                <i class="fab fa-whatsapp"></i>
                <h3>Suporte Ágil via WhatsApp</h3>
                <p>Abra chamados, tire dúvidas e resolva pendências direto do seu celular.</p>
            </div>
        </div>
    </section>

    <!-- Cobertura -->
    <section id="cobertura" class="cobertura">
        <h2 class="section-title hidden">Onde Estamos</h2>
        <p class="section-subtitle hidden">Atendendo sua região com qualidade e proximidade.</p>
        
        <div class="cidades-grid hidden">
            <div class="cidade-tag"><i class="fas fa-map-pin"></i> Campo Belo - MG</div>
            <div class="cidade-tag"><i class="fas fa-map-pin"></i> Santana do Jacaré - MG</div>
            <div class="cidade-tag"><i class="fas fa-map-pin"></i> Candeias - MG</div>
            <div class="cidade-tag"><i class="fas fa-tractor"></i> Zonas Rurais</div>
        </div>
    </section>

    <!-- Planos -->
    <section id="planos" class="light-bg">
        <h2 class="section-title hidden">Escolha seu Plano Ideal</h2>
        <p class="section-subtitle hidden">Navegue sem limites com nossa fibra óptica.</p>
        
        <div class="planos-grid hidden">
            
            <!-- Plano 1 -->
            <div class="plano-card">
                <div class="plano-mega">350 <span>MEGA</span></div>
                <p class="plano-desc">Ideal para navegação diária, redes sociais e vídeos em HD.</p>
                <a href="https://wa.me/5535998252502?text=Gostaria%20de%20saber%20a%20disponibilidade%20do%20plano%20de%20350%20MEGA!" class="btn" target="_blank">Consultar disponibilidade</a>
            </div>

            <!-- Plano 2 -->
            <div class="plano-card">
                <div class="plano-mega">450 <span>MEGA</span></div>
                <p class="plano-desc">Perfeito para famílias, streaming 4K e downloads rápidos.</p>
                <a href="https://wa.me/5535998252502?text=Gostaria%20de%20saber%20a%20disponibilidade%20do%20plano%20de%20450%20MEGA!" class="btn" target="_blank">Consultar disponibilidade</a>
            </div>

            <!-- Plano 3 (Destaque) -->
            <div class="plano-card plano-destaque">
                <div class="badge-destaque">Mais Contratado</div>
                <div class="plano-mega">620 <span>MEGA</span></div>
                <p class="plano-desc">Alta performance para home office, jogos online e múltiplos dispositivos.</p>
                <a href="https://wa.me/5535998252502?text=Gostaria%20de%20saber%20a%20disponibilidade%20do%20plano%20de%20620%20MEGA!" class="btn" target="_blank">Consultar disponibilidade</a>
            </div>

            <!-- Plano 4 -->
            <div class="plano-card">
                <div class="plano-mega">750 <span>MEGA</span></div>
                <p class="plano-desc">Velocidade extrema para usuários exigentes e criadores de conteúdo.</p>
                <a href="https://wa.me/5535998252502?text=Gostaria%20de%20saber%20a%20disponibilidade%20do%20plano%20de%20750%20MEGA!" class="btn" target="_blank">Consultar disponibilidade</a>
            </div>

            <!-- Plano 5 -->
            <div class="plano-card">
                <div class="plano-mega">900 <span>MEGA</span></div>
                <p class="plano-desc">A experiência máxima de conectividade. O melhor da fibra óptica.</p>
                <a href="https://wa.me/5535998252502?text=Gostaria%20de%20saber%20a%20disponibilidade%20do%20plano%20de%20900%20MEGA!" class="btn" target="_blank">Consultar disponibilidade</a>
            </div>

        </div>
    </section>

    <!-- Como Funciona -->
    <section id="como-funciona">
        <h2 class="section-title hidden">Como Funciona</h2>
        <p class="section-subtitle hidden">Três passos simples para você ter a melhor internet.</p>
        
        <div class="passos-grid hidden">
            <div class="passo">
                <div class="passo-numero">1</div>
                <h3>Chame no WhatsApp</h3>
                <p>Clique em qualquer botão do site e fale diretamente com nossa equipe.</p>
            </div>
            <div class="passo">
                <div class="passo-numero">2</div>
                <h3>Consulte Disponibilidade</h3>
                <p>Envie seu endereço e verificamos a viabilidade para sua rua na hora.</p>
            </div>
            <div class="passo">
                <div class="passo-numero">3</div>
                <h3>Agende sua Instalação</h3>
                <p>Tudo certo? Agendamos o melhor horário para instalar sua nova internet.</p>
            </div>
        </div>
    </section>

    <!-- Prova Social -->
    <section id="prova-social" class="light-bg">
        <h2 class="section-title hidden">O que dizem nossos clientes</h2>
        <p class="section-subtitle hidden">A satisfação de quem já navega em alta velocidade.</p>
        
        <div class="depoimentos-grid hidden">
            <div class="depoimento-card">
                <i class="fas fa-quote-left"></i>
                <p class="depoimento-texto">"Finalmente achei uma internet que não cai quando chove. O suporte deles pelo WhatsApp é fantástico e resolve na hora!"</p>
                <div class="depoimento-autor">
                    <div class="autor-avatar">M</div>
                    <div class="autor-info">
                        <h4>Marcelo Silva</h4>
                        <span>Campo Belo - MG</span>
                    </div>
                </div>
            </div>
            <div class="depoimento-card">
                <i class="fas fa-quote-left"></i>
                <p class="depoimento-texto">"Trabalho em home office e precisava de estabilidade. O plano de 620 Mega me atende perfeitamente. Super recomendo a Rede Minas Net."</p>
                <div class="depoimento-autor">
                    <div class="autor-avatar">A</div>
                    <div class="autor-info">
                        <h4>Aline Costa</h4>
                        <span>Santana do Jacaré - MG</span>
                    </div>
                </div>
            </div>
            <div class="depoimento-card">
                <i class="fas fa-quote-left"></i>
                <p class="depoimento-texto">"Mesmo morando na zona rural, a conexão chega com ótima qualidade. Instalação rápida e equipe muito educada."</p>
                <div class="depoimento-autor">
                    <div class="autor-avatar">R</div>
                    <div class="autor-info">
                        <h4>Roberto Nunes</h4>
                        <span>Zona Rural</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Final CTA -->
    <section class="final-cta">
        <div class="hidden">
            <h2>Pare de sofrer com internet instável.</h2>
            <p>Consulte disponibilidade para sua rua agora mesmo e faça a mudança que sua casa merece.</p>
            <a href="https://wa.me/5535998252502?text=Olá,%20quero%20parar%20de%20sofrer%20com%20internet%20ruim.%20Podem%20verificar%20a%20disponibilidade%20para%20mim?" class="btn" target="_blank" style="font-size: 1.3rem; padding: 20px 40px;">
                <i class="fab fa-whatsapp"></i> Falar com atendente agora
            </a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-logo">
            <img src="logosemfundo.png" alt="Rede Minas Net Logo">
        </div>
        <div class="footer-info">
            <p>Rede Minas Net - Provedor de Internet Fibra Óptica</p>
            <p>Campo Belo | Santana do Jacaré | Candeias | Zonas Rurais</p>
            <p style="margin-top: 10px;"><i class="fab fa-whatsapp"></i> (35) 99825-2502</p>
        </div>
        <div class="footer-copy">
            <p>&copy; 2026 Rede Minas Net. Todos os direitos reservados.</p>
        </div>
    </footer>

    <!-- Botão Flutuante WhatsApp -->
    <a href="https://wa.me/5535998252502?text=Olá,%20gostaria%20de%20consultar%20a%20disponibilidade%20de%20internet!" class="whatsapp-float pulse" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>

    <!-- Scripts -->
    <script>
        // Menu Mobile Toggle
        const menuToggle = document.getElementById('mobile-menu');
        const navList = document.getElementById('nav-list');
        
        menuToggle.addEventListener('click', () => {
            navList.classList.toggle('active');
        });

        // Fechar menu ao clicar num link
        document.querySelectorAll('#nav-list a').forEach(link => {
            link.addEventListener('click', () => {
                navList.classList.remove('active');
            });
        });

        // Scroll Animation (Intersection Observer)
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if(entry.isIntersecting) {
                    entry.target.classList.add('show');
                }
            });
        }, {
            threshold: 0.1
        });

        const hiddenElements = document.querySelectorAll('.hidden');
        hiddenElements.forEach((el) => observer.observe(el));
    </script>
</body>
</html>
