<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NatureShape - Emagrecimento Natural e Saudável</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Variáveis e reset */
        :root {
            --primary: #2e7d32;
            --secondary: #7cb342;
            --accent: #ff8f00;
            --light: #f5f9f5;
            --dark: #1b5e20;
            --text: #212121;
            --text-light: #757575;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--light);
            color: var(--text);
            line-height: 1.6;
        }
        
        /* Container */
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .logo img {
            height: 50px;
        }
        
        .logo h1 {
            color: var(--primary);
            font-size: 1.8rem;
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
        }
        
        nav a {
            text-decoration: none;
            color: var(--text);
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav a:hover {
            color: var(--primary);
        }
        
        .cart-btn {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 5px;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: background-color 0.3s;
        }
        
        .cart-btn:hover {
            background-color: var(--dark);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(to right, rgba(46, 125, 50, 0.9), rgba(124, 179, 66, 0.8)), url('https://images.unsplash.com/photo-1490818387583-1baba5e638af?ixlib=rb-4.0.3&auto=format&fit=crop&w=1200&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 100px 0;
            text-align: center;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h2 {
            font-size: 3rem;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--accent);
            color: white;
            padding: 15px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            transition: transform 0.3s, background-color 0.3s;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            background-color: #ff6f00;
        }
        
        /* Features */
        .features {
            padding: 80px 0;
            background-color: white;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            color: var(--primary);
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            margin-bottom: 15px;
        }
        
        .section-title p {
            color: var(--text-light);
            max-width: 700px;
            margin: 0 auto;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .feature-card {
            text-align: center;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
        }
        
        .feature-icon {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 20px;
        }
        
        .feature-card h3 {
            margin-bottom: 15px;
            color: var(--dark);
        }
        
        /* Products */
        .products {
            padding: 80px 0;
            background-color: var(--light);
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }
        
        .product-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
        }
        
        .product-card:hover {
            transform: translateY(-5px);
        }
        
        .product-img {
            height: 200px;
            width: 100%;
            object-fit: cover;
        }
        
        .product-info {
            padding: 20px;
        }
        
        .product-title {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: var(--dark);
        }
        
        .product-price {
            font-size: 1.3rem;
            color: var(--primary);
            font-weight: bold;
            margin-bottom: 15px;
        }
        
        .product-desc {
            color: var(--text-light);
            margin-bottom: 20px;
        }
        
        .add-to-cart {
            width: 100%;
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 12px;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        
        .add-to-cart:hover {
            background-color: var(--dark);
        }
        
        /* Testimonials */
        .testimonials {
            padding: 80px 0;
            background-color: white;
        }
        
        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .testimonial-card {
            background-color: var(--light);
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 20px;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .author-img {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            object-fit: cover;
        }
        
        .author-info h4 {
            color: var(--dark);
        }
        
        .author-info p {
            color: var(--text-light);
            font-size: 0.9rem;
        }
        
        /* About */
        .about {
            padding: 80px 0;
            background-color: var(--light);
        }
        
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }
        
        .about-img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .about-text h2 {
            color: var(--primary);
            margin-bottom: 20px;
        }
        
        .about-text p {
            margin-bottom: 20px;
        }
        
        /* Contact */
        .contact {
            padding: 80px 0;
            background-color: white;
        }
        
        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }
        
        .contact-info h3 {
            color: var(--primary);
            margin-bottom: 20px;
        }
        
        .contact-details {
            margin-bottom: 30px;
        }
        
        .contact-details p {
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 15px;
            margin-bottom: 20px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        
        .contact-form textarea {
            height: 150px;
        }
        
        .submit-btn {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 15px 30px;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        
        .submit-btn:hover {
            background-color: var(--dark);
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 50px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 30px;
        }
        
        .footer-column h3 {
            margin-bottom: 20px;
            font-size: 1.2rem;
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column a {
            color: #ddd;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-column a:hover {
            color: white;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
        }
        
        .social-links a {
            display: inline-block;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            text-align: center;
            line-height: 40px;
            transition: background-color 0.3s;
        }
        
        .social-links a:hover {
            background-color: var(--accent);
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
            color: #ddd;
        }
        
        /* Responsividade */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 20px;
            }
            
            nav ul {
                gap: 15px;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .about-content,
            .contact-grid {
                grid-template-columns: 1fr;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <i class="fas fa-leaf fa-2x" style="color: var(--primary)"></i>
                    <h1>NatureShape</h1>
                </div>
                <nav>
                    <ul>
                        <li><a href="#home">Início</a></li>
                        <li><a href="#products">Produtos</a></li>
                        <li><a href="#about">Sobre</a></li>
                        <li><a href="#testimonials">Depoimentos</a></li>
                        <li><a href="#contact">Contato</a></li>
                    </ul>
                </nav>
                <button class="cart-btn">
                    <i class="fas fa-shopping-cart"></i>
                    <span>Carrinho (0)</span>
                </button>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h2>Emagrecimento Natural e Saudável</h2>
                <p>Descubra a poderosa combinação de produtos naturais que vão transformar sua saúde e ajudar você a alcançar o corpo dos seus sonhos.</p>
                <a href="#products" class="btn">Conhecer Produtos</a>
            </div>
        </div>
    </section>

    <!-- Features -->
    <section class="features">
        <div class="container">
            <div class="section-title">
                <h2>Por que escolher nossos produtos?</h2>
                <p>Nossa linha de produtos naturais foi desenvolvida para oferecer os melhores resultados com total segurança para sua saúde.</p>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-seedling"></i>
                    </div>
                    <h3>100% Natural</h3>
                    <p>Ingredientes totalmente naturais, sem adição de produtos químicos ou sintéticos.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-heart"></i>
                    </div>
                    <h3>Saúde em Primeiro Lugar</h3>
                    <p>Foco no bem-estar e saúde, não apenas na perda de peso.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-flask"></i>
                    </div>
                    <h3>Comprovadamente Eficaz</h3>
                    <p>Resultados comprovados por milhares de clientes satisfeitos.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-shipping-fast"></i>
                    </div>
                    <h3>Entrega Rápida</h3>
                    <p>Entregamos em todo o Brasil com rapidez e discrição.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Products -->
    <section class="products" id="products">
        <div class="container">
            <div class="section-title">
                <h2>Nossos Produtos</h2>
                <p>Conheça nossa linha de produtos desenvolvidos para auxiliar no emagrecimento saudável.</p>
            </div>
            <div class="products-grid">
                <div class="product-card">
                    <img src="https://images.unsplash.com/photo-1551183053-bf91a1d81141?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Detox Natural" class="product-img">
                    <div class="product-info">
                        <h3 class="product-title">Detox Natural</h3>
                        <p class="product-price">R$ 89,90</p>
                        <p class="product-desc">Limpeza completa do organismo, eliminando toxinas e acelerando o metabolismo.</p>
                        <button class="add-to-cart">Adicionar ao Carrinho</button>
                    </div>
                </div>
                <div class="product-card">
                    <img src="https://images.unsplash.com/photo-1551183053-bf91a1d81141?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Chá Emagrecedor" class="product-img">
                    <div class="product-info">
                        <h3 class="product-title">Chá Emagrecedor</h3>
                        <p class="product-price">R$ 59,90</p>
                        <p class="product-desc">Combinação especial de ervas que auxiliam na queima de gordura naturalmente.</p>
                        <button class="add-to-cart">Adicionar ao Carrinho</button>
                    </div>
                </div>
                <div class="product-card">
                    <img src="https://images.unsplash.com/photo-1551183053-bf91a1d81141?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Cápsulas Termogênicas" class="product-img">
                    <div class="product-info">
                        <h3 class="product-title">Cápsulas Termogênicas</h3>
                        <p class="product-price">R$ 119,90</p>
                        <p class="product-desc">Aumenta a temperatura corporal, potencializando a queima de gordura.</p>
                        <button class="add-to-cart">Adicionar ao Carrinho</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section class="testimonials" id="testimonials">
        <div class="container">
            <div class="section-title">
                <h2>O que nossos clientes dizem</h2>
                <p>Confira os depoimentos de pessoas reais que transformaram suas vidas com nossos produtos.</p>
            </div>
            <div class="testimonials-grid">
                <div class="testimonial-card">
                    <p class="testimonial-text">"Perdi 12kg em 3 meses com os produtos NatureShape. Além do emagrecimento, minha saúde melhorou muito!"</p>
                    <div class="testimonial-author">
                        <img src="https://randomuser.me/api/portraits/women/65.jpg" alt="Maria Silva" class="author-img">
                        <div class="author-info">
                            <h4>Maria Silva</h4>
                            <p>São Paulo, SP</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <p class="testimonial-text">"Finalmente encontrei uma forma saudável de emagrecer. Os produtos são incríveis e não tive nenhum efeito colateral."</p>
                    <div class="testimonial-author">
                        <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="João Santos" class="author-img">
                        <div class="author-info">
                            <h4>João Santos</h4>
                            <p>Belo Horizonte, MG</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <p class="testimonial-text">"Depois de tentar diversas dietas malucas, os produtos naturais da NatureShape foram a solução que eu precisava."</p>
                    <div class="testimonial-author">
                        <img src="https://randomuser.me/api/portraits/women/45.jpg" alt="Ana Costa" class="author-img">
                        <div class="author-info">
                            <h4>Ana Costa</h4>
                            <p>Rio de Janeiro, RJ</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About -->
    <section class="about" id="about">
        <div class="container">
            <div class="about-content">
                <div>
                    <img src="https://images.unsplash.com/photo-1540420773420-3366772f4999?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Sobre a NatureShape" class="about-img">
                </div>
                <div class="about-text">
                    <h2>Sobre a NatureShape</h2>
                    <p>A NatureShape nasceu da paixão por uma vida saudável e natural. Nossa missão é oferecer produtos que realmente funcionam, com transparência e respeito ao seu corpo.</p>
                    <p>Todos os nossos produtos são desenvolvidos por especialistas em nutrição e fitoterapia, utilizando apenas ingredientes de alta qualidade e comprovada eficácia.</p>
                    <p>Acreditamos que o emagrecimento saudável é uma jornada que deve ser feita com produtos que cuidam do seu corpo, não apenas com foco na perda de peso.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact -->
    <section class="contact" id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Entre em Contato</h2>
                <p>Tire suas dúvidas ou faça seu pedido diretamente conosco.</p>
            </div>
            <div class="contact-grid">
                <div class="contact-info">
                    <h3>Informações de Contato</h3>
                    <div class="contact-details">
                        <p><i class="fas fa-map-marker-alt"></i> Rua das Flores, 123 - Jardim Paulista, São Paulo - SP</p>
                        <p><i class="fas fa-phone"></i> (11) 99999-9999</p>
                        <p><i class="fas fa-envelope"></i> contato@natureshape.com.br</p>
                    </div>
                    <h3>Redes Sociais</h3>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-whatsapp"></i></a>
                    </div>
                </div>
                <div class="contact-form">
                    <form>
                        <input type="text" placeholder="Seu nome" required>
                        <input type="email" placeholder="Seu e-mail" required>
                        <input type="tel" placeholder="Seu telefone">
                        <textarea placeholder="Sua mensagem" required></textarea>
                        <button type="submit" class="submit-btn">Enviar Mensagem</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>NatureShape</h3>
                    <p>Emagrecimento natural e saudável com produtos 100% naturais desenvolvidos para cuidar do seu corpo.</p>
                </div>
                <div class="footer-column">
                    <h3>Links Rápidos</h3>
                    <ul>
                        <li><a href="#home">Início</a></li>
                        <li><a href="#products">Produtos</a></li>
                        <li><a href="#about">Sobre</a></li>
                        <li><a href="#contact">Contato</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Produtos</h3>
                    <ul>
                        <li><a href="#">Detox Natural</a></li>
                        <li><a href="#">Chá Emagrecedor</a></li>
                        <li><a href="#">Cápsulas Termogênicas</a></li>
                        <li><a href="#">Todos os Produtos</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Newsletter</h3>
                    <p>Inscreva-se para receber dicas e promoções exclusivas.</p>
                    <form>
                        <input type="email" placeholder="Seu e-mail" style="padding: 10px; width: 100%; margin-bottom: 10px; border-radius: 5px; border: none;">
                        <button type="submit" class="submit-btn" style="padding: 10px 15px;">Inscrever</button>
                    </form>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 NatureShape - Todos os direitos reservados.</p>
            </div>
        </div>
    </footer>

    <script>
        // Funcionalidade simples do carrinho
        document.querySelectorAll('.add-to-cart').forEach(button => {
            button.addEventListener('click', function() {
                let count = parseInt(document.querySelector('.cart-btn span').textContent.match(/\d+/)[0]);
                count++;
                document.querySelector('.cart-btn span').textContent = `Carrinho (${count})`;
                
                // Feedback visual
                this.textContent = 'Adicionado!';
                setTimeout(() => {
                    this.textContent = 'Adicionar ao Carrinho';
                }, 1500);
            });
        });
        
        // Smooth scroll para links internos
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
    </script>
</body>
</html>