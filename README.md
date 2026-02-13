<!DOCTYPE html>
<html lang="pt-pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Proposta Estratégica | ANGOSEGUROS & Lunara Florence</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;800&family=Inter:wght@300;400;500&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <style>
        :root {
            --bg-black: #010409;
            --deep-blue: #000b1a;
            --brilliant-blue: #0066ff;
            --electric-blue: #00d4ff;
            --silver-bright: linear-gradient(135deg, #cfd9df 0%, #e2ebf0 50%, #a1abb3 100%);
            --silver-static: #c0c0c0;
            --text-silver: #94a3b8;
            --pure-white: #ffffff;
            --glass-border: rgba(0, 102, 255, 0.2);
            --glow: 0 0 25px rgba(0, 102, 255, 0.4);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        html { scroll-behavior: smooth; }

        body {
            background-color: var(--bg-black);
            color: var(--text-silver);
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            overflow-x: hidden;
        }

        h1, h2, h3, h4 { 
            font-family: 'Montserrat', sans-serif; 
            text-transform: uppercase; 
            letter-spacing: 2px; 
            color: var(--pure-white);
        }

        .silver-text {
            background: var(--silver-bright);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 800;
        }

        /* 1. INTRO SPLASH SCREEN */
        #splash {
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: var(--bg-black);
            z-index: 1000;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            flex-direction: column;
            animation: fadeOut 1.5s ease 4s forwards;
        }

        @keyframes fadeOut {
            to { opacity: 0; visibility: hidden; }
        }

        .splash-phrase {
            font-size: clamp(1rem, 4vw, 1.8rem);
            font-weight: 300;
            letter-spacing: 8px;
            color: var(--pure-white);
            padding: 0 20px;
        }

        .splash-phrase span {
            display: block;
            margin-top: 10px;
            color: var(--brilliant-blue);
            text-shadow: var(--glow);
            font-weight: 700;
        }

        /* 2. HERO SECTION */
        header {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 80px 20px;
            text-align: center;
            background: radial-gradient(circle at center, var(--deep-blue) 0%, var(--bg-black) 100%);
        }

        .hero-content h1 { 
            font-size: clamp(2rem, 8vw, 4.5rem); 
            font-weight: 800; 
            line-height: 1.1;
            margin-bottom: 25px;
        }

        .hero-content p { 
            font-size: clamp(1rem, 2.5vw, 1.25rem); 
            max-width: 800px; 
            margin: 0 auto 45px;
            color: var(--text-silver);
        }

        /* 3. BOTÕES */
        .btn-group { display: flex; gap: 20px; justify-content: center; flex-wrap: wrap; }

        .btn {
            padding: 18px 40px;
            text-decoration: none;
            font-weight: 700;
            letter-spacing: 2px;
            text-transform: uppercase;
            font-size: 0.9rem;
            border-radius: 4px;
            transition: 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            display: inline-flex;
            align-items: center;
            gap: 10px;
            cursor: pointer;
        }

        .btn-blue {
            background: var(--brilliant-blue);
            color: #fff;
            box-shadow: var(--glow);
            border: none;
        }

        .btn-blue:hover { background: var(--electric-blue); transform: translateY(-5px); }

        .btn-silver {
            background: transparent;
            color: #fff;
            border: 1px solid var(--silver-static);
        }

        .btn-silver:hover { background: rgba(255, 255, 255, 0.05); border-color: var(--pure-white); transform: translateY(-5px); }

        /* 4. CONCEITO E FILOSOFIA */
        .section { padding: 100px 0; border-bottom: 1px solid var(--glass-border); }
        .container { max-width: 1200px; margin: 0 auto; padding: 0 30px; }

        .label { 
            color: var(--brilliant-blue); 
            font-size: 0.8rem; 
            font-weight: 700; 
            letter-spacing: 4px; 
            margin-bottom: 15px; 
            display: block; 
        }

        .philosophy-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 80px; align-items: start; }

        .info-card {
            background: rgba(255, 255, 255, 0.02);
            padding: 50px;
            border-top: 4px solid var(--brilliant-blue);
            border-right: 1px solid var(--glass-border);
            border-bottom: 1px solid var(--glass-border);
            border-left: 1px solid var(--glass-border);
        }

        /* 5. ESTRUTURAS WEB (PRICING) */
        .web-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 40px; margin-top: 60px; }

        .price-card {
            padding: 60px 40px;
            background: rgba(0, 8, 20, 0.5);
            border: 1px solid var(--glass-border);
            position: relative;
            transition: 0.5s;
        }

        .price-card.featured { border: 1px solid var(--brilliant-blue); box-shadow: var(--glow); }
        
        .price-value { font-size: 3.5rem; font-weight: 800; color: #fff; margin: 20px 0; }
        .price-value span { font-size: 1rem; color: var(--text-silver); font-weight: 400; }

        .features-list { list-style: none; margin: 40px 0; }
        .features-list li { margin-bottom: 18px; display: flex; align-items: flex-start; gap: 12px; font-size: 1.05rem; }
        .features-list li i { color: var(--brilliant-blue); margin-top: 5px; }

        /* 6. REDES SOCIAIS E CONTEÚDO */
        .social-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 20px; margin-top: 50px; }
        .social-item { background: #000; padding: 30px; border-left: 3px solid var(--brilliant-blue); }
        .social-item h4 { font-size: 0.75rem; color: var(--electric-blue); margin-bottom: 10px; }

        /* 7. ESTRATÉGIAS DE DIFERENCIAÇÃO */
        .strategy-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 40px; margin-top: 60px; text-align: center; }
        .strategy-item i { font-size: 2.5rem; color: var(--brilliant-blue); margin-bottom: 25px; display: block; }

        /* 8. LUNARA IDENTITY */
        .identity-block { padding: 120px 0; text-align: center; background: radial-gradient(circle at top, var(--deep-blue) 0%, var(--bg-black) 100%); }
        .identity-link { 
            font-size: clamp(1.5rem, 5vw, 2.5rem); 
            color: #fff; 
            text-decoration: none; 
            border-bottom: 1px solid var(--brilliant-blue); 
            padding-bottom: 10px;
            transition: 0.3s;
        }
        .identity-link:hover { color: var(--electric-blue); border-color: #fff; }

        /* 9. FOOTER / CTA */
        footer { padding: 100px 0; text-align: center; }
        .footer-note { font-size: 0.8rem; margin-top: 60px; opacity: 0.5; letter-spacing: 2px; }

        /* RESPONSIVIDADE */
        @media (max-width: 968px) {
            .philosophy-grid, .web-grid, .strategy-grid { grid-template-columns: 1fr; }
            .social-grid { grid-template-columns: 1fr 1fr; }
        }
    </style>
</head>
<body>

    <!-- 1. INTRO IMERSIVA -->
    <div id="splash">
        <div class="splash-phrase">
            CONSTRUA A SUA <span class="silver-text">FORTALEZA DIGITAL</span>
            <span>ANGOSEGUROS</span>
        </div>
    </div>

    <!-- 2. HERO SECTION -->
    <header>
        <div class="hero-content container">
            <span class="label">ESTRATÉGIA & LUXO</span>
            <h1>UMA ARQUITETURA DE <span class="silver-text">CONFIANÇA</span></h1>
            <p>Mais do que uma presença online, projetamos a infraestrutura intelectual que separa a sua corretora do mercado comum. Exclusividade, interatividade e rigor ARSEG.</p>
            <div class="btn-group">
                <a href="https://wa.me/lunaraflorence" target="_blank" class="btn btn-blue">
                    <i class="fab fa-whatsapp"></i> Falar com a Arquiteta
                </a>
                <a href="#proposta" class="btn btn-silver">Explorar Portfólio</a>
            </div>
        </div>
    </header>

    <!-- 3. FILOSOFIA LUNARA FLORENCE -->
    <section class="section" id="proposta">
        <div class="container philosophy-grid">
            <div>
                <span class="label">O NOSSO DNA</span>
                <h2 style="font-size: 2.2rem; margin-bottom: 30px;">O INTELECTO COMO <span class="silver-text">PRODUTO</span></h2>
                <p>Na minha abordagem, a criatividade é o motor da conversão. Enquanto o meu site é um laboratório experimental, a solução para a <strong>ANGOSEGUROS</strong> será uma estrutura fixa e centralizada, desenhada para atrair, educar e converter.</p>
                <p style="margin-top: 20px;">Cobramos pela arquitetura da marca e pela engenharia de SEO. Somos <strong>"Premium para Todos"</strong>: modulamos a densidade do projeto mantendo o selo de exclusividade artesanal.</p>
            </div>
            <div class="info-card">
                <h4 style="margin-bottom: 25px; color: var(--electric-blue);">DIFERENCIAIS TÉCNICOS</h4>
                <ul class="features-list">
                    <li><i class="fas fa-microchip"></i> Sistemas Baseados em Comandos Próprios.</li>
                    <li><i class="fas fa-brain"></i> Curadoria de Conteúdo SEO para Angola.</li>
                    <li><i class="fas fa-gem"></i> Estética Imersiva Prateada & Azul.</li>
                    <li><i class="fas fa-shield-halved"></i> Realce da Autoridade ARSEG.</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- 4. INFRAESTRUTURA WEB -->
    <section class="section container">
        <span class="label text-center" style="text-align: center;">PLANO DE IMPLEMENTAÇÃO</span>
        <h2 style="text-align: center; margin-bottom: 10px;">A SUA <span class="silver-text">BASE DIGITAL</span></h2>
        
        <div class="web-grid">
            <!-- SITE IMERSIVO -->
            <div class="price-card featured">
                <span class="label" style="font-size: 0.7rem;">INFRAESTRUTURA PREMIUM</span>
                <h3>SITE IMERSIVO</h3>
                <div class="price-value">255€ <span class="silver-text">/ plano anual</span></div>
                <p>Plataforma Própria Única para experiências de alto impacto.</p>
                <ul class="features-list">
                    <li><i class="fas fa-check"></i> <strong>Estrutura Fixa:</strong> Todos os seguros num só lugar.</li>
                    <li><i class="fas fa-check"></i> <strong>Interatividade:</strong> Programação fluida e imersiva.</li>
                    <li><i class="fas fa-check"></i> <strong>Performance:</strong> Velocidade máxima e segurança.</li>
                    <li><i class="fas fa-check"></i> <strong>Central de Cotação:</strong> Simuladores inteligentes.</li>
                </ul>
                <p style="font-size: 0.8rem; opacity: 0.6;">* Valor referente à manutenção e infraestrutura da plataforma fixa.</p>
            </div>

            <!-- SITE ESTÁTICO -->
            <div class="price-card">
                <span class="label" style="font-size: 0.7rem;">ESTABILIDADE STANDARD</span>
                <h3>SITE ESTÁTICO</h3>
                <div class="price-value">90€ <span class="silver-text">/ mensal</span></div>
                <p>Alojamento e Domínio válidos por 12 meses.</p>
                <ul class="features-list">
                    <li><i class="fas fa-check"></i> <strong>Programação Manual:</strong> Foco em clareza informativa.</li>
                    <li><i class="fas fa-check"></i> <strong>Design Limpo:</strong> Transmissão direta de valores.</li>
                    <li><i class="fas fa-check"></i> <strong>Manutenção Inclusa:</strong> Estabilidade mensal.</li>
                    <li><i class="fas fa-check"></i> <strong>Presença Digital:</strong> O cartão de visita 2.0.</li>
                </ul>
                <p style="font-size: 0.8rem; opacity: 0.6;">* Pagamento mensal recorrente com custos de domínio anuais.</p>
            </div>
        </div>

        <div style="margin-top: 50px; padding: 40px; background: rgba(0, 102, 255, 0.05); border: 1px dashed var(--brilliant-blue); border-radius: 4px;">
            <h4 style="color: var(--electric-blue); margin-bottom: 15px;">NOTA SOBRE MÃO DE OBRA INTELECTUAL</h4>
            <p style="font-size: 0.95rem;">Os valores acima referem-se à <strong>manutenção operacional</strong>. O investimento na <strong>mão de obra</strong> (criação artesanal de conteúdo, engenharia de páginas, design estratégico e organização do portfólio expandido) é calculado separadamente, refletindo a exclusividade de cada comando programado.</p>
        </div>
    </section>

    <!-- 5. GESTÃO DE REDES E CONTEÚDO -->
    <section class="section" style="background: var(--deep-blue);">
        <div class="container">
            <span class="label">CONTEÚDO ESTRATÉGICO</span>
            <h2>O INSTAGRAM COMO <span class="silver-text">AUTORIDADE</span></h2>
            
            <div class="social-grid">
                <div class="social-item">
                    <h4>SEMANA 1</h4>
                    <h3 style="font-size: 1.1rem; margin-bottom: 10px;">MANIFESTO</h3>
                    <p style="font-size: 0.9rem;">Apresentação da sede na Urbanização Nova Vida e valores de confiança.</p>
                </div>
                <div class="social-item">
                    <h4>SEMANA 2</h4>
                    <h3 style="font-size: 1.1rem; margin-bottom: 10px;">ANÁLISE</h3>
                    <p style="font-size: 0.9rem;">Série "Anatomia do Risco": O que o seu Seguro de Acidentes não conta.</p>
                </div>
                <div class="social-item">
                    <h4>SEMANA 3</h4>
                    <h3 style="font-size: 1.1rem; margin-bottom: 10px;">PORTFÓLIO</h3>
                    <p style="font-size: 0.9rem;">Expansão: Saúde, Vida e Multirriscos com visão consultiva.</p>
                </div>
                <div class="social-item">
                    <h4>SEMANA 4</h4>
                    <h3 style="font-size: 1.1rem; margin-bottom: 10px;">CONVERSÃO</h3>
                    <p style="font-size: 0.9rem;">Dúvidas ARSEG e chamadas para o simulador no site imersivo.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 6. DIFERENCIAÇÃO -->
    <section class="section container">
        <span class="label text-center" style="text-align: center;">CONVERSÃO E VÍDEO</span>
        <h2 style="text-align: center; margin-bottom: 60px;">METODOLOGIA DE <span class="silver-text">IMPACTO</span></h2>

        <div class="strategy-grid">
            <div class="strategy-item">
                <i class="fas fa-film"></i>
                <h3 style="font-size: 1.2rem; margin-bottom: 15px;">VÍDEOS DE ANÁLISE</h3>
                <p>Scripts cinematográficos para humanizar a marca e explicar coberturas complexas.</p>
            </div>
            <div class="strategy-item">
                <i class="fas fa-bullseye"></i>
                <h3 style="font-size: 1.2rem; margin-bottom: 15px;">MICRO-ADS</h3>
                <p>Anúncios em pequena escala (Meta Ads) para atrair leads qualificados com baixo custo.</p>
            </div>
            <div class="strategy-item">
                <i class="fas fa-magnifying-glass-chart"></i>
                <h3 style="font-size: 1.2rem; margin-bottom: 15px;">SEO ARTESANAL</h3>
                <p>Programação focada em ser a primeira opção de busca para "Seguros em Angola".</p>
            </div>
        </div>
    </section>

    <!-- 7. LUNARA IDENTITY -->
    <section class="identity-block container">
        <span class="label">VISITE O LABORATÓRIO</span>
        <div style="margin-bottom: 40px;">
            <a href="https://lunaraflorence.com/" target="_blank" class="identity-link">LUNARAFLORENCE.COM</a>
        </div>
        <p style="max-width: 700px; margin: 0 auto;">Visite o meu ecossistema criativo para compreender o nível de interatividade que traremos para a ANGOSEGUROS.</p>
    </section>

    <!-- 8. FOOTER CTA -->
    <footer>
        <div class="container">
            <h2 style="font-size: clamp(1.8rem, 5vw, 3rem); margin-bottom: 30px;">PRONTO PARA A <span class="silver-text">DEMONSTRAÇÃO</span>?</h2>
            <p style="margin-bottom: 50px; max-width: 800px; margin-left: auto; margin-right: auto;">Estou pronta para enviar uma demonstração funcional do site imersivo. Sinta na prática como a nossa arquitetura centralizada elevará o vosso negócio.</p>
            
            <div class="btn-group">
                <a href="https://wa.me/lunaraflorence" target="_blank" class="btn btn-blue">
                    <i class="fab fa-whatsapp"></i> Iniciar Imersão no WhatsApp
                </a>
            </div>

            <p class="footer-note">PROPOSTA EXCLUSIVA PARA ANGOSEGUROS | © 2026 LUNARA FLORENCE</p>
        </div>
    </footer>

</body>
</html>

