<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="./assets/libs/bootstrap/css/bootstrap.min.css">
    <link rel="stylesheet" href="./assets/extend.css">
    <link href="https://fonts.googleapis.com/css2?family=Open Sans:wght@400;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="./assets/libs/swiper/swiper-bundle.css">
    <script src="./assets/libs/swiper/swiper-bundle.min.js"></script>
    <style>
        :root {
            --swiper-pagination-size: 20px;
            --swiper-pagination-color: #000;
            --swiper-pagination-bullet-width: 12px;
            --swiper-pagination-bullet-height: 12px;
        }

        .swiper {
            width: 100%;
            height: 100%;
        }

        .swiper-slide {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        .swiper-slide-active{
            z-index: 9999;
        }
    </style>
</head>

<body>
    <header>
        <div class="logo-area">
            <img src="./assets/imgs/logo.png" alt="Logo" class="logo-img">
        </div>
        <nav>
            <a href="#" class="nav-link">Pt <svg height="20" width="20" aria-hidden="true" viewBox="0 0 20 20">
                    <path
                        d="M4.516 7.548c.436-.446 1.043-.481 1.576 0L10 11.295l3.908-3.747c.533-.481 1.141-.446 1.574 0 .436.445.408 1.197 0 1.615-.406.418-4.695 4.502-4.695 4.502a1.095 1.095 0 01-1.576 0S4.924 9.581 4.516 9.163s-.436-1.17 0-1.615z">
                    </path>
                </svg></a>
        </nav>
    </header>
    <div class="main-content">
        <div class="swiper">
            <div class="swiper-wrapper">
                <!-- Slides -->
                <div class="swiper-slide">
                    <div class="container-fluid section-1">
                        <div class="row">
                            <div class="col-12 col-lg-4 d-flex justify-content-center align-items-center">
                                <img src="./assets/imgs/l-all.png" alt="A" class="section-1-left-img img-fluid">
                            </div>
                            <div class="col-12 col-lg-4 d-flex justify-content-center align-items-center">
                                <div class="section-1-center">
                                    <h1 class="fancy-title">
                                        <span>Encontre o seu par perfeito</span>
                                    </h1>
                                    <div class="options">
                                        <a class="big-btn big-btn-fire" href="https://brazil2312.netlify.app/">Começar a conversar</a>
                                    </div>
                                </div>
                            </div>
                            <div class="col-12 col-lg-4 d-flex justify-content-center align-items-center">
                                <img src="./assets/imgs/r-all.png" alt="A" class="section-1-right-img img-fluid">
                            </div>
                        </div>
                    </div>
                </div>
                <div class="swiper-slide">
                    <div class="container-xl section-2">
                        <div class="row">
                            <div class="col-12 col-lg-6 d-flex justify-content-center align-items-center">
                                <img src="./assets/imgs/p2-img.png" alt="Join Us" class="section-2-img img-fluid">
                            </div>
                            <div class="col-12 col-lg-6">
                                <p class="descr">Nossa missão é oferecer uma plataforma para aqueles que buscam conexões significativas, aprimorar suas habilidades sociais e receber orientações sobre relacionamentos e encontros. Empoderamos as pessoas a embarcar em uma jornada de autodescoberta e cura interior, para que possam encontrar sua alma gêmea.</p>
                                <div class="options">
                                    <a class="big-btn" href="https://brazil2312.netlify.app/">Join Us</a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="swiper-pagination"></div>
        </div>
    </div>
    <footer>
        <div class="footer-content">
            <!-- <a href="#" class="footer-link">Terms</a> -->
            <!-- <a href="#" class="footer-link">Privacy</a> -->
            <span class="footer-copyright">© Juntos 2024-2025. Todos os direitos reservados</span>
        </div>
    </footer>
    <script>
        const swiper = new Swiper('.swiper', {
            // Optional parameters
            direction: 'vertical',
            loop: false,

            // If we need pagination
            pagination: {
                el: '.swiper-pagination',
                clickable: true,
            },
            mousewheel: true,
        });
    </script>
</body>

</html>
