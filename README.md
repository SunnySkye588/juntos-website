<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <title>Encontros - Conexões Significativas</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css">
    <link rel="stylesheet" href="./assets/extend.css">
    <link href="https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://unpkg.com/swiper@8/swiper-bundle.min.css">
    <script src="https://unpkg.com/swiper@8/swiper-bundle.min.js"></script>
    <style>
        :root {
            --swiper-pagination-size: 18px;
            --swiper-pagination-color: #E63946;
            --swiper-pagination-bullet-width: 10px;
            --swiper-pagination-bullet-height: 10px;
            --swiper-pagination-bullet-inactive-color: #ccc;
        }

        .swiper {
            width: 100%;
            height: 100vh;
        }

        .swiper-slide {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 80px 20px 60px;
        }
        
        .swiper-slide-active {
            z-index: 10;
        }

        body {
            margin: 0;
            padding: 0;
            font-family: 'Open Sans', sans-serif;
            overflow-x: hidden;
        }

        header {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            padding: 20px 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            background-color: white;
            z-index: 999;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }

        .logo-img {
            height: 50px;
            object-fit: contain;
        }

        .nav-link {
            color: #333;
            text-decoration: none;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: color 0.3s;
        }

        .nav-link:hover {
            color: #E63946;
        }

        .fancy-title {
            font-size: 2.8rem;
            font-weight: 800;
            text-align: center;
            margin-bottom: 40px;
            line-height: 1.2;
        }

        .big-btn {
            display: inline-block;
            padding: 15px 40px;
            background-color: #333;
            color: white;
            text-decoration: none;
            font-weight: 700;
            border-radius: 50px;
            font-size: 1.1rem;
            transition: all 0.3s;
        }

        .big-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            color: white;
        }

        .big-btn-fire {
            background-color: #E63946;
            position: relative;
            overflow: hidden;
        }

        .big-btn-fire::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
            transition: 0.6s;
        }

        .big-btn-fire:hover::before {
            left: 100%;
        }

        .descr {
            font-size: 1.1rem;
            line-height: 1.8;
            margin-bottom: 40px;
            color: #555;
        }

        footer {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            padding: 15px 20px;
            background-color: #f8f9fa;
            text-align: center;
            z-index: 999;
        }

        .footer-copyright {
            color: #777;
            font-size: 0.9rem;
        }

        .section-1 .row, .section-2 .row {
            align-items: center;
            height: 100%;
        }

        @media (max-width: 992px) {
            .fancy-title {
                font-size: 2rem;
                margin-bottom: 30px;
            }

            .section-1 .col-12 {
                margin-bottom: 30px;
            }

            .section-1 .col-12:last-child {
                margin-bottom: 0;
            }

            .section-2 .col-12.col-lg-6:first-child {
                margin-bottom: 40px;
            }

            .descr {
                font-size: 1rem;
                margin-bottom: 30px;
            }
        }

        @media (max-width: 576px) {
            header {
                padding: 15px 20px;
            }

            .logo-img {
                height: 40px;
            }

            .big-btn {
                padding: 12px 30px;
                font-size: 1rem;
            }

            .swiper-slide {
                padding-top: 70px;
            }
        }
    </style>
</head>

<body>
    <header>
        <div class="logo-area">
            <img src="https://via.placeholder.com/120x50?text=Encontros" alt="Logo" class="logo-img">
        </div>
        <nav>
            <a href="#" class="nav-link">Pt 
                <svg height="20" width="20" aria-hidden="true" viewBox="0 0 20 20">
                    <path
                        d="M4.516 7.548c.436-.446 1.043-.481 1.576 0L10 11.295l3.908-3.747c.533-.481 1.141-.446 1.574 0 .436.445.408 1.197 0 1.615-.406.418-4.695 4.502-4.695 4.502a1.095 1.095 0 01-1.576 0S4.924 9.581 4.516 9.163s-.436-1.17 0-1.615z">
                    </path>
                </svg>
            </a>
        </nav>
    </header>
    
    <div class="main-content">
        <div class="swiper">
            <div class="swiper-wrapper">
                <!-- Primeiro Slide -->
                <div class="swiper-slide">
                    <div class="container-fluid section-1">
                        <div class="row">
                            <div class="col-12 col-lg-4 d-flex justify-content-center">
                                <img src="https://via.placeholder.com/300x400?text=Pessoas+Felizes" alt="Conexões" class="section-1-left-img img-fluid" style="max-height: 400px;">
                            </div>
                            <div class="col-12 col-lg-4 d-flex flex-column justify-content-center align-items-center text-center">
                                <div class="section-1-center">
                                    <h1 class="fancy-title">
                                        <span>Conecte-se com pessoas speciais</span>
                                    </h1>
                                    <div class="options">
                                        <a class="big-btn big-btn-fire" href="https://en571.netlify.app/">Iniciar agora</a>
                                    </div>
                                </div>
                            </div>
                            <div class="col-12 col-lg-4 d-flex justify-content-center">
                                <img src="https://via.placeholder.com/300x400?text=Relacionamentos" alt="Encontros" class="section-1-right-img img-fluid" style="max-height: 400px;">
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Segundo Slide -->
                <div class="swiper-slide">
                    <div class="container-xl section-2">
                        <div class="row">
                            <div class="col-12 col-lg-6 d-flex justify-content-center">
                                <img src="https://via.placeholder.com/500x400?text=Comunidade" alt="Nossa Missão" class="section-2-img img-fluid" style="max-height: 400px; border-radius: 10px;">
                            </div>
                            <div class="col-12 col-lg-6">
                                <p class="descr">
                                    Nosso objetivo é criar um espaço seguro para quem busca relacionamentos verdadeiros, amizades duradouras e experiências significativas. Aqui, você pode compartilhar, aprender e crescer junto com pessoas que buscam o mesmo que você: conexões autênticas e felicidade.
                                </p>
                                <div class="options">
                                    <a class="big-btn" href="https://en571.netlify.app/">Participe Agora</a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="swiper-pagination" style="bottom: 80px;"></div>
        </div>
    </div>
    
    <footer>
        <div class="footer-content">
            <span class="footer-copyright">© Encontros 2024-2025. Todos os direitos reservados</span>
        </div>
    </footer>

    <script>
        const swiper = new Swiper('.swiper', {
            direction: 'vertical',
            loop: false,
            pagination: {
                el: '.swiper-pagination',
                clickable: true,
            },
            mousewheel: {
                sensitivity: 1,
            },
            speed: 500,
        });

        // Adiciona efeito de fade-in nas imagens
        document.querySelectorAll('img').forEach(img => {
            img.style.opacity = "0";
            img.style.transition = "opacity 0.8s ease";
            
            img.onload = function() {
                this.style.opacity = "1";
            }
            
            // Se a imagem já está carregada
            if (img.complete) {
                img.style.opacity = "1";
            }
        });
    </script>
</body>
</html>
