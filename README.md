<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <title>Encontros - Conexões Significativas</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- 引入Swiper CSS和JS -->
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
        /* 其他样式 */
    </style>
</head>
<body>
    <!-- Swiper容器和内容 -->
    <div class="swiper">...</div>
    <script>
        // 初始化Swiper
        const swiper = new Swiper('.swiper', {
            direction: 'vertical',
            pagination: { el: '.swiper-pagination', clickable: true },
            mousewheel: true
        });
    </script>
</body>
</html>
