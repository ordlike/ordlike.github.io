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
  }

  /* 테마 자체의 너비 제한을 풀어서 카드가 더 넓어질 수 있게 합니다 */
  #main {
    max-width: 1880px !important; /* 전체 컨테이너 확장 */
  }

  .page__content { 
    background-color: var(--bg-main) !important; 
    padding: 40px 20px !important; /* 위아래 여백 축소 */
  }

  /* [수정] 카드 디자인: 너비를 늘리고 높이감은 줄임 */
  .contact-card {
    max-width: 100%; /* 본문 영역을 꽉 채우도록 설정 */
    margin: 0 auto;
    background: var(--card-bg);
    border-radius: 24px;
    padding: 40px 50px; /* 위아래 패딩 축소 */
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
    border: 1px solid rgba(226, 232, 240, 0.8);
  }

  .contact-header {
    text-align: center;
    margin-bottom: 30px; /* 제목 아래 여백 축소 */
  }

  .contact-header h1 {
    font-size: 2.2rem;
    font-weight: 850;
    color: var(--dark-blue);
    margin-bottom: 8px;
  }

  /* 폼 요소 간격 조절 */
  #contact-form {
    display: flex;
    flex-direction: column;
    gap: 18px; /* 항목 간 간격 좁힘 */
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
    padding: 12px 18px; /* 입력창 높이 축소 */
    border-radius: 10px;
    border: 1px solid var(--border);
    background-color: #f8fafc;
    font-size: 0.9rem;
    width: 100%;
    box-sizing: border-box;
  }

  /* [수정] 메시지 박스 높이 축소 (너무 길지 않게) */
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

  @media (max-width: 800px) {
    .form-row { grid-template-columns: 1fr; }
    .contact-card { padding: 30px 20px; }
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

<script type="text/javascript" src="https://cdn.jsdelivr.net/npm/emailjs-com@3/dist/email.min.js"></script>
<script type="text/javascript">
  (function() { emailjs.init('6NrA1NVH-yQj6Nas4'); })();

  window.onload = function() {
    document.getElementById('contact-form').addEventListener('submit', function(event) {
      event.preventDefault();
      this.contact_number.value = Math.random() * 100000 | 0;

      if (!this.title.value || !this.email.value || !this.message.value) {
        window.alert('Please fill in all required fields.');
        return;
      }

      const btn = document.querySelector('.submit-btn');
      btn.value = 'Sending...';
      btn.disabled = true;

      emailjs.sendForm('service_ybo0xbb', 'template_fz0bb1f', this)
        .then(function() {
          window.alert('Message sent successfully!');
          location.reload(); 
        }, function(error) {
          window.alert('Failed to send message.');
          btn.value = 'Send Message';
          btn.disabled = false;
        });
    });
  }
</script>