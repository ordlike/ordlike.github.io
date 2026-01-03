---
layout: splash
permalink: /team/
author_profile: true
sidebar_main: false
---

<style>
  /* ===== Theme ===== */
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

  /* ===== Section Title ===== */
  .section-header { margin: 70px 0 34px 0; }
  .section-label {
    font-size: 1.8rem;
    font-weight: 850;
    color: var(--accent-blue);
    margin-bottom: 12px;
    display: block;
    letter-spacing: -0.5px;
  }
  .line-thick { width: 100%; height: 3px; background-color: var(--accent-blue); margin-bottom: 5px; }
  /* ✅ 회색선 제거하고 싶으면 아래 줄을 주석/삭제하면 됨 */
  .line-thin { width: 100%; height: 1px; background-color: #cbd5e1; }

  /* ===== Grid ===== */
  .member-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 30px;
    margin-bottom: 60px;
  }

  /* ===== Card ===== */
  .member-card {
    background: var(--card-bg);
    border-radius: 32px;
    padding: 35px;
    box-shadow: var(--shadow);
    border: 1px solid var(--border);
    display: flex;
    align-items: center;
    gap: 32px;
    transition: transform .25s ease, box-shadow .25s ease, border-color .25s ease;
    text-decoration: none !important;
    color: inherit !important;
    overflow: hidden; /* ✅ 모바일에서 내부가 튀어나오지 않게 */
  }

  .member-card:hover {
    transform: translateY(-6px);
    box-shadow: 0 20px 40px rgba(0,0,0,0.10);
    border-color: rgba(14,74,132,0.35);
  }

  /* ===== Image Box (Desktop) ===== */
  .member-img-box {
    flex: 0 0 140px;
    height: 180px;
    border-radius: 40px;
    overflow: hidden;
    box-shadow: 0 10px 25px rgba(0,0,0,0.10);
    background: #fff;
  }

  .member-img-box img {
    width: 100%;
    height: 100%;
    object-fit: cover;

    /* ✅ 얼굴이 위로 잘리는 경우가 많아서 기본은 살짝 위쪽(=눈/얼굴) 잡기 */
    object-position: center 25%;

    /* ✅ hover 확대는 데스크탑에서만 자연스러움 */
    transform: scale(1.02);
    transition: transform .25s ease;
    display:block;
  }

  .member-card:hover .member-img-box img {
    transform: scale(1.10);
  }

  /* ===== Text ===== */
  .member-info { flex: 1; min-width: 0; }

  .member-info h2 {
    margin: 0 0 10px 0;
    font-size: 1.5rem;
    font-weight: 850;
    color: var(--accent-blue);
    line-height: 1.15;
  }

  .member-meta {
    font-size: 0.88rem;
    line-height: 1.75;
    color: var(--text-main);
  }
  .member-meta strong { color: var(--accent-blue); font-weight: 800; }

  .research-tag {
    display: inline-block;
    margin-top: 14px;
    padding: 7px 16px;
    background: #f1f5f9;
    border-radius: 999px;
    font-size: 0.82rem;
    font-weight: 800;
    color: var(--text-muted);
    border: 1px solid rgba(15, 23, 42, 0.06);
  }

  /* ===== Responsive ===== */
  @media (max-width: 950px) {
    .member-grid { grid-template-columns: 1fr; }
    .member-card { padding: 28px; gap: 22px; }
    .member-img-box { flex: 0 0 150px; height: 150px; border-radius: 34px; }
    .member-info h2 { font-size: 1.35rem; }
  }

  /* ✅ 핵심: 모바일(좁은 화면)에서는 "가로 배너"가 아니라 "프로필 비율"로! */

/* ===============================
   MOBILE: 가로형 카드 유지
================================ */
@media (max-width: 560px) {

  .member-card {
    flex-direction: row;     /* ✅ 가로 유지 */
    align-items: center;
    gap: 16px;
    padding: 18px;
  }

  .member-img-box {
    flex: 0 0 90px;          /* ✅ 얼굴 크기 고정 */
    width: 90px;
    height: 120px;           /* 세로 살짝 긴 증명사진 비율 */
    border-radius: 16px;
  }

  .member-img-box img {
    width: 100%;
    height: 100%;
    object-fit: cover;       /* 이 비율에서는 잘림 거의 없음 */
    object-position: center 20%;
    transform: none !important;  /* ✅ 확대 완전 제거 */
  }

  .member-card:hover .member-img-box img {
    transform: none !important;
  }

  .member-info h2 {
    font-size: 1.15rem;
    margin-bottom: 6px;
  }

  .member-meta {
    font-size: 0.78rem;
    line-height: 1.45;
  }

  .research-tag {
    margin-top: 8px;
    font-size: 0.72rem;
    padding: 4px 10px;
  }
}



  

</style>

<div class="team-container">

  <div class="section-header">
    <span class="section-label">EE Design Project Team</span>
    <div class="line-thick"></div>
  </div>

  <div class="member-grid">
    <a href="https://softrobotics.snu.ac.kr/people.php" class="member-card" target="_blank" rel="noopener">
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

    <a href="https://sites.google.com/view/hyu-mm/members" class="member-card" target="_blank" rel="noopener">
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
  </div>

  <div class="member-grid">
    <a href="https://sites.google.com/hanyang.ac.kr/tsdlab/members" class="member-card" target="_blank" rel="noopener">
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

    <a href="https://sites.google.com/hanyang.ac.kr/tsdlab/members" class="member-card" target="_blank" rel="noopener">
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
