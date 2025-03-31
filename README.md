# mariposa.yun
Abstract Art Gallery
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mariposa | 抽象艺术画廊</title>
    <style>
        :root {
            --gallery-white: #F8F5F2;
            --bronze-gold: #D4AF37;
            --black-hole: #1A1A1A;
            --thought-gray: #5C5C5C;
            --artwork-bg: #111213;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', -apple-system, sans-serif;
        }
        
        body {
            background-color: var(--gallery-white);
            color: var(--black-hole);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        header {
            padding: 2rem;
            text-align: center;
            border-bottom: 1px solid rgba(0,0,0,0.1);
        }
        
        .logo {
            font-size: 2.5rem;
            font-weight: 300;
            letter-spacing: 0.5rem;
            margin-bottom: 1rem;
        }
        
        .tagline {
            font-size: 1.1rem;
            max-width: 600px;
            margin: 0 auto;
            color: var(--thought-gray);
        }
        
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
            padding: 3rem;
        }
        
        .artwork {
            position: relative;
            overflow: hidden;
            height: 400px;
            background-color: var(--artwork-bg);
            transition: transform 0.3s ease;
        }
        
        .artwork:hover {
            transform: translateY(-5px);
        }
        
        .artwork-img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            opacity: 0.9;
            transition: opacity 0.3s ease;
        }
        
        .artwork:hover .artwork-img {
            opacity: 1;
        }
        
        .artwork-info {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(to top, rgba(0,0,0,0.8), transparent);
            padding: 1.5rem;
            color: white;
        }
        
        .artwork-title {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }
        
        .artwork-desc {
            font-size: 0.9rem;
            opacity: 0.8;
            margin-bottom: 1rem;
        }
        
        .purchase-btn {
            background: transparent;
            border: 1px solid var(--bronze-gold);
            color: white;
            padding: 0.5rem 1.5rem;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 0.9rem;
        }
        
        .purchase-btn:hover {
            background: rgba(212, 175, 55, 0.2);
        }
        
        footer {
            text-align: center;
            padding: 3rem;
            color: var(--thought-gray);
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            .gallery {
                grid-template-columns: 1fr;
                padding: 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="logo">MARIPOSA</div>
        <div class="tagline">抽象艺术不是"看不懂"，而是"看见自己"——你的情绪，藏在Mariposa的色彩里</div>
    </header>
    
    <main class="gallery">
        <!-- 艺术作品1 -->
        <div class="artwork">
            <img src="https://source.unsplash.com/random/600x800/?abstract,painting,1" alt="抽象艺术作品" class="artwork-img">
            <div class="artwork-info">
                <h3 class="artwork-title">《她决定在周一爆炸》</h3>
                <p class="artwork-desc">当克莱因蓝遇见梵高黄——这是颜料在画布上的爵士即兴</p>
                <button class="purchase-btn">认领这片色彩 →</button>
            </div>
        </div>
        
        <!-- 艺术作品2 -->
        <div class="artwork">
            <img src="https://source.unsplash.com/random/600x800/?abstract,painting,2" alt="抽象艺术作品" class="artwork-img">
            <div class="artwork-info">
                <h3 class="artwork-title">《当孤独变成紫色》</h3>
                <p class="artwork-desc">MIT色彩实验室证实：这组靛青+铬橙会刺激大脑杏仁核</p>
                <button class="purchase-btn">捕捉这段波长 →</button>
            </div>
        </div>
        
        <!-- 艺术作品3 -->
        <div class="artwork">
            <img src="https://source.unsplash.com/random/600x800/?abstract,painting,3" alt="抽象艺术作品" class="artwork-img">
            <div class="artwork-info">
                <h3 class="artwork-title">《上帝忘了上色的角落》</h3>
                <p class="artwork-desc">2142年火星殖民地批准的治愈色组，仅存3天原始波长</p>
                <button class="purchase-btn">收藏宇宙碎片 →</button>
            </div>
        </div>
    </main>
    
    <footer>
        <p>© 2024 Mariposa 抽象艺术 | 每幅作品都是宇宙的唯一碎片</p>
    </footer>

    <script>
        // 交互效果
        document.querySelectorAll('.artwork').forEach(item => {
            item.addEventListener('mouseenter', function() {
                const colors = ['#D4AF37', '#59C3C3', '#EB8258'];
                const randomColor = colors[Math.floor(Math.random() * colors.length)];
                this.querySelector('.purchase-btn').style.borderColor = randomColor;
            });
            
            item.addEventListener('mouseleave', function() {
                this.querySelector('.purchase-btn').style.borderColor = '#D4AF37';
            });
        });
    </script>
</body>
</html>
