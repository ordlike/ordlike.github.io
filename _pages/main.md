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

    --bg-light: #f8fafc;
    --text-main: #1e293b;
    --text-muted: #64748b;

    --card-shadow: 0 10px 25px rgba(0,0,0,0.05);
    --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);

    --paper-bg: #f3ead7;
  }

  .page__content {
    background-color: var(--bg-light) !important;
    padding: 0 !important;
    position: relative;
    z-index: 0;
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

  .main-content-wrapper {
    max-width: 1200px;
    margin: 0 auto;
    padding: 60px 20px;
    position: relative;
    z-index: 2;
  }

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

  @media (max-width: 900px) {
    .nav-grid { grid-template-columns: 1fr; }
    .news-card { flex-direction: column; }
    .news-img { min-height: 200px; }
    .news-text { padding: 30px; }
  }
</style>

<style>
  /* =========================================================
     DOT MODE + VINTAGE (overlay를 .page__content에만 적용)
     ========================================================= */

  body.dot-mode{
    filter: saturate(1.05) contrast(1.08) sepia(0.22);
  }

  body.dot-mode .page__content{
    background:
      radial-gradient(900px 520px at 18% 12%, rgba(60,45,25,0.10) 0%, rgba(60,45,25,0.00) 62%),
      radial-gradient(900px 520px at 82% 28%, rgba(184,141,72,0.12) 0%, rgba(184,141,72,0.00) 60%),
      radial-gradient(900px 520px at 40% 88%, rgba(60,45,25,0.08) 0%, rgba(60,45,25,0.00) 55%),
      linear-gradient(180deg, rgba(243,234,215,0.92), rgba(243,234,215,0.92)) !important;
  }

  body.dot-mode .nav-card,
  body.dot-mode .news-card,
  body.dot-mode .department-banner{
    background: rgba(255,255,255,0.80);
    border-color: rgba(90, 70, 35, 0.12);
    box-shadow: 0 14px 36px rgba(45, 35, 20, 0.10);
  }

  body.dot-mode .department-banner{ border-bottom-color: rgba(90, 70, 35, 0.18); }
  body.dot-mode .section-title::after{ background: rgba(90, 70, 35, 0.22); }

  body.dot-mode .page__content::before,
  body.dot-mode .page__content::after{
    content:"";
    position: fixed;
    inset: 0;
    pointer-events: none;
    z-index: 1;
  }

  body.dot-mode .page__content::before{
    opacity: 0.30;
    mix-blend-mode: multiply;
    background:
      linear-gradient(to right, rgba(55,40,22,0.20) 0 1.6px, transparent 1.6px 100%) 0 0 / 28px 28px,
      linear-gradient(to bottom, rgba(55,40,22,0.20) 0 1.6px, transparent 1.6px 100%) 0 0 / 28px 28px,
      linear-gradient(to right, rgba(55,40,22,0.10) 0 1px, transparent 1px 100%) 0 0 / 14px 14px,
      linear-gradient(to bottom, rgba(55,40,22,0.10) 0 1px, transparent 1px 100%) 0 0 / 14px 14px,
      radial-gradient(circle, rgba(0,0,0,0.18) 1.35px, transparent 1.9px) 0 0 / 7px 7px;
  }

  body.dot-mode .page__content::after{
    opacity: 0.22;
    mix-blend-mode: multiply;
    background:
      radial-gradient(circle at 12% 18%, rgba(45,35,20,0.10) 0 1px, transparent 1px 100%) 0 0 / 8px 8px,
      radial-gradient(circle at 78% 42%, rgba(45,35,20,0.08) 0 1px, transparent 1px 100%) 0 0 / 9px 9px,
      radial-gradient(circle at 34% 76%, rgba(45,35,20,0.07) 0 1px, transparent 1px 100%) 0 0 / 10px 10px,
      repeating-linear-gradient(
        to bottom,
        rgba(0,0,0,0.26) 0px,
        rgba(0,0,0,0.26) 1px,
        rgba(0,0,0,0) 4px,
        rgba(0,0,0,0) 8px
      );
  }

  /* badge */
  .dotmode-badge{
    display: none;
    position: fixed;
    right: 14px;
    bottom: 14px;
    z-index: 20000;
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
     - ✅ 말풍선이 고양이 내부 absolute라 항상 같은 거리 유지
     - ✅ flip(scaleX)은 cat-sprite만 적용 (말풍선 글씨 반전 방지)
     - ✅ 클릭/터치 시 조금씩 커짐: --cat-scale
     ========================================================= */
  .cat-walker{
    position: fixed;
    left: 20px;
    top: 45vh;

    width: clamp(180px, 82vw, 352px);
    height: clamp(180px, 82vw, 352px);

    z-index: 25000;
    user-select: none;

    opacity: 0;
    visibility: hidden;
    pointer-events: none;

    /* ✅ translate + scale */
    transform: translate3d(var(--x, 0px), var(--y, 0px), 0) scale(var(--cat-scale, 1));
    transform-origin: center;
    filter: drop-shadow(0 12px 14px rgba(0,0,0,0.18));
    transition: opacity .25s ease, visibility .25s ease;
    will-change: transform;
    touch-action: pan-y;
  }

  body.cat-on .cat-walker{
    opacity: 1;
    visibility: visible;
    pointer-events: auto;
  }

  .cat-sprite{
    width: 100%;
    height: 100%;
    transform: scaleX(var(--sx, 1));
    transform-origin: center;
    will-change: transform;
  }

  .cat-sprite img{
    width: 100%;
    height: 100%;
    object-fit: contain;
    display: block;
  }

  body.cat-on .cat-walker.is-moving{
    animation: catBounce .35s ease-in-out infinite alternate;
  }
  @keyframes catBounce{
    from { transform: translate3d(var(--x,0px), var(--y,0px), 0) scale(var(--cat-scale,1)); }
    to   { transform: translate3d(var(--x,0px), calc(var(--y,0px) - 2px), 0) scale(var(--cat-scale,1)); }
  }

  body.cat-on .cat-walker.is-sitting{
    animation: catBreathe 2.5s ease-in-out infinite !important;
  }
  @keyframes catBreathe {
    0%, 100% { transform: translate3d(var(--x,0px), var(--y,0px), 0) scale(calc(var(--cat-scale,1) * 0.92)); }
    50%      { transform: translate3d(var(--x,0px), calc(var(--y,0px) + 1px), 0) scale(calc(var(--cat-scale,1) * 0.94)); }
  }

  /* =========================================================
     CUTE BUBBLE (cat 기준 absolute)
     ========================================================= */
  .cat-bubble{
    position: absolute;
    left: 18%;
    top: -14px;
    z-index: 26000;

    padding: 10px 14px;
    border-radius: 999px;
    font-weight: 900;
    font-size: 13px;
    letter-spacing: 0.02em;

    color: rgba(15,15,112,0.98);
    background: linear-gradient(180deg, rgba(255,255,255,0.98), rgba(245,248,255,0.95));
    border: 1px solid rgba(0,0,0,0.08);

    box-shadow:
      0 14px 34px rgba(0,0,0,0.12),
      inset 0 1px 0 rgba(255,255,255,0.85);

    opacity: 0;
    transform: translateY(8px) scale(0.98);
    pointer-events: none;
    transition: opacity .18s ease, transform .18s ease;
    will-change: transform, opacity;
  }

  .cat-bubble::after{
    content:"";
    position: absolute;
    left: 18px;
    bottom: -7px;
    width: 12px;
    height: 12px;
    background: inherit;
    border-left: 1px solid rgba(0,0,0,0.08);
    border-bottom: 1px solid rgba(0,0,0,0.08);
    transform: rotate(45deg);
    border-bottom-left-radius: 3px;
    filter: drop-shadow(0 6px 10px rgba(0,0,0,0.08));
  }

  .cat-bubble.show{
    opacity: 1;
    transform: translateY(0) scale(1);
    animation: bubblePop .35s ease-out;
  }

  @keyframes bubblePop{
    0%   { transform: translateY(10px) scale(0.92); }
    60%  { transform: translateY(-2px) scale(1.04); }
    100% { transform: translateY(0) scale(1); }
  }

  body.dot-mode .cat-bubble{
    color: rgba(55,40,22,0.92);
    background: linear-gradient(180deg, rgba(243,234,215,0.98), rgba(238,226,200,0.94));
    border-color: rgba(55,40,22,0.18);
    box-shadow: 0 16px 36px rgba(45, 35, 20, 0.14);
  }
  body.dot-mode .cat-bubble::after{
    border-left-color: rgba(55,40,22,0.18);
    border-bottom-color: rgba(55,40,22,0.18);
  }
</style>

<div class="dotmode-badge">VINTAGE DOT</div>

<div class="cat-walker" id="catWalker" aria-label="ORDLIKE Cat" title="Click me!">
  <div class="cat-sprite">
    <img src="/assets/new_images/esteregg/ordlike_cat.png" alt="ORDLIKE Cat">
  </div>
  <div class="cat-bubble" id="catBubble" aria-hidden="true">냐옹!</div>
</div>

<script>
/* =========================================================
   Easter Egg Trigger
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
   CAT Behavior (PC / Mobile different scale rules)
   ✅ PC/모바일 자동 분기 + 창 리사이즈 시 실시간 반영
   ✅ 클릭/터치 시 조금씩 커짐
   ✅ 10초마다 조금씩 원래 크기로 복귀
   ========================================================= */
(function(){
  const cat = document.getElementById("catWalker");
  const bubble = document.getElementById("catBubble");
  if(!cat || !bubble) return;

  const EDGE_PAD = 24;

  // ===============================
  // Breakpoints
  // ===============================
  const MOBILE_BREAKPOINT = 900; // px

  function getVP(){
    const vv = window.visualViewport;
    const width  = vv ? vv.width  : window.innerWidth;
    const height = vv ? vv.height : window.innerHeight;
    return { width, height };
  }
  function isMobileNow(){
    return getVP().width <= MOBILE_BREAKPOINT;
  }

  // ===============================
  // EXTRA_Y (Responsive + Live)
  // ===============================
  const EXTRA_Y_PC = 700;
  const EXTRA_Y_MOBILE_ADD = 300;
  let extraY = EXTRA_Y_PC;

  function recomputeExtraY(){
    extraY = isMobileNow() ? (EXTRA_Y_PC + EXTRA_Y_MOBILE_ADD) : EXTRA_Y_PC;
  }

  // ===============================
  // SCALE PROFILES (핵심: 모바일/PC 다르게)
  // ===============================
  const SCALE_PROFILE_PC = {
    base: 1.00,   // PC 시작 크기
    max: 5.2,    // ✅ PC 최대치 (원하면 여기만 바꾸면 됨)
    step: 0.2    // 클릭 1번당 증가량
  };

  const SCALE_PROFILE_MOBILE = {
    base: 0.75,   // ✅ 모바일 시작 크기 더 작게
    max: 1.7,    // ✅ 모바일 최대치 더 작게
    step: 0.05    // 모바일 클릭 증가량도 더 작게
  };

  // 현재 적용중 프로필
  let scaleBase = SCALE_PROFILE_PC.base;
  let scaleMax  = SCALE_PROFILE_PC.max;
  let scaleStep = SCALE_PROFILE_PC.step;

  // 실제 스케일 값
  let catScale = scaleBase;

  function applyScaleProfile(forceClampNow){
    const mobile = isMobileNow();
    const p = mobile ? SCALE_PROFILE_MOBILE : SCALE_PROFILE_PC;

    const prevBase = scaleBase;
    scaleBase = p.base;
    scaleMax  = p.max;
    scaleStep = p.step;

    // 켜진 상태에서 리사이즈로 프로필이 바뀌면:
    // - base는 "원래 크기(복귀 목표)"라 바뀌는 게 정상
    // - 현재 catScale이 새 max를 넘으면 즉시 깎아줌
    // - 원하면 base 변화에 비율로 따라가게도 가능하지만, 여기선 안정적으로 clamp만
    if(forceClampNow){
      catScale = Math.min(catScale, scaleMax);
      catScale = Math.max(catScale, scaleBase);
      clampWithVP(x, y);
      setCSSVars();
    }else{
      // 처음 enable 시에는 base로 맞춰 시작
      catScale = scaleBase;
    }

    // base가 바뀌면 decay의 목표도 자동으로 바뀜
    // (SCALE_BASE를 별도 상수로 두지 않고 scaleBase 사용)
    if(Math.abs(prevBase - scaleBase) > 1e-6){
      // nothing else needed
    }
  }

  // ===============================
  // Scale Decay (10초마다 조금씩 "scaleBase"로)
  // ===============================
  const SCALE_DECAY_INTERVAL_MS = 20; // ✅ 10초마다
  const SCALE_DECAY_STEP = 0.005;         // ✅ 한 번에 줄어드는 양
  let scaleDecayTimer = null;

  function startScaleDecay(){
    stopScaleDecay();
    scaleDecayTimer = setInterval(()=>{
      if(!enabled) return;

      // 이미 목표(base)에 도달했으면 유지
      if(catScale <= scaleBase + 1e-6){
        catScale = scaleBase;
        return;
      }

      // 조금씩 감소
      catScale = Math.max(scaleBase, catScale - SCALE_DECAY_STEP);

      clampWithVP(x, y);
      setCSSVars();
    }, SCALE_DECAY_INTERVAL_MS);
  }

  function stopScaleDecay(){
    if(scaleDecayTimer){
      clearInterval(scaleDecayTimer);
      scaleDecayTimer = null;
    }
  }

  // ===============================
  // Motion tuning
  // ===============================
  const BASE_SPEED = 2.15;
  const FOLLOW_BOOST = 1.10;
  const MAX_SPEED  = 5.0;
  const TURN_RATE  = 0.055;
  const BRAKE_LERP = 0.06;

  const NEAR_DIST   = 150;
  const FOLLOW_DIST = 380;

  const TARGET_REPICK_MS = 2400;
  const ARRIVE_DIST = 34;
  const ARRIVE_GRACE_MS = 500;

  const SIT_ENABLE = true;
  const SIT_MS = 420;
  const SIT_COOLDOWN_MS = 6500;
  const SIT_CHANCE = 0.10;
  const SIT_MIN_MOVE_MS = 2200;

  const BUBBLE_SHOW_MS = 950;

  let enabled = false;

  let x = 40;
  let y = window.innerHeight * 0.55;

  let vx = 0, vy = 0;
  let tx = 1, ty = 0;

  let targetX = x, targetY = y;
  let lastTargetPick = 0;
  let lastArriveTime = 0;

  let mouseX = window.innerWidth * 0.5;
  let mouseY = window.innerHeight * 0.5;

  let sitUntil = 0;
  let lastSit = 0;
  let lastMovedAt = Date.now();

  function rand(min, max){ return Math.random() * (max - min) + min; }
  function clamp(v, a, b){ return Math.max(a, Math.min(b, v)); }

  function getCatSize(){
    const r = cat.getBoundingClientRect();
    return { w: r.width, h: r.height };
  }

  function clampWithVP(px, py){
    const vp = getVP();
    const cs = getCatSize();

    const maxX = vp.width  - EDGE_PAD - cs.w;
    const maxY = (vp.height + extraY) - EDGE_PAD - cs.h;

    x = clamp(px, EDGE_PAD, Math.max(EDGE_PAD, maxX));
    y = clamp(py, EDGE_PAD, Math.max(EDGE_PAD, maxY));
  }

  function pickRandomTarget(){
    const vp = getVP();
    targetX = rand(EDGE_PAD, Math.max(EDGE_PAD, vp.width  - EDGE_PAD));
    targetY = rand(EDGE_PAD, Math.max(EDGE_PAD, (vp.height + extraY) - EDGE_PAD));
    lastTargetPick = Date.now();
  }

  function setCSSVars(){
    cat.style.setProperty("--x", x + "px");
    cat.style.setProperty("--y", y + "px");
    cat.style.setProperty("--sx", (vx >= 0 ? 1 : -1));
    cat.style.setProperty("--cat-scale", catScale.toFixed(3));
  }

  function showMeow(text){
    bubble.textContent = text || "냐옹~ 🐾";
    bubble.classList.add("show");
    clearTimeout(showMeow.__t);
    showMeow.__t = setTimeout(()=> bubble.classList.remove("show"), BUBBLE_SHOW_MS);
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

  window.__ORDLIKE_CAT_ENABLE = function(on){
    enabled = !!on;
    if(enabled){
      recomputeExtraY();
      applyScaleProfile(false);   // ✅ enable 시 모바일/PC에 맞는 base로 시작
      pickRandomTarget();
      clampWithVP(x, y);
      setCSSVars();
      cat.classList.add("is-moving");
      startScaleDecay();
      requestAnimationFrame(step);
    }else{
      cat.classList.remove("is-moving", "is-sitting");
      bubble.classList.remove("show");
      stopScaleDecay();
    }
  };

  window.addEventListener("mousemove", (e)=>{ mouseX = e.clientX; mouseY = e.clientY; }, {passive:true});
  window.addEventListener("touchstart", (e)=>{ if(e.touches?.[0]){ mouseX=e.touches[0].clientX; mouseY=e.touches[0].clientY; }}, {passive:true});
  window.addEventListener("touchmove",  (e)=>{ if(e.touches?.[0]){ mouseX=e.touches[0].clientX; mouseY=e.touches[0].clientY; }}, {passive:true});

  cat.addEventListener("click", (e)=>{
    e.stopPropagation();

    // ✅ 클릭마다 증가 (모바일/PC 각기 다른 step/max 적용)
    catScale = Math.min(scaleMax, catScale + scaleStep);

    clampWithVP(x, y);
    setCSSVars();

    const msgs = ["냐옹! 🐾", "두둥..두둥..", "meow! ✨", "ORDLIKE! 💙", "냥냥~ 😺", "커진다냥! 😆"];
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
    const vp = getVP();

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

    if(SIT_ENABLE){
      const canSit = (now - lastSit > SIT_COOLDOWN_MS) && (now - lastMovedAt > SIT_MIN_MOVE_MS);
      if(canSit && isInsideAnyNavCard(cx, cy) && Math.random() < SIT_CHANCE){
        sitUntil = now + SIT_MS;
        lastSit = now;
        requestAnimationFrame(step);
        return;
      }
    }

    if(now - lastTargetPick > TARGET_REPICK_MS){
      pickRandomTarget();
    }

    const mdx = cx - mouseX;
    const mdy = cy - mouseY;
    const mdist = Math.hypot(mdx, mdy);

    let desiredX = targetX;
    let desiredY = targetY;
    let desiredSpeed = BASE_SPEED;

    if(mdist < NEAR_DIST){
      const ux = mdx / (mdist || 1);
      const uy = mdy / (mdist || 1);
      desiredX = clamp(cx + ux * 280, EDGE_PAD, vp.width  - EDGE_PAD);
      desiredY = clamp(cy + uy * 280, EDGE_PAD, (vp.height + extraY) - EDGE_PAD);
      desiredSpeed = MAX_SPEED;
      lastTargetPick = now - (TARGET_REPICK_MS - 900);
    }else if(mdist > FOLLOW_DIST){
      desiredX = targetX * 0.55 + mouseX * 0.45;
      desiredY = targetY * 0.55 + mouseY * 0.45;
      desiredSpeed = BASE_SPEED * FOLLOW_BOOST;
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

    tx = tx + (ndx - tx) * TURN_RATE;
    ty = ty + (ndy - ty) * TURN_RATE;

    const dvx = tx * desiredSpeed;
    const dvy = ty * desiredSpeed;

    vx = vx + (dvx - vx) * (BRAKE_LERP + 0.02);
    vy = vy + (dvy - vy) * (BRAKE_LERP + 0.02);

    x += vx;
    y += vy;

    clampWithVP(x, y);

    if(Math.abs(vx) + Math.abs(vy) > 0.35) lastMovedAt = now;

    setCSSVars();
    requestAnimationFrame(step);
  }

  function onViewportChange(){
    if(!enabled) return;

    recomputeExtraY();

    // ✅ 리사이즈(PC↔모바일 전환 포함) 시 스케일 프로필 즉시 반영
    applyScaleProfile(true);

    clampWithVP(x, y);
    pickRandomTarget();
    setCSSVars();
  }

  window.addEventListener("resize", onViewportChange, {passive:true});
  if(window.visualViewport){
    window.visualViewport.addEventListener("resize", onViewportChange, {passive:true});
    window.visualViewport.addEventListener("scroll", ()=> {
      if(!enabled) return;
      recomputeExtraY();
      clampWithVP(x, y);
      setCSSVars();
    }, {passive:true});
  }

  // (페이지 로드 직후에도 프로필 미리 계산해두기)
  recomputeExtraY();
  applyScaleProfile(false);
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
