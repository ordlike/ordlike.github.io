---
title: "Welcome to ORDLIKE!"
layout: splash
permalink: /main/
date: 2025-02-02    
header:
  overlay_color: "#000"
  overlay_filter: "0.3"
  overlay_image: /assets/new_images/main.gif
  actions:
    - label: "Download CV"
      url: "https://raw.githubusercontent.com/ordlike/ordlike.github.io/master/Files/C.V_Chaehwan%20Park.pdf" 
    - label: "Direct Contact"
      url: "/contact/"
excerpt: "Hello! I'm Chae-Hwan Park. <br> ORDLIKE Website is My personal homepage. "

feature_row2:
  - image_path: /assets/new_images/news2.jpg
    alt: "placeholder image 2"
    title: "Playing the drums at the Band Club Hanwoollim Performance!"
    excerpt: "On October 6, 2023, I played the drums for 'Buzz - Journey For Myself' at the Hanwoollim Freshman Performance, a band club at Hanyang University's College of Engineering."
    url: "/third/"
    btn_label: "Read More"
    btn_class: "btn--primary"
---

<style>
  /* ===== 디자인 테마 설정 (세련된 스타일 유지) ===== */
  :root {
    --primary-blue: #0E4A84;
    --dark-blue: #05192D;
    --bg-light: #f8fafc;
    --text-main: #1e293b;
    --text-muted: #64748b;
    --card-shadow: 0 10px 25px rgba(0,0,0,0.05);
    --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  }

  .page__content { background-color: var(--bg-light) !important; padding: 0 !important; }

  /* 상단 소속 정보 */
  .department-banner {
    background: #fff;
    padding: 25px 20px;
    text-align: center;
    border-bottom: 1px solid #DCDCDC;
    font-family: 'Pretendard', sans-serif;
  }
  .department-banner p {
    margin: 0; font-size: 11px; color: #000; line-height: 1.6;
  }
  .department-banner em { font-style: italic; }

  /* 메인 컨테이너 */
  .main-content-wrapper {
    max-width: 1200px;
    margin: 0 auto;
    padding: 60px 20px;
  }

  /* 네비게이션 그리드 카드 */
  .nav-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 30px;
    margin-bottom: 80px;
  }

  .nav-card {
    background: #fff;
    border-radius: 24px;
    overflow: hidden;
    box-shadow: var(--card-shadow);
    transition: var(--transition);
    text-decoration: none !important;
    display: flex;
    flex-direction: column;
    border: 1px solid rgba(226, 232, 240, 0.5);
    min-height: 480px;
  }

  .nav-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 20px 40px rgba(0,0,0,0.1);
  }

  .nav-card .img-box {
    width: 100%;
    height: 320px;
    overflow: hidden;
  }

  .nav-card .img-box img {
    width: 100%; height: 100%; object-fit: cover;
    transition: var(--transition);
  }

  .nav-card:hover .img-box img { transform: scale(1.1); }

  .nav-card .text-box {
    padding: 30px;
    text-align: center;
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .nav-card h1 {
    margin: 0 0 12px; font-size: 1.5rem; color: #000; font-weight: 800;
  }

  .nav-card p {
    margin: 0; font-size: 0.95rem; color: #000; line-height: 1.5;
  }

  /* 뉴스 섹션 헤더 */
  .hot-news-header {
    font-weight: bold;
    font-size: 35px;
    margin-bottom: 40px;
    text-align: left;
    border-top: 1px solid #DCDCDC;
    padding-top: 40px;
    color: #000000;
  }

  /* 뉴스 카드 디자인 (Bento Style) */
  .news-card {
    background: #fff;
    border-radius: 28px;
    display: flex;
    overflow: hidden;
    box-shadow: var(--card-shadow);
    border: 1px solid rgba(226, 232, 240, 0.8);
    transition: var(--transition);
    text-decoration: none !important;
  }

  .news-card:hover { box-shadow: 0 15px 35px rgba(0,0,0,0.08); }

  .news-img {
    flex: 0 0 45%;
    min-height: 300px;
  }
  .news-img img { width: 100%; height: 100%; object-fit: cover; }

  .news-text {
    flex: 1;
    padding: 50px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: left;
  }

  .news-text h1 {
    font-size: 1.8rem; margin: 0 0 20px; color: #000; font-weight: 800; line-height: 1.3;
  }

  .news-text p {
    font-size: 1.05rem; color: #000; margin-bottom: 30px; line-height: 1.6;
  }

  .btn--primary {
    align-self: flex-start;
    padding: 12px 28px;
    background-color: #0E4A84;
    color: #fff !important;
    border-radius: 5px;
    font-weight: bold;
    text-decoration: none;
    transition: background-color 0.3s ease-in-out;
  }
  .btn--primary:hover { background-color: rgb(15, 15, 112); }

  @media (max-width: 900px) {
    .nav-grid { grid-template-columns: 1fr; }
    .news-card { flex-direction: column; }
    .nav-card { min-height: auto; }
    .news-img { min-height: 200px; }
    .news-text { padding: 30px; }
  }
</style>

<div class="department-banner">
  <p>
    Dept. of <em>Electrical and Computer Engineering</em> at Seoul National University, Seoul.<br>
    If you have any questions, please feel free to contact me.
  </p>
</div>

<div class="main-content-wrapper">
  
  <section class="nav-grid">
    <a href="/about" class="nav-card">
      <div class="img-box"><img src="/assets/new_images/aboutme_final.gif" alt="About me"></div>
      <div class="text-box">
        <h1>About me</h1>
        <p>If you want more information <strong>About me</strong>, please come in!</p>
      </div>
    </a>

    <a href="/team" class="nav-card">
      <div class="img-box"><img src="/assets/new_images/Team_2_final.jpg" alt="Team"></div>
      <div class="text-box">
        <h1>Team</h1>
        <p>Introducing the <strong>Team members</strong> who worked with me.</p>
      </div>
    </a>

    <a href="/research" class="nav-card">
      <div class="img-box"><img src="/assets/new_images/project2_original.jpg" alt="research"></div>
      <div class="text-box">
        <h1>Research</h1>
        <p>Let me introduce the <strong>Research</strong> I've been working on!</p>
      </div>
    </a>
  </section>

  <h1 class="hot-news-header">:: HOT News ::</h1>
  
  <section class="hot-news-container">
    <a href="/fifth/" class="news-card">
      <div class="news-img">
        <img src="/assets/new_images/news4.png" alt="hot 1">
      </div>
      <div class="news-text">
        <h1>Completed the full marathon course!</h1>
        <p>On November 3rd, 2024, I completed the 42.195km full course of the Seoul Marathon hosted by JTBC in 5 hours, 39 minutes and 29 seconds. Please congratulate me!</p>
        <span class="btn--primary">Read More</span>
      </div>
    </a>
  </section>

</div>