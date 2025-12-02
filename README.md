<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>withAI | 助成金活用型 AI人材育成プログラム</title>
    <meta name="description" content="中小企業の経営者・役員層に特化した、実践的AI活用ビデオプログラム。人材開発支援助成金を活用し、大幅なコスト削減を実現します。">
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;700&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
    
    <style>
        /* =========================================
           基本設定 / カラーパレット
           ========================================= */
        :root {
            --color-navy: #0F172A;       /* ベースカラー */
            --color-navy-light: #1E293B; 
            --color-gold: #C29B40;       /* アクセント */
            --color-gold-hover: #D4AF37; 
            --color-gold-light: #FDF8E8; 
            --color-red: #DC2626;        /* 強調 */
            
            --color-text-body: #334155;
            --color-text-white: #FFFFFF;
            --color-bg-light: #F8FAFC;
            
            --font-main: "Noto Sans JP", sans-serif;
            --font-serif: "Playfair Display", serif; /* Qアイコン用 */
            --max-width: 1080px;         
            
            --btn-shadow: 0 4px 15px rgba(194, 155, 64, 0.4);
            --easing: cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }

        /* リセットCSS */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body {
            font-family: var(--font-main);
            color: var(--color-text-body);
            line-height: 1.8;
            background-color: var(--color-bg-light);
            font-size: 16px;
            padding-bottom: 80px;
        }

        a { text-decoration: none; color: inherit; transition: 0.3s; }
        img { max-width: 100%; height: auto; display: block; object-fit: cover; }
        ul { list-style: none; }

        /* =========================================
           共通コンポーネント
           ========================================= */
        .container {
            max-width: var(--max-width);
            margin: 0 auto;
            padding: 0 24px;
        }

        .section {
            padding: 100px 0;
        }

        .section-header {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title {
            font-size: 2.2rem;
            color: var(--color-navy);
            font-weight: 700;
            margin-bottom: 16px;
            position: relative;
            display: inline-block;
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 3px;
            background-color: var(--color-gold);
            margin: 16px auto 0;
        }

        .section-subtitle {
            font-size: 1rem;
            color: #64748B;
        }

        .btn-cta {
            display: inline-block;
            background: linear-gradient(135deg, var(--color-gold) 0%, #B08D38 100%);
            color: white;
            font-weight: 700;
            font-size: 1.1rem;
            padding: 18px 48px;
            border-radius: 4px;
            box-shadow: var(--btn-shadow);
            text-align: center;
            letter-spacing: 0.05em;
            width: 100%;
            max-width: 320px;
            transition: transform 0.3s var(--easing), box-shadow 0.3s var(--easing);
        }

        .btn-cta:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(194, 155, 64, 0.6);
            opacity: 0.95;
        }
        
        .btn-cta small {
            display: block;
            font-size: 0.8em;
            font-weight: 500;
            margin-bottom: 4px;
            opacity: 0.9;
        }

        @media (max-width: 768px) {
            .section { padding: 60px 0; }
            .section-title { font-size: 1.75rem; }
            .container { padding: 0 20px; }
        }

        /* =========================================
           ヘッダー
           ========================================= */
        header {
            background-color: white;
            height: 70px;
            display: flex;
            align-items: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .header-inner {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 100%;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--color-navy);
            display: flex;
            align-items: center;
            gap: 4px;
            letter-spacing: -0.02em;
        }
        
        .logo span { color: var(--color-gold); }

        .header-btn {
            background-color: var(--color-navy);
            color: white;
            padding: 10px 24px;
            font-size: 0.9rem;
            border-radius: 4px;
            font-weight: 500;
        }
        
        @media (max-width: 768px) {
            .header-btn { display: none; }
        }

        /* =========================================
           ヒーローセクション
           ========================================= */
        .hero {
            background-color: var(--color-navy);
            background-image: linear-gradient(rgba(15, 23, 42, 0.85), rgba(15, 23, 42, 0.8)), url('https://images.unsplash.com/photo-1556761175-5973dc0f32e7?q=80&w=2000&auto=format&fit=crop');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 80px 0 100px;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0; left: 0; right: 0; bottom: 0;
            background-image: radial-gradient(#ffffff 1px, transparent 1px);
            background-size: 40px 40px;
            opacity: 0.05;
        }

        .hero-container {
            position: relative;
            z-index: 2;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 50px;
        }

        .hero-text {
            max-width: 550px;
        }

        .hero-badge {
            background-color: var(--color-gold);
            color: white;
            font-size: 0.9rem;
            padding: 6px 16px;
            display: inline-block;
            margin-bottom: 24px;
            font-weight: 500;
        }

        .hero h1 {
            font-size: 2.8rem;
            line-height: 1.4;
            margin-bottom: 30px;
            font-weight: 700;
        }

        .hero h1 span {
            color: #FFD700;
            background: linear-gradient(to right, #FFD700, #FDB931);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero p {
            font-size: 1.1rem;
            color: #CBD5E1;
            margin-bottom: 40px;
            line-height: 1.8;
        }

        .hero-image {
            flex: 1;
            display: flex;
            justify-content: center;
        }
        
        .hero-img-stat {
            width: 100%;
            max-width: 500px;
            border-radius: 12px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.3);
            border: 4px solid rgba(255,255,255,0.1);
        }

        @media (max-width: 768px) {
            .hero-container { flex-direction: column; text-align: left; }
            .hero h1 { font-size: 2rem; }
            .hero { padding: 60px 0; }
            .hero-image { width: 100%; margin-top: 20px; }
        }

        /* =========================================
           課題・助成金解説
           ========================================= */
        .problems { background-color: white; }
        
        .problems-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 32px;
        }

        .problem-item {
            background-color: var(--color-bg-light);
            padding: 32px 24px;
            border-top: 4px solid var(--color-navy);
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
        }

        .problem-icon { font-size: 2rem; margin-bottom: 16px; color: var(--color-navy); }
        .problem-item h3 { font-size: 1.2rem; margin-bottom: 16px; color: var(--color-navy); }

        .subsidy-section {
            background: linear-gradient(to bottom, #F8FAFC, #FFFFFF);
            border-bottom: 1px solid #eee;
        }

        .subsidy-box {
            background: white;
            border: 2px solid var(--color-red);
            border-radius: 12px;
            padding: 40px;
            position: relative;
            box-shadow: 0 10px 30px rgba(220, 38, 38, 0.08);
        }

        .subsidy-label {
            position: absolute;
            top: -15px;
            left: 50%;
            transform: translateX(-50%);
            background: var(--color-red);
            color: white;
            padding: 5px 24px;
            font-weight: 700;
            border-radius: 50px;
        }

        .subsidy-content h3 {
            text-align: center;
            font-size: 1.8rem;
            color: var(--color-navy);
            margin-bottom: 30px;
        }

        .subsidy-points {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            margin-bottom: 30px;
        }

        .subsidy-point {
            text-align: center;
            background: #FEF2F2;
            padding: 20px;
            border-radius: 8px;
        }
        
        .subsidy-point strong {
            display: block; color: var(--color-red); font-size: 1.2rem; margin-bottom: 8px;
        }
        
        .subsidy-math {
            background: var(--color-navy);
            color: white;
            padding: 20px;
            border-radius: 8px;
            text-align: center;
            font-size: 1.1rem;
            position: relative;
        }

        .subsidy-math span {
            color: #FCD34D;
            font-weight: 700;
            font-size: 1.4rem;
        }

        .subsidy-caution {
            background: #fff;
            border: 1px solid var(--color-red);
            color: var(--color-red);
            font-size: 0.9rem;
            padding: 12px;
            margin-top: 15px;
            text-align: center;
            border-radius: 4px;
            font-weight: bold;
        }

        @media (max-width: 768px) {
            .problems-grid, .subsidy-points { grid-template-columns: 1fr; }
            .subsidy-content h3 { font-size: 1.4rem; }
            .subsidy-math { font-size: 1rem; }
        }

        /* =========================================
           動画カリキュラムリスト
           ========================================= */
        .curriculum-list {
            max-width: 900px;
            margin: 0 auto;
        }
        
        .curriculum-item {
            display: flex;
            align-items: center;
            background: white;
            border: 1px solid #E2E8F0;
            margin-bottom: 16px;
            padding: 20px 24px;
            border-radius: 8px;
            transition: 0.3s;
        }
        
        .curriculum-item:hover {
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            border-color: var(--color-navy);
        }
        
        .chapter-badge {
            background: var(--color-navy);
            color: white;
            font-size: 0.8rem;
            font-weight: 700;
            padding: 4px 10px;
            border-radius: 4px;
            margin-right: 20px;
            flex-shrink: 0;
        }
        
        .chapter-content h3 {
            font-size: 1.1rem;
            color: var(--color-navy);
            margin-bottom: 4px;
        }
        
        .chapter-content p {
            font-size: 0.9rem;
            color: #64748B;
            margin: 0;
        }

        /* =========================================
           導入ステップ
           ========================================= */
        .flow-container {
            display: flex;
            justify-content: space-between;
            gap: 20px;
            margin-top: 40px;
        }
        
        .flow-card {
            background: white;
            border: 1px solid #E2E8F0;
            border-radius: 8px;
            padding: 30px 20px;
            text-align: center;
            flex: 1;
            position: relative;
        }
        
        /* 矢印 */
        .flow-card:not(:last-child)::after {
            content: '▶';
            position: absolute;
            right: -20px;
            top: 50%;
            transform: translateY(-50%);
            color: var(--color-navy);
            font-size: 1.2rem;
            z-index: 1;
        }
        
        .flow-step {
            display: inline-block;
            background: var(--color-gold);
            color: white;
            font-size: 0.8rem;
            font-weight: 700;
            padding: 4px 12px;
            border-radius: 20px;
            margin-bottom: 16px;
        }
        
        .flow-title {
            font-weight: 700;
            font-size: 1.1rem;
            color: var(--color-navy);
            line-height: 1.4;
        }

        @media (max-width: 768px) {
            .flow-container { flex-direction: column; gap: 40px; }
            .flow-card:not(:last-child)::after {
                content: '▼';
                right: 50%;
                bottom: -30px;
                top: auto;
                transform: translateX(50%);
            }
        }

        /* =========================================
           講座タイプ
           ========================================= */
        .course-types {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            margin-bottom: 40px;
        }
        
        .course-card {
            background: white;
            border: 1px solid #E2E8F0;
            padding: 20px;
            border-radius: 8px;
            display: flex;
            align-items: center;
            gap: 16px;
        }
        
        .course-card-icon {
            background: var(--color-navy);
            color: white;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            flex-shrink: 0;
        }
        
        @media (max-width: 768px) {
            .course-types { grid-template-columns: 1fr; }
        }

        /* =========================================
           料金プラン
           ========================================= */
        .pricing-section {
            background-color: white;
        }

        .pricing-wrapper {
            display: flex;
            justify-content: center;
            gap: 30px;
            align-items: stretch;
            flex-wrap: wrap;
        }

        .pricing-card {
            background: white;
            border: 1px solid #E2E8F0;
            border-radius: 12px;
            width: 100%;
            max-width: 480px;
            padding: 40px 30px;
            display: flex;
            flex-direction: column;
            position: relative;
            transition: 0.3s;
        }

        /* プランA */
        .pricing-card.plan-a { border-top: 6px solid var(--color-navy); }

        /* プランB */
        .pricing-card.plan-b {
            border: 2px solid var(--color-gold);
            background: #FFFCF5;
            box-shadow: 0 20px 40px rgba(194, 155, 64, 0.15);
            transform: scale(1.02);
            z-index: 2;
        }

        .plan-badge {
            position: absolute;
            top: -15px;
            left: 50%;
            transform: translateX(-50%);
            background: var(--color-gold);
            color: white;
            padding: 6px 20px;
            border-radius: 30px;
            font-weight: 700;
            font-size: 0.9rem;
            white-space: nowrap;
        }

        .pricing-title {
            font-size: 1.4rem;
            font-weight: 700;
            color: var(--color-navy);
            margin-bottom: 10px;
            text-align: center;
        }

        .pricing-price {
            text-align: center;
            margin: 20px 0;
            color: var(--color-navy);
        }

        .price-large { font-size: 2.5rem; font-weight: 700; }
        .price-sub { font-size: 0.9rem; color: #64748B; }
        
        .price-highlight {
            color: var(--color-red);
            font-weight: 700;
            display: block;
            margin-top: 5px;
            font-size: 1.1rem;
        }

        .pricing-features { margin: 20px 0; flex-grow: 1; }
        .pricing-features li {
            margin-bottom: 12px;
            padding-left: 24px;
            position: relative;
            font-size: 0.95rem;
        }
        .pricing-features li::before {
            content: '✔'; position: absolute; left: 0; color: var(--color-gold); font-weight: bold;
        }
        .pricing-features li.required { color: var(--color-red); font-weight: bold; }
        .pricing-features li.required::before { content: '⚠️'; color: inherit; }

        .campaign-box {
            background: var(--color-navy);
            color: white;
            padding: 15px;
            border-radius: 8px;
            text-align: center;
            margin-bottom: 20px;
        }
        .campaign-box strong { color: #FCD34D; font-size: 1.1rem; }

        /* =========================================
           FAQセクション（リッチデザイン）
           ========================================= */
        .faq-section {
            background-color: #F8FAFC;
        }

        .faq-container {
            max-width: 800px;
            margin: 0 auto;
        }

        .faq-item {
            background: white;
            margin-bottom: 20px;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0,0,0,0.02);
            border: 1px solid #E2E8F0;
            transition: all 0.3s var(--easing);
        }

        .faq-item:hover {
            box-shadow: 0 10px 15px rgba(0,0,0,0.05);
            transform: translateY(-2px);
        }

        .faq-question {
            padding: 24px 32px;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: space-between;
            font-weight: 700;
            color: var(--color-navy);
            position: relative;
        }

        .faq-q-icon {
            display: flex;
            align-items: center;
            gap: 16px;
        }

        .q-mark {
            font-family: var(--font-serif);
            font-size: 1.5rem;
            background: linear-gradient(135deg, #D4AF37, #C29B40);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-style: italic;
            flex-shrink: 0;
        }

        .faq-toggle {
            width: 24px;
            height: 24px;
            position: relative;
            transition: transform 0.3s ease;
        }

        .faq-toggle::before, .faq-toggle::after {
            content: '';
            position: absolute;
            background-color: var(--color-gold);
            border-radius: 2px;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }

        .faq-toggle::before { width: 16px; height: 2px; }
        .faq-toggle::after { width: 2px; height: 16px; transition: transform 0.3s ease; }

        .faq-item.active .faq-toggle { transform: rotate(180deg); }
        .faq-item.active .faq-toggle::after { transform: translate(-50%, -50%) rotate(90deg); opacity: 0; }

        .faq-answer {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.4s var(--easing);
            background-color: #fdfdfd;
        }

        .faq-answer-inner {
            padding: 0 32px 32px 64px; /* Qアイコン分インデント */
            color: var(--color-text-body);
            font-size: 0.95rem;
            line-height: 1.8;
            border-top: 1px solid #F1F5F9;
            padding-top: 20px;
        }

        @media (max-width: 768px) {
            .faq-answer-inner { padding: 20px; }
        }

        /* =========================================
           プロンプト体験
           ========================================= */
        .demo-section {
            background-color: var(--color-gold-light);
            padding: 100px 0;
        }
        .demo-wrapper {
            max-width: 800px;
            margin: 0 auto;
            background: white;
            padding: 40px;
            border-radius: 12px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.05);
            border: 1px solid rgba(194, 155, 64, 0.2);
        }
        .prompt-textarea {
            width: 100%; height: 150px; padding: 20px;
            border: 2px solid #E2E8F0; border-radius: 8px;
            background-color: #F8FAFC; font-family: monospace; resize: none;
            color: #334155; margin-bottom: 16px;
        }
        .copy-btn {
            display: block; width: 100%; background-color: var(--color-navy);
            color: white; border: none; padding: 14px;
            border-radius: 6px; font-weight: 700; cursor: pointer;
        }

        /* =========================================
           フッター
           ========================================= */
        footer {
            background-color: var(--color-navy);
            color: white;
            padding: 60px 0 100px;
            text-align: center;
        }
        .copyright {
            border-top: 1px solid rgba(255,255,255,0.1);
            padding-top: 20px;
            font-size: 0.8rem;
            color: #64748B;
        }
        .bottom-cta-bar {
            position: fixed; bottom: 0; left: 0; width: 100%;
            background-color: white; padding: 16px;
            box-shadow: 0 -4px 20px rgba(0,0,0,0.1); z-index: 9999;
            display: flex; justify-content: center;
        }
        @media (min-width: 769px) { .bottom-cta-bar { display: none; } }

    </style>
</head>
<body>

    <!-- ヘッダー -->
    <header>
        <div class="container header-inner">
            <div class="logo">withAI</div>
            <a href="#pricing" class="header-btn">プラン・料金を見る</a>
        </div>
    </header>

    <!-- ヒーロー -->
    <section class="hero">
        <div class="container hero-container">
            <div class=
