---
layout: splash
permalink: /gallery/
author_profile: true
sidebar_main: false
---

<style>
  /* ===== 테마 변수 (기존 디자인 시스템 통합) ===== */
  :root {
    --primary-blue: #0E4A84;
    --dark-blue: #05192D;
    --bg-main: #f9fbfe;
    --card-bg: #ffffff;
    --shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
    --shadow-hover: 0 20px 40px rgba(14, 74, 132, 0.15);
    --transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
  }

  .page__content { background-color: var(--bg-main) !important; padding: 0 !important; }

  .gallery-container {
    max-width: 1200px;
    margin: 60px auto;
    padding: 0 20px;
    font-family: 'Pretendard', sans-serif;
  }

  /* ===== 섹션 헤더 (일관성 유지) ===== */
  .section-header { margin-bottom: 50px; text-align: left; }
  .section-label {
    font-size: 2.2rem;
    font-weight: 850;
    color: var(--dark-blue);
    letter-spacing: -1px;
    display: block;
    margin-bottom: 10px;
  }
  .header-line {
    width: 100%; height: 4px; background: var(--primary-blue);
    border-radius: 2px; position: relative;
  }
  .header-line::after {
    content: ""; position: absolute; left: 0; top: 10px;
    width: 60%; height: 1px; background: #cbd5e1;
  }

  /* ===== 갤러리 그리드 ===== */
  .gallery-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 25px;
  }

  .gallery-item {
    position: relative;
    border-radius: 28px;
    overflow: hidden;
    background: var(--card-bg);
    box-shadow: var(--shadow);
    transition: var(--transition);
    cursor: zoom-in;
    aspect-ratio: 1 / 1; /* 모든 이미지를 정삼각형으로 통일하여 정갈하게 배치 */
  }

  .gallery-item:hover {
    transform: translateY(-10px);
    box-shadow: var(--shadow-hover);
  }

  .gallery-item img {
    width: 100%;
    height: 100%;
    object-fit: cover; /* 비율에 맞춰 꽉 채움 */
    transition: var(--transition);
  }

  .gallery-item:hover img {
    transform: scale(1.1);
  }

  /* ===== 오버레이 (글래스모피즘 스타일) ===== */
  .gallery-overlay {
    position: absolute;
    inset: 0;
    background: rgba(5, 25, 45, 0.4);
    backdrop-filter: blur(4px); /* 현대적인 블러 효과 */
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    opacity: 0;
    transition: var(--transition);
    padding: 20px;
    text-align: center;
  }

  .gallery-item:hover .gallery-overlay {
    opacity: 1;
  }

  .gallery-overlay h3 {
    color: #fff;
    font-size: 1.4rem;
    font-weight: 800;
    margin: 0;
    transform: translateY(20px);
    transition: var(--transition);
  }

  .gallery-item:hover .gallery-overlay h3 {
    transform: translateY(0);
  }

  .gallery-overlay p {
    color: rgba(255,255,255,0.8);
    font-size: 0.9rem;
    margin-top: 10px;
    font-weight: 500;
  }

  /* ===== Lightbox (확대 보기) ===== */
  .lightbox {
    display: none; position: fixed; z-index: 10000; inset: 0;
    background: rgba(5, 25, 45, 0.96); backdrop-filter: blur(12px);
    justify-content: center; align-items: center; cursor: zoom-out;
  }
  .lightbox-img { max-width: 90%; max-height: 85%; border-radius: 16px; box-shadow: 0 0 50px rgba(0,0,0,0.5); }
  .close-btn { position: absolute; top: 30px; right: 40px; color: #fff; font-size: 50px; cursor: pointer; opacity: 0.6; }
  .close-btn:hover { opacity: 1; transform: rotate(90deg); transition: 0.3s; }

  @media (max-width: 768px) {
    .gallery-grid { grid-template-columns: repeat(2, 1fr); gap: 15px; }
    .section-label { font-size: 1.8rem; }
  }
</style>

<div class="gallery-container">
  <div class="section-header">
    <span class="section-label">Gallery of Memories</span>
    <div class="header-line"></div>
  </div>

  <div class="gallery-grid">
    <div class="gallery-item" onclick="openGallery('./../assets/new_images/team/secret/kmid.png')">
      <img src="./../assets/new_images/team/secret/kmid.png" alt="KMID 2025">
      <div class="gallery-overlay">
        <h3>KMID 2025</h3>
        <p>Conference Memory</p>
      </div>
    </div>

    <div class="gallery-item" onclick="openGallery('./../assets/new_images/team/secret/2024-02-17.jpg')">
      <img src="./../assets/new_images/team/secret/2024-02-17.jpg" alt="대관령여행">
      <div class="gallery-overlay">
        <h3>대관령여행</h3>
        <p>Feb 2024 • Winter Trip</p>
      </div>
    </div>

    <div class="gallery-item" onclick="openGallery('./../assets/new_images/team/secret/2023-11-20.jpg')">
      <img src="./../assets/new_images/team/secret/2023-11-20.jpg" alt="시상식">
      <div class="gallery-overlay">
        <h3>시상식</h3>
        <p>Nov 2023 • Achievement</p>
      </div>
    </div>

    <div class="gallery-item" onclick="openGallery('./../assets/new_images/team/secret/2023-08-28.jpg')">
      <img src="./../assets/new_images/team/secret/2023-08-28.jpg" alt="제주여행">
      <div class="gallery-overlay">
        <h3>제주여행</h3>
        <p>Aug 2023 • Summer Vacation</p>
      </div>
    </div>

    <div class="gallery-item" onclick="openGallery('./../assets/new_images/team/secret/beech.jpg')">
      <img src="./../assets/new_images/team/secret/beech.jpg" alt="속초여행">
      <div class="gallery-overlay">
        <h3>속초여행</h3>
        <p>Ocean Breeze</p>
      </div>
    </div>

    <div class="gallery-item" onclick="openGallery('./../assets/new_images/team/secret/baseball.jpg')">
      <img src="./../assets/new_images/team/secret/baseball.jpg" alt="잠실야구장">
      <div class="gallery-overlay">
        <h3>잠실야구장</h3>
        <p>Baseball Night</p>
      </div>
    </div>

    <div class="gallery-item" onclick="openGallery('./../assets/new_images/team/secret/youngme.jpg')">
      <img src="./../assets/new_images/team/secret/youngme.jpg" alt="어린시절">
      <div class="gallery-overlay">
        <h3>어린시절</h3>
        <p>Throwback Memory</p>
      </div>
    </div>
  </div>
</div>

<div class="lightbox" id="lightbox" onclick="closeGallery()">
  <span class="close-btn">&times;</span>
  <img class="lightbox-img" id="lightboxImg" src="">
</div>

<script>
  function openGallery(src) {
    const lightbox = document.getElementById("lightbox");
    const lightboxImg = document.getElementById("lightboxImg");
    lightboxImg.src = src;
    lightbox.style.display = "flex";
    document.body.style.overflow = "hidden"; // 스크롤 방지
  }

  function closeGallery() {
    const lightbox = document.getElementById("lightbox");
    lightbox.style.display = "none";
    document.body.style.overflow = "auto";
  }

  // ESC 키로 닫기
  document.addEventListener("keydown", (e) => {
    if (e.key === "Escape") closeGallery();
  });
</script>