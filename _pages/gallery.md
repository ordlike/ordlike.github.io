---
layout: splash
permalink: /gallery/
author_profile: true
sidebar_main: false
---

<style>
  :root {
    --accent: #0E4A84;
    --bg: #f9fbfe;
    --card: #ffffff;
    --text: #1f2937;
    --muted: #6b7280;
    --line: #e5e7eb;

    --shadow: 0 16px 50px rgba(14, 74, 132, 0.08);
    --shadow-hover: 0 22px 65px rgba(14, 74, 132, 0.14);

    --radius: 26px;
    --t: 0.35s cubic-bezier(0.165, 0.84, 0.44, 1);

    /* ✅ 메뉴바 높이 (JS가 자동으로 실제 높이로 업데이트) */
    --masthead-h: 80px;
  }

  .page__content { background: var(--bg) !important; padding: 0 !important; }

  /* ✅ 메뉴바는 항상 위에 */
  .masthead, .masthead__inner-wrap, .greedy-nav { z-index: 50000 !important; }

  .gallery-container {
    max-width: 1200px;
    margin: 70px auto;
    padding: 0 20px 40px 20px;
    font-family: 'Pretendard', -apple-system, system-ui, sans-serif;
    color: var(--text);
  }

  /* ===== Header ===== */
  .section-header { margin-bottom: 34px; }
  .section-label {
    font-size: 2.25rem;
    font-weight: 900;
    color: var(--accent);
    letter-spacing: -0.6px;
    margin: 0 0 14px 0;
  }
  .section-divider { width: 100%; }
  .section-divider .line-bold { height: 4px; background: var(--accent); border-radius: 6px; }


  /* ===== Grid ===== */
  .gallery-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
    gap: 22px;
  }

  .gallery-item {
    position: relative;
    border-radius: var(--radius);
    overflow: hidden;
    background: var(--card);
    box-shadow: var(--shadow);
    transition: transform var(--t), box-shadow var(--t);
    cursor: zoom-in;
    aspect-ratio: 1 / 1;
    border: 1px solid rgba(0,0,0,0.03);
    isolation: isolate;
  }

  .gallery-item:hover { transform: translateY(-8px); box-shadow: var(--shadow-hover); }

  .gallery-item img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
    transition: transform var(--t), filter var(--t);
    transform: scale(1.01);
  }
  .gallery-item:hover img { transform: scale(1.07); filter: saturate(1.06); }

  .gallery-item::after {
    content: "";
    position: absolute;
    inset: -30%;
    background: radial-gradient(circle at 30% 20%, rgba(255,255,255,0.20), transparent 55%);
    opacity: 0;
    transition: opacity var(--t);
    pointer-events: none;
    z-index: 2;
  }
  .gallery-item:hover::after { opacity: 1; }

  .gallery-overlay {
    position: absolute;
    inset: 0;
    background: linear-gradient(
      to bottom,
      rgba(5, 25, 45, 0.05) 0%,
      rgba(5, 25, 45, 0.35) 55%,
      rgba(5, 25, 45, 0.78) 100%
    );
    display: grid;
    align-content: end;
    gap: 6px;
    padding: 18px 18px 16px 18px;
    opacity: 0;
    transition: opacity var(--t);
    z-index: 3;
  }
  .gallery-item:hover .gallery-overlay { opacity: 1; }

  .gallery-overlay h3 {
    color: #fff;
    font-size: 1.15rem;
    font-weight: 900;
    margin: 0;
    letter-spacing: -0.2px;
    transform: translateY(10px);
    transition: transform var(--t);
  }
  .gallery-overlay p {
    color: rgba(255,255,255,0.82);
    font-size: 0.88rem;
    margin: 0;
    font-weight: 650;
    transform: translateY(10px);
    transition: transform var(--t);
  }
  .gallery-item:hover .gallery-overlay h3,
  .gallery-item:hover .gallery-overlay p { transform: translateY(0); }
     

     /* =========================================
   Gallery 페이지: 테마 기본 구분선 완전 제거
   ========================================= */

    /* h2 / section-label 아래 자동 border 제거 */
    .section-header,
    .section-header h2,
    .section-label {
    border-bottom: none !important;
    }

    /* 테마가 넣는 hr 제거 */
    .page__content hr {
    display: none !important;
    }

    /* section-header 뒤에 붙는 가상요소 제거 */
    .section-header::after,
    .section-header::before,
    .section-label::after,
    .section-label::before {
    content: none !important;
    }

    /* 혹시 남아있는 얇은 separator 대비 */
    .page__content > * {
    border-top: none !important;
    }

    /* =========================================
   Gallery 제목-파란선 간격 정밀 조정
   ========================================= */

    /* 제목 아래 여백 줄이기 */
    .section-label {
    margin-bottom: 0px !important;  /* 기본값보다 대폭 감소 */
    }

    /* divider 자체 위 여백 제거 */
    .section-divider {
    margin-top: 0 !important;
    }

    /* 혹시 남아있는 h2 기본 여백 제거 */
    .section-header h2 {
    margin-bottom: 0px !important;
    }


  /* =========================================================
     ✅ Lightbox가 메뉴바 아래에서만 뜨게
     ========================================================= */
  .lightbox {
    display: none;
    position: fixed;
    left: 0; right: 0; bottom: 0;
    top: var(--masthead-h);
    height: calc(100vh - var(--masthead-h));
    z-index: 20000; /* 메뉴바보다 낮게 */
    background: rgba(5, 15, 25, 0.92);
    backdrop-filter: blur(14px);
    -webkit-backdrop-filter: blur(14px);
    justify-content: center;
    align-items: center;
    padding: 26px 18px;
    cursor: zoom-out;
  }

  .lightbox-inner {
    width: min(1100px, 96vw);
    display: grid;
    gap: 14px;
    justify-items: center;
    cursor: default;
  }

  .lightbox-img {
    width: 100%;
    max-height: 70vh;
    object-fit: contain;
    border-radius: 18px;
    box-shadow: 0 0 60px rgba(0,0,0,0.5);
    background: rgba(255,255,255,0.02);
  }

  .lightbox-caption {
    width: 100%;
    display: grid;
    gap: 4px;
    text-align: center;
    color: #fff;
  }
  .cap-title { font-weight: 900; font-size: 1.05rem; letter-spacing: -0.2px; }
  .cap-sub { color: rgba(255,255,255,0.75); font-weight: 650; font-size: 0.92rem; }

  .close-btn {
    position: absolute;
    top: 14px;
    right: 18px;
    width: 46px;
    height: 46px;
    border-radius: 14px;
    border: 1px solid rgba(255,255,255,0.16);
    background: rgba(255,255,255,0.06);
    color: #fff;
    font-size: 28px;
    display: grid;
    place-items: center;
    cursor: pointer;
    transition: transform 0.2s ease, background 0.25s ease, opacity 0.25s ease;
    opacity: 0.85;
  }
  .close-btn:hover { opacity: 1; background: rgba(255,255,255,0.10); transform: rotate(90deg); }

  .nav-btn{
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    width: 48px;
    height: 48px;
    border-radius: 16px;
    border: 1px solid rgba(255,255,255,0.16);
    background: rgba(255,255,255,0.06);
    color: #fff;
    cursor: pointer;
    display: grid;
    place-items: center;
    font-size: 22px;
    transition: background 0.25s ease, transform 0.2s ease, opacity 0.25s ease;
    opacity: 0.85;
  }
  .nav-btn:hover{ opacity: 1; background: rgba(255,255,255,0.10); transform: translateY(-50%) scale(1.03); }
  .nav-prev{ left: 16px; }
  .nav-next{ right: 16px; }

  @media (max-width: 768px) {
    .section-label { font-size: 1.85rem; }
    .gallery-grid { grid-template-columns: repeat(2, 1fr); gap: 14px; }
    .nav-btn{ display: none; }
    .lightbox-img{ max-height: 62vh; }
  }
