<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>جامعة المنصورة الأهلية | Mansoura National University</title>
<meta name="description" content="جامعة المنصورة الأهلية - صرح تعليمي متميز يقدم برامج أكاديمية معتمدة دولياً">
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700;900&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<style>
  :root {
    --primary: #1a3a6c;
    --secondary: #2c5aa0;
    --accent: #d4af37;
    --accent-light: #e8c860;
    --light: #f5f7fa;
    --white: #ffffff;
    --text: #2c3e50;
    --gray: #6c757d;
    --shadow: 0 10px 40px rgba(0,0,0,0.1);
    --shadow-lg: 0 20px 60px rgba(26,58,108,0.2);
    --transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }

  body {
    font-family: 'Cairo', sans-serif;
    color: var(--text);
    background: var(--white);
    overflow-x: hidden;
    line-height: 1.7;
  }

  /* ===== Header ===== */
  header {
    position: fixed;
    top: 0; right: 0; left: 0;
    z-index: 1000;
    background: rgba(255,255,255,0.97);
    backdrop-filter: blur(20px);
    box-shadow: 0 2px 20px rgba(0,0,0,0.08);
    transition: var(--transition);
  }

  .topbar {
    background: var(--primary);
    color: var(--white);
    padding: 8px 5%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 0.85rem;
  }

  .topbar-info span { margin-left: 20px; }
  .topbar-info i { color: var(--accent); margin-left: 5px; }
  .topbar-info a {
    color: var(--white);
    text-decoration: none;
    transition: var(--transition);
  }
  .topbar-info a:hover { color: var(--accent); }

  .topbar-social a {
    color: var(--white);
    margin-right: 12px;
    transition: var(--transition);
    font-size: 1rem;
  }
  .topbar-social a:hover { color: var(--accent); transform: translateY(-2px); }

  nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 15px 5%;
  }

  .logo {
    display: flex;
    align-items: center;
    gap: 12px;
    font-weight: 900;
    font-size: 1.35rem;
    color: var(--primary);
  }

  .logo-icon {
    width: 55px; height: 55px;
    background: linear-gradient(135deg, var(--primary), var(--secondary));
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--accent);
    font-size: 1.7rem;
    box-shadow: var(--shadow);
    border: 2px solid var(--accent);
    flex-shrink: 0;
  }

  .logo-text small {
    display: block;
    font-size: 0.7rem;
    color: var(--gray);
    font-weight: 400;
    letter-spacing: 2px;
  }

  .nav-menu {
    display: flex;
    list-style: none;
    gap: 30px;
  }

  .nav-menu a {
    text-decoration: none;
    color: var(--text);
    font-weight: 600;
    font-size: 0.98rem;
    position: relative;
    transition: var(--transition);
    padding: 5px 0;
  }

  .nav-menu a::after {
    content: '';
    position: absolute;
    bottom: -5px; right: 0;
    width: 0; height: 3px;
    background: var(--accent);
    transition: var(--transition);
    border-radius: 3px;
  }

  .nav-menu a:hover { color: var(--secondary); }
  .nav-menu a:hover::after { width: 100%; }

  .btn-nav {
    background: linear-gradient(135deg, var(--accent), var(--accent-light));
    color: var(--primary);
    padding: 12px 28px;
    border-radius: 30px;
    text-decoration: none;
    font-weight: 700;
    transition: var(--transition);
    box-shadow: 0 5px 20px rgba(212,175,55,0.4);
    font-size: 0.95rem;
  }

  .btn-nav:hover {
    transform: translateY(-3px);
    box-shadow: 0 10px 30px rgba(212,175,55,0.6);
  }

  .menu-toggle {
    display: none;
    font-size: 1.8rem;
    color: var(--primary);
    cursor: pointer;
    background: none;
    border: none;
  }

  /* ===== Hero ===== */
  .hero {
    height: 100vh;
    min-height: 700px;
    position: relative;
    display: flex;
    align-items: center;
    padding: 0 5%;
    margin-top: 100px;
    background: linear-gradient(135deg, rgba(26,58,108,0.92), rgba(44,90,160,0.85)),
                url('https://images.unsplash.com/photo-1562774053-701939374585?w=1920') center/cover;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    top: -50%; left: -50%;
    width: 200%; height: 200%;
    background: radial-gradient(circle, rgba(212,175,55,0.15) 0%, transparent 60%);
    animation: rotate 30s linear infinite;
  }

  @keyframes rotate {
    from { transform: rotate(0deg); }
    to { transform: rotate(360deg); }
  }

  .hero-content {
    position: relative;
    z-index: 2;
    max-width: 750px;
    color: var(--white);
    animation: fadeInUp 1.2s ease;
  }

  @keyframes fadeInUp {
    from { opacity: 0; transform: translateY(50px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .hero-badge {
    display: inline-block;
    background: rgba(212,175,55,0.2);
    border: 1px solid var(--accent);
    color: var(--accent);
    padding: 8px 20px;
    border-radius: 30px;
    font-size: 0.9rem;
    font-weight: 600;
    margin-bottom: 25px;
    backdrop-filter: blur(10px);
  }

  .hero h1 {
    font-size: 3.3rem;
    font-weight: 900;
    line-height: 1.2;
    margin-bottom: 20px;
  }

  .hero h1 span {
    background: linear-gradient(135deg, var(--accent), var(--accent-light));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .hero p {
    font-size: 1.2rem;
    margin-bottom: 35px;
    opacity: 0.95;
    max-width: 600px;
  }

  .hero-buttons {
    display: flex;
    gap: 20px;
    flex-wrap: wrap;
  }

  .btn {
    padding: 15px 35px;
    border-radius: 50px;
    text-decoration: none;
    font-weight: 700;
    font-size: 1rem;
    transition: var(--transition);
    display: inline-flex;
    align-items: center;
    gap: 10px;
    cursor: pointer;
    border: none;
    font-family: inherit;
  }

  .btn-primary {
    background: linear-gradient(135deg, var(--accent), var(--accent-light));
    color: var(--primary);
    box-shadow: 0 10px 30px rgba(212,175,55,0.4);
  }

  .btn-primary:hover {
    transform: translateY(-5px);
    box-shadow: 0 15px 40px rgba(212,175,55,0.6);
  }

  .btn-outline {
    background: transparent;
    color: var(--white);
    border: 2px solid var(--white);
  }

  .btn-outline:hover {
    background: var(--white);
    color: var(--primary);
    transform: translateY(-5px);
  }

  /* ===== Stats ===== */
  .stats {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 0;
    background: var(--primary);
    padding: 60px 5%;
    position: relative;
    z-index: 3;
  }

  .stat-item {
    text-align: center;
    color: var(--white);
    padding: 20px;
    border-left: 1px solid rgba(255,255,255,0.1);
    transition: var(--transition);
  }

  .stat-item:first-child { border-left: none; }
  .stat-item:hover { background: rgba(212,175,55,0.1); }

  .stat-icon {
    font-size: 2.5rem;
    color: var(--accent);
    margin-bottom: 15px;
  }

  .stat-number {
    font-size: 2.8rem;
    font-weight: 900;
    color: var(--white);
    line-height: 1;
  }

  .stat-label {
    font-size: 1rem;
    opacity: 0.8;
    margin-top: 8px;
  }

  /* ===== Sections ===== */
  section { padding: 100px 5%; }

  .section-header {
    text-align: center;
    max-width: 700px;
    margin: 0 auto 70px;
  }

  .section-tag {
    color: var(--accent);
    font-weight: 700;
    font-size: 1rem;
    letter-spacing: 3px;
    text-transform: uppercase;
    margin-bottom: 15px;
    display: block;
  }

  .section-title {
    font-size: 2.8rem;
    font-weight: 900;
    color: var(--primary);
    margin-bottom: 20px;
    line-height: 1.2;
  }

  .section-desc {
    color: var(--gray);
    font-size: 1.1rem;
  }

  /* ===== About ===== */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 70px;
    align-items: center;
  }

  .about-image {
    position: relative;
    border-radius: 20px;
    overflow: hidden;
    box-shadow: var(--shadow-lg);
  }

  .about-image img {
    width: 100%;
    height: 500px;
    object-fit: cover;
    transition: var(--transition);
  }

  .about-image:hover img { transform: scale(1.05); }

  .about-badge {
    position: absolute;
    bottom: 30px; right: 30px;
    background: var(--accent);
    color: var(--primary);
    padding: 20px 30px;
    border-radius: 15px;
    font-weight: 900;
    font-size: 1.1rem;
    box-shadow: var(--shadow);
  }

  .about-badge span {
    display: block;
    font-size: 2.3rem;
    line-height: 1;
  }

  .about-content h2 {
    font-size: 2.2rem;
    color: var(--primary);
    margin-bottom: 20px;
    font-weight: 900;
  }

  .about-content p {
    color: var(--gray);
    margin-bottom: 20px;
    font-size: 1.05rem;
  }

  .about-features {
    list-style: none;
    margin-top: 30px;
  }

  .about-features li {
    display: flex;
    align-items: center;
    gap: 15px;
    padding: 12px 0;
    font-weight: 600;
    color: var(--text);
  }

  .about-features i {
    width: 35px; height: 35px;
    background: rgba(212,175,55,0.15);
    color: var(--accent);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
  }

  /* ===== Video Section ===== */
  .video-section {
    background: linear-gradient(135deg, rgba(26,58,108,0.95), rgba(44,90,160,0.9)),
                url('https://images.unsplash.com/photo-1523050854058-8df90110c9f1?w=1920') center/cover;
    padding: 100px 5%;
    text-align: center;
  }

  .video-section .section-header { margin-bottom: 50px; }

  .video-section .section-title { color: var(--white); }
  .video-section .section-desc { color: rgba(255,255,255,0.85); }

  .video-wrapper {
    max-width: 900px;
    margin: 0 auto;
    position: relative;
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 0 30px 80px rgba(0,0,0,0.5);
    aspect-ratio: 16/9;
  }

  .video-wrapper iframe {
    width: 100%;
    height: 100%;
    border: none;
    display: block;
  }

  /* ===== Programs ===== */
  .programs { background: var(--light); }

  .programs-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
  }

  .program-card {
    background: var(--white);
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 0 5px 25px rgba(0,0,0,0.06);
    transition: var(--transition);
    cursor: pointer;
  }

  .program-card:hover {
    transform: translateY(-10px);
    box-shadow: var(--shadow-lg);
  }

  .program-image {
    height: 220px;
    position: relative;
    overflow: hidden;
  }

  .program-image img {
    width: 100%; height: 100%;
    object-fit: cover;
    transition: var(--transition);
  }

  .program-card:hover .program-image img { transform: scale(1.1); }

  .program-icon {
    position: absolute;
    bottom: -25px; right: 25px;
    width: 60px; height: 60px;
    background: linear-gradient(135deg, var(--accent), var(--accent-light));
    border-radius: 15px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.6rem;
    color: var(--primary);
    box-shadow: var(--shadow);
  }

  .program-body { padding: 40px 25px 25px; }

  .program-body h3 {
    font-size: 1.3rem;
    color: var(--primary);
    margin-bottom: 12px;
    font-weight: 700;
  }

  .program-body p {
    color: var(--gray);
    margin-bottom: 20px;
    font-size: 0.95rem;
  }

  .program-meta {
    display: flex;
    justify-content: space-between;
    padding-top: 20px;
    border-top: 1px solid #eee;
    font-size: 0.9rem;
    color: var(--gray);
  }

  .program-meta i { color: var(--accent); margin-left: 5px; }

  /* ===== News ===== */
  .news-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 30px;
  }

  .news-card {
    background: var(--white);
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 0 5px 25px rgba(0,0,0,0.06);
    transition: var(--transition);
  }

  .news-card:hover {
    transform: translateY(-8px);
    box-shadow: var(--shadow-lg);
  }

  .news-image {
    height: 200px;
    overflow: hidden;
    position: relative;
  }

  .news-image img {
    width: 100%; height: 100%;
    object-fit: cover;
    transition: var(--transition);
  }

  .news-card:hover .news-image img { transform: scale(1.1); }

  .news-date {
    position: absolute;
    top: 20px; right: 20px;
    background: var(--accent);
    color: var(--primary);
    padding: 10px 15px;
    border-radius: 10px;
    text-align: center;
    font-weight: 700;
    line-height: 1.2;
  }

  .news-date span { display: block; font-size: 1.5rem; }

  .news-body { padding: 25px; }

  .news-body .category {
    color: var(--accent);
    font-size: 0.85rem;
    font-weight: 700;
    letter-spacing: 1px;
    text-transform: uppercase;
  }

  .news-body h3 {
    color: var(--primary);
    margin: 12px 0;
    font-size: 1.15rem;
    font-weight: 700;
    line-height: 1.4;
  }

  .news-body p { color: var(--gray); font-size: 0.95rem; }

  .news-link {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    color: var(--secondary);
    font-weight: 700;
    text-decoration: none;
    margin-top: 15px;
    transition: var(--transition);
  }

  .news-link:hover { gap: 15px; color: var(--accent); }

  /* ===== Registration Form ===== */
  .register-section {
    background: linear-gradient(135deg, var(--primary), var(--secondary));
    position: relative;
    overflow: hidden;
    padding: 100px 5%;
  }

  .register-section::before {
    content: '';
    position: absolute;
    top: -50%; right: -20%;
    width: 600px; height: 600px;
    background: radial-gradient(circle, rgba(212,175,55,0.2), transparent);
    border-radius: 50%;
  }

  .register-section::after {
    content: '';
    position: absolute;
    bottom: -50%; left: -20%;
    width: 600px; height: 600px;
    background: radial-gradient(circle, rgba(212,175,55,0.15), transparent);
    border-radius: 50%;
  }

  .register-wrapper {
    position: relative;
    z-index: 2;
    max-width: 900px;
    margin: 0 auto;
  }

  .register-section .section-header { margin-bottom: 40px; }
  .register-section .section-title { color: var(--white); }
  .register-section .section-desc { color: rgba(255,255,255,0.9); }
  .register-section .section-tag { color: var(--accent); }

  .register-form {
    background: var(--white);
    border-radius: 25px;
    padding: 45px 40px;
    box-shadow: 0 30px 80px rgba(0,0,0,0.3);
  }

  .form-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
  }

  .form-group {
    display: flex;
    flex-direction: column;
    gap: 8px;
  }

  .form-group.full-width { grid-column: 1 / -1; }

  .form-group label {
    color: var(--primary);
    font-weight: 700;
    font-size: 0.95rem;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .form-group label i { color: var(--accent); }

  .form-group label .required {
    color: #e74c3c;
    font-size: 1.1rem;
  }

  .form-group input,
  .form-group select,
  .form-group textarea {
    padding: 14px 18px;
    border: 2px solid #e8ecf1;
    border-radius: 12px;
    font-family: inherit;
    font-size: 1rem;
    color: var(--text);
    transition: var(--transition);
    background: #f8f9fc;
    outline: none;
  }

  .form-group input:focus,
  .form-group select:focus,
  .form-group textarea:focus {
    border-color: var(--accent);
    background: #fff;
    box-shadow: 0 0 0 4px rgba(212,175,55,0.15);
  }

  .form-group textarea {
    resize: vertical;
    min-height: 100px;
  }

  .form-group select {
    cursor: pointer;
    appearance: none;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='%23d4af37'%3E%3Cpath d='M7 10l5 5 5-5z'/%3E%3C/svg%3E");
    background-repeat: no-repeat;
    background-position: left 15px center;
    background-size: 20px;
    padding-left: 45px;
  }

  .radio-group {
    display: flex;
    gap: 15px;
    flex-wrap: wrap;
    margin-top: 5px;
  }

  .radio-option {
    display: flex;
    align-items: center;
    gap: 8px;
    padding: 12px 18px;
    background: #f8f9fc;
    border: 2px solid #e8ecf1;
    border-radius: 12px;
    cursor: pointer;
    transition: var(--transition);
    font-size: 0.95rem;
    font-weight: 600;
  }

  .radio-option:hover {
    border-color: var(--accent);
    background: #fff;
  }

  .radio-option input {
    accent-color: var(--accent);
    width: 18px;
    height: 18px;
    cursor: pointer;
  }

  .radio-option input:checked + span {
    color: var(--primary);
  }

  .form-submit {
    grid-column: 1 / -1;
    margin-top: 15px;
  }

  .form-submit button {
    width: 100%;
    padding: 18px;
    background: linear-gradient(135deg, var(--accent), var(--accent-light));
    color: var(--primary);
    border: none;
    border-radius: 12px;
    font-family: inherit;
    font-size: 1.15rem;
    font-weight: 700;
    cursor: pointer;
    transition: var(--transition);
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
    box-shadow: 0 10px 30px rgba(212,175,55,0.3);
  }

  .form-submit button:hover {
    transform: translateY(-3px);
    box-shadow: 0 15px 40px rgba(212,175,55,0.5);
  }

  .form-submit button:active {
    transform: translateY(-1px);
  }

  .form-note {
    grid-column: 1 / -1;
    text-align: center;
    color: var(--gray);
    font-size: 0.9rem;
    margin-top: 10px;
  }

  /* ===== Map ===== */
  .map-wrapper {
    max-width: 1200px;
    margin: 0 auto;
    border-radius: 20px;
    overflow: hidden;
    box-shadow: var(--shadow-lg);
    height: 450px;
    position: relative;
  }

  .map-wrapper iframe {
    width: 100%;
    height: 100%;
    border: none;
    display: block;
    filter: grayscale(20%);
    transition: var(--transition);
  }

  .map-wrapper:hover iframe {
    filter: grayscale(0%);
  }

  /* ===== Contact Info Section ===== */
  .contact-info {
    background: var(--light);
    padding: 80px 5%;
  }

  .contact-info-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 30px;
    max-width: 1200px;
    margin: 0 auto;
  }

  .contact-card {
    background: var(--white);
    padding: 35px 25px;
    border-radius: 20px;
    text-align: center;
    box-shadow: 0 5px 25px rgba(0,0,0,0.06);
    transition: var(--transition);
    border-bottom: 4px solid transparent;
  }

  .contact-card:hover {
    transform: translateY(-8px);
    box-shadow: var(--shadow-lg);
    border-bottom-color: var(--accent);
  }

  .contact-card-icon {
    width: 70px; height: 70px;
    background: linear-gradient(135deg, var(--primary), var(--secondary));
    color: var(--accent);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.8rem;
    margin: 0 auto 20px;
    transition: var(--transition);
  }

  .contact-card:hover .contact-card-icon {
    transform: rotate(360deg) scale(1.1);
  }

  .contact-card h4 {
    color: var(--primary);
    font-size: 1.2rem;
    margin-bottom: 12px;
    font-weight: 700;
  }

  .contact-card p,
  .contact-card a {
    color: var(--gray);
    text-decoration: none;
    font-size: 1rem;
    transition: var(--transition);
    display: block;
    direction: ltr;
  }

  .contact-card a:hover {
    color: var(--accent);
    font-weight: 700;
  }

  /* ===== CTA ===== */
  .cta {
    background: linear-gradient(135deg, var(--primary), var(--secondary));
    padding: 80px 5%;
    text-align: center;
    color: var(--white);
    position: relative;
    overflow: hidden;
  }

  .cta::before {
    content: '';
    position: absolute;
    top: -50%; right: -20%;
    width: 500px; height: 500px;
    background: radial-gradient(circle, rgba(212,175,55,0.25), transparent);
    border-radius: 50%;
  }

  .cta-content { position: relative; z-index: 2; max-width: 700px; margin: 0 auto; }

  .cta h2 {
    font-size: 2.5rem;
    font-weight: 900;
    margin-bottom: 20px;
  }

  .cta p { font-size: 1.15rem; margin-bottom: 35px; opacity: 0.95; }

  /* ===== Footer ===== */
  footer {
    background: #0d1f3c;
    color: #a8b4c0;
    padding: 70px 5% 0;
  }

  .footer-grid {
    display: grid;
    grid-template-columns: 1.5fr 1fr 1fr 1.5fr;
    gap: 50px;
    padding-bottom: 50px;
    border-bottom: 1px solid rgba(255,255,255,0.08);
  }

  .footer-col h4 {
    color: var(--white);
    font-size: 1.2rem;
    margin-bottom: 25px;
    font-weight: 700;
    position: relative;
    padding-bottom: 12px;
  }

  .footer-col h4::after {
    content: '';
    position: absolute;
    bottom: 0; right: 0;
    width: 40px; height: 3px;
    background: var(--accent);
    border-radius: 3px;
  }

  .footer-col p { margin-bottom: 15px; font-size: 0.95rem; }

  .footer-col ul { list-style: none; }
  .footer-col ul li { margin-bottom: 12px; }

  .footer-col ul a {
    color: #a8b4c0;
    text-decoration: none;
    transition: var(--transition);
    font-size: 0.95rem;
    display: inline-flex;
    align-items: center;
    gap: 8px;
  }

  .footer-col ul a:hover { color: var(--accent); padding-right: 5px; }

  .footer-col ul a i { font-size: 0.7rem; }

  .footer-contact-item {
    display: flex;
    align-items: center;
    gap: 12px;
    margin-bottom: 15px;
    font-size: 0.95rem;
  }

  .footer-contact-item i {
    color: var(--accent);
    width: 20px;
  }

  .footer-contact-item a {
    color: #a8b4c0;
    text-decoration: none;
    transition: var(--transition);
    direction: ltr;
  }

  .footer-contact-item a:hover { color: var(--accent); }

  .footer-social {
    display: flex;
    gap: 12px;
    margin-top: 20px;
  }

  .footer-social a {
    width: 40px; height: 40px;
    background: rgba(255,255,255,0.08);
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--white);
    text-decoration: none;
    transition: var(--transition);
  }

  .footer-social a:hover {
    background: var(--accent);
    color: var(--primary);
    transform: translateY(-3px);
  }

  .newsletter {
    display: flex;
    background: rgba(255,255,255,0.05);
    border-radius: 10px;
    overflow: hidden;
    margin-top: 15px;
  }

  .newsletter input {
    flex: 1;
    padding: 14px 18px;
    border: none;
    background: transparent;
    color: var(--white);
    font-family: inherit;
    outline: none;
  }

  .newsletter input::placeholder { color: #6b7a8a; }

  .newsletter button {
    background: var(--accent);
    color: var(--primary);
    border: none;
    padding: 0 22px;
    cursor: pointer;
    font-size: 1.1rem;
    transition: var(--transition);
  }

  .newsletter button:hover { background: var(--accent-light); }

  .footer-bottom {
    text-align: center;
    padding: 25px 0;
    font-size: 0.9rem;
  }

  .footer-bottom span { color: var(--accent); font-weight: 700; }

  /* ===== Scroll Top ===== */
  .scroll-top {
    position: fixed;
    bottom: 110px; left: 30px;
    width: 50px; height: 50px;
    background: linear-gradient(135deg, var(--accent), var(--accent-light));
    color: var(--primary);
    border: none;
    border-radius: 50%;
    font-size: 1.2rem;
    cursor: pointer;
    box-shadow: var(--shadow);
    opacity: 0;
    visibility: hidden;
    transition: var(--transition);
    z-index: 999;
  }

  .scroll-top.show { opacity: 1; visibility: visible; }
  .scroll-top:hover { transform: translateY(-5px); }

  /* ===== زر الاتصال العائم ===== */
  .floating-call-btn {
    position: fixed;
    bottom: 30px;
    right: 30px;
    width: 65px;
    height: 65px;
    background: linear-gradient(135deg, #d4af37, #e8c860);
    color: #1a3a6c;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.6rem;
    text-decoration: none;
    box-shadow: 0 10px 30px rgba(212,175,55,0.5);
    z-index: 998;
    transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
    animation: floatPulse 2.5s infinite;
    cursor: pointer;
  }

  .floating-call-btn:hover {
    transform: scale(1.1) translateY(-5px);
    box-shadow: 0 15px 40px rgba(212,175,55,0.7);
  }

  @keyframes floatPulse {
    0%, 100% {
      box-shadow: 0 10px 30px rgba(212,175,55,0.5), 0 0 0 0 rgba(212,175,55,0.7);
    }
    50% {
      box-shadow: 0 10px 30px rgba(212,175,55,0.5), 0 0 0 20px rgba(212,175,55,0);
    }
  }

  .call-tooltip {
    position: absolute;
    right: 80px;
    background: #1a3a6c;
    color: #fff;
    padding: 10px 18px;
    border-radius: 10px;
    font-size: 0.9rem;
    font-weight: 600;
    white-space: nowrap;
    opacity: 0;
    visibility: hidden;
    transform: translateX(10px);
    transition: all 0.3s;
    pointer-events: none;
    font-family: 'Cairo', sans-serif;
  }

  .call-tooltip::after {
    content: '';
    position: absolute;
    right: -6px;
    top: 50%;
    transform: translateY(-50%);
    border: 6px solid transparent;
    border-right: none;
    border-left-color: #1a3a6c;
  }

  .floating-call-btn:hover .call-tooltip {
    opacity: 1;
    visibility: visible;
    transform: translateX(0);
  }

  /* ===== نافذة الاتصال ===== */
  .phone-modal {
    position: fixed;
    top: 0; left: 0;
    width: 100%; height: 100%;
    background: rgba(26, 58, 108, 0.85);
    backdrop-filter: blur(8px);
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 9999;
    opacity: 0;
    visibility: hidden;
    transition: all 0.4s ease;
    padding: 20px;
  }

  .phone-modal.active {
    opacity: 1;
    visibility: visible;
  }

  .phone-modal-content {
    background: #fff;
    border-radius: 25px;
    padding: 45px 35px 30px;
    max-width: 480px;
    width: 100%;
    position: relative;
    transform: scale(0.85) translateY(30px);
    transition: all 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
    box-shadow: 0 30px 80px rgba(0,0,0,0.4);
    max-height: 90vh;
    overflow-y: auto;
    font-family: 'Cairo', sans-serif;
  }

  .phone-modal.active .phone-modal-content {
    transform: scale(1) translateY(0);
  }

  .phone-close {
    position: absolute;
    top: 15px;
    left: 15px;
    width: 38px;
    height: 38px;
    background: #f0f2f5;
    border: none;
    border-radius: 50%;
    font-size: 1.5rem;
    color: #1a3a6c;
    cursor: pointer;
    transition: all 0.3s;
    display: flex;
    align-items: center;
    justify-content: center;
    line-height: 1;
    font-family: inherit;
  }

  .phone-close:hover {
    background: #d4af37;
    transform: rotate(90deg);
  }

  .phone-icon-big {
    width: 90px;
    height: 90px;
    background: linear-gradient(135deg, #1a3a6c, #2c5aa0);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 20px;
    font-size: 2.3rem;
    color: #d4af37;
    animation: iconPulse 2s infinite;
    box-shadow: 0 10px 30px rgba(26,58,108,0.3);
  }

  @keyframes iconPulse {
    0%, 100% {
      box-shadow: 0 10px 30px rgba(26,58,108,0.3), 0 0 0 0 rgba(212,175,55,0.5);
    }
    50% {
      box-shadow: 0 10px 30px rgba(26,58,108,0.3), 0 0 0 20px rgba(212,175,55,0);
    }
  }

  .phone-modal-content h3 {
    text-align: center;
    color: #1a3a6c;
    font-size: 1.6rem;
    margin-bottom: 8px;
    font-weight: 900;
  }

  .phone-modal-content > p {
    text-align: center;
    color: #6c757d;
    margin-bottom: 30px;
    font-size: 0.95rem;
  }

  .phone-numbers {
    display: flex;
    flex-direction: column;
    gap: 12px;
  }

  .phone-item {
    display: flex;
    align-items: center;
    gap: 15px;
    padding: 15px 18px;
    background: #f8f9fc;
    border-radius: 15px;
    text-decoration: none;
    color: #2c3e50;
    transition: all 0.3s;
    border: 2px solid transparent;
    cursor: pointer;
    font-family: inherit;
    width: 100%;
    text-align: right;
    font-size: 1rem;
  }

  .phone-item.main {
    background: linear-gradient(135deg, rgba(212,175,55,0.1), rgba(232,200,96,0.05));
    border-color: #d4af37;
  }

  .phone-item:hover {
    background: #fff;
    border-color: #d4af37;
    transform: translateX(-5px);
    box-shadow: 0 8px 25px rgba(26,58,108,0.12);
  }

  .phone-item-icon {
    width: 48px;
    height: 48px;
    background: linear-gradient(135deg, #1a3a6c, #2c5aa0);
    color: #d4af37;
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.2rem;
    flex-shrink: 0;
  }

  .phone-item.whatsapp .phone-item-icon {
    background: linear-gradient(135deg, #25d366, #128c7e);
    color: #fff;
  }

  .phone-item.copy-btn .phone-item-icon {
    background: linear-gradient(135deg, #6c757d, #495057);
    color: #fff;
  }

  .phone-item-info {
    flex: 1;
    display: flex;
    flex-direction: column;
    gap: 3px;
  }

  .phone-item-info small {
    color: #6c757d;
    font-size: 0.8rem;
    font-weight: 500;
  }

  .phone-item-info strong {
    color: #1a3a6c;
    font-size: 1.15rem;
    font-weight: 700;
    letter-spacing: 1px;
  }

  .phone-item-action {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 3px;
    color: #d4af37;
    font-size: 1.1rem;
    flex-shrink: 0;
  }

  .phone-item-action span {
    font-size: 0.7rem;
    font-weight: 700;
    color: #1a3a6c;
  }

  .phone-footer {
    margin-top: 20px;
    padding-top: 20px;
    border-top: 1px solid #eee;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
    color: #6c757d;
    font-size: 0.85rem;
  }

  .phone-footer i {
    color: #d4af37;
  }

  /* ===== Success Message ===== */
  .success-message {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) scale(0.8);
    background: #fff;
    padding: 45px 50px;
    border-radius: 25px;
    box-shadow: 0 30px 80px rgba(0,0,0,0.4);
    text-align: center;
    z-index: 10001;
    opacity: 0;
    visibility: hidden;
    transition: all 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
    max-width: 420px;
    width: 90%;
    font-family: 'Cairo', sans-serif;
  }

  .success-message.show {
    opacity: 1;
    visibility: visible;
    transform: translate(-50%, -50%) scale(1);
  }

  .success-icon {
    width: 90px;
    height: 90px;
    background: linear-gradient(135deg, #25d366, #128c7e);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 20px;
    font-size: 2.5rem;
    color: #fff;
    animation: successPop 0.6s ease;
  }

  @keyframes successPop {
    0% { transform: scale(0); }
    50% { transform: scale(1.2); }
    100% { transform: scale(1); }
  }

  .success-message h3 {
    color: #1a3a6c;
    font-size: 1.6rem;
    margin-bottom: 12px;
    font-weight: 900;
  }

  .success-message p {
    color: #6c757d;
    margin-bottom: 25px;
    font-size: 1rem;
    line-height: 1.6;
  }

  .success-message button {
    background: linear-gradient(135deg, #d4af37, #e8c860);
    color: #1a3a6c;
    border: none;
    padding: 12px 40px;
    border-radius: 30px;
    font-family: inherit;
    font-size: 1rem;
    font-weight: 700;
    cursor: pointer;
    transition: all 0.3s;
  }

  .success-message button:hover {
    transform: translateY(-3px);
    box-shadow: 0 10px 25px rgba(212,175,55,0.4);
  }

  /* ===== Responsive ===== */
  @media (max-width: 992px) {
    .hero h1 { font-size: 2.4rem; }
    .about-grid { grid-template-columns: 1fr; gap: 40px; }
    .stats { grid-template-columns: repeat(2, 1fr); }
    .footer-grid { grid-template-columns: 1fr 1fr; }
    .section-title { font-size: 2rem; }
    .form-grid { grid-template-columns: 1fr; }
  }

  @media (max-width: 768px) {
    .topbar-info span:not(:first-child) { display: none; }
    .menu-toggle { display: block; }
    .btn-nav { display: none; }

    .nav-menu {
      position: fixed;
      top: 0; right: -100%;
      width: 280px; height: 100vh;
      background: var(--white);
      flex-direction: column;
      padding: 100px 30px;
      gap: 25px;
      box-shadow: -10px 0 40px rgba(0,0,0,0.1);
      transition: var(--transition);
    }

    .nav-menu.active { right: 0; }

    .hero { height: auto; padding: 100px 5% 80px; text-align: center; }
    .hero h1 { font-size: 2rem; }
    .hero p { font-size: 1rem; }
    .hero-buttons { justify-content: center; }

    .stats { grid-template-columns: 1fr 1fr; padding: 40px 5%; }
    .stat-number { font-size: 2rem; }

    section { padding: 70px 5%; }
    .footer-grid { grid-template-columns: 1fr; gap: 35px; }
    .cta h2 { font-size: 1.8rem; }

    .phone-modal-content { padding: 40px 22px 25px; }
    .phone-modal-content h3 { font-size: 1.3rem; }
    .phone-item { padding: 12px 14px; gap: 12px; }
    .phone-item-icon { width: 42px; height: 42px; font-size: 1rem; }
    .phone-item-info strong { font-size: 1rem; }
    .phone-item-action span { display: none; }

    .floating-call-btn {
      width: 58px;
      height: 58px;
      bottom: 20px;
      right: 20px;
      font-size: 1.4rem;
    }

    .call-tooltip { display: none; }

    .copy-toast {
      bottom: 90px;
      right: 20px;
      left: 20px;
      justify-content: center;
    }

    .scroll-top {
      bottom: 90px;
      left: 20px;
      width: 45px;
      height: 45px;
    }

    .register-form { padding: 30px 20px; }
    .map-wrapper { height: 350px; }
    .video-wrapper { border-radius: 15px; }
  }

  /* إشعار النسخ */
  .copy-toast {
    position: fixed;
    bottom: 110px;
    right: 30px;
    background: #1a3a6c;
    color: #fff;
    padding: 14px 22px;
    border-radius: 12px;
    font-weight: 600;
    font-size: 0.95rem;
    box-shadow: 0 10px 30px rgba(0,0,0,0.3);
    z-index: 10000;
    transform: translateY(100px);
    opacity: 0;
    transition: all 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
    display: flex;
    align-items: center;
    gap: 10px;
    font-family: 'Cairo', sans-serif;
  }

  .copy-toast.show {
    transform: translateY(0);
    opacity: 1;
  }

  .copy-toast i {
    color: #d4af37;
    font-size: 1.2rem;
  }
</style>
</head>
<body>

<!-- ===== Header ===== -->
<header>
  <div class="topbar">
    <div class="topbar-info">
      <span><i class="fas fa-phone"></i> <a href="tel:01273111734">0127 311 1734</a></span>
      <span><i class="fas fa-envelope"></i> <a href="mailto:info@mnu.edu.eg">info@mnu.edu.eg</a></span>
      <span><i class="fas fa-map-marker-alt"></i> المنصورة، الدقهلية</span>
    </div>
    <div class="topbar-social">
      <a href="#" aria-label="Facebook"><i class="fab fa-facebook-f"></i></a>
      <a href="#" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
      <a href="#" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
      <a href="#" aria-label="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
      <a href="#" aria-label="YouTube"><i class="fab fa-youtube"></i></a>
    </div>
  </div>

  <nav>
    <div class="logo">
      <div class="logo-icon"><i class="fas fa-graduation-cap"></i></div>
      <div class="logo-text">
        جامعة المنصورة الأهلية
        <small>MANSOURA NATIONAL UNIVERSITY</small>
      </div>
    </div>

    <ul class="nav-menu" id="navMenu">
      <li><a href="#home">الرئيسية</a></li>
      <li><a href="#about">عن الجامعة</a></li>
      <li><a href="#programs">الكليات</a></li>
      <li><a href="#register">التسجيل</a></li>
      <li><a href="#news">الأخبار</a></li>
      <li><a href="javascript:void(0)" onclick="showPhone()">اتصل بنا</a></li>
    </ul>

    <a href="#register" class="btn-nav"><i class="fas fa-user-plus"></i> سجل الآن</a>
    <button class="menu-toggle" id="menuToggle" aria-label="القائمة"><i class="fas fa-bars"></i></button>
  </nav>
</header>

<!-- ===== Hero ===== -->
<section class="hero" id="home">
  <div class="hero-content">
    <span class="hero-badge"><i class="fas fa-award"></i> جامعة أهلية معتمدة من المجلس الأعلى للجامعات</span>
    <h1>مرحباً بكم في <span>جامعة المنصورة الأهلية</span></h1>
    <p>صرح تعليمي وبحثي متميز يقدم برامج أكاديمية معتمدة دولياً، ويساهم في خدمة المجتمع وتنمية الدلتا بأحدث المعايير العالمية.</p>
    <div class="hero-buttons">
      <a href="#register" class="btn btn-primary"><i class="fas fa-user-plus"></i> سجل الآن</a>
      <a href="#video" class="btn btn-outline"><i class="fas fa-play"></i> شاهد الفيديو</a>
    </div>
  </div>
</section>

<!-- ===== Stats ===== -->
<div class="stats">
  <div class="stat-item">
    <div class="stat-icon"><i class="fas fa-user-graduate"></i></div>
    <div class="stat-number" data-count="12000">0</div>
    <div class="stat-label">طالب وطالبة</div>
  </div>
  <div class="stat-item">
    <div class="stat-icon"><i class="fas fa-chalkboard-teacher"></i></div>
    <div class="stat-number" data-count="450">0</div>
    <div class="stat-label">عضو هيئة تدريس</div>
  </div>
  <div class="stat-item">
    <div class="stat-icon"><i class="fas fa-building-columns"></i></div>
    <div class="stat-number" data-count="8">0</div>
    <div class="stat-label">كلية أكاديمية</div>
  </div>
  <div class="stat-item">
    <div class="stat-icon"><i class="fas fa-trophy"></i></div>
    <div class="stat-number" data-count="30">0</div>
    <div class="stat-label">برنامج دراسي</div>
  </div>
</div>

<!-- ===== About ===== -->
<section id="about">
  <div class="about-grid">
    <div class="about-image">
      <img src="https://images.unsplash.com/photo-1541339907198-e08756dedf3f?w=800" alt="حرم جامعة المنصورة الأهلية">
      <div class="about-badge">
        <span>2023</span>
        سنة التأسيس
      </div>
    </div>

    <div class="about-content">
      <span class="section-tag">من نحن</span>
      <h2>جامعة المنصورة الأهلية — مستقبل التعليم في الدلتا</h2>
      <p>جامعة المنصورة الأهلية هي مؤسسة تعليمية غير هادفة للربح، أُنشئت بقرار من المجلس الأعلى للجامعات، لتكون إضافة نوعية لمنظومة التعليم العالي في مصر.</p>
      <p>تقدم الجامعة برامج أكاديمية متطورة تواكب سوق العمل المحلي والدولي، مع التركيز على البحث العلمي وخدمة المجتمع.</p>

      <ul class="about-features">
        <li><i class="fas fa-check"></i> معتمدة من المجلس الأعلى للجامعات المصرية</li>
        <li><i class="fas fa-check"></i> برامج دراسية بمعايير دولية</li>
        <li><i class="fas fa-check"></i> حرم جامعي حديث ومجهز بأحدث التقنيات</li>
        <li><i class="fas fa-check"></i> شراكات أكاديمية محلية ودولية</li>
      </ul>

      <a href="#programs" class="btn btn-primary" style="margin-top:25px;"><i class="fas fa-arrow-left"></i> تعرف على الكليات</a>
    </div>
  </div>
</section>

<!-- ===== Video Section ===== -->
<section class="video-section" id="video">
  <div class="section-header">
    <span class="section-tag">جولة في الجامعة</span>
    <h2 class="section-title">تعرف على جامعة المنصورة الأهلية</h2>
    <p class="section-desc">شاهد الفيديو التعريفي واستكشف مرافق الجامعة وبرامجها الأكاديمية</p>
  </div>

  <div class="video-wrapper">
    <iframe 
      src="https://www.youtube.com/embed/dQw4w9WgXcQ?rel=0" 
      title="فيديو تعريفي - جامعة المنصورة الأهلية"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
      allowfullscreen>
    </iframe>
  </div>
</section>

<!-- ===== Programs ===== -->
<section class="programs" id="programs">
  <div class="section-header">
    <span class="section-tag">برامجنا الأكاديمية</span>
    <h2 class="section-title">كليات جامعة المنصورة الأهلية</h2>
    <p class="section-desc">اختر من بين مجموعة واسعة من التخصصات المصممة لتلبية احتياجات سوق العمل</p>
  </div>

  <div class="programs-grid">
    <div class="program-card">
      <div class="program-image">
        <img src="https://images.unsplash.com/photo-1518770660439-4636190af475?w=600" alt="هندسة">
        <div class="program-icon"><i class="fas fa-microchip"></i></div>
      </div>
      <div class="program-body">
        <h3>كلية الهندسة</h3>
        <p>برامج متقدمة في الهندسة المدنية والميكانيكية والكهربائية والميكاترونكس.</p>
        <div class="program-meta">
          <span><i class="fas fa-clock"></i> 5 سنوات</span>
          <span><i class="fas fa-user-graduate"></i> بكالوريوس</span>
        </div>
      </div>
    </div>

    <div class="program-card">
      <div class="program-image">
        <img src="https://images.unsplash.com/photo-1576091160399-112ba8d25d1d?w=600" alt="طب">
        <div class="program-icon"><i class="fas fa-stethoscope"></i></div>
      </div>
      <div class="program-body">
        <h3>كلية الطب</h3>
        <p>تخريج أطباء مؤهلين وفق أحدث المعايير العالمية مع تدريب عملي مكثف.</p>
        <div class="program-meta">
          <span><i class="fas fa-clock"></i> 6 سنوات</span>
          <span><i class="fas fa-user-graduate"></i> بكالوريوس</span>
        </div>
      </div>
    </div>

    <div class="program-card">
      <div class="program-image">
        <img src="https://images.unsplash.com/photo-1517245386807-bb43f82c33c4?w=600" alt="حاسبات">
        <div class="program-icon"><i class="fas fa-laptop-code"></i></div>
      </div>
      <div class="program-body">
        <h3>كلية الحاسبات والذكاء الاصطناعي</h3>
        <p>برامج في علوم الحاسب، هندسة البرمجيات، الأمن السيبراني والذكاء الاصطناعي.</p>
        <div class="program-meta">
          <span><i class="fas fa-clock"></i> 4 سنوات</span>
          <span><i class="fas fa-user-graduate"></i> بكالوريوس</span>
        </div>
      </div>
    </div>

    <div class="program-card">
      <div class="program-image">
        <img src="https://images.unsplash.com/photo-1554224155-6726b3ff858f?w=600" alt="إدارة">
        <div class="program-icon"><i class="fas fa-chart-line"></i></div>
      </div>
      <div class="program-body">
        <h3>كلية إدارة الأعمال</h3>
        <p>تخصصات في المحاسبة، التسويق، التمويل، وإدارة الموارد البشرية.</p>
        <div class="program-meta">
          <span><i class="fas fa-clock"></i> 4 سنوات</span>
          <span><i class="fas fa-user-graduate"></i> بكالوريوس</span>
        </div>
      </div>
    </div>

    <div class="program-card">
      <div class="program-image">
        <img src="https://images.unsplash.com/photo-1581091226825-a6a2a5aee158?w=600" alt="علوم">
        <div class="program-icon"><i class="fas fa-flask"></i></div>
      </div>
      <div class="program-body">
        <h3>كلية العلوم</h3>
        <p>تخصصات في الفيزياء، الكيمياء، الأحياء، والرياضيات التطبيقية.</p>
        <div class="program-meta">
          <span><i class="fas fa-clock"></i> 4 سنوات</span>
          <span><i class="fas fa-user-graduate"></i> بكالوريوس</span>
        </div>
      </div>
    </div>

    <div class="program-card">
      <div class="program-image">
        <img src="https://images.unsplash.com/photo-1503676260728-1c00da094a0b?w=600" alt="آداب">
        <div class="program-icon"><i class="fas fa-book"></i></div>
      </div>
      <div class="program-body">
        <h3>كلية الآداب</h3>
        <p>برامج في اللغات، التاريخ، الجغرافيا، وعلم النفس والاجتماع.</p>
        <div class="program-meta">
          <span><i class="fas fa-clock"></i> 4 سنوات</span>
          <span><i class="fas fa-user-graduate"></i> بكالوريوس</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ===== Registration Form ===== -->
<section class="register-section" id="register">
  <div class="register-wrapper">
    <div class="section-header">
      <span class="section-tag">التسجيل الإلكتروني</span>
      <h2 class="section-title">سجل الآن في جامعة المنصورة الأهلية</h2>
      <p class="section-desc">املأ البيانات التالية وسيتواصل معك فريق القبول والتسجيل في أقرب وقت</p>
    </div>

    <form class="register-form" id="registerForm" onsubmit="handleSubmit(event)">
      <div class="form-grid">
        <div class="form-group">
          <label><i class="fas fa-user"></i> الاسم الكامل <span class="required">*</span></label>
          <input type="text" name="fullName" placeholder="مثال: أحمد محمد علي" required minlength="3">
        </div>

        <div class="form-group">
          <label><i class="fas fa-id-card"></i> الرقم القومي <span class="required">*</span></label>
          <input type="text" name="nationalId" placeholder="14 رقم" required pattern="[0-9]{14}" maxlength="14" inputmode="numeric">
        </div>

        <div class="form-group">
          <label><i class="fas fa-mobile-alt"></i> رقم الموبايل <span class="required">*</span></label>
          <input type="tel" name="phone" placeholder="مثال: 01012345678" required pattern="01[0-2,5][0-9]{8}" maxlength="11" inputmode="numeric">
        </div>

        <div class="form-group">
          <label><i class="fas fa-envelope"></i> البريد الإلكتروني <span class="required">*</span></label>
          <input type="email" name="email" placeholder="example@email.com" required>
        </div>

        <div class="form-group">
          <label><i class="fas fa-calendar"></i> تاريخ الميلاد <span class="required">*</span></label>
          <input type="date" name="birthDate" required>
        </div>

        <div class="form-group">
          <label><i class="fas fa-flag"></i> الجنسية <span class="required">*</span></label>
          <select name="nationality" required>
            <option value="">اختر الجنسية</option>
            <option value="مصري" selected>مصري</option>
            <option value="سعودي">سعودي</option>
            <option value="إماراتي">إماراتي</option>
            <option value="كويتي">كويتي</option>
            <option value="أردني">أردني</option>
            <option value="سوري">سوري</option>
            <option value="أخرى">أخرى</option>
          </select>
        </div>

        <div class="form-group">
          <label><i class="fas fa-venus-mars"></i> النوع <span class="required">*</span></label>
          <div class="radio-group">
            <label class="radio-option">
              <input type="radio" name="gender" value="ذكر" required>
              <span>ذكر</span>
            </label>
            <label class="radio-option">
              <input type="radio" name="gender" value="أنثى" required>
              <span>أنثى</span>
            </label>
          </div>
        </div>

        <div class="form-group">
          <label><i class="fas fa-school"></i> الكلية المرغوبة <span class="required">*</span></label>
          <select name="faculty" required>
            <option value="">اختر الكلية</option>
            <option value="الهندسة">كلية الهندسة</option>
            <option value="الطب">كلية الطب</option>
            <option value="الحاسبات والذكاء الاصطناعي">كلية الحاسبات والذكاء الاصطناعي</option>
            <option value="إدارة الأعمال">كلية إدارة الأعمال</option>
            <option value="العلوم">كلية العلوم</option>
            <option value="الآداب">كلية الآداب</option>
          </select>
        </div>

        <div class="form-group full-width">
          <label><i class="fas fa-comment-alt"></i> ملاحظات إضافية</label>
          <textarea name="notes" placeholder="اكتب أي ملاحظات أو استفسارات إضافية..."></textarea>
        </div>

        <div class="form-submit">
          <button type="submit">
            <i class="fas fa-paper-plane"></i>
            إرسال طلب التسجيل
          </button>
        </div>

        <p class="form-note">
          <i class="fas fa-lock"></i> بياناتك محفوظة ولن يتم مشاركتها مع أي طرف ثالث
        </p>
      </div>
    </form>
  </div>
</section>

<!-- ===== News ===== -->
<section id="news">
  <div class="section-header">
    <span class="section-tag">آخر المستجدات</span>
    <h2 class="section-title">أخبار الجامعة</h2>
    <p class="section-desc">تابع أحدث الأنشطة والفعاليات والإنجازات في جامعة المنصورة الأهلية</p>
  </div>

  <div class="news-grid">
    <div class="news-card">
      <div class="news-image">
        <img src="https://images.unsplash.com/photo-1540575467063-178a50c2df87?w=600" alt="مؤتمر">
        <div class="news-date"><span>15</span> مايو</div>
      </div>
      <div class="news-body">
        <span class="category">فعاليات</span>
        <h3>مؤتمر علمي دولي حول الذكاء الاصطناعي</h3>
        <p>استضافت الجامعة نخبة من العلماء والباحثين لمناقشة أحدث تطبيقات الذكاء الاصطناعي.</p>
        <a href="#" class="news-link">اقرأ المزيد <i class="fas fa-arrow-left"></i></a>
      </div>
    </div>

    <div class="news-card">
      <div class="news-image">
        <img src="https://images.unsplash.com/photo-1581092160562-40aa08e78837?w=600" alt="معمل">
        <div class="news-date"><span>12</span> مايو</div>
      </div>
      <div class="news-body">
        <span class="category">إنجازات</span>
        <h3>افتتاح معمل متطور لكلية الهندسة</h3>
        <p>تم تجهيز المعمل بأحدث المعدات والتقنيات لخدمة الطلاب والباحثين في مختلف التخصصات.</p>
        <a href="#" class="news-link">اقرأ المزيد <i class="fas fa-arrow-left"></i></a>
      </div>
    </div>

    <div class="news-card">
      <div class="news-image">
        <img src="https://images.unsplash.com/photo-1523050854058-8df90110c9f1?w=600" alt="تكريم">
        <div class="news-date"><span>10</span> مايو</div>
      </div>
      <div class="news-body">
        <span class="category">طلاب</span>
        <h3>تكريم الطلاب المتفوقين في الأنشطة الطلابية</h3>
        <p>كرمت الجامعة الطلاب الحاصلين على مراكز متقدمة في المسابقات المحلية والدولية.</p>
        <a href="#" class="news-link">اقرأ المزيد <i class="fas fa-arrow-left"></i></a>
      </div>
    </div>
  </div>
</section>

<!-- ===== Map Section ===== -->
<section id="location" style="background: var(--light);">
  <div class="section-header">
    <span class="section-tag">موقعنا</span>
    <h2 class="section-title">مقر جامعة المنصورة الأهلية</h2>
    <p class="section-desc">تفضل بزيارتنا في الحرم الجامعي بالمنصورة، محافظة الدقهلية</p>
  </div>

  <div class="map-wrapper">
    <iframe 
      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3418.9432!2d31.3545!3d31.0409!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x14f79d5e6a1e9e3f%3A0x8e5f8b8e5f8b8e5f!2sMansoura%20University!5e0!3m2!1sar!2seg!4v1700000000000"
      title="موقع جامعة المنصورة الأهلية"
      loading="lazy"
      referrerpolicy="no-referrer-when-downgrade"
      allowfullscreen>
    </iframe>
  </div>
</section>

<!-- ===== Contact Info Section ===== -->
<section class="contact-info" id="contact">
  <div class="section-header">
    <span class="section-tag">تواصل معنا</span>
    <h2 class="section-title">نحن في خدمتك</h2>
    <p class="section-desc">تواصل معنا عبر أي وسيلة من الوسائل التالية</p>
  </div>

  <div class="contact-info-grid">
    <div class="contact-card">
      <div class="contact-card-icon"><i class="fas fa-mobile-alt"></i></div>
      <h4>موبايل</h4>
      <a href="tel:01273111734" dir="ltr">0127 311 1734</a>
    </div>

    <div class="contact-card">
      <div class="contact-card-icon"><i class="fab fa-whatsapp"></i></div>
      <h4>واتساب</h4>
      <a href="https://wa.me/201273111734" target="_blank" rel="noopener">راسلنا الآن</a>
    </div>

    <div class="contact-card">
      <div class="contact-card-icon"><i class="fas fa-envelope"></i></div>
      <h4>البريد الإلكتروني</h4>
      <a href="mailto:info@mnu.edu.eg" dir="ltr">info@mnu.edu.eg</a>
    </div>

    <div class="contact-card">
      <div class="contact-card-icon"><i class="fas fa-map-marker-alt"></i></div>
      <h4>العنوان</h4>
      <p>المنصورة، محافظة الدقهلية، مصر</p>
    </div>
  </div>
</section>

<!-- ===== CTA ===== -->
<section class="cta">
  <div class="cta-content">
    <h2>هل أنت مستعد للانضمام إلينا؟</h2>
    <p>سجل الآن وابدأ رحلتك الأكاديمية في جامعة المنصورة الأهلية، وكن جزءاً من مستقبل مشرق.</p>
    <div class="hero-buttons" style="justify-content:center;">
      <a href="#register" class="btn btn-primary"><i class="fas fa-user-plus"></i> سجل الآن</a>
      <a href="javascript:void(0)" onclick="showPhone()" class="btn btn-outline"><i class="fas fa-phone"></i> اتصل بنا</a>
    </div>
  </div>
</section>

<!-- ===== Footer ===== -->
<footer>
  <div class="footer-grid">
    <div class="footer-col">
      <h4>جامعة المنصورة الأهلية</h4>
      <p>صرح تعليمي متميز يقدم برامج أكاديمية معتمدة دولياً، ويساهم في خدمة المجتمع وتنمية الدلتا.</p>
      <div class="footer-social">
        <a href="#" aria-label="Facebook"><i class="fab fa-facebook-f"></i></a>
        <a href="#" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
        <a href="#" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
        <a href="#" aria-label="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
        <a href="#" aria-label="YouTube"><i class="fab fa-youtube"></i></a>
      </div>
    </div>

    <div class="footer-col">
      <h4>روابط سريعة</h4>
      <ul>
        <li><a href="#home"><i class="fas fa-chevron-left"></i> الرئيسية</a></li>
        <li><a href="#about"><i class="fas fa-chevron-left"></i> عن الجامعة</a></li>
        <li><a href="#programs"><i class="fas fa-chevron-left"></i> الكليات</a></li>
        <li><a href="#register"><i class="fas fa-chevron-left"></i> التسجيل</a></li>
        <li><a href="#news"><i class="fas fa-chevron-left"></i> الأخبار</a></li>
      </ul>
    </div>

    <div class="footer-col">
      <h4>الكليات</h4>
      <ul>
        <li><a href="#programs"><i class="fas fa-chevron-left"></i> الهندسة</a></li>
        <li><a href="#programs"><i class="fas fa-chevron-left"></i> الطب</a></li>
        <li><a href="#programs"><i class="fas fa-chevron-left"></i> الحاسبات</a></li>
        <li><a href="#programs"><i class="fas fa-chevron-left"></i> إدارة الأعمال</a></li>
        <li><a href="#programs"><i class="fas fa-chevron-left"></i> العلوم</a></li>
      </ul>
    </div>

    <div class="footer-col">
      <h4>تواصل معنا</h4>
      <div class="footer-contact-item">
        <i class="fas fa-mobile-alt"></i>
        <a href="tel:01273111734" dir="ltr">0127 311 1734</a>
      </div>
      <div class="footer-contact-item">
        <i class="fas fa-envelope"></i>
        <a href="mailto:info@mnu.edu.eg" dir="ltr">info@mnu.edu.eg</a>
      </div>
      <div class="footer-contact-item">
        <i class="fas fa-map-marker-alt"></i>
        <span>المنصورة، الدقهلية</span>
      </div>
      <h4 style="margin-top:25px;">النشرة البريدية</h4>
      <form class="newsletter" onsubmit="event.preventDefault(); alert('تم الاشتراك بنجاح!');">
        <input type="email" placeholder="بريدك الإلكتروني" required>
        <button type="submit" aria-label="اشترك"><i class="fas fa-paper-plane"></i></button>
      </form>
    </div>
  </div>

  <div class="footer-bottom">
    © 2024 <span>جامعة المنصورة الأهلية</span> — جميع الحقوق محفوظة
  </div>
</footer>

<!-- ===== زر الاتصال العائم ===== -->
<a href="javascript:void(0)" onclick="showPhone()" class="floating-call-btn" aria-label="اتصل بنا">
  <i class="fas fa-phone-volume"></i>
  <span class="call-tooltip">اتصل بنا الآن</span>
</a>

<!-- ===== زر العودة للأعلى ===== -->
<button class="scroll-top" id="scrollTop" aria-label="العودة للأعلى">
  <i class="fas fa-arrow-up"></i>
</button>

<!-- ===== نافذة الاتصال ===== -->
<div id="phoneModal" class="phone-modal">
  <div class="phone-modal-content">
    <button class="phone-close" onclick="closePhone()" aria-label="إغلاق">&times;</button>

    <div class="phone-icon-big">
      <i class="fas fa-phone-volume"></i>
    </div>

    <h3>تواصل معنا</h3>
    <p>فريق جامعة المنصورة الأهلية في خدمتك</p>

    <div class="phone-numbers">
      <a href="tel:01273111734" class="phone-item main">
        <div class="phone-item-icon"><i class="fas fa-mobile-alt"></i></div>
        <div class="phone-item-info">
          <small>موبايل - القبول والتسجيل</small>
          <strong dir="ltr">0127 311 1734</strong>
        </div>
        <div class="phone-item-action">
          <i class="fas fa-phone"></i>
          <span>اتصل</span>
        </div>
      </a>

      <a href="https://wa.me/201273111734?text=مرحباً، أريد الاستفسار عن جامعة المنصورة الأهلية" 
         target="_blank" 
         rel="noopener"
         class="phone-item whatsapp">
        <div class="phone-item-icon"><i class="fab fa-whatsapp"></i></div>
        <div class="phone-item-info">
          <small>واتساب</small>
          <strong>تواصل عبر واتساب</strong>
        </div>
        <div class="phone-item-action">
          <i class="fab fa-whatsapp"></i>
          <span>محادثة</span>
        </div>
      </a>

      <button onclick="copyPhone()" class="phone-item copy-btn">
        <div class="phone-item-icon"><i class="fas fa-copy"></i></div>
        <div class="phone-item-info">
          <small>نسخ الرقم</small>
          <strong dir="ltr">0127 311 1734</strong>
        </div>
        <div class="phone-item-action">
          <i class="fas fa-copy"></i>
          <span>نسخ</span>
        </div>
      </button>
    </div>

    <div class="phone-footer">
      <i class="fas fa-clock"></i>
      <span>من السبت للخميس: 9 صباحاً - 5 مساءً</span>
    </div>
  </div>
</div>

<!-- ===== رسالة النجاح ===== -->
<div class="success-message" id="successMessage">
  <div class="success-icon">
    <i class="fas fa-check"></i>
  </div>
  <h3>تم إرسال طلبك بنجاح!</h3>
  <p>شكراً لتسجيلك في جامعة المنصورة الأهلية.<br>سيتواصل معك فريق القبول والتسجيل قريباً.</p>
  <button onclick="closeSuccess()">حسناً، شكراً</button>
</div>

<script>
  /* ===== قائمة الموبايل ===== */
  const menuToggle = document.getElementById('menuToggle');
  const navMenu = document.getElementById('navMenu');

  if (menuToggle) {
    menuToggle.addEventListener('click', () => {
      navMenu.classList.toggle('active');
      const icon = menuToggle.querySelector('i');
      if (navMenu.classList.contains('active')) {
        icon.classList.remove('fa-bars');
        icon.classList.add('fa-times');
      } else {
        icon.classList.remove('fa-times');
        icon.classList.add('fa-bars');
      }
    });

    navMenu.querySelectorAll('a').forEach(link => {
      link.addEventListener('click', () => {
        navMenu.classList.remove('active');
        const icon = menuToggle.querySelector('i');
        icon.classList.remove('fa-times');
        icon.classList.add('fa-bars');
      });
    });
  }

  /* ===== عداد الأرقام ===== */
  const counters = document.querySelectorAll('.stat-number');
  let countersStarted = false;

  function startCounters() {
    counters.forEach(counter => {
      const target = +counter.getAttribute('data-count');
      const duration = 2000;
      const step = target / (duration / 16);
      let current = 0;

      const updateCount = () => {
        current += step;
        if (current < target) {
          counter.textContent = Math.floor(current).toLocaleString('ar-EG');
          requestAnimationFrame(updateCount);
        } else {
          counter.textContent = target.toLocaleString('ar-EG');
        }
      };
      updateCount();
    });
  }

  window.addEventListener('scroll', () => {
    const statsSection = document.querySelector('.stats');
    if (!statsSection) return;
    const sectionTop = statsSection.offsetTop;
    if (!countersStarted && window.scrollY + window.innerHeight > sectionTop + 100) {
      countersStarted = true;
      startCounters();
    }
  });

  /* ===== زر العودة للأعلى ===== */
  const scrollTopBtn = document.getElementById('scrollTop');
  window.addEventListener('scroll', () => {
    if (window.scrollY > 500) {
      scrollTopBtn.classList.add('show');
    } else {
      scrollTopBtn.classList.remove('show');
    }
  });

  scrollTopBtn.addEventListener('click', () => {
    window.scrollTo({ top: 0, behavior: 'smooth' });
  });

  /* ===== نافذة الاتصال ===== */
  function showPhone() {
    document.getElementById('phoneModal').classList.add('active');
    document.body.style.overflow = 'hidden';
  }

  function closePhone() {
    document.getElementById('phoneModal').classList.remove('active');
    document.body.style.overflow = '';
  }

  /* ===== نسخ الرقم ===== */
  function copyPhone() {
    const phoneNumber = '01273111734';

    if (navigator.clipboard && window.isSecureContext) {
      navigator.clipboard.writeText(phoneNumber).then(showCopyToast);
    } else {
      const textArea = document.createElement('textarea');
      textArea.value = phoneNumber;
      textArea.style.position = 'fixed';
      textArea.style.opacity = '0';
      document.body.appendChild(textArea);
      textArea.select();
      try {
        document.execCommand('copy');
        showCopyToast();
      } catch (err) {
        alert('الرقم: ' + phoneNumber);
      }
      document.body.removeChild(textArea);
    }
  }

  function showCopyToast() {
    const toast = document.createElement('div');
    toast.className = 'copy-toast';
    toast.innerHTML = '<i class="fas fa-check-circle"></i> تم نسخ الرقم بنجاح: 01273111734';
    document.body.appendChild(toast);

    setTimeout(() => toast.classList.add('show'), 100);

    setTimeout(() => {
      toast.classList.remove('show');
      setTimeout(() => toast.remove(), 400);
    }, 2500);
  }

  /* ===== إغلاق النافذة ===== */
  document.addEventListener('DOMContentLoaded', function() {
    const modal = document.getElementById('phoneModal');
    if (modal) {
      modal.addEventListener('click', function(e) {
        if (e.target === this) closePhone();
      });
    }
  });

  document.addEventListener('keydown', function(e) {
    if (e.key === 'Escape') closePhone();
  });

  /* ===== فورم التسجيل ===== */
  function handleSubmit(event) {
    event.preventDefault();

    const form = event.target;
    const formData = new FormData(form);

    // التحقق من البيانات
    const data = {};
    formData.forEach((value, key) => {
      data[key] = value;
    });

    console.log('📋 بيانات التسجيل:', data);

    // إظهار رسالة النجاح
    document.getElementById('successMessage').classList.add('show');
    document.body.style.overflow = 'hidden';

    // إعادة تعيين الفورم
    form.reset();

    // اختياري: إرسال البيانات لواتساب
    // sendToWhatsApp(data);
  }

  function closeSuccess() {
    document.getElementById('successMessage').classList.remove('show');
    document.body.style.overflow = '';
  }

  // إغلاق الرسالة بالضغط خارجها
  document.addEventListener('click', function(e) {
    const successMsg = document.getElementById('successMessage');
    if (successMsg.classList.contains('show') && e.target === successMsg) {
      closeSuccess();
    }
  });

  /* ===== إرسال البيانات لواتساب (اختياري) ===== */
  function sendToWhatsApp(data) {
    const message = `
🎓 *طلب تسجيل جديد - جامعة المنصورة الأهلية*

👤 *الاسم:* ${data.fullName}
🆔 *الرقم القومي:* ${data.nationalId}
📱 *الموبايل:* ${data.phone}
📧 *الإيميل:* ${data.email}
🎂 *تاريخ الميلاد:* ${data.birthDate}
🌍 *الجنسية:* ${data.nationality}
⚧ *النوع:* ${data.gender}
🏛️ *الكلية:* ${data.faculty}
📝 *ملاحظات:* ${data.notes || 'لا يوجد'}
    `.trim();

    const whatsappUrl = `https://wa.me/201273111734?text=${encodeURIComponent(message)}`;
    // window.open(whatsappUrl, '_blank');
  }

  /* ===== Smooth scroll للناف بار ===== */
  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function(e) {
      const href = this.getAttribute('href');
      if (href === '#' || href === 'javascript:void(0)') return;
      
      const target = document.querySelector(href);
      if (target) {
        e.preventDefault();
        const headerOffset = 100;
        const elementPosition = target.getBoundingClientRect().top;
        const offsetPosition = elementPosition + window.pageYOffset - headerOffset;

        window.scrollTo({
          top: offsetPosition,
          behavior: 'smooth'
        });
      }
    });
  });
</script>

</body>
</html>
