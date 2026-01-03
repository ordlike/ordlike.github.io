---
layout: single
permalink: /contact/
author_profile: true
sidebar_main: false
---

<style>
  /* ===== 테마 전체 폭 확장 및 배경 설정 ===== */
  :root {
    --bg-main: #f9fbfe;
    --card-bg: #ffffff;
    --accent-blue: #0E4A84;
    --dark-blue: rgb(15, 15, 112);
    --text-muted: #64748b;
    --border: #e2e8f0;

    /* ✅ 메뉴바 높이 (JS가 자동 업데이트) */
    --masthead-h: 80px;
  }

  /* ✅ 메뉴바는 항상 위에 */
  .masthead, .masthead__inner-wrap, .greedy-nav { z-index: 50000 !important; }

  /* 테마 자체의 너비 제한을 풀어서 카드가 더 넓어질 수 있게 합니다 */
  #main {
    max-width: 1880px !important; /* 전체 컨테이너 확장 */
  }

  .page__content { 
    background-color: var(--bg-main) !important; 
    padding: 40px 20px !important; /* 위아래 여백 축소 */
  }

  /* 카드 디자인 */
  .contact-card {
    max-width: 100%;
    margin: 0 auto;
    background: var(--card-bg);
    border-radius: 24px;
    padding: 40px 50px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
    border: 1px solid rgba(226, 232, 240, 0.8);
  }

  .contact-header {
    text-align: center;
    margin-bottom: 30px;
  }

  .contact-header h1 {
    font-size: 2.2rem;
    font-weight: 850;
    color: var(--dark-blue);
    margin-bottom: 8px;
  }

  .contact-header p {
    margin: 0;
    color: var(--text-muted);
    font-weight: 600;
  }

  /* 폼 요소 간격 */
  #contact-form {
    display: flex;
    flex-direction: column;
    gap: 18px;
  }

  .form-row {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
  }

  .form-group {
    display: flex;
    flex-direction: column;
    gap: 6px;
  }

  .form-group label {
    font-weight: 700;
    font-size: 0.85rem;
    color: var(--dark-blue);
  }

  .form-group input, 
  .form-group textarea {
    padding: 12px 18px;
    border-radius: 10px;
    border: 1px solid var(--border);
    background-color: #f8fafc;
    font-size: 0.9rem;
    width: 100%;
    box-sizing: border-box;
    outline: none;
    transition: border-color .2s ease, box-shadow .2s ease;
  }

  .form-group input:focus,
  .form-group textarea:focus {
    border-color: rgba(14, 74, 132, 0.35);
    box-shadow: 0 0 0 4px rgba(14, 74, 132, 0.10);
  }

  .form-group textarea {
    min-height: 140px; 
    resize: vertical;
  }

  .submit-btn {
    align-self: center;
    width: 200px;
    padding: 14px;
    border-radius: 10px;
    border: none;
    background-color: var(--accent-blue);
    color: white;
    font-weight: 800;
    cursor: pointer;
    transition: all 0.3s ease;
    margin-top: 10px;
  }

  .submit-btn:hover {
    background-color: var(--dark-blue);
    transform: translateY(-2px);
  }

  .submit-btn:disabled {
    opacity: 0.7;
    cursor: not-allowed;
    transform: none;
  }

  @media (max-width: 800px) {
    .form-row { grid-template-columns: 1fr; }
    .contact-card { padding: 30px 20px; }
  }

  /* ================= Contact Result Modal (✅ 메뉴바 미침범 버전) ================= */
  .contact-modal-overlay{
    display:none;
    position: fixed;

    /* ✅ 핵심: 메뉴바 높이만큼 아래에서만 덮기 */
    left: 0; right: 0; bottom: 0;
    top: var(--masthead-h);
    height: calc(100vh - var(--masthead-h));

    /* ✅ 메뉴바보다 낮게 */
    z-index: 20000;

    background: rgba(3, 10, 18, 0.62);
    backdrop-filter: blur(10px);
    -webkit-backdrop-filter: blur(10px);
    align-items: center;
    justify-content: center;
    padding: 18px;
  }

  .contact-modal{
    width: min(560px, 92vw);
    background: rgba(255,255,255,0.92);
    border-radius: 24px;
    border: 1px solid rgba(226, 232, 240, 0.85);
    box-shadow: 0 24px 70px rgba(0,0,0,0.22);
    overflow: hidden;
    animation: contactPop .18s ease-out forwards;
  }

  @keyframes contactPop{
    from { opacity: 0; transform: translateY(12px) scale(0.99); }
    to   { opacity: 1; transform: translateY(0) scale(1); }
  }

  .contact-modal-top{
    padding: 16px 18px 14px 18px;
    background: linear-gradient(135deg, rgba(14,74,132,0.95), rgba(15,15,112,0.95));
    color: #fff;
    display:flex;
    justify-content: space-between;
    align-items: center;
    gap: 10px;
  }

  .contact-modal-title{
    font-weight: 850;
    letter-spacing: -0.02em;
    font-size: 1.05rem;
    margin: 0;
  }

  .contact-modal-close{
    width: 38px;
    height: 38px;
    border-radius: 12px;
    border: 1px solid rgba(255,255,255,0.22);
    background: rgba(255,255,255,0.12);
    color:#fff;
    font-size: 20px;
    cursor: pointer;
    display:grid;
    place-items:center;
    transition: transform .15s ease, background .2s ease;
  }
  .contact-modal-close:hover{
    transform: rotate(90deg);
    background: rgba(255,255,255,0.18);
  }

  .contact-modal-body{
    padding: 18px;
    color: rgba(31,42,55,0.88);
    line-height: 1.65;
    font-weight: 600;
  }

  .contact-modal-actions{
    padding: 0 18px 18px 18px;
    display:flex;
    gap: 10px;
    justify-content: flex-end;
  }

  .contact-modal-btn{
    border: 1px solid rgba(14,74,132,0.20);
    background: rgba(14,74,132,0.06);
    color: rgb(15, 15, 112);
    font-weight: 900;
    border-radius: 12px;
    padding: 10px 14px;
    cursor:pointer;
    transition: transform .15s ease, background .2s ease;
    min-width: 140px;
  }
  .contact-modal-btn:hover{
    transform: translateY(-1px);
    background: rgba(14,74,132,0.10);
  }