</style>

<div class="gallery-container">
  <div class="section-header">
    <h2 class="section-label">Gallery of Memories</h2>
    <div class="section-divider">
      <div class="line-bold"></div>
    </div>
  </div>

  <!-- ✅ grid는 딱 1번만 열기 -->
  <div class="gallery-grid">

    <div class="gallery-item"
         data-src="./../assets/new_images/team/secret/2025-12-24.jpg"
         data-title="2025 Christmas eve"
         data-sub="Lab year-end party">
      <img src="./../assets/new_images/team/secret/2025-12-24.jpg" alt="2025 Christmas eve">
      <div class="gallery-overlay"><h3>2025 Christmas eve</h3><p>Lab year-end party</p></div>
    </div>

    <div class="gallery-item"
         data-src="./../assets/new_images/team/secret/kmid.png"
         data-title="KMID 2025"
         data-sub="Conference Memory">
      <img src="./../assets/new_images/team/secret/kmid.png" alt="KMID 2025">
      <div class="gallery-overlay"><h3>KMID 2025</h3><p>Conference Memory</p></div>
    </div>

    <div class="gallery-item"
         data-src="./../assets/new_images/team/secret/2024-02-17.jpg"
         data-title="대관령여행"
         data-sub="Feb 2024 • Winter Trip">
      <img src="./../assets/new_images/team/secret/2024-02-17.jpg" alt="대관령여행">
      <div class="gallery-overlay"><h3>대관령여행</h3><p>Feb 2024 • Winter Trip</p></div>
    </div>

    <div class="gallery-item"
         data-src="./../assets/new_images/team/secret/2023-11-20.jpg"
         data-title="시상식"
         data-sub="Nov 2023 • Achievement">
      <img src="./../assets/new_images/team/secret/2023-11-20.jpg" alt="시상식">
      <div class="gallery-overlay"><h3>시상식</h3><p>Nov 2023 • Achievement</p></div>
    </div>

    <div class="gallery-item"
         data-src="./../assets/new_images/team/secret/2023-08-28.jpg"
         data-title="제주여행"
         data-sub="Aug 2023 • Summer Vacation">
      <img src="./../assets/new_images/team/secret/2023-08-28.jpg" alt="제주여행">
      <div class="gallery-overlay"><h3>제주여행</h3><p>Aug 2023 • Summer Vacation</p></div>
    </div>

    <div class="gallery-item"
         data-src="./../assets/new_images/team/secret/beech.jpg"
         data-title="속초여행"
         data-sub="Ocean Breeze">
      <img src="./../assets/new_images/team/secret/beech.jpg" alt="속초여행">
      <div class="gallery-overlay"><h3>속초여행</h3><p>Ocean Breeze</p></div>
    </div>

    <div class="gallery-item"
         data-src="./../assets/new_images/team/secret/baseball.jpg"
         data-title="잠실야구장"
         data-sub="Baseball Night">
      <img src="./../assets/new_images/team/secret/baseball.jpg" alt="잠실야구장">
      <div class="gallery-overlay"><h3>잠실야구장</h3><p>Baseball Night</p></div>
    </div>

    <div class="gallery-item"
         data-src="./../assets/new_images/team/secret/youngme.jpg"
         data-title="어린시절"
         data-sub="Throwback Memory">
      <img src="./../assets/new_images/team/secret/youngme.jpg" alt="어린시절">
      <div class="gallery-overlay"><h3>어린시절</h3><p>Throwback Memory</p></div>
    </div>

  </div>
