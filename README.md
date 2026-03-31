<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>YYZH - 绘画爱好者 · 萌宠治愈站</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        :root {
            --primary-dark: #0a192f;
            --primary-blue: #1e3a5f;
            --accent-gold: #d4af37;
            --light-bg: #f5f7fa;
            --text-light: #e6f1ff;
            --text-dark: #333333;
            --pet-card-bg: #fff9ef;
        }
        
        body {
            background-color: var(--primary-dark);
            color: var(--text-light);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* 头部样式 */
        header {
            padding: 30px 0;
            position: relative;
            overflow: hidden;
        }
        
        .header-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, var(--primary-dark) 0%, var(--primary-blue) 100%);
            z-index: -1;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }
        
        .logo {
            font-size: 2.8rem;
            font-weight: 800;
            background: linear-gradient(to right, var(--accent-gold), #ffd700);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            letter-spacing: 3px;
        }
        
        .logo span {
            font-size: 1.2rem;
            font-weight: 400;
            letter-spacing: 8px;
            margin-left: 10px;
            color: rgba(255, 255, 255, 0.7);
        }
        
        nav ul {
            display: flex;
            list-style: none;
            flex-wrap: wrap;
        }
        
        nav ul li {
            margin-left: 30px;
        }
        
        nav ul li a {
            color: var(--text-light);
            text-decoration: none;
            font-size: 1.1rem;
            transition: color 0.3s;
            padding: 5px 10px;
            border-radius: 4px;
        }
        
        nav ul li a:hover {
            color: var(--accent-gold);
            background-color: rgba(255, 255, 255, 0.1);
        }
        
        /* 主内容区域 */
        .hero {
            padding: 80px 0;
            text-align: center;
            position: relative;
        }
        
        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            line-height: 1.2;
        }
        
        .hero-content h1 span {
            color: var(--accent-gold);
        }
        
        .hero-content p {
            font-size: 1.4rem;
            max-width: 700px;
            margin: 0 auto 40px;
            color: rgba(230, 241, 255, 0.8);
        }
        
        .cta-button {
            display: inline-block;
            background-color: var(--accent-gold);
            color: var(--primary-dark);
            padding: 15px 40px;
            font-size: 1.2rem;
            font-weight: 600;
            text-decoration: none;
            border-radius: 50px;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(212, 175, 55, 0.3);
        }
        
        .cta-button:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(212, 175, 55, 0.4);
        }
        
        /* 关于区域 */
        .section {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 60px;
            position: relative;
        }
        
        .section-title:after {
            content: '';
            position: absolute;
            width: 80px;
            height: 4px;
            background-color: var(--accent-gold);
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .about-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 50px;
        }
        
        .about-text {
            flex: 1;
            min-width: 300px;
        }
        
        .about-text h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--accent-gold);
        }
        
        .about-text p {
            font-size: 1.2rem;
            margin-bottom: 20px;
            color: rgba(230, 241, 255, 0.8);
        }
        
        .about-image {
            flex: 1;
            min-width: 300px;
            text-align: center;
        }
        
        .painting-icon {
            font-size: 15rem;
            color: var(--accent-gold);
            opacity: 0.8;
        }
        
        /* 爱好区域 */
        .hobbies {
            background-color: var(--light-bg);
            color: var(--text-dark);
        }
        
        .hobbies .section-title {
            color: var(--primary-dark);
        }
        
        .hobbies .section-title:after {
            background-color: var(--primary-blue);
        }
        
        .hobby-cards {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 30px;
        }
        
        .hobby-card {
            background-color: white;
            border-radius: 10px;
            padding: 40px 30px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease;
        }
        
        .hobby-card:hover {
            transform: translateY(-10px);
        }
        
        .hobby-card i {
            font-size: 3.5rem;
            color: var(--accent-gold);
            margin-bottom: 25px;
        }
        
        .hobby-card h3 {
            font-size: 1.6rem;
            margin-bottom: 15px;
            color: var(--primary-dark);
        }
        
        .hobby-card p {
            color: #666;
            font-size: 1.1rem;
        }
        
        /* 画廊区域 */
        .gallery {
            padding-bottom: 80px;
        }
        
        .art-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 25px;
        }
        
        .art-item {
            border-radius: 10px;
            overflow: hidden;
            height: 250px;
            position: relative;
            cursor: pointer;
        }
        
        .art-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .art-item:hover img {
            transform: scale(1.1);
        }
        
        .art-item .art-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(10, 25, 47, 0.8);
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .art-item:hover .art-overlay {
            opacity: 1;
        }
        
        .art-overlay h4 {
            font-size: 1.5rem;
            color: var(--accent-gold);
        }
        
        /* ========== 宠物生成器区域 ========== */
        .pet-section {
            background: linear-gradient(135deg, #fef9e6 0%, #fff5e0 100%);
            padding: 80px 0;
        }
        
        .pet-container {
            max-width: 700px;
            margin: 0 auto;
            background: white;
            border-radius: 40px;
            padding: 40px 30px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        
        .pet-header {
            margin-bottom: 30px;
        }
        
        .pet-header h2 {
            font-size: 2rem;
            color: var(--primary-dark);
            margin-bottom: 10px;
        }
        
        .pet-header p {
            color: #8b6b4d;
            font-size: 1.1rem;
        }
        
        .pet-header i {
            color: var(--accent-gold);
            margin-right: 8px;
        }
        
        /* 切换按钮组 */
        .pet-tabs {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 30px;
            flex-wrap: wrap;
        }
        
        .pet-tab {
            padding: 10px 25px;
            font-size: 1rem;
            font-weight: 600;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            background: #f0f0f0;
            color: #555;
        }
        
        .pet-tab.active {
            background: var(--accent-gold);
            color: var(--primary-dark);
            box-shadow: 0 4px 12px rgba(212, 175, 55, 0.3);
        }
        
        .pet-tab:hover:not(.active) {
            background: #e0e0e0;
            transform: translateY(-2px);
        }
        
        /* 图片区域 */
        .pet-image-container {
            background: #faf7f0;
            border-radius: 30px;
            padding: 30px;
            margin-bottom: 25px;
            min-height: 380px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .pet-image {
            max-width: 100%;
            max-height: 350px;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
            transition: opacity 0.3s ease;
            object-fit: contain;
        }
        
        .pet-image.fade-in {
            animation: fadeIn 0.4s ease-in-out;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: scale(0.98); }
            to { opacity: 1; transform: scale(1); }
        }
        
        /* 加载状态 */
        .loading-state {
            text-align: center;
            padding: 60px 20px;
        }
        
        .loading-spinner {
            display: inline-block;
            width: 50px;
            height: 50px;
            border: 4px solid #f0e0c0;
            border-top-color: var(--accent-gold);
            border-radius: 50%;
            animation: spin 0.8s linear infinite;
            margin-bottom: 15px;
        }
        
        @keyframes spin {
            to { transform: rotate(360deg); }
        }
        
        .loading-text {
            font-size: 1.2rem;
            color: #8b6b4d;
        }
        
        /* 换一张按钮 */
        .refresh-btn {
            background: linear-gradient(135deg, var(--primary-dark), var(--primary-blue));
            color: white;
            border: none;
            padding: 14px 35px;
            font-size: 1.1rem;
            font-weight: 600;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }
        
        .refresh-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        .refresh-btn:active {
            transform: translateY(0);
        }
        
        /* 错误提示 */
        .error-message {
            background: #ffe0e0;
            color: #c44;
            padding: 20px;
            border-radius: 20px;
            text-align: center;
        }
        
        /* 页脚 */
        footer {
            background-color: var(--primary-blue);
            padding: 60px 0 30px;
            text-align: center;
        }
        
        .contact-info {
            margin-bottom: 40px;
        }
        
        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--accent-gold);
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }
        
        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            background-color: rgba(255, 255, 255, 0.1);
            color: var(--text-light);
            border-radius: 50%;
            font-size: 1.3rem;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background-color: var(--accent-gold);
            color: var(--primary-dark);
            transform: translateY(-5px);
        }
        
        .copyright {
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: rgba(230, 241, 255, 0.7);
            font-size: 0.9rem;
        }
        
        /* 响应式设计 */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 20px;
                justify-content: center;
            }
            
            nav ul li {
                margin: 5px 10px;
            }
            
            .hero-content h1 {
                font-size: 2.5rem;
            }
            
            .hero-content p {
                font-size: 1.2rem;
            }
            
            .painting-icon {
                font-size: 10rem;
            }
            
            .pet-container {
                padding: 25px 20px;
            }
            
            .pet-tabs {
                gap: 10px;
            }
            
            .pet-tab {
                padding: 8px 18px;
                font-size: 0.9rem;
            }
        }
        
        @media (max-width: 480px) {
            .logo {
                font-size: 2.2rem;
            }
            
            .hero {
                padding: 60px 0;
            }
            
            .hero-content h1 {
                font-size: 2rem;
            }
            
            .section {
                padding: 60px 0;
            }
            
            .section-title {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- 头部区域 -->
    <header>
        <div class="header-bg"></div>
        <div class="container header-content">
            <div class="logo">YYZH<span>绘画爱好者</span></div>
            <nav>
                <ul>
                    <li><a href="#home">首页</a></li>
                    <li><a href="#about">关于我</a></li>
                    <li><a href="#hobbies">我的爱好</a></li>
                    <li><a href="#gallery">作品集</a></li>
                    <li><a href="#pet">萌宠治愈站</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- 主内容区域 -->
    <section class="hero" id="home">
        <div class="container hero-content">
            <h1>你好，我是<span>YYZH</span></h1>
            <p>一位热爱绘画的创作者，用色彩和线条表达内心的世界，探索艺术与美的无限可能。</p>
            <a href="#gallery" class="cta-button">查看我的作品</a>
        </div>
    </section>

    <!-- 关于区域 -->
    <section class="section" id="about">
        <div class="container">
            <h2 class="section-title">关于我</h2>
            <div class="about-content">
                <div class="about-text">
                    <h3>用画笔记录生活，用色彩表达情感</h3>
                    <p>我是YYZH，从记事起就开始画画。对我来说，绘画不仅仅是一种爱好，更是一种表达内心世界的方式，一种与自我对话的途径。</p>
                    <p>我擅长水彩画、素描和数字绘画，喜欢尝试不同的艺术风格和技巧。我的作品灵感来源于日常生活、自然景观以及内心情感。</p>
                    <p>在绘画的世界里，每一笔每一划都是思想的延伸，每一抹色彩都是情感的流露。我享受在画布上创造新世界的过程，也乐于与他人分享我的艺术视角。</p>
                </div>
                <div class="about-image">
                    <i class="fas fa-palette painting-icon"></i>
                </div>
            </div>
        </div>
    </section>

    <!-- 爱好区域 -->
    <section class="section hobbies" id="hobbies">
        <div class="container">
            <h2 class="section-title">我的爱好</h2>
            <div class="hobby-cards">
                <div class="hobby-card">
                    <i class="fas fa-paint-brush"></i>
                    <h3>水彩绘画</h3>
                    <p>喜欢水彩画的透明感和流动性，它能创造出独特而柔和的色彩效果，特别适合表现自然风景和情感表达。</p>
                </div>
                <div class="hobby-card">
                    <i class="fas fa-pencil-alt"></i>
                    <h3>素描与速写</h3>
                    <p>随身携带素描本，随时记录生活中的美好瞬间。素描是基础，也是观察力与表现力的最好训练。</p>
                </div>
                <div class="hobby-card">
                    <i class="fas fa-laptop"></i>
                    <h3>数字艺术</h3>
                    <p>探索数字绘画的无限可能，使用平板和绘图软件创作插画和概念艺术，结合传统技法与现代技术。</p>
                </div>
                <div class="hobby-card">
                    <i class="fas fa-book-open"></i>
                    <h3>艺术史研究</h3>
                    <p>研究不同时期和文化的艺术发展，从古典到现代，从东方到西方，汲取灵感并理解艺术的演变。</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 画廊区域 -->
    <section class="section gallery" id="gallery">
        <div class="container">
            <h2 class="section-title">作品展示</h2>
            <div class="art-grid">
                <div class="art-item">
                    <img src="https://images.unsplash.com/photo-1541961017774-22349e4a1262?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="水彩风景画">
                    <div class="art-overlay"><h4>水彩风景</h4></div>
                </div>
                <div class="art-item">
                    <img src="https://images.unsplash.com/photo-1578301978693-85fa9c0320b9?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="素描肖像">
                    <div class="art-overlay"><h4>素描肖像</h4></div>
                </div>
                <div class="art-item">
                    <img src="https://images.unsplash.com/photo-1542744095-fcf48d80b0fd?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="抽象艺术">
                    <div class="art-overlay"><h4>抽象艺术</h4></div>
                </div>
                <div class="art-item">
                    <img src="https://images.unsplash.com/photo-1513475382585-d06e58bcb0e0?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="数字绘画">
                    <div class="art-overlay"><h4>数字绘画</h4></div>
                </div>
            </div>
        </div>
    </section>

    <!-- ========== 随机宠物生成器区域 ========== -->
    <section class="pet-section" id="pet">
        <div class="container">
            <div class="pet-container">
                <div class="pet-header">
                    <h2><i class="fas fa-paw"></i> 萌宠治愈站</h2>
                    <p>每天吸一口，快乐一整天 ✨</p>
                </div>
                
                <div class="pet-tabs">
                    <button class="pet-tab active" data-type="random">🐕‍🦺 随机</button>
                    <button class="pet-tab" data-type="dog">🐕 只看狗狗</button>
                    <button class="pet-tab" data-type="cat">🐈 只看猫咪</button>
                </div>
                
                <div class="pet-image-container" id="petImageContainer">
                    <div class="loading-state" id="loadingState">
                        <div class="loading-spinner"></div>
                        <div class="loading-text" id="loadingText">🐕 汪汪加载中…</div>
                    </div>
                    <img id="petImage" class="pet-image" style="display: none;" alt="可爱宠物">
                </div>
                
                <button class="refresh-btn" id="refreshBtn">
                    <i class="fas fa-sync-alt"></i> 换一张
                </button>
            </div>
        </div>
    </section>

    <!-- 页脚 -->
    <footer>
        <div class="container">
            <div class="contact-info">
                <h3>联系我</h3>
                <p>如果你对我的作品感兴趣，或者想要交流艺术心得，欢迎与我联系！</p>
                <div class="social-links">
                    <a href="#"><i class="fab fa-weixin"></i></a>
                    <a href="#"><i class="fab fa-weibo"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="far fa-envelope"></i></a>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 YYZH 个人主页. 保留所有权利. 设计灵感来源于对艺术和萌宠的热爱</p>
            </div>
        </div>
    </footer>

    <script>
        // ========== 原有交互 ==========
        // 平滑滚动
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // 画廊图片悬停效果
        const artItems = document.querySelectorAll('.art-item');
        artItems.forEach(item => {
            item.addEventListener('mouseenter', function() {
                this.style.transform = 'scale(1.05)';
                this.style.transition = 'transform 0.3s ease';
            });
            item.addEventListener('mouseleave', function() {
                this.style.transform = 'scale(1)';
            });
        });
        
        // 页面加载动画
        window.addEventListener('load', function() {
            document.body.style.opacity = '0';
            document.body.style.transition = 'opacity 0.5s ease';
            setTimeout(() => {
                document.body.style.opacity = '1';
            }, 100);
        });
        
        // ========== 宠物生成器逻辑 ==========
        let currentPetType = 'random'; // random, dog, cat
        let isLoading = false;
        
        const petImage = document.getElementById('petImage');
        const loadingState = document.getElementById('loadingState');
        const loadingText = document.getElementById('loadingText');
        const refreshBtn = document.getElementById('refreshBtn');
        const tabs = document.querySelectorAll('.pet-tab');
        
        // 设置加载状态文本
        function setLoadingText(type) {
            if (type === 'dog') {
                loadingText.textContent = '🐕 汪汪加载中…';
            } else if (type === 'cat') {
                loadingText.textContent = '🐈 喵喵加载中…';
            } else {
                loadingText.textContent = '🐕‍🦺 萌宠加载中…';
            }
        }
        
        // 显示加载状态
        function showLoading() {
            loadingState.style.display = 'block';
            petImage.style.display = 'none';
        }
        
        // 隐藏加载状态，显示图片
        function hideLoading() {
            loadingState.style.display = 'none';
            petImage.style.display = 'block';
        }
        
        // 显示错误
        function showError(message) {
            loadingState.style.display = 'block';
            petImage.style.display = 'none';
            loadingText.innerHTML = `<i class="fas fa-exclamation-triangle" style="margin-right: 8px;"></i> ${message}`;
            setTimeout(() => {
                if (isLoading === false) {
                    setLoadingText(currentPetType);
                }
            }, 2000);
        }
        
        // 添加淡入动画
        function addFadeAnimation(imgElement) {
            imgElement.classList.remove('fade-in');
            void imgElement.offsetWidth; // 强制重绘
            imgElement.classList.add('fade-in');
        }
        
        // 获取随机狗狗图片
        async function fetchRandomDog() {
            const response = await fetch('https://dog.ceo/api/breeds/image/random');
            if (!response.ok) throw new Error('狗狗API请求失败');
            const data = await response.json();
            if (data.status !== 'success') throw new Error('获取狗狗图片失败');
            return data.message;
        }
        
        // 获取随机猫咪图片
        async function fetchRandomCat() {
            const response = await fetch('https://api.thecatapi.com/v1/images/search');
            if (!response.ok) throw new Error('猫咪API请求失败');
            const data = await response.json();
            if (!data || data.length === 0) throw new Error('获取猫咪图片失败');
            return data[0].url;
        }
        
        // 获取随机宠物（随机选择狗或猫）
        async function fetchRandomPet() {
            const isDog = Math.random() < 0.5;
            if (isDog) {
                const url = await fetchRandomDog();
                return { url, type: 'dog' };
            } else {
                const url = await fetchRandomCat();
                return { url, type: 'cat' };
            }
        }
        
        // 根据当前类型获取图片
        async function fetchPetImage() {
            if (currentPetType === 'dog') {
                const url = await fetchRandomDog();
                return { url, type: 'dog' };
            } else if (currentPetType === 'cat') {
                const url = await fetchRandomCat();
                return { url, type: 'cat' };
            } else {
                return await fetchRandomPet();
            }
        }
        
        // 加载并显示新图片
        async function loadNewPet() {
            if (isLoading) return;
            isLoading = true;
            
            setLoadingText(currentPetType);
            showLoading();
            
            try {
                const { url, type } = await fetchPetImage();
                
                // 预加载图片
                const img = new Image();
                await new Promise((resolve, reject) => {
                    img.onload = resolve;
                    img.onerror = reject;
                    img.src = url;
                });
                
                petImage.src = url;
                addFadeAnimation(petImage);
                hideLoading();
                
            } catch (error) {
                console.error('加载宠物图片失败:', error);
                showError('网络出问题啦！点击换一张重试~');
            } finally {
                isLoading = false;
            }
        }
        
        // 切换标签
        function switchTab(type) {
            currentPetType = type;
            
            // 更新标签样式
            tabs.forEach(tab => {
                if (tab.getAttribute('data-type') === type) {
                    tab.classList.add('active');
                } else {
                    tab.classList.remove('active');
                }
            });
            
            // 重新加载图片
            loadNewPet();
        }
        
        // 绑定事件
        refreshBtn.addEventListener('click', () => {
            loadNewPet();
        });
        
        tabs.forEach(tab => {
            tab.addEventListener('click', () => {
                const type = tab.getAttribute('data-type');
                if (type !== currentPetType) {
                    switchTab(type);
                }
            });
        });
        
        // 页面加载后自动获取第一张图片
        loadNewPet();
    </script>
</body>
</html>