</style>

<div class="contact-card">
  <div class="contact-header">
    <h1>Direct Message</h1>
    <p>Please feel free to reach out if you have any questions.</p>
  </div>

  <form id="contact-form">
    <input type="hidden" name="contact_number">

    <div class="form-row">
      <div class="form-group">
        <label>Your Name</label>
        <input type="text" name="name" placeholder="Enter your name">
      </div>
      <div class="form-group">
        <label>Your Email address</label>
        <input type="email" name="email" placeholder="email@example.com">
      </div>
    </div>

    <div class="form-group">
      <label>Message Title</label>
      <input type="text" name="title" placeholder="What is this about?">
    </div>

    <div class="form-group">
      <label>Message</label>
      <textarea name="message" placeholder="Type your message here..."></textarea>
    </div>

    <input type="submit" class="submit-btn" value="Send Message">
  </form>
</div>

<!-- ================= Contact Result Modal ================= -->
<div class="contact-modal-overlay" id="contactModalOverlay" onclick="closeContactModal(false)">
  <div class="contact-modal" onclick="event.stopPropagation()">
    <div class="contact-modal-top">
      <h3 class="contact-modal-title" id="contactModalTitle">Notice</h3>
      <button class="contact-modal-close" type="button" onclick="closeContactModal(false)">&times;</button>
    </div>
    <div class="contact-modal-body" id="contactModalBody">
      Message
    </div>
    <div class="contact-modal-actions">
      <button class="contact-modal-btn" type="button" onclick="closeContactModal(true)">OK</button>
    </div>
  </div>
</div>

<script type="text/javascript" src="https://cdn.jsdelivr.net/npm/emailjs-com@3/dist/email.min.js"></script>

<script type="text/javascript">
  (function() { emailjs.init('6NrA1NVH-yQj6Nas4'); })();

  /* ✅ 메뉴바 높이 자동 측정 → 모달이 메뉴바 아래에서만 뜨게 */
  function setMastheadHeight() {
    const masthead =
      document.querySelector('.masthead') ||
      document.querySelector('.site-header') ||
      document.querySelector('header');

    if (!masthead) return;
    const h = Math.ceil(masthead.getBoundingClientRect().height);
    if (h > 0) document.documentElement.style.setProperty('--masthead-h', h + 'px');
  }
  window.addEventListener('load', setMastheadHeight);
  window.addEventListener('resize', setMastheadHeight);

  /* ===== Modal Helpers ===== */
  let _reloadOnClose = false;

  function showContactModal(title, message, reloadOnClose){
    setMastheadHeight(); // ✅ 열기 직전에 한 번 더
    const overlay = document.getElementById('contactModalOverlay');
    const t = document.getElementById('contactModalTitle');
    const b = document.getElementById('contactModalBody');

    t.textContent = title || 'Notice';
    b.textContent = message || '';
    _reloadOnClose = !!reloadOnClose;

    overlay.style.display = 'flex';
    document.body.style.overflow = 'hidden';
  }

  function closeContactModal(okClicked){
    const overlay = document.getElementById('contactModalOverlay');
    overlay.style.display = 'none';
    document.body.style.overflow = 'auto';

    if (_reloadOnClose) location.reload();
  }

  window.onload = function() {
    const form = document.getElementById('contact-form');
    const btn = document.querySelector('.submit-btn');

    form.addEventListener('submit', function(event) {
      event.preventDefault();
      this.contact_number.value = (Math.random() * 100000) | 0;

      if (!this.title.value || !this.email.value || !this.message.value) {
        showContactModal(
          'Missing Required Fields',
          'Please fill in Title, Email, and Message before sending.',
          false
        );
        return;
      }

      btn.value = 'Sending...';
      btn.disabled = true;

      emailjs.sendForm('service_ybo0xbb', 'template_fz0bb1f', this)
        .then(function() {
          showContactModal(
            'Message Sent',
            'Thank you for reaching out. I will get back to you as soon as possible.',
            true
          );
        }, function(error) {
          showContactModal(
            'Failed to Send',
            'Something went wrong. Please try again later.',
            false
          );
          btn.value = 'Send Message';
          btn.disabled = false;
        });
    });

    /* ESC 키로 모달 닫기 */
    document.addEventListener('keydown', (e) => {
      const overlay = document.getElementById('contactModalOverlay');
      if (e.key === 'Escape' && overlay.style.display === 'flex') {
        closeContactModal(false);
      }
    });
  }
</script>