</div>

<div class="lightbox" id="lightbox">
  <button class="close-btn" id="closeBtn" aria-label="Close">&times;</button>
  <button class="nav-btn nav-prev" id="prevBtn" aria-label="Previous">&#10094;</button>
  <button class="nav-btn nav-next" id="nextBtn" aria-label="Next">&#10095;</button>

  <div class="lightbox-inner">
    <img class="lightbox-img" id="lightboxImg" src="" alt="">
    <div class="lightbox-caption">
      <div class="cap-title" id="capTitle"></div>
      <div class="cap-sub" id="capSub"></div>
    </div>
  </div>
</div>

<script>
  // ✅ 메뉴바 높이 자동 측정 → lightbox가 그 아래에서만 뜨게
  function setMastheadHeight() {
    const masthead = document.querySelector('.masthead') || document.querySelector('header');
    if (!masthead) return;
    const h = Math.ceil(masthead.getBoundingClientRect().height);
    document.documentElement.style.setProperty('--masthead-h', h + 'px');
  }
  window.addEventListener('load', setMastheadHeight);
  window.addEventListener('resize', setMastheadHeight);

  // ====== Gallery Lightbox ======
  const items = Array.from(document.querySelectorAll('.gallery-item'));

  const lightbox   = document.getElementById('lightbox');
  const imgEl      = document.getElementById('lightboxImg');
  const capTitleEl = document.getElementById('capTitle');
  const capSubEl   = document.getElementById('capSub');

  const closeBtn = document.getElementById('closeBtn');
  const prevBtn  = document.getElementById('prevBtn');
  const nextBtn  = document.getElementById('nextBtn');

  let currentIndex = 0;

  function lockScroll(lock) {
    document.body.style.overflow = lock ? 'hidden' : 'auto';
  }

  function openAt(index) {
    setMastheadHeight(); // 열기 직전에 한번 더 정확히
    currentIndex = index;

    const item  = items[currentIndex];
    const src   = item.dataset.src;
    const title = item.dataset.title || '';
    const sub   = item.dataset.sub || '';

    imgEl.src = src;
    imgEl.alt = title;

    capTitleEl.textContent = title;
    capSubEl.textContent = sub;

    lightbox.style.display = 'flex';
    lockScroll(true);
  }

  function closeGallery() {
    lightbox.style.display = 'none';
    imgEl.src = '';
    lockScroll(false);
  }

  function prev() { openAt((currentIndex - 1 + items.length) % items.length); }
  function next() { openAt((currentIndex + 1) % items.length); }

  items.forEach((item, idx) => item.addEventListener('click', () => openAt(idx)));

  closeBtn.addEventListener('click', (e) => { e.stopPropagation(); closeGallery(); });

  // 배경(오버레이) 클릭만 닫기
  lightbox.addEventListener('click', (e) => {
    if (e.target === lightbox) closeGallery();
  });

  prevBtn.addEventListener('click', (e) => { e.stopPropagation(); prev(); });
  nextBtn.addEventListener('click', (e) => { e.stopPropagation(); next(); });

  document.addEventListener('keydown', (e) => {
    if (lightbox.style.display !== 'flex') return;
    if (e.key === 'Escape') closeGallery();
    if (e.key === 'ArrowLeft') prev();
    if (e.key === 'ArrowRight') next();
  });
</script>
