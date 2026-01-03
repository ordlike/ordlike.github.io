---
layout: splash
permalink: /about/
author_profile: true
sidebar_main: true
---

<style>
  /* ===== 테마 설정 ===== */
  :root {
    --bg-main: #f9fbfe; /* 본문 하늘색 배경 */
    --card-bg: #ffffff;
    --accent-blue: #0E4A84;
    --text-main: #334155;
    --text-muted: #64748b;
    --border: #f1f5f9;
    --shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
  }

  /* 전체 페이지 배경 설정 */
  .page__content { background-color: var(--bg-main) !important; color: var(--text-main); padding-bottom: 0 !important; }

  .bento-container {
    max-width: 1200px;
    margin: 0 auto;
    font-family: 'Pretendard', -apple-system, sans-serif;
    padding: 40px 20px;
    line-height: 1.7;
  }

  /* ===== 섹션 타이틀 양식 ===== */
  .section-header { margin: 80px 0 40px 0; }
  .section-label {
    font-size: 2.6rem;
    font-weight: 850;
    color: var(--accent-blue);
    margin-bottom: 12px;
    display: block;
    letter-spacing: -1px;
  }
  .line-thick { width: 100%; height: 3.5px; background-color: var(--accent-blue); margin-bottom: 6px; }
  .line-thin { width: 100%; height: 1px; background-color: #cbd5e1; }

  /* ===== Hero Card (프로필) ===== */
  .hero-card {
    background: var(--card-bg);
    border-radius: 32px;
    padding: 60px;
    box-shadow: var(--shadow);
    display: flex;
    gap: 50px;
    align-items: center;
    margin-bottom: 40px;
    border: 1px solid var(--border);
  }
  .hero-img {
    flex: 0 0 220px; height: 220px;
    border-radius: 55px;
    overflow: hidden;
    box-shadow: 0 15px 35px rgba(0,0,0,0.1);
  }
  .hero-img img { width: 100%; height: 100%; object-fit: cover; }
  
  .hero-text h1 { 
    font-size: 2.4rem; 
    margin: 0 0 15px; 
    color: rgb(15, 15, 112); 
    font-weight: 850; 
  }
  
  .link-chip {
    padding: 10px 20px; border-radius: 12px; border: 1px solid var(--border);
    text-decoration: none; color: var(--text-main); font-weight: 700; font-size: 0.95rem;
    background: #f8fafc; transition: 0.3s; display: inline-block; margin-top: 20px;
  }
  .link-chip:hover { background: var(--accent-blue); color: #fff; transform: translateY(-3px); }

  /* ===== Bento Grid & Cards ===== */
  .bento-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 30px;
    align-items: start;
  }
  .full-width { grid-column: span 2; }

  .bento-card {
    background: var(--card-bg);
    border-radius: 28px;
    padding: 45px;
    box-shadow: var(--shadow);
    border: 1px solid var(--border);
  }
  .card-label { font-size: 0.85rem; font-weight: 800; color: var(--accent-blue); text-transform: uppercase; margin-bottom: 25px; letter-spacing: 2px; }

  /* 이미지 프레임 */
  .img-frame {
    width: 100%;
    border-radius: 16px;
    border: 1px solid var(--border);
    overflow: hidden;
    margin: 15px 0 25px 0;
    background: #f8fafd;
  }
  .img-frame img { width: 100%; height: auto; display: block; }

  /* 리스트 스타일 */
  .info-list { list-style: none; padding: 0; margin: 0; }
  .info-list li { margin-bottom: 20px; padding-left: 28px; position: relative; font-size: 1.05rem; }
  .info-list li::before { content: "✔️"; position: absolute; left: 0; top: 2px; color: var(--accent-blue); font-weight: bold; }
  
  .date-tag { 
    color: var(--accent-blue); 
    font-weight: 700; 
    font-size: 0.9rem; 
    display: inline-block; 
    margin-left: 8px; 
  }

  /* Coursework Grid */
  .course-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(230px, 1fr));
    gap: 15px;
  }
  .course-item {
    background: #f8fafc; padding: 14px 18px; border-radius: 12px;
    display: flex; justify-content: space-between; 
    align-items: center; /* 줄바꿈 시 Grade 수직 중앙 정렬 */
    font-size: 0.95rem; font-weight: 600;
    border: 1px solid var(--border);
    line-height: 1.3; /* 줄바꿈 시 간격 조절 */
  }
  .grade { color: var(--accent-blue); font-weight: 800; }

  @media (max-width: 850px) {
    .hero-card { flex-direction: column; text-align: center; padding: 40px; }
    .bento-grid { grid-template-columns: 1fr; }
    .full-width { grid-column: span 1; }
    .section-label { font-size: 2.2rem; }
  }
</style>

<div class="bento-container">

  <div class="hero-card">
    <div class="hero-img">
      <img src="/assets/new_images/ORD.jpg" alt="Chae-Hwan Park">
    </div>
    <div class="hero-text">
      <h1>Chae-Hwan Park</h1>
      <div class="hero-info">
        <p><strong>B.S.</strong>&nbsp;&nbsp;ME and EE, Hanyang University</p>
        <p><strong>E-mail</strong> ordlike@snu.ac.kr</p>
        <p><strong>Research Areas</strong> CMOS/TFT Circuit Design, Neuromorphic Device and System Design</p>
      </div>
      <div style="display: flex; gap: 10px; flex-wrap: wrap;">
        <a href="https://blog.naver.com/ordlike" target="_blank" class="link-chip">Blog</a>
        <a href="https://instagram.com/chae_wanny?igshid=ZDc4ODBmN[jlmNQ==" target="_blank" class="link-chip">Instagram</a>
        <a href="https://sites.google.com/view/snu-acelab" target="_blank" class="link-chip">Laboratory</a>
      </div>
    </div>
  </div>

  <div class="section-header">
    <span class="section-label">Education</span>
    <div class="double-line"><div class="line-thick"></div><div class="line-thin"></div></div>
  </div>
  
  <div class="bento-grid">
    <div class="bento-card full-width">
      <span class="card-label">Degrees & Path</span>
      <ul class="info-list">
        <li><strong>Seoul National University</strong>&nbsp; Integrated M.S.-Ph.D in <a href="https://ece.snu.ac.kr/" style="color: inherit; text-decoration: underline;">Electrical and Computer Engineering</a> <span class="date-tag">Mar 2024 - Present</span></li>
        <li><strong>Hanyang University</strong>&nbsp; B.S. in <a href="http://me.hanyang.ac.kr/" style="color: inherit; text-decoration: underline;">Mechanical Engineering</a> & <a href="http://ee.hanyang.ac.kr/" style="color: inherit; text-decoration: underline;">Electronic Engineering</a> <span class="date-tag">Mar 2018 - Feb 2024</span></li>
      </ul>
    </div>
    <div class="bento-card full-width">
      <span class="card-label">Relevant Coursework</span>
      <div class="course-grid">
        <div class="course-item">Electric Engineering <span class="grade">A+</span></div>
        <div class="course-item">Electronic Engineering <span class="grade">A+</span></div>
        <div class="course-item">Circuit<br>Theory 1 <span class="grade">A+</span></div>
        <div class="course-item">The Physics of Solid-state <span class="grade">A+</span></div>
        <div class="course-item">Circuit<br>Theory 2 <span class="grade">A+</span></div>
        <div class="course-item">Semiconductor Devices <span class="grade">A+</span></div>
        <div class="course-item">Electronic Circuit 1 <span class="grade">A0</span></div>
        <div class="course-item">Semiconductor Fabrications <span class="grade">A+</span></div>
        <div class="course-item">Electronic Circuit 2 <span class="grade">A+</span></div>
        <div class="course-item">VLSI Engineering <span class="grade">A0</span></div>
      </div>
    </div>
  </div>

  <div class="section-header">
    <span class="section-label">Awards</span>
    <div class="double-line"><div class="line-thick"></div><div class="line-thin"></div></div>
  </div>
  <div class="bento-grid">
    <div class="bento-card full-width">
      <span class="card-label">Honors & Recognition</span>
      <ul class="info-list">
        <li><strong>Hanyang Academic Excellence Award</strong><span class="date-tag">Feb 2024</span></li>
        <div class="img-frame" style="max-width: 400px; margin: 15px auto 25px auto;"><img src="/images/about/graduate_award.jpg" alt="Award"></div>
        <li><strong>Hanyang Academic Town Program Award</strong><span class="date-tag">Dec 2023 / Dec 2022</span></li>
        <li><strong>Mechanical Engineering Design Project 1/2 Award</strong><span class="date-tag">May 2023 / Nov 2023</span></li>
        <li><strong>LG Electronics Product Design Project Award</strong><span class="date-tag">Jun 2023</span></li>
        <li><strong>Hanyang Learning Pacemaker Program Award</strong><span class="date-tag">Jul 2023</span></li>
        <li><strong>Hanyang Engineering Drone Design Award</strong><span class="date-tag">Jun 2018</span></li>
        <div class="img-frame"><img src="/images/about/awards.png" alt="Awards Collection"></div>
      </ul>
    </div>
  </div>

  <div class="section-header">
    <span class="section-label">Experiences</span>
    <div class="double-line"><div class="line-thick"></div><div class="line-thin"></div></div>
  </div>
  <div class="bento-grid">
    <div class="bento-card full-width">
      <span class="card-label">Activities & Milestones</span>
      <ul class="info-list">
        <li><strong>KIDS Display School: Backplane / Drive and Circuit</strong><span class="date-tag">2024</span></li>
        <div class="img-frame" style="max-width: 400px; margin: 15px auto 25px auto;"><img src="/images/about/KIDSschool.png" alt="KIDS school"></div>
        <li><strong>Samsung Dream Class Mentoring Completion</strong><span class="date-tag">2022 - 2024</span></li>
        <div class="img-frame" style="max-width: 950px; margin: 15px auto 25px auto;"><img src="/images/about/dreamclass3.png" alt="Dream Class"></div>
        <li><strong>Athletic Achievements & Land Run</strong></li>
        <p style="padding-left: 28px; color: var(--text-muted); margin-bottom: 5px;">
          - Chuncheon Marathon 42.195km (Full-course) <span class="date-tag">2025</span><br>
          - JTBC Seoul Marathon 42.195km (Full-course) <span class="date-tag">2024</span><br>
          - Busan-Incheon 633km Bicycle Land Run <span class="date-tag">2020</span>
        </p>
        <div class="img-frame"><img src="/images/about/마라톤2_국토종주.png" alt="Sports"></div>
      </ul>
    </div>
  </div>

  <div class="section-header">
    <span class="section-label">Personal</span>
    <div class="double-line"><div class="line-thick"></div><div class="line-thin"></div></div>
  </div>
  <div class="bento-card full-width" style="padding: 60px; margin-bottom: 40px;">
    <div style="text-align: center;">
      <p style="font-size: 1.5rem; font-weight: 700; color: var(--accent-blue); margin-bottom: 20px;">Piano 🎹 & Drums 🥁</p>
      <p style="font-size: 1.1rem;">My hobbies are playing the piano and drums! I'm very interested in music!<br></p>
    </div>
  </div>

</div> 

<div style="background-color: #ffffff; width: 100%; padding: 80px 0 40px 0; border-top: 1px solid #f1f5f9; margin-top: 50px;">
  <div style="max-width: 1100px; margin: 0 auto; padding: 0 20px;">
    <div style="width: 100%; margin-bottom: 40px; text-align: center;">
      <img src="/images/about/bottom.jpg" alt="Bottom Banner" style="width: 100%; max-width: 1000px; border-radius: 20px;">
    </div>
    <footer style="text-align: center; color: var(--text-muted); font-size: 0.95rem; font-family: sans-serif;">
      Last Update: 2026/01/03
    </footer>
  </div>
</div>