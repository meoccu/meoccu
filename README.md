## Hi there 👋
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>✨ O Meow · GitHub Profile Preview ✨</title>
    <!-- Google Fonts 引入优雅字体 -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
    <!-- Font Awesome 6 (免费图标库) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(145deg, #f9fafc 0%, #f1f5f9 100%);
            font-family: 'Inter', sans-serif;
            color: #0f172a;
            padding: 2rem 1.5rem;
        }

        /* 主容器: 呼吸感边距 + 最大宽度优雅居中 */
        .container {
            max-width: 1300px;
            margin: 0 auto;
            background: rgba(255,255,255,0.5);
            backdrop-filter: blur(2px);
            border-radius: 3rem;
            padding: 2rem 2rem 3rem;
            box-shadow: 0 25px 45px -12px rgba(0,0,0,0.08);
        }

        /* 顶部导航区 (简约致敬GitHub社区) */
        .top-bar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1rem;
            margin-bottom: 2rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid rgba(100,116,139,0.2);
        }
        .logo-area {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .github-icon {
            font-size: 2rem;
            color: #1f2937;
            transition: all 0.2s ease;
        }
        .logo-text {
            font-weight: 700;
            font-size: 1.25rem;
            background: linear-gradient(135deg, #1e293b, #3b82f6);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            letter-spacing: -0.3px;
        }
        .badge-tag {
            background: #eef2ff;
            padding: 0.3rem 1rem;
            border-radius: 40px;
            font-size: 0.8rem;
            font-weight: 500;
            color: #2563eb;
            box-shadow: 0 1px 2px rgba(0,0,0,0.02);
        }

        /* 英雄区 Header —— 个人品牌 */
        .hero {
            background: linear-gradient(115deg, #ffffff 0%, #fef9e6 100%);
            border-radius: 2rem;
            padding: 2rem 2rem;
            margin-bottom: 2.5rem;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0 8px 20px rgba(0,0,0,0.02), 0 2px 4px rgba(0,0,0,0.02);
            border: 1px solid rgba(255,255,240,0.8);
        }
        .profile-intro h1 {
            font-size: 2.4rem;
            font-weight: 800;
            background: linear-gradient(130deg, #0f172a, #2563eb);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            letter-spacing: -0.02em;
        }
        .username {
            font-family: 'JetBrains Mono', monospace;
            background: #e9ecef;
            display: inline-block;
            padding: 0.2rem 1rem;
            border-radius: 40px;
            font-size: 0.9rem;
            font-weight: 500;
            margin-top: 0.5rem;
            color: #1e293b;
        }
        .hero-desc {
            margin-top: 1rem;
            max-width: 450px;
            color: #334155;
            line-height: 1.5;
        }
        .profile-avatar {
            background: white;
            width: 100px;
            height: 100px;
            border-radius: 40% 60% 65% 35% / 45% 40% 60% 55%;
            background: linear-gradient(145deg, #fbcfe8, #bae6fd);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3.4rem;
            box-shadow: 0 20px 30px -15px rgba(0,0,0,0.1);
            transition: transform 0.25s ease;
        }
        .profile-avatar:hover {
            transform: scale(1.02);
        }
        .profile-avatar i {
            filter: drop-shadow(0 4px 6px rgba(0,0,0,0.1));
        }

        /* 打字机动效模拟区 (文章第10点) */
        .typing-area {
            background: #0f172a;
            border-radius: 1.5rem;
            padding: 1rem 1.8rem;
            margin-bottom: 2rem;
            display: flex;
            align-items: center;
            gap: 1rem;
            flex-wrap: wrap;
            box-shadow: 0 5px 12px rgba(0,0,0,0.05);
        }
        .typing-text {
            font-family: 'JetBrains Mono', monospace;
            font-size: 1.2rem;
            color: #e2e8f0;
        }
        .cursor-blink {
            background: #3b82f6;
            width: 3px;
            height: 1.4rem;
            display: inline-block;
            animation: blink 1s infinite;
        }
        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0; }
        }

        /* 卡片通用样式 */
        .section-title {
            font-size: 1.6rem;
            font-weight: 600;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 0.6rem;
            color: #0f172a;
            letter-spacing: -0.3px;
        }
        .section-title i {
            background: #eef2ff;
            padding: 0.4rem;
            border-radius: 14px;
            color: #2563eb;
        }
        .card-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.8rem;
            margin-bottom: 2.2rem;
        }
        .card {
            background: rgba(255,255,255,0.9);
            backdrop-filter: blur(4px);
            border-radius: 1.8rem;
            padding: 1.5rem 1.4rem;
            box-shadow: 0 6px 14px rgba(0,0,0,0.02), 0 1px 2px rgba(0,0,0,0.03);
            transition: all 0.25s;
            border: 1px solid rgba(203,213,225,0.5);
        }
        .card:hover {
            transform: translateY(-4px);
            box-shadow: 0 20px 28px -12px rgba(0,0,0,0.1);
            border-color: rgba(59,130,246,0.3);
            background: white;
        }
        .card h3 {
            font-size: 1.3rem;
            margin-bottom: 1rem;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            border-left: 3px solid #3b82f6;
            padding-left: 0.75rem;
        }
        .stats-img {
            width: 100%;
            border-radius: 24px;
            margin: 0.5rem 0;
            background: #f8fafc;
            padding: 0.2rem;
        }
        .badge-cloud {
            display: flex;
            flex-wrap: wrap;
            gap: 0.6rem;
            margin-top: 1rem;
        }
        .badge-cloud img {
            height: 28px;
            transition: all 0.15s;
        }
        .visitor-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 1rem;
        }
        .streak-card {
            text-align: center;
        }

        /* 双列混合布局区域 (奖杯+活动图 或 额外) */
        .double-col {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.8rem;
            margin-bottom: 2rem;
        }
        @media (max-width: 760px) {
            .double-col {
                grid-template-columns: 1fr;
            }
            .hero {
                flex-direction: column;
                text-align: center;
                gap: 1.5rem;
            }
        }

        .footer-note {
            text-align: center;
            margin-top: 3rem;
            padding-top: 1.5rem;
            border-top: 1px solid rgba(100,116,139,0.2);
            font-size: 0.85rem;
            color: #475569;
            display: flex;
            justify-content: center;
            gap: 1rem;
            flex-wrap: wrap;
        }
        .footer-note a {
            text-decoration: none;
            color: #2563eb;
            font-weight: 500;
        }
        hr {
            margin: 1rem 0;
            border-color: #e2e8f0;
        }

        /* 小工具适配 */
        iframe, .card img {
            max-width: 100%;
            border-radius: 16px;
        }
    </style>
</head>
<body>
<div class="container">
    <!-- 导航栏 轻拟态 -->
    <div class="top-bar">
        <div class="logo-area">
            <i class="fab fa-github github-icon"></i>
            <span class="logo-text">GitHub Profile · 灵感工坊</span>
        </div>
        <div class="badge-tag">
            <i class="fas fa-cat"></i> 献给所有热爱美化的开发者
        </div>
    </div>

    <!-- 英雄区 用户名 & 昵称 精准植入 -->
    <div class="hero">
        <div class="profile-intro">
            <h1>🐾 O Meow · 姜饼猫的代码宇宙</h1>
            <div class="username">
                <i class="fab fa-github-alt"></i> @meoccu
            </div>
            <div class="hero-desc">
                热爱优雅的代码与设计，追求实用与美感的平衡。<br>
                这里是我的 GitHub 动态仪表板，每天进步一点点✨
            </div>
        </div>
        <div class="profile-avatar">
            <i class="fas fa-cat" style="font-size: 3rem; color:#1e293b;"></i>
        </div>
    </div>

    <!-- 打字特效 参考文章第10点 炫酷动态 -->
    <div class="typing-area">
        <i class="fas fa-terminal" style="color:#60a5fa; font-size: 1.5rem;"></i>
        <div class="typing-text">
            <span id="dynamicTyping">console.log("Hello, world!")</span>
            <span class="cursor-blink"></span>
        </div>
        <span style="font-size:0.75rem; color:#94a3b8; margin-left:auto;">✨ 动态效果 · README 同款</span>
    </div>

    <!-- 1. Metrics 信息统计 与 GitHub Stats Card 双卡片布局 (满足 metrics 和 stats card) -->
    <div class="section-title">
        <i class="fas fa-chart-line"></i> 核心 · GitHub 数据仪表盘
    </div>
    <div class="card-grid">
        <!-- Metrics 经典卡片 -->
        <div class="card">
            <h3><i class="fas fa-chart-pie"></i> Metrics 全景</h3>
            <p style="font-size: 0.8rem; color:#475569; margin-bottom: 0.5rem;">综合贡献、仓库活动数据</p>
            <img class="stats-img" src="https://metrics.lecoq.io/meoccu?template=classic&config.timezone=Asia%2FShanghai" alt="Metrics for meoccu" loading="lazy">
            <div style="margin-top: 0.8rem; font-size:0.7rem; background:#f1f5f9; padding:6px 12px; border-radius: 50px;">
                <i class="fas fa-sync-alt"></i> 动态更新 · 来自 metrics.lecoq.io
            </div>
        </div>
        <!-- GitHub Stats Card  -->
        <div class="card">
            <h3><i class="fas fa-chart-simple"></i> GitHub Stats Card</h3>
            <p style="margin-bottom: 8px;">🔥 提交、PR、Stars 总和</p>
            <img class="stats-img" src="https://github-readme-stats.vercel.app/api?username=meoccu&show_icons=true&theme=radical&hide_border=true&bg_color=ffffff00&icon_color=ef4444" alt="GitHub Stats Card">
            <div class="badge-cloud">
                <i class="fas fa-star" style="color:#facc15;"></i> 动态实时生成
            </div>
        </div>
    </div>

    <!-- 第二排：Most used languages + 访客徽章 + Shields.io 融合布局 好看协调 -->
    <div class="card-grid">
        <!-- 语言统计卡片 -->
        <div class="card">
            <h3><i class="fas fa-code"></i> 常用语言图谱</h3>
            <img class="stats-img" src="https://github-readme-stats.vercel.app/api/top-langs/?username=meoccu&layout=compact&hide_border=true&langs_count=8&theme=vue" alt="Top Languages">
            <div class="visitor-row">
                <span><i class="fas fa-eye"></i> 访客徽章 · 页面温度</span>
                <img src="https://visitor-badge.glitch.me/badge?page_id=meoccu.github.profile" alt="visitor badge" style="border-radius: 30px;">
            </div>
        </div>
        <!-- 技术栈徽章 Shields.io 区域 原文提到的CSS/HTML/JS徽章更精致 -->
        <div class="card">
            <h3><i class="fas fa-crown"></i> 技术 · 流光徽章</h3>
            <div class="badge-cloud">
                <img src="https://img.shields.io/badge/-HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" alt="HTML5">
                <img src="https://img.shields.io/badge/-CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" alt="CSS3">
                <img src="https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript">
                <img src="https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=black" alt="React">
                <img src="https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
                <img src="https://img.shields.io/badge/-Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind">
                <img src="https://img.shields.io/badge/-Vue-4FC08D?style=flat-square&logo=vue.js&logoColor=white" alt="Vue">
            </div>
            <p style="font-size:0.75rem; margin-top: 1rem;"><i class="fas fa-palette"></i> shields.io 动态徽章，开源项目加持</p>
        </div>
    </div>

    <!-- 双列豪华布局: 奖杯 + 活动统计图(Github Readme Activity Graph) + 连续打卡(Streak) 紧凑且协调 -->
    <div class="double-col">
        <div class="card">
            <h3><i class="fas fa-trophy"></i> GitHub 成就奖杯</h3>
            <img src="https://github-profile-trophy.vercel.app/?username=meoccu&theme=onedark&no-frame=true&row=2&column=3" alt="trophy" style="width:100%; border-radius: 20px;">
        </div>
        <div class="card">
            <h3><i class="fas fa-chart-line"></i> 31日活跃热力 · Activity Graph</h3>
            <img src="https://activity-graph.herokuapp.com/graph?username=meoccu&theme=github-light&area=true&hide_border=true" alt="activity graph" style="width:100%; border-radius: 18px;">
        </div>
    </div>

    <!-- 第三行 连续打卡 streak 与 社交统计示例 部分社交卡片 -->
    <div class="card-grid">
        <div class="card streak-card">
            <h3><i class="fas fa-fire"></i> 坚持打卡 · Git Streak</h3>
            <img src="https://github-readme-streak-stats.herokuapp.com/?user=meoccu&theme=ayu-mirage&hide_border=true" alt="streak stats" style="width:100%; border-radius: 1rem;">
            <p style="margin-top: 0.5rem;"><i class="fas fa-calendar-alt"></i> 连续贡献的勋章轨迹</p>
        </div>
        <!-- 社交统计 + 原文章提到的额外卡片风格 csdn 或 b站等 用一个优雅占位符展示友好 -->
        <div class="card">
            <h3><i class="fas fa-share-alt"></i> 灵感社交 · 开发日常</h3>
            <div style="display: flex; gap: 15px; flex-wrap: wrap; margin: 1rem 0;">
                <span><i class="fab fa-twitter" style="color:#1DA1F2;"></i> @meoccu_dev</span>
                <span><i class="fab fa-bilibili"></i> 喵喵码日常</span>
                <span><i class="fab fa-dev"></i> dev.to/meoccu</span>
            </div>
            <!-- 模拟其他社交统计卡片 —— 令整体更饱满 -->
            <img src="https://stats.justsong.cn/api/csdn?username=meoccu_example" alt="social stats placeholder" style="border-radius: 40px; opacity:0.7; background:#f1f5f9; padding: 6px;" onerror="this.src='https://via.placeholder.com/300x80?text=✨+社交+数据+即将连接+✨'">
            <p class="visitor-row"><i class="fas fa-mug-hot"></i> 全平台创意开发者 O Meow</p>
        </div>
    </div>

    <!-- 额外小彩蛋: 优秀案例致敬 + 拿来主义精神 -->
    <div class="card" style="background: linear-gradient(115deg,#faf5ff, #f3e8ff);">
        <h3><i class="fas fa-hand-peace"></i> ✨ 拿来主义 · 灵感共鸣 ✨</h3>
        <p>“我们要运用脑髓，放出眼光，自己来拿！” —— 致敬开源社区，感谢 Metrics、github-readme-stats、活动图等优秀项目。我的用户名 meoccu，昵称 O Meow 在此展示协调之美。</p>
        <div style="display: flex; gap: 1rem; margin-top: 1rem;">
            <i class="fab fa-github"></i> 教程核心贡献: Metrics · 统计卡片 · 访客徽章 · 打字动画
        </div>
    </div>

    <div class="footer-note">
        <span><i class="far fa-copyright"></i> 设计灵感源自腾讯云 · Github首页美化教程 | 用户名 meoccu 动态展示</span>
        <a href="#"><i class="fab fa-markdown"></i> README.md 风格参考</a>
        <a href="#"><i class="fas fa-cat"></i> O Meow · 让个人主页更有趣</a>
    </div>
</div>

<script>
    // 动态打字特效 来自教程第十点 增强协调感
    const phrases = [
        "git commit -m '✨ fresh design'",
        "npm install beautiful-profile",
        "echo 'hello O Meow'",
        "Metrics loaded · stats updated",
        "🐱 meoccu's creative space"
    ];
    let idx = 0;
    let charIndex = 0;
    let currentText = "";
    let isDeleting = false;
    const typingSpan = document.getElementById("dynamicTyping");
    function typeEffect() {
        if (!typingSpan) return;
        const fullText = phrases[idx % phrases.length];
        if (isDeleting) {
            currentText = fullText.substring(0, charIndex - 1);
            charIndex--;
        } else {
            currentText = fullText.substring(0, charIndex + 1);
            charIndex++;
        }
        typingSpan.innerText = currentText;
        if (!isDeleting && charIndex === fullText.length) {
            isDeleting = true;
            setTimeout(typeEffect, 1800);
            return;
        }
        if (isDeleting && charIndex === 0) {
            isDeleting = false;
            idx++;
            setTimeout(typeEffect, 400);
            return;
        }
        const speed = isDeleting ? 60 : 100;
        setTimeout(typeEffect, speed);
    }
    setTimeout(typeEffect, 300);
</script>
</body>
</html>
