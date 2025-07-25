<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <title>Juntos - Encontre seu Par Perfeito</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- 外部资源 -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://unpkg.com/swiper@8/swiper-bundle.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;700;800&display=swap" rel="stylesheet">
    <script src="https://unpkg.com/swiper@8/swiper-bundle.min.js"></script>
    
    <style>
        /* 全局样式 */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Open Sans', sans-serif;
        }

        :root {
            --primary-color: #FF5A5F;
            --dark-color: #2A2A2A;
            --light-color: #F9F9F9;
            --swiper-pagination-color: var(--primary-color);
            --swiper-pagination-bullet-inactive-color: #ccc;
            --swiper-pagination-bullet-inactive-opacity: 1;
        }

        body {
            background-color: var(--light-color);
            color: var(--dark-color);
            overflow-x: hidden;
        }

        /* 头部样式 */
        header {
            padding: 20px 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            background-color: rgba(255, 255, 255, 0.9);
            z-index: 9999;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
        }

        .logo-img {
            height: 50px;
            object-fit: contain;
        }

        .nav-link {
            color: var(--dark-color);
            text-decoration: none;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: color 0.3s;
        }

        .nav-link:hover {
            color: var(--primary-color);
        }

        /* 主内容区 */
        .main-content {
            margin-top: 90px;
            height: calc(100vh - 180px);
        }

        .swiper {
            width: 100%;
            height: 100%;
        }

        .swiper-slide {
            height: 100% !important;
        }

        /* 按钮样式 */
        .big-btn {
            display: inline-block;
            padding: 15px 40px;
            background-color: var(--dark-color);
            color: white;
            text-decoration: none;
            font-weight: 800;
            border-radius: 50px;
            font-size: 1.1rem;
            transition: all 0.3s;
            text-align: center;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
        }

        .big-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
            color: white;
        }

        .big-btn-fire {
            background-color: var(--primary-color);
            position: relative;
            overflow: hidden;
        }

        .big-btn-fire::after {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: all 0.6s;
        }

        .big-btn-fire:hover::after {
            left: 100%;
        }

        /* 第一屏样式 */
        .section-1 {
            height: 100%;
            padding: 40px;
        }

        .fancy-title {
            font-size: 2.5rem;
            font-weight: 800;
            text-align: center;
            margin-bottom: 40px;
            line-height: 1.3;
        }

        @media (max-width: 992px) {
            .fancy-title {
                font-size: 2rem;
            }
        }

        .section-1-left-img, .section-1-right-img {
            max-height: 400px;
            object-fit: contain;
        }

        .section-1-center {
            padding: 20px;
        }

        .options {
            display: flex;
            justify-content: center;
        }

        /* 第二屏样式 */
        .section-2 {
            height: 100%;
            padding: 80px 40px;
            display: flex;
            align-items: center;
        }

        .section-2-img {
            max-height: 500px;
            object-fit: contain;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .descr {
            font-size: 1.2rem;
            line-height: 1.8;
            margin-bottom: 40px;
            text-align: justify;
            padding: 20px;
        }

        /* 页脚样式 */
        footer {
            padding: 20px 40px;
            background-color: var(--dark-color);
            color: white;
            text-align: center;
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
        }

        .footer-copyright {
            font-size: 0.9rem;
            opacity: 0.8;
        }

        /* 响应式调整 */
        @media (max-width: 768px) {
            header {
                padding: 15px 20px;
            }

            .main-content {
                margin-top: 70px;
                height: calc(100vh - 140px);
            }

            .section-1 {
                padding: 20px 10px;
            }

            .section-1-left-img, .section-1-right-img {
                max-height: 200px;
                margin-bottom: 20px;
            }

            .section-2 {
                padding: 40px 20px;
                text-align: center;
            }

            .descr {
                font-size: 1rem;
                margin-bottom: 30px;
            }

            .section-2-img {
                margin-bottom: 40px;
                max-height: 300px;
            }

            .fancy-title {
                font-size: 1.8rem;
                margin-bottom: 30px;
            }

            .big-btn {
                padding: 12px 30px;
                font-size: 1rem;
            }
        }

        /* 动画效果 */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .swiper-slide-active .section-1,
        .swiper-slide-active .section-2 {
            animation: fadeIn 0.8s ease forwards;
        }

        /* 底部样式 */
        footer {
            padding: 15px;
        }
    </style>
</head>

<body>
    <header>
        <div class="logo-area">
            <!-- 替换为你的logo图片 -->
            <img src="https://via.placeholder.com/150x50?text=JUNTOS" alt="Logo Juntos" class="logo-img">
        </div>
        <nav>
            <a href="#" class="nav-link">
                Pt 
                <svg height="20" width="20" aria-hidden="true" viewBox="0 0 20 20">
                    <path d="M4.516 7.548c.436-.446 1.043-.481 1.576 0L10 11.295l3.908-3.747c.533-.481 1.141-.446 1.574 0 .436.445.408 1.197 0 1.615-.406.418-4.695 4.502-4.695 4.502a1.095 1.095 0 01-1.576 0S4.924 9.581 4.516 9.163s-.436-1.17 0-1.615z"></path>
                </svg>
            </a>
        </nav>
    </header>

    <div class="main-content">
        <div class="swiper">
            <div class="swiper-wrapper">
                <!-- 第一屏 -->
                <div class="swiper-slide">
                    <div class="container-fluid section-1">
                        <div class="row">
                            <div class="col-12 col-lg-4 d-flex justify-content-center align-items-center">
                                <!-- 左侧图片 -->
                                <img src="https://via.placeholder.com/300x400?text=Imagem+Esquerda" alt="Ilustração" class="section-1-left-img img-fluid">
                            </div>
                            <div class="col-12 col-lg-4 d-flex justify-content-center align-items-center">
                                <div class="section-1-center">
                                    <h1 class="fancy-title">
                                        <span>Encontre o seu par perfeito</span>
                                    </h1>
                                    <div class="options">
                                        <a class="big-btn big-btn-fire" href="https://diva88.netlify.app/">Começar a conversar</a>
                                    </div>
                                </div>
                            </div>
                            <div class="col-12 col-lg-4 d-flex justify-content-center align-items-center">
                                <!-- 右侧图片 -->
                                <img src="https://via.placeholder.com/300x400?text=Imagem+Direita" alt="Ilustração" class="section-1-right-img img-fluid">
                            </div>
                        </div>
                    </div>
                </div>

                <!-- 第二屏 -->
                <div class="swiper-slide">
                    <div class="container-xl section-2">
                        <div class="row align-items-center">
                            <div class="col-12 col-lg-6 d-flex justify-content-center align-items-center">
                                <!-- 中间图片 -->
                                <img src="https://via.placeholder.com/500x400?text=Junte-se+a+nós" alt="Join Us" class="section-2-img img-fluid">
                            </div>
                            <div class="col-12 col-lg-6">
                                <p class="descr">
                                    Nossa missão é oferecer uma plataforma para aqueles que buscam conexões significativas, aprimorar suas habilidades sociais e receber orientações sobre relacionamentos e encontros. Empoderamos as pessoas a embarcar em uma jornada de autodescoberta e cura interior, para que possam encontrar sua alma gêmea.
                                </p>
                                <div class="options">
                                    <a class="big-btn" href="https://diva88.netlify.app/">Join Us</a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- 轮播指示器 -->
            <div class="swiper-pagination"></div>
        </div>
    </div>

    <footer>
        <div class="footer-content">
            <span class="footer-copyright">© Juntos 2024-2025. Todos os direitos reservados</span>
        </div>
    </footer>

    <script>
        // 初始化Swiper
        const swiper = new Swiper('.swiper', {
            direction: 'vertical', // 垂直滑动
            loop: false, // 不循环
            pagination: {
                el: '.swiper-pagination',
                clickable: true, // 允许点击指示器切换
            },
            mousewheel: true, // 允许鼠标滚轮控制
            speed: 600, // 滑动速度
            effect: 'slide', // 滑动效果
        });

        // 图片加载错误时显示备用图片
        document.querySelectorAll('img').forEach(img => {
            img.addEventListener('error', function() {
                this.src = `https://via.placeholder.com/${this.width}x${this.height}?text=Imagem+Indisponível`;
            });
        });
    </script>
</body>
</html>
