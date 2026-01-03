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
  /* =========================================================
     BASE STYLE
     ========================================================= */
  :root {
    --primary-blue: rgb(15, 15, 112);
    --dark-blue: #05192D;

    /* 기본 라이트 톤 */
    --bg-light: #f8fafc;
    --text-main: #1e293b;
    --text-muted: #64748b;

    --card-shadow: 0 10px 25px rgba(0,0,0,0.05);
    --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);

    /* ===== Vintage palette (dot-mode에서만 사용) ===== */
    --paper-bg: #f3ead7;               /* 바랜 종이 배경 */
    --paper-warm: rgba(184, 141, 72, 0.22); /* 세피아 워밍 */
    --paper-dark: rgba(60, 45, 25, 0.12);   /* 종이 얼룩/음영 */
    --grid-ink: rgba(55, 40, 22, 0.18);     /* 격자 잉크 */
    --grain-ink: rgba(45, 35, 20, 0.12);    /* 그레인 */
  }

  .page__content {
    background-color: var(--bg-light) !important;
    padding: 0 !important;
  }

  /* 상단 소속 정보 */
  .department-banner {
    background: #fff;
    padding: 25px 20px;
    text-align: center;
    border-bottom: 1px solid #e2e8f0;
    font-family: 'Pretendard', sans-serif;
  }
  .department-banner p {
    margin: 0;
    font-size: 0.95rem;
    color: var(--text-main);
    line-height: 1.6;
  }
  .department-banner em {
    color: var(--primary-blue);
    font-style: normal;
    font-weight: 700;
  }

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
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: var(--transition);
  }

  .nav-card:hover .img-box img { transform: scale(1.1); }

  .nav-card .text-box {
    padding: 30px;
    text-align: center;
  }

  .nav-card h2 {
    margin: 0 0 12px;
    font-size: 1.5rem;
    color: var(--primary-blue);
    font-weight: 800;
  }

  .nav-card p {
    margin: 0;
    font-size: 0.95rem;
    color: var(--text-muted);
    line-height: 1.5;
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
    content: "";
    flex: 1;
    height: 1px;
    background: #e2e8f0;
  }

  /* 뉴스 카드 */
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

  .news-img { flex: 0 0 45%; min-height: 300px; }
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
    font-size: 1.8rem;
    margin: 0 0 20px;
    color: var(--text-main);
    font-weight: 800;
    line-height: 1.3;
  }

  .news-text p {
    font-size: 1.05rem;
    color: var(--text-muted);
    margin-bottom: 30px;
    line-height: 1.6;
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

  /* 반응형 */
  @media (max-width: 900px) {
    .nav-grid { grid-template-columns: 1fr; }
    .news-card { flex-direction: column; }
    .news-img { min-height: 200px; }
    .news-text { padding: 30px; }
  }
</style>

<style>
  /* =========================================================
     DOT MODE + VINTAGE PAPER (Sepia + Grain + Thicker Grid)
     - dot-mode 켜질 때만 동작
     - 격자는 더 굵게 / 종이 질감 + 세피아 + 빈티지 톤
     ========================================================= */

  /* 전체 톤: 세피아/콘트라스트 살짝 */
  body.dot-mode{
    filter: saturate(1.05) contrast(1.08) sepia(0.22);
  }

  /* 배경을 종이처럼 */
  body.dot-mode .page__content{
    background:
      /* 종이 음영(얼룩) */
      radial-gradient(900px 520px at 18% 12%, rgba(60,45,25,0.10) 0%, rgba(60,45,25,0.00) 62%),
      radial-gradient(900px 520px at 82% 28%, rgba(184,141,72,0.12) 0%, rgba(184,141,72,0.00) 60%),
      radial-gradient(900px 520px at 40% 88%, rgba(60,45,25,0.08) 0%, rgba(60,45,25,0.00) 55%),
      /* 기본 종이 색 */
      linear-gradient(180deg, rgba(243,234,215,0.92), rgba(243,234,215,0.92)) !important;
  }

  /* 카드/배너도 살짝 종이 톤 */
  body.dot-mode .nav-card,
  body.dot-mode .news-card,
  body.dot-mode .department-banner{
    background: rgba(255,255,255,0.80);
    border-color: rgba(90, 70, 35, 0.12);
    box-shadow: 0 14px 36px rgba(45, 35, 20, 0.10);
  }

  body.dot-mode .department-banner{
    border-bottom-color: rgba(90, 70, 35, 0.18);
  }

  body.dot-mode .section-title::after{
    background: rgba(90, 70, 35, 0.22);
  }

  /* ====== 오버레이: 격자(굵게) + 그레인 + 스캔라인 ====== */
  body.dot-mode::before{
    content:"";
    position: fixed;
    inset: 0;
    pointer-events: none;
    z-index: 9998;
    opacity: 0.30;
    mix-blend-mode: multiply;

    /* ✅ 더 굵은 격자 + 점(도트) */
    background:
      /* 굵은 격자: 1.6px */
      linear-gradient(to right, rgba(55,40,22,0.20) 0 1.6px, transparent 1.6px 100%) 0 0 / 28px 28px,
      linear-gradient(to bottom, rgba(55,40,22,0.20) 0 1.6px, transparent 1.6px 100%) 0 0 / 28px 28px,

      /* 보조 격자(살짝): 1px */
      linear-gradient(to right, rgba(55,40,22,0.10) 0 1px, transparent 1px 100%) 0 0 / 14px 14px,
      linear-gradient(to bottom, rgba(55,40,22,0.10) 0 1px, transparent 1px 100%) 0 0 / 14px 14px,

      /* 도트(점): 조금 큼 */
      radial-gradient(circle, rgba(0,0,0,0.18) 1.35px, transparent 1.9px) 0 0 / 7px 7px;
  }

  body.dot-mode::after{
    content:"";
    position: fixed;
    inset: 0;
    pointer-events: none;
    z-index: 9999;
    mix-blend-mode: multiply;

    /* ✅ 종이 그레인 + 스캔라인(기존 느낌 유지) */
    background:
      /* grain */
      radial-gradient(circle at 12% 18%, rgba(45,35,20,0.10) 0 1px, transparent 1px 100%) 0 0 / 8px 8px,
      radial-gradient(circle at 78% 42%, rgba(45,35,20,0.08) 0 1px, transparent 1px 100%) 0 0 / 9px 9px,
      radial-gradient(circle at 34% 76%, rgba(45,35,20,0.07) 0 1px, transparent 1px 100%) 0 0 / 10px 10px,

      /* scanline */
      repeating-linear-gradient(
        to bottom,
        rgba(0,0,0,0.26) 0px,
        rgba(0,0,0,0.26) 1px,
        rgba(0,0,0,0) 4px,
        rgba(0,0,0,0) 8px
      );

    opacity: 0.22;
  }

  /* DOT MODE 뱃지 */
  .dotmode-badge{
    display: none;
    position: fixed;
    right: 14px;
    bottom: 14px;
    z-index: 10000;
    padding: 10px 12px;
    border-radius: 12px;
    font-weight: 900;
    font-size: 12px;
    letter-spacing: 0.10em;
    color: #fff;
    background: linear-gradient(135deg, rgba(14,74,132,0.95), rgba(15,15,112,0.95));
    border: 1px solid rgba(255,255,255,0.18);
    box-shadow: 0 14px 34px rgba(14,74,132,0.22);
    user-select: none;
    pointer-events: none;
  }
  body.dot-mode .dotmode-badge{ display: block; }

  /* =========================================================
     CAT (PNG)
     ========================================================= */
  .cat-walker{
    position: fixed;
    left: 20px;
    top: 45vh;
    width: 352px;
    height: 352px;
    z-index: 10001;
    user-select: none;
    opacity: 0;
    pointer-events: auto;
    transform: translate3d(var(--x, 0px), var(--y, 0px), 0) scaleX(var(--sx, 1));
    filter: drop-shadow(0 12px 14px rgba(0,0,0,0.18));
    transition: opacity .25s ease;
    will-change: transform;
  }
  body.cat-on .cat-walker{ opacity: 1; }

  .cat-walker img{
    width: 100%;
    height: 100%;
    object-fit: contain;
    display: block;
  }

  body.cat-on .cat-walker.is-moving{
    animation: catBounce .35s ease-in-out infinite alternate;
  }
  @keyframes catBounce{
    from { transform: translate3d(var(--x,0px), var(--y,0px), 0) scaleX(var(--sx,1)); }
    to   { transform: translate3d(var(--x,0px), calc(var(--y,0px) - 2px), 0) scaleX(var(--sx,1)); }
  }

  body.cat-on .cat-walker.is-sitting{
    animation: catBreathe 2.5s ease-in-out infinite !important;
  }

  @keyframes catBreathe {
    0%, 100% {
      transform: translate3d(var(--x,0px), var(--y,0px), 0) scaleX(var(--sx,1)) scale(0.92);
    }
    50% {
      transform: translate3d(var(--x,0px), calc(var(--y,0px) + 1px), 0) scaleX(var(--sx,1)) scale(0.94);
    }
  }

  .cat-bubble{
    position: fixed;
    z-index: 10002;
    padding: 9px 12px;
    background: rgba(255,255,255,0.95);
    border: 1px solid rgba(0,0,0,0.08);
    border-radius: 999px;
    box-shadow: 0 14px 34px rgba(0,0,0,0.12);
    font-weight: 900;
    font-size: 13px;
    color: rgba(15,15,112,0.95);
    opacity: 0;
    transform: translateY(6px);
    pointer-events: none;
    transition: opacity .18s ease, transform .18s ease;
  }
  .cat-bubble.show{
    opacity: 1;
    transform: translateY(0);
  }

  /* 빈티지 모드에서는 말풍선도 살짝 종이톤 */
  body.dot-mode .cat-bubble{
    background: rgba(243,234,215,0.95);
    border-color: rgba(55,40,22,0.18);
    color: rgba(55,40,22,0.92);
    box-shadow: 0 16px 36px rgba(45, 35, 20, 0.14);
  }
</style>

<div class="dotmode-badge">VINTAGE DOT</div>

<div class="cat-walker" id="catWalker" aria-label="ORDLIKE Cat" title="Click me!">
  <img src="/assets/new_images/esteregg/ordlike_cat.png" alt="ORDLIKE Cat">
</div>
<div class="cat-bubble" id="catBubble" aria-hidden="true">야옹!</div>

<script>
/* =========================================================
   Easter Egg Trigger:
   - "Welcome to ORDLIKE!" title box multi-click => DOT + CAT together
   ========================================================= */
(function(){
  const REQUIRED_CLICKS = 5;
  const WINDOW_MS = 1600;

  let clickCount = 0;
  let lastClickTime = 0;

  function toggleDotAndCat(){
    document.body.classList.toggle("dot-mode");

    const catOn = document.body.classList.toggle("cat-on");
    window.__ORDLIKE_CAT_ENABLE && window.__ORDLIKE_CAT_ENABLE(catOn);

    try { if (navigator.vibrate) navigator.vibrate(25); } catch(_){}
  }

  function findWelcomeTitle(){
    const candidates = [
      ".page__hero--overlay .page__title",
      ".page__hero .page__title",
      "h1.page__title",
      ".page__title",
      "h1"
    ];
    for(const sel of candidates){
      const els = document.querySelectorAll(sel);
      for(const el of els){
        const t = (el.textContent || "").trim().toLowerCase();
        if(t.includes("welcome to ordlike")) return el;
      }
    }
    return null;
  }

  const titleEl = findWelcomeTitle();

  function onClick(){
    const now = Date.now();
    if(now - lastClickTime > WINDOW_MS) clickCount = 0;
    lastClickTime = now;

    clickCount++;
    if(clickCount >= REQUIRED_CLICKS){
      toggleDotAndCat();
      clickCount = 0;
    }
  }

  if(titleEl){
    titleEl.style.cursor = "pointer";
    titleEl.title = "Click multiple times 😉";
    titleEl.addEventListener("click", onClick);
  }else{
    document.addEventListener("click", onClick, {passive:true});
  }
})();
</script>

<script>
/* =========================================================
   CAT Behavior (PNG Walker) - Smooth Version
   - roam (main), gentle steering
   - slight follow when far
   - run away when near (but no sudden "stop")
   - click => meow bubble
   - sit on nav-cards: VERY RARE (almost never)
   ========================================================= */
(function(){
  const cat = document.getElementById("catWalker");
  const bubble = document.getElementById("catBubble");
  if(!cat || !bubble) return;

  // ============ MUST MATCH CSS ============
  const CAT_SIZE = 352;
  const CAT_HALF = CAT_SIZE / 2;

  // ============ Tunables (smoother) ============
  const EDGE_PAD = 24;

  // motion
  const BASE_SPEED = 2.15;
  const FOLLOW_BOOST = 1.10;
  const MAX_SPEED  = 5.0;
  const TURN_RATE  = 0.055;
  const BRAKE_LERP = 0.06;

  // behavior distances
  const NEAR_DIST   = 150;
  const FOLLOW_DIST = 380;

  // target management
  const TARGET_REPICK_MS = 2400;
  const ARRIVE_DIST = 34;
  const ARRIVE_GRACE_MS = 500;

  // sitting: make it "almost never"
  const SIT_ENABLE = true;
  const SIT_MS = 420;
  const SIT_COOLDOWN_MS = 6500;
  const SIT_CHANCE = 0.10;
  const SIT_MIN_MOVE_MS = 2200;

  let enabled = false;

  // cat pos stored as TOP-LEFT in viewport coords
  let x = 40;
  let y = window.innerHeight * 0.55;

  // velocity (smoothed)
  let vx = 0, vy = 0;

  // steering direction
  let tx = 1, ty = 0;

  // target
  let targetX = x, targetY = y;
  let lastTargetPick = 0;
  let lastArriveTime = 0;

  // mouse
  let mouseX = window.innerWidth * 0.5;
  let mouseY = window.innerHeight * 0.5;

  // sit state
  let sitUntil = 0;
  let lastSit = 0;
  let lastMovedAt = Date.now();

  function rand(min, max){ return Math.random() * (max - min) + min; }
  function clamp(v, a, b){ return Math.max(a, Math.min(b, v)); }

  function pickRandomTarget(){
    const w = window.innerWidth, h = window.innerHeight;
    targetX = rand(EDGE_PAD, Math.max(EDGE_PAD, w - EDGE_PAD));
    targetY = rand(EDGE_PAD, Math.max(EDGE_PAD, h - EDGE_PAD));
    lastTargetPick = Date.now();
  }

  function setCSSVars(){
    cat.style.setProperty("--x", x + "px");
    cat.style.setProperty("--y", y + "px");
    cat.style.setProperty("--sx", (vx >= 0 ? 1 : -1));
  }

  function showMeow(text){
    bubble.textContent = text || "야옹!";
    bubble.classList.add("show");

    const r = cat.getBoundingClientRect();
    bubble.style.left = (r.left + r.width * 0.15) + "px";
    bubble.style.top  = (r.top - 12) + "px";

    clearTimeout(showMeow.__t);
    showMeow.__t = setTimeout(()=> bubble.classList.remove("show"), 900);
  }

  function setSitting(on){
    if(on){
      cat.classList.remove("is-moving");
      cat.classList.add("is-sitting");
    }else{
      cat.classList.remove("is-sitting");
      cat.classList.add("is-moving");
    }
  }

  // external toggle (called by trigger)
  window.__ORDLIKE_CAT_ENABLE = function(on){
    enabled = !!on;
    if(enabled){
      pickRandomTarget();
      setCSSVars();
      cat.classList.add("is-moving");
      requestAnimationFrame(step);
    }else{
      cat.classList.remove("is-moving", "is-sitting");
      bubble.classList.remove("show");
    }
  };

  // mouse tracking
  window.addEventListener("mousemove", (e)=>{ mouseX = e.clientX; mouseY = e.clientY; }, {passive:true});
  window.addEventListener("touchmove", (e)=>{
    if(!e.touches || !e.touches[0]) return;
    mouseX = e.touches[0].clientX;
    mouseY = e.touches[0].clientY;
  }, {passive:true});

  // click cat => bubble
  cat.addEventListener("click", (e)=>{
    e.stopPropagation();
    const msgs = ["Wanny!", "tung..tung..", "meow!", "ORDLIKE!", "🐾"];
    showMeow(msgs[Math.floor(Math.random() * msgs.length)]);
    try { if (navigator.vibrate) navigator.vibrate(18); } catch(_){}
  });

  function isInsideAnyNavCard(cx, cy){
    const cards = document.querySelectorAll(".nav-grid .nav-card");
    for(const el of cards){
      const r = el.getBoundingClientRect();
      if(cx >= r.left && cx <= r.right && cy >= r.top && cy <= r.bottom){
        return true;
      }
    }
    return false;
  }

  function step(){
    if(!enabled) return;

    const now = Date.now();
    const w = window.innerWidth, h = window.innerHeight;

    // sitting window
    if(now < sitUntil){
      setSitting(true);
      vx *= (1 - BRAKE_LERP);
      vy *= (1 - BRAKE_LERP);
      setCSSVars();
      requestAnimationFrame(step);
      return;
    }else{
      setSitting(false);
    }

    const r = cat.getBoundingClientRect();
    const cx = r.left + r.width * 0.5;
    const cy = r.top  + r.height * 0.5;

    // Rare sit logic
    if(SIT_ENABLE){
      const canSit = (now - lastSit > SIT_COOLDOWN_MS) && (now - lastMovedAt > SIT_MIN_MOVE_MS);
      if(canSit && isInsideAnyNavCard(cx, cy) && Math.random() < SIT_CHANCE){
        sitUntil = now + SIT_MS;
        lastSit = now;
        requestAnimationFrame(step);
        return;
      }
    }

    // target repick
    if(now - lastTargetPick > TARGET_REPICK_MS){
      pickRandomTarget();
    }

    // distance to mouse
    const mdx = cx - mouseX;
    const mdy = cy - mouseY;
    const mdist = Math.hypot(mdx, mdy);

    let desiredX = targetX;
    let desiredY = targetY;
    let desiredSpeed = BASE_SPEED;

    if(mdist < NEAR_DIST){
      const ux = mdx / (mdist || 1);
      const uy = mdy / (mdist || 1);

      desiredX = clamp(cx + ux * 280, EDGE_PAD, w - EDGE_PAD);
      desiredY = clamp(cy + uy * 280, EDGE_PAD, h - EDGE_PAD);

      desiredSpeed = MAX_SPEED;
      lastTargetPick = now - (TARGET_REPICK_MS - 900);
    }else if(mdist > FOLLOW_DIST){
      desiredX = targetX * 0.55 + mouseX * 0.45;
      desiredY = targetY * 0.55 + mouseY * 0.45;
      desiredSpeed = BASE_SPEED * FOLLOW_BOOST;
    }else{
      desiredX = targetX;
      desiredY = targetY;
      desiredSpeed = BASE_SPEED;
    }

    const dx = desiredX - cx;
    const dy = desiredY - cy;
    const dist = Math.hypot(dx, dy);

    if(dist < ARRIVE_DIST && (now - lastArriveTime > ARRIVE_GRACE_MS)){
      lastArriveTime = now;
      pickRandomTarget();
    }

    const ndx = dx / (dist || 1);
    const ndy = dy / (dist || 1);

    // smooth turn
    tx = tx + (ndx - tx) * TURN_RATE;
    ty = ty + (ndy - ty) * TURN_RATE;

    // desired velocity
    const dvx = tx * desiredSpeed;
    const dvy = ty * desiredSpeed;

    // smooth velocity
    vx = vx + (dvx - vx) * (BRAKE_LERP + 0.02);
    vy = vy + (dvy - vy) * (BRAKE_LERP + 0.02);

    // apply move
    x += vx;
    y += vy;

    // clamp inside viewport
    x = clamp(x, EDGE_PAD, w - EDGE_PAD - CAT_SIZE);
    y = clamp(y, EDGE_PAD, h - EDGE_PAD - CAT_SIZE);

    if(Math.abs(vx) + Math.abs(vy) > 0.35){
      lastMovedAt = now;
    }

    setCSSVars();
    requestAnimationFrame(step);
  }

  window.addEventListener("resize", ()=>{
    if(!enabled) return;
    const w = window.innerWidth, h = window.innerHeight;
    x = clamp(x, EDGE_PAD, w - EDGE_PAD - CAT_SIZE);
    y = clamp(y, EDGE_PAD, h - EDGE_PAD - CAT_SIZE);
    pickRandomTarget();
    setCSSVars();
  });
})();
</script>

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
