---
title: "Welcome to ORDLIKE!"
layout: splash
permalink: /main/
date: 2025-02-02    
header:
  overlay_color: "#05192D"
  overlay_filter: "0.35"
  overlay_image: /assets/new_images/main.gif
  actions:
    - label: "<i class='fas fa-file-download'></i> Download CV"
      url: "https://raw.githubusercontent.com/ordlike/ordlike.github.io/master/Files/C.V_Chaehwan%20Park.pdf" 
    - label: "<i class='fas fa-envelope'></i> Contact Me"
      url: "/contact/"
excerpt: "<strong>Hello! I'm Chae-Hwan Park. </strong><br>Integrated M.S.-Ph.D Researcher at SNU ACE Lab.<br><small></small>"
---

<style>
  /* ===== 전역 스타일 최적화 ===== */
  :root {
    --primary-blue: rgb(15, 15, 112);
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
    border-bottom: 1px solid #e2e8f0;
    font-family: 'Pretendard', sans-serif;
  }
  .department-banner p {
    margin: 0; font-size: 0.95rem; color: var(--text-main); line-height: 1.6;
  }
  .department-banner em { color: var(--primary-blue); font-style: normal; font-weight: 700; }

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
  }

  .nav-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 20px 40px rgba(0,0,0,0.1);
  }

  .nav-card .img-box {
    width: 100%;
    height: 220px;
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
  }

  .nav-card h2 {
    margin: 0 0 12px; font-size: 1.5rem; color: var(--primary-blue); font-weight: 800;
  }

  .nav-card p {
    margin: 0; font-size: 0.95rem; color: var(--text-muted); line-height: 1.5;
  }

  /* 뉴스 섹션 헤더 */
  .section-title {
    font-size: 2rem;
    font-weight: 850;
    color: var(--primary-blue);
    margin-bottom: 40px;
    display: flex;
    align-items: center;
    gap: 15px;
  }
  .section-title::after {
    content: ""; flex: 1; height: 1px; background: #e2e8f0;
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
  }

  .news-tag {
    color: var(--primary-blue);
    font-weight: 800;
    font-size: 0.85rem;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 15px;
    display: block;
  }

  .news-text h3 {
    font-size: 1.8rem; margin: 0 0 20px; color: var(--text-main); font-weight: 800; line-height: 1.3;
  }

  .news-text p {
    font-size: 1.05rem; color: var(--text-muted); margin-bottom: 30px; line-height: 1.6;
  }

  .read-more-btn {
    align-self: flex-start;
    padding: 12px 28px;
    background: var(--primary-blue);
    color: #fff !important;
    border-radius: 12px;
    font-weight: 700;
    font-size: 0.95rem;
    transition: var(--transition);
  }
  .news-card:hover .read-more-btn { background: var(--dark-blue); transform: translateX(5px); }

  /* 반응형 처리 */
  @media (max-width: 900px) {
    .nav-grid { grid-template-columns: 1fr; }
    .news-card { flex-direction: column; }
    .news-img { min-height: 200px; }
    .news-text { padding: 30px; }
  }
</style>

<div class="department-banner">
  <p>
    Dept. of <em>Electrical and Computer Engineering</em> at <em>Seoul National University</em>, South Korea.<br>
    If you have any questions, please feel free to contact me.
  </p>
</div>

<div class="main-content-wrapper">
  
  <section class="nav-grid">
    <a href="/about" class="nav-card">
      <div class="img-box"><img src="/assets/new_images/aboutme_final.gif" alt="About"></div>
      <div class="text-box">
        <h2>About Me</h2>
        <p>If you want more information About me, please come in!</p>
      </div>
    </a>
    <a href="/team" class="nav-card">
      <div class="img-box"><img src="/assets/new_images/Team_2_final.jpg" alt="Team"></div>
      <div class="text-box">
        <h2>Team</h2>
        <p>Introducing the Team members who worked with me.</p>
      </div>
    </a>
    <a href="/research" class="nav-card">
      <div class="img-box"><img src="/assets/new_images/project2_original.jpg" alt="Research"></div>
      <div class="text-box">
        <h2>Research</h2>
        <p>Let me introduce the Research I've been working on!</p>
      </div>
    </a>
  </section>

  <div class="section-title">Latest Updates</div>
  
  <section class="hot-news-section">
    <a href="/fifth/" class="news-card">
      <div class="news-img">
        <img src="/assets/new_images/news4.png" alt="Marathon">
      </div>
      <div class="news-text">
        <span class="news-tag">Achievement • Nov 2024</span>
        <h3>Completed the Full Marathon Course!</h3>
        <p>Successfully finished the 42.195km JTBC Seoul Marathon in 5h 39m. A meaningful journey testing physical and mental limits.</p>
        <span class="read-more-btn">Read Full Story →</span>
      </div>
    </a>
  </section>

</div>