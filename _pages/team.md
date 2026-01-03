---
layout: splash
permalink: /team/
author_profile: true
sidebar_main: false
---

<style>
  /* ===== 테마 설정 ===== */
  :root {
    --bg-main: #f9fbfe;
    --card-bg: #ffffff;
    --accent-blue: #0E4A84;
    --text-main: #334155;
    --text-muted: #64748b;
    --border: #f1f5f9;
    --shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
  }

  .page__content { background-color: var(--bg-main) !important; color: var(--text-main); }

  .team-container {
    max-width: 1200px;
    margin: 0 auto;
    font-family: 'Pretendard', -apple-system, sans-serif;
    padding: 40px 20px;
  }

  /* ===== 섹션 타이틀 ===== */
  .section-header { margin: 80px 0 40px 0; }
  .section-label {
    font-size: 2.2rem;
    font-weight: 850;
    color: var(--accent-blue);
    margin-bottom: 12px;
    display: block;
    letter-spacing: -0.5px;
  }
  .line-thick { width: 100%; height: 3px; background-color: var(--accent-blue); margin-bottom: 5px; }
  .line-thin { width: 100%; height: 1px; background-color: #cbd5e1; }

  /* ===== 팀 멤버 그리드 ===== */
  .member-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 30px;
    margin-bottom: 60px;
  }

  .member-card {
    background: var(--card-bg);
    border-radius: 32px;
    padding: 35px;
    box-shadow: var(--shadow);
    border: 1px solid var(--border);
    display: flex;
    align-items: center;
    gap: 35px;
    transition: all 0.3s ease;
    text-decoration: none !important;
    color: inherit !important;
  }

  .member-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 20px 40px rgba(0,0,0,0.1);
    border-color: var(--accent-blue);
  }

  /* 멤버 사진 박스 (크기 200px 유지) */
  .member-img-box {
    flex: 0 0 130px; 
    height: 180px;    
    border-radius: 40px;
    overflow: hidden; /* 넘치는 이미지 숨김 */
    box-shadow: 0 10px 25px rgba(0,0,0,0.1);
    background-color: #fff;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  /* [수정됨] 내부 이미지 확대 설정 */
  .member-img-box img {
    width: 105%;
    height: 105%;
    object-fit: cover; /* 박스를 꽉 채우도록 설정 */
    transform: scale(1); /* 기본 상태에서 15% 확대 (이 수치를 조절하세요) */
    transition: transform 0.3s ease;
  }
  /* 마우스 호버 시 조금 더 확대 */
  .member-card:hover .member-img-box img { transform: scale(1.25); }

  /* 멤버 정보 */
  .member-info { flex: 1; }
  .member-info h2 {
    margin: 0 0 11px 0;
    font-size: 1.5rem;
    font-weight: 800;
    color: var(--accent-blue);
  }
  .member-meta {
    font-size: 0.8rem;
    line-height: 1.7;
    color: var(--text-main);
  }
  .member-meta strong { color: var(--accent-blue); font-weight: 700; }
  
  .research-tag {
    display: inline-block;
    margin-top: 15px;
    padding: 6px 16px;
    background: #f1f5f9;
    border-radius: 10px;
    font-size: 0.8rem;
    font-weight: 700;
    color: var(--text-muted);
  }

  /* 반응형 */
  @media (max-width: 950px) {
    .member-grid { grid-template-columns: 1fr; }
    .member-card { padding: 30px; gap: 25px; }
    .member-img-box { flex: 0 0 160px; height: 160px; }
  }
</style>

<div class="team-container">

  <div class="section-header">
    <span class="section-label">EE Design Project Team</span>
    <div class="line-thick"></div>
    <div class="line-thin"></div>
  </div>

  <div class="member-grid">
    <a href="https://softrobotics.snu.ac.kr/people.php" class="member-card" target="_blank">
      <div class="member-img-box"><img src="/assets/new_images/team/yonghyun_final.jpg" alt="Yong-hyeon Lee"></div>
      <div class="member-info">
        <h2>Yong-hyeon Lee</h2>
        <div class="member-meta">
          <strong>B.S.</strong> ME, Hanyang University<br>
          <strong>E-mail</strong> younnj@snu.ac.kr
        </div>
        <div class="research-tag">Robot operating system</div>
      </div>
    </a>

    <a href="https://sites.google.com/view/hyu-mm/members" class="member-card" target="_blank">
      <div class="member-img-box"><img src="/assets/new_images/team/seungju_final.jpg" alt="Seung-ju Cha"></div>
      <div class="member-info">
        <h2>Seung-ju Cha</h2>
        <div class="member-meta">
          <strong>B.S.</strong> ME, Hanyang University<br>
          <strong>E-mail</strong> chaseungju990201@gmail.com
        </div>
        <div class="research-tag">Machine learning</div>
      </div>
    </a>

    <a href="#" class="member-card">
      <div class="member-img-box"><img src="/assets/new_images/team/changjun_final.jpg" alt="Chang-jun Lee"></div>
      <div class="member-info">
        <h2>Chang-jun Lee</h2>
        <div class="member-meta">
          <strong>B.S.</strong> ME, Hanyang University<br>
          <strong>E-mail</strong> changjoon@kaist.ac.kr
        </div>
        <div class="research-tag">3D CAD modeling</div>
      </div>
    </a>

    <a href="#" class="member-card">
      <div class="member-img-box"><img src="/assets/new_images/team/donghoon_final.jpg" alt="Dong-hoon Oh"></div>
      <div class="member-info">
        <h2>Dong-hoon Oh</h2>
        <div class="member-meta">
          <strong>UG Year 4</strong> ME, Hanyang University<br>
          <strong>E-mail</strong> hoon6049@hanyang.ac.kr
        </div>
        <div class="research-tag">Computer Vision</div>
      </div>
    </a>
  </div>

  <div class="section-header">
    <span class="section-label">ME Design Project Team</span>
    <div class="line-thick"></div>
    <div class="line-thin"></div>
  </div>

  <div class="member-grid">
    <a href="https://sites.google.com/hanyang.ac.kr/tsdlab/members" class="member-card" target="_blank">
      <div class="member-img-box"><img src="/assets/new_images/team/jeonghoon_final.jpg" alt="Jeong-hoon Lee"></div>
      <div class="member-info">
        <h2>Jeong-hoon Lee</h2>
        <div class="member-meta">
          <strong>B.S.</strong> ME, Hanyang University<br>
          <strong>E-mail</strong> chjklmpwy@hanyang.ac.kr
        </div>
        <div class="research-tag">Translational Soft Devices</div>
      </div>
    </a>

    <a href="https://sites.google.com/hanyang.ac.kr/tsdlab/members" class="member-card" target="_blank">
      <div class="member-img-box"><img src="/assets/new_images/team/jeongwoo_final.jpg" alt="Jeong-woo Woo"></div>
      <div class="member-info">
        <h2>Jeong-woo Woo</h2>
        <div class="member-meta">
          <strong>B.S.</strong> ME, Hanyang University<br>
          <strong>E-mail</strong> korwoo1@hanyang.ac.kr
        </div>
        <div class="research-tag">Translational Soft Devices</div>
      </div>
    </a>
  </div>

  <div class="section-header">
    <span class="section-label">Hanyang Academic Town</span>
    <div class="line-thick"></div>
    <div class="line-thin"></div>
  </div>

  <div class="member-grid">
    <a href="#" class="member-card">
      <div class="member-img-box"><img src="/assets/new_images/team/seonghyeon_final.jpg" alt="Seoung-hyeon Yuk"></div>
      <div class="member-info">
        <h2>Seoung-hyeon Yuk</h2>
        <div class="member-meta">
          <strong>B.S.</strong> ME, Hanyang University<br>
          <strong>E-mail</strong> seonghyeon.yuk@mobis.com
        </div>
        <div class="research-tag">Power semiconductor module</div>
      </div>
    </a>

    <a href="#" class="member-card">
      <div class="member-img-box"><img src="/assets/new_images/team/euihyeon_final.jpg" alt="Eui-hyeon Park"></div>
      <div class="member-info">
        <h2>Eui-hyeon Park</h2>
        <div class="member-meta">
          <strong>UG Year 4</strong> ME, Hanyang University<br>
          <strong>E-mail</strong> pyh4683@hanyang.ac.kr
        </div>
        <div class="research-tag">Vehicle controls</div>
      </div>
    </a>
  </div>

</div>