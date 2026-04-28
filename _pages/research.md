---
layout: splash
permalink: /research/
author_profile: true
sidebar_main: false
---

<style>
  :root {
    --primary: #0E4A84;
    --primary2: rgb(15, 15, 112);
    --dark: #0b233d;

    --bg: #ffffff;
    --soft: #f7f8fb;
    --line: rgba(0,0,0,0.08);

    --txt: #1f2a37;
    --muted: rgba(31,42,55,0.70);

    --shadow: 0 14px 46px rgba(7, 29, 51, 0.10);
    --shadow2: 0 18px 56px rgba(14, 74, 132, 0.14);

    --r-lg: 22px;
    --r: 16px;
  }

  *, *::before, *::after { box-sizing: border-box; }

  .section-container{
    max-width: 1200px;
    margin: 46px auto;
    padding: 0 18px;
    font-family: 'Pretendard', 'Segoe UI', Roboto, sans-serif;
    color: var(--txt);
  }

  .section-title{
    display: inline-flex;
    align-items: center;
    gap: 10px;
    color: rgb(15, 15, 112);
    font-size: 1.85rem;
    font-weight: 700;
    letter-spacing: -0.02em;
    margin: 0 0 20px 0;
    padding: 6px 0;
    position: relative;
    border-bottom: none !important;
    box-shadow: none !important;
    background: none !important;
    background-image: none !important;
  }

  .section-title::before{
    content:"";
    width: 12px;
    height: 12px;
    border-radius: 4px;
    background: linear-gradient(135deg, var(--primary), var(--primary2));
    box-shadow: 0 10px 20px rgba(14,74,132,0.18);
  }

  .section-title::after{
    content:"";
    position:absolute;
    left:0;
    bottom:-8px;
    width: 100%;
    height: 3px;
    border-radius: 999px;
    background: linear-gradient(90deg, var(--primary), rgba(14,74,132,0.12));
  }

  h2.section-title *{
    border-bottom: none !important;
    background-image: none !important;
  }

  .uni-header{
    background: linear-gradient(135deg, var(--primary), var(--primary2));
    color: #fff;
    padding: 14px 18px;
    border-radius: var(--r);
    margin: 26px 0 16px 0;
    box-shadow: 0 14px 34px rgba(14,74,132,0.14);
    position: relative;
    overflow: hidden;
  }

  .uni-header::after{
    content:"";
    position:absolute;
    right:-70px;
    top:-70px;
    width: 180px;
    height: 180px;
    background: radial-gradient(circle, rgba(255,255,255,0.18), rgba(255,255,255,0));
    transform: rotate(25deg);
  }

  .uni-header h1{
    margin: 0;
    font-size: 1.05rem;
    font-weight: 800;
    letter-spacing: 0.06em;
    text-transform: uppercase;
  }

  /* ================= Publications ================= */
  .pub-block{
    background: #fff;
    border: 1px solid var(--line);
    border-radius: var(--r-lg);
    box-shadow: 0 12px 30px rgba(0,0,0,0.055);
    padding: 20px;
    margin-bottom: 22px;
  }

  .pub-subtitle{
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap: 12px;
    margin: 0 0 14px 0;
    padding-bottom: 12px;
    border-bottom: 1px solid rgba(0,0,0,0.07);
  }

  .pub-subtitle h3{
    margin: 0;
    font-size: 1.05rem;
    font-weight: 850;
    color: rgb(15, 15, 112);
    letter-spacing: -0.02em;
  }

  .pub-count{
    font-size: 0.78rem;
    font-weight: 800;
    color: var(--primary);
    background: rgba(14,74,132,0.08);
    border: 1px solid rgba(14,74,132,0.14);
    padding: 5px 10px;
    border-radius: 999px;
    white-space: nowrap;
  }

  .pub-list{
    list-style: none;
    padding: 0;
    margin: 0;
    display: grid;
    gap: 10px;
  }

  .pub-item{
    display: grid;
    grid-template-columns: 86px 1fr;
    gap: 14px;
    padding: 13px 14px;
    border: 1px solid rgba(0,0,0,0.065);
    border-radius: 14px;
    background: linear-gradient(180deg, #ffffff, #fbfcfe);
    transition: transform .2s ease, border-color .2s ease, box-shadow .2s ease;
  }

  .pub-item:hover{
    transform: translateY(-2px);
    border-color: rgba(14,74,132,0.22);
    box-shadow: 0 10px 24px rgba(14,74,132,0.08);
  }

  .pub-year{
    display:flex;
    align-items:center;
    justify-content:center;
    height: 34px;
    border-radius: 999px;
    background: linear-gradient(135deg, var(--primary), var(--primary2));
    color:#fff;
    font-size: 0.82rem;
    font-weight: 850;
    letter-spacing: 0.02em;
  }

  .pub-content{
    min-width: 0;
  }

  .pub-authors{
    color: var(--muted);
    font-size: 0.86rem;
    display:block;
    margin-bottom: 4px;
    font-weight: 600;
    line-height: 1.35;
  }

  .pub-title{
    font-weight: 750;
    font-size: 0.93rem;
    line-height: 1.38;
    color: #162231;
    margin-bottom: 6px;
  }

  .pub-title a{
    color: inherit;
    text-decoration: none;
    background-image: linear-gradient(transparent 78%, rgba(14,74,132,0.16) 0);
    background-size: 100% 100%;
    background-repeat: no-repeat;
    transition: color .2s ease;
  }

  .pub-title a:hover{
    color: var(--primary);
  }

  .pub-meta{
    display:flex;
    align-items:center;
    gap: 8px;
    flex-wrap: wrap;
    font-size: 0.82rem;
    font-weight: 750;
    color: var(--primary);
  }

  .pub-venue{
    color: var(--primary);
  }

  .type-tag{
    font-size: 0.72rem;
    font-weight: 800;
    padding: 4px 9px;
    border-radius: 999px;
    background: rgba(14,74,132,0.08);
    border: 1px solid rgba(14,74,132,0.16);
    color: var(--primary);
    line-height: 1.2;
  }

  .status-tag{
    font-size: 0.72rem;
    font-weight: 800;
    padding: 4px 9px;
    border-radius: 999px;
    background: rgba(15,15,112,0.06);
    border: 1px solid rgba(15,15,112,0.14);
    color: rgb(15, 15, 112);
    line-height: 1.2;
  }

  .pub-actions{
    margin-top: 8px;
    display:flex;
    gap: 8px;
    flex-wrap: wrap;
  }

  .pill-btn{
    display:inline-flex;
    align-items:center;
    gap: 6px;
    padding: 6px 10px;
    border-radius: 999px;
    font-size: 0.78rem;
    font-weight: 800;
    text-decoration: none;
    border: 1px solid rgba(14,74,132,0.18);
    color: var(--primary);
    background: rgba(255,255,255,0.92);
    transition: transform .2s ease, background .2s ease;
  }

  .pill-btn:hover{
    transform: translateY(-1px);
    background: rgba(14,74,132,0.05);
  }

  /* ================= Research Hero ================= */
  .research-hero{
    width: 100%;
    display:grid;
    grid-template-columns: 1.1fr 0.9fr;
    gap: 18px;
    background: radial-gradient(1200px 500px at 10% 0%, rgba(14,74,132,0.09), transparent 60%),
                radial-gradient(800px 400px at 90% 20%, rgba(15,15,112,0.07), transparent 55%),
                linear-gradient(180deg, var(--soft), #fff);
    border: 1px solid rgba(0,0,0,0.06);
    padding: 24px;
    border-radius: var(--r-lg);
    box-shadow: var(--shadow);
    overflow: hidden;
    position: relative;
  }

  .research-hero::after{
    content:"";
    position:absolute;
    inset:auto -120px -160px auto;
    width: 420px;
    height: 420px;
    background: radial-gradient(circle, rgba(14,74,132,0.14), rgba(14,74,132,0));
    transform: rotate(20deg);
    pointer-events:none;
  }

  .research-hero-text h2{
    margin: 0 0 10px 0;
    font-size: 1.4rem;
    font-weight: 700;
    letter-spacing: -0.03em;
    color: rgb(15, 15, 112);
  }

  .research-hero-text p{
    margin: 0 0 12px 0;
    line-height: 1.75;
    color: rgba(31,42,55,0.86);
    font-weight: 500;
  }

  .research-hero-text b{
    font-weight: 700;
    color: rgba(20,36,58,0.92);
  }

  .keyword-row{
    display:flex;
    flex-wrap:wrap;
    gap: 8px;
    margin-top: 12px;
  }

  .keyword-chip{
    font-size: 0.78rem;
    font-weight: 700;
    color: #fff;
    background: linear-gradient(135deg, var(--primary), var(--primary2));
    border: 1px solid rgba(255,255,255,0.16);
    padding: 7px 11px;
    border-radius: 999px;
    box-shadow: 0 10px 22px rgba(14,74,132,0.14);
  }

  .hero-cta{
    display:flex;
    gap: 10px;
    flex-wrap: wrap;
    margin-top: 16px;
  }

  .btn{
    display:inline-flex;
    align-items:center;
    gap: 8px;
    padding: 10px 14px;
    border-radius: 14px;
    font-size: 0.9rem;
    font-weight: 750;
    text-decoration:none;
    transition: transform .2s ease, box-shadow .2s ease, background .2s ease;
    border: 1px solid transparent;
    cursor: pointer;
  }

  .btn.primary{
    background: linear-gradient(135deg, var(--primary), var(--primary2));
    color:#fff;
    box-shadow: 0 12px 28px rgba(14,74,132,0.18);
  }

  .btn.primary:hover{
    transform: translateY(-2px);
    box-shadow: 0 16px 36px rgba(14,74,132,0.22);
  }

  .btn.ghost{
    background: rgba(255,255,255,0.86);
    color: var(--primary);
    border-color: rgba(14,74,132,0.18);
  }

  .btn.ghost:hover{
    transform: translateY(-2px);
    background: rgba(14,74,132,0.05);
  }

  .research-hero-media{
    position: relative;
    border-radius: var(--r-lg);
    overflow:hidden;
    cursor:pointer;
    border: 1px solid rgba(0,0,0,0.08);
    box-shadow: 0 14px 34px rgba(0,0,0,0.10);
    min-height: 280px;
    width: 100%;
  }

  .research-hero-media img{
    width:100%;
    height:100%;
    object-fit: cover;
    display:block;
    transition: transform .35s ease;
  }

  .research-hero-media:hover img{ transform: scale(1.035); }

  /* ================= Projects Grid ================= */
  .custom-grid{
    display:grid;
    grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
    gap: 18px;
    margin-top: 18px;
    align-items: stretch;
  }

  .custom-card{
    background: #fff;
    border-radius: var(--r-lg);
    overflow:hidden;
    border: 1px solid var(--line);
    text-decoration: none;
    color: inherit;

    width: 100%;
    justify-self: stretch;
    align-self: stretch;

    display:flex;
    flex-direction: column;

    box-shadow: 0 12px 26px rgba(0,0,0,0.06);
    transition: transform .25s ease, box-shadow .25s ease, border-color .25s ease;
    position: relative;
    cursor: pointer;
  }

  .custom-card:hover{
    transform: translateY(-5px);
    box-shadow: var(--shadow2);
    border-color: rgba(14,74,132,0.28);
  }

  .card-img-wrap{
    width:100%;
    height: 220px;
    position: relative;
    overflow:hidden;
    flex: 0 0 auto;
  }

  .card-img-wrap img{
    width:100%;
    height:100%;
    object-fit: cover;
    display:block;
    transition: transform .35s ease;
  }

  .custom-card:hover .card-img-wrap img{ transform: scale(1.035); }

  .card-img-wrap::after{
    content:"";
    position:absolute;
    inset:0;
    background: linear-gradient(180deg, rgba(0,0,0,0) 44%, rgba(0,0,0,0.30) 100%);
    pointer-events:none;
    opacity: 0.92;
  }

  .card-corner{
    position:absolute;
    top: 14px;
    left: 14px;
    padding: 8px 10px;
    border-radius: 999px;
    color:#fff;
    font-size: 0.78rem;
    font-weight: 700;
    background: rgba(0,0,0,0.52);
    backdrop-filter: blur(6px);
    border: 1px solid rgba(255,255,255,0.16);
    z-index: 2;
  }

  .card-hint{
    position:absolute;
    right: 14px;
    top: 14px;
    padding: 8px 10px;
    border-radius: 999px;
    color:#fff;
    font-size: 0.78rem;
    font-weight: 700;
    background: linear-gradient(135deg, rgba(14,74,132,0.90), rgba(15,15,112,0.90));
    box-shadow: 0 10px 22px rgba(14,74,132,0.16);
    z-index: 2;
  }

  .card-content{
    padding: 18px;
    flex: 1 1 auto;
  }

  .card-tag{
    font-size: 0.72rem;
    font-weight: 750;
    text-transform: uppercase;
    letter-spacing: .06em;
    color: var(--primary);
    margin-bottom: 8px;
    display:block;
  }

  .card-title{
    font-size: 1.10rem;
    font-weight: 750;
    margin: 0 0 10px 0;
    line-height: 1.25;
    color: #152232;
  }

  .card-desc{
    font-size: 0.93rem;
    color: var(--muted);
    line-height: 1.6;
    margin: 0;
    font-weight: 450;
  }

  .card-footer{
    display:flex;
    justify-content: space-between;
    align-items:center;
    padding: 12px 18px 18px 18px;
    border-top: 1px solid rgba(0,0,0,0.06);
    gap: 10px;
    flex-wrap: wrap;
    flex: 0 0 auto;
  }

  .youtube-label{
    font-size: 0.88rem;
    font-weight: 700;
    color: #e03131;
    display:flex;
    align-items:center;
    gap: 6px;
  }

  /* ================= Lightbox Image Zoom ================= */
  .gallery-container{
    display:none;
    position: fixed;
    z-index: 9999;
    left:0; top:0;
    width:100%; height:100%;
    background: rgba(0,0,0,0.92);
    justify-content:center;
    align-items:center;
    backdrop-filter: blur(7px);
  }

  .gallery-image{
    max-width: 92%;
    max-height: 86%;
    border-radius: 12px;
    box-shadow: 0 0 40px rgba(255,255,255,0.16);
  }

  .close-btn{
    position:absolute;
    top: 22px;
    right: 26px;
    width: 44px;
    height: 44px;
    border-radius: 999px;
    display:flex;
    align-items:center;
    justify-content:center;
    color:#fff;
    font-size: 26px;
    cursor:pointer;
    background: rgba(255,255,255,0.12);
    border: 1px solid rgba(255,255,255,0.16);
    transition: transform .2s ease, background .2s ease;
    user-select:none;
  }

  .close-btn:hover{
    transform: scale(1.05);
    background: rgba(255,255,255,0.18);
  }

  /* ================= Coming Soon Modal ================= */
  .comingsoon-overlay{
    display:none;
    position: fixed;
    inset: 0;
    z-index: 99999;
    background: rgba(3, 10, 18, 0.62);
    backdrop-filter: blur(10px);
    -webkit-backdrop-filter: blur(10px);
    align-items: center;
    justify-content: center;
    padding: 18px;
  }

  .comingsoon-modal{
    width: min(520px, 92vw);
    border-radius: 18px;
    background: rgba(255,255,255,0.92);
    border: 1px solid rgba(0,0,0,0.10);
    box-shadow: 0 24px 70px rgba(0,0,0,0.22);
    overflow: hidden;
    transform: translateY(8px);
    animation: comingPop .18s ease-out forwards;
  }

  @keyframes comingPop{
    from { opacity: 0; transform: translateY(10px) scale(0.99); }
    to   { opacity: 1; transform: translateY(0) scale(1); }
  }

  .comingsoon-top{
    padding: 16px 18px 14px 18px;
    background: linear-gradient(135deg, rgba(14,74,132,0.95), rgba(15,15,112,0.95));
    color: #fff;
    display:flex;
    justify-content: space-between;
    align-items: center;
    gap: 10px;
  }

  .comingsoon-title{
    font-weight: 850;
    letter-spacing: -0.02em;
    font-size: 1.05rem;
    margin: 0;
  }

  .comingsoon-close{
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

  .comingsoon-close:hover{
    transform: rotate(90deg);
    background: rgba(255,255,255,0.18);
  }

  .comingsoon-body{
    padding: 18px;
    color: rgba(31,42,55,0.88);
    line-height: 1.65;
    font-weight: 500;
  }

  .comingsoon-actions{
    padding: 0 18px 18px 18px;
    display:flex;
    gap: 10px;
    justify-content: flex-end;
  }

  .comingsoon-btn{
    border: 1px solid rgba(14,74,132,0.20);
    background: rgba(14,74,132,0.06);
    color: rgb(15, 15, 112);
    font-weight: 800;
    border-radius: 12px;
    padding: 10px 14px;
    cursor:pointer;
    transition: transform .15s ease, background .2s ease;
  }

  .comingsoon-btn:hover{
    transform: translateY(-1px);
    background: rgba(14,74,132,0.10);
  }

  /* ================= Video Modal ================= */
  .video-overlay{
    display:none;
    position: fixed;
    inset: 0;
    z-index: 100000;
    background: rgba(0,0,0,0.88);
    backdrop-filter: blur(10px);
    -webkit-backdrop-filter: blur(10px);
    align-items: center;
    justify-content: center;
    padding: 18px;
  }

  .video-modal{
    width: min(960px, 92vw);
    border-radius: 18px;
    background: rgba(0,0,0,0.35);
    border: 1px solid rgba(255,255,255,0.16);
    box-shadow: 0 24px 70px rgba(0,0,0,0.40);
    overflow: hidden;
    position: relative;
    transform: translateY(8px);
    animation: videoPop .18s ease-out forwards;
  }

  @keyframes videoPop{
    from { opacity: 0; transform: translateY(10px) scale(0.99); }
    to   { opacity: 1; transform: translateY(0) scale(1); }
  }

  .video-modal video{
    width: 100%;
    height: auto;
    display: block;
    background: #000;
  }

  .video-close{
    position:absolute;
    top: 12px;
    right: 14px;
    width: 40px;
    height: 40px;
    border-radius: 12px;
    display:flex;
    align-items:center;
    justify-content:center;
    color:#fff;
    font-size: 26px;
    cursor:pointer;
    background: rgba(255,255,255,0.10);
    border: 1px solid rgba(255,255,255,0.16);
    transition: transform .15s ease, background .2s ease;
    user-select:none;
    z-index: 2;
  }

  .video-close:hover{
    transform: rotate(90deg);
    background: rgba(255,255,255,0.16);
  }

  /* ================= Responsive ================= */
  @media (max-width: 900px){
    .research-hero{
      grid-template-columns: 1fr;
      padding: 18px;
    }

    .section-title{
      font-size: 1.55rem;
    }

    .card-img-wrap{
      height: 210px;
    }

    .custom-grid{
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    }

    .hero-cta{
      flex-wrap: nowrap;
      gap: 8px;
    }

    .hero-cta .btn{
      flex: 1 1 0;
      justify-content: center;
      white-space: nowrap;
      padding: 10px 10px;
      font-size: 0.84rem;
    }
  }

  @media (max-width: 700px){
    .pub-block{
      padding: 16px;
    }

    .pub-item{
      grid-template-columns: 1fr;
      gap: 8px;
      padding: 13px;
    }

    .pub-year{
      width: fit-content;
      padding: 0 12px;
      height: 30px;
      font-size: 0.78rem;
    }

    .pub-subtitle{
      align-items:flex-start;
      flex-direction: column;
      gap: 8px;
    }
  }
</style>

<!-- ========================= Publications ========================= -->
<div class="section-container" id="publications">
  <h2 class="section-title">Publications</h2>

<!-- ================= Journals ================= -->
<div class="pub-block" id="journals">
  <div class="pub-subtitle">
    <h3>Journals</h3>
    <span class="pub-count">Selected journal papers</span>
  </div>

  <ul class="pub-list">

    <li class="pub-item">
      <div class="pub-year">2026</div>
      <div class="pub-content">
        <span class="pub-authors">Sunyeol Bae, Junhyeong Park, Hyung-Jun Noh, Jaybum Kim, Yumin Yun, Chae-Hwan Park, and Soo-Yeon Lee</span>
        <div class="pub-title">
          <a href="https://doi.org/10.1002/jsid.70054" target="_blank" rel="noopener">
            Subthreshold Swing Control in IGZO TFTs Using Floating-Gate Engineering for AMOLED Displays
          </a>
        </div>
        <div class="pub-meta">
          <span class="pub-venue">Journal of the Society for Information Display</span>
          <span class="status-tag">Accepted</span>
        </div>
        <div class="pub-actions">
          <a class="pill-btn" href="https://doi.org/10.1002/jsid.70054" target="_blank" rel="noopener">🔗 Paper</a>
        </div>
      </div>
    </li>

    <li class="pub-item">
      <div class="pub-year">2026</div>
      <div class="pub-content">
        <span class="pub-authors">Yumin Yun, Junhyeong Park, Sunyeol Bae, Chae-Hwan Park, Dong Hyeon Lee, and Soo-Yeon Lee</span>
        <div class="pub-title">
          <a href="https://doi.org/10.1002/aisy.70374" target="_blank" rel="noopener">
            A Neuromorphic Simulation Framework for IGZO Charge-Trap Synaptic Transistors: From Device Modeling to System Simulation
          </a>
        </div>
        <div class="pub-meta">
          <span class="pub-venue">Advanced Intelligent Systems</span>
          <span class="status-tag">Accepted</span>
        </div>
        <div class="pub-actions">
          <a class="pill-btn" href="https://doi.org/10.1002/aisy.70374" target="_blank" rel="noopener">🔗 Paper</a>
        </div>
      </div>
    </li>

  </ul>
</div>

  <!-- ================= Conferences ================= -->
  <div class="pub-block" id="conferences">
    <div class="pub-subtitle">
      <h3>Conferences</h3>
      <span class="pub-count">Conference papers & presentations</span>
    </div>

    <ul class="pub-list">

      <li class="pub-item">
        <div class="pub-year">2026</div>
        <div class="pub-content">
          <span class="pub-authors">Chae-Hwan Park, Seung Yoon Shin, Seong Eun Kim, Min Kang, and Soo-Yeon Lee</span>
          <div class="pub-title">
            <span>A Schmitt-Trigger Comparator-Based Noise-Robust Reconfigurable Leaky Integrate-and-Fire Neuron Circuit for Spiking Neural Networks</span>
          </div>
          <div class="pub-meta">
            <span class="pub-venue">KCS 2026 · Jeongseon, Korea</span>
            <span class="type-tag">Poster</span>
          </div>
        </div>
      </li>

      <li class="pub-item">
        <div class="pub-year">2025</div>
        <div class="pub-content">
          <span class="pub-authors">Chae-Hwan Park, Jaybum Kim, Kyeong-Soo Kang, Hyeon-Gu Kang, and Soo-Yeon Lee</span>
          <div class="pub-title">
            <a href="https://sid.onlinelibrary.wiley.com/doi/abs/10.1002/sdtp.18459" target="_blank" rel="noopener">
              Micro-LED Pixel Circuit with A Novel NMOS-Oxide TFT Inverter for Reducing Falling Time and Enhancing Gray-Level Expression
            </a>
          </div>
          <div class="pub-meta">
            <span class="pub-venue">SID 2025 · San Jose, USA</span>
            <span class="type-tag">Poster</span>
          </div>
          <div class="pub-actions">
            <a class="pill-btn" href="https://sid.onlinelibrary.wiley.com/doi/abs/10.1002/sdtp.18459" target="_blank" rel="noopener">🔗 Paper</a>
          </div>
        </div>
      </li>

      <li class="pub-item">
        <div class="pub-year">2025</div>
        <div class="pub-content">
          <span class="pub-authors">Chae-Hwan Park, Soobin An, Seungyoon Shin, Ji-Ho Lee, Hyeonjun Choi, and Soo-Yeon Lee</span>
          <div class="pub-title">
            <span>고성능 디스플레이 화소 회로 설계를 위한 TFT 인버터 특성 비교</span>
          </div>
          <div class="pub-meta">
            <span class="pub-venue">KMID 2025 · Gangneung, Korea</span>
            <span class="type-tag">Poster</span>
          </div>
        </div>
      </li>

      <li class="pub-item">
        <div class="pub-year">2024</div>
        <div class="pub-content">
          <span class="pub-authors">Chae-Hwan Park, Kyeong-Soo Kang, Ji-Hwan Park, Chanjin Park, and Soo-Yeon Lee</span>
          <div class="pub-title">
            <span>μLED Pixel Circuit Based on Low-Temperature Polysilicon and Oxide Thin-Film Transistors for Pulse-Width Modulation with Extremely Short Falling Time</span>
          </div>
          <div class="pub-meta">
            <span class="pub-venue">ICEP-ITA 2024 · Tashkent, Uzbekistan</span>
            <span class="type-tag">Oral</span>
          </div>
        </div>
      </li>

    </ul>
  </div>
</div>

<!-- ========================= Research Showcase ========================= -->
<div class="section-container">
  <h2 class="section-title">Research Topic</h2>

  <div class="research-hero">
    <div class="research-hero-text">
      <h2>CMOS/TFT Circuit Design</h2>
      <p>
        I conduct research on <b>Si-based CMOS</b> and <b>IGZO-based TFT</b> circuit design and verification,
        focusing on <b>neuromorphic</b> (SNN-based neuron circuit) and <b>display driving circuits</b> (OLED, μLED),
        with a growing interest in mixed-signal circuit design integrating <b>analog and digital circuits</b>.
      </p>
      <div class="keyword-row">
        <span class="keyword-chip">Si-CMOS</span>
        <span class="keyword-chip">IGZO-TFT</span>
        <span class="keyword-chip">Neuron circuit</span>
      </div>

      <div class="hero-cta">
        <button class="btn primary" type="button"
          onclick="showComingSoon('Details', 'The project details page is currently under preparation.')">
          📌 Details
        </button>

        <button class="btn ghost" type="button"
          onclick="showComingSoon('Download Materials', 'There is currently no uploaded material.')">
          ⬇️ Download Materials
        </button>
      </div>
    </div>

    <div class="research-hero-media" onclick="openGallery('/assets/new_images/research/circuit.png')">
      <img src="/assets/new_images/research/circuit.png" alt="CMOS/TFT Circuit Design">
    </div>
  </div>

  <div style="height: 50px;"></div>

  <div class="research-hero">
    <div class="research-hero-text">
      <h2>System Architecture Design</h2>
      <p>
        I focus on <b>hardware system design</b> bridging custom devices, CMOS circuits, and PCB-level electronics.
        My work includes <b>MCU/FPGA-based control</b>, <b>AFE-optimized sensing</b>, and low-power integrated platforms
        for future sensing, display-integrated, and <b>neuromorphic systems</b>.
      </p>
      <div class="keyword-row">
        <span class="keyword-chip">PCB</span>
        <span class="keyword-chip">FPGA</span>
        <span class="keyword-chip">MCU/MPU</span>
        <span class="keyword-chip">Sensor</span>
      </div>

      <div class="hero-cta">
        <button class="btn primary" type="button"
          onclick="showComingSoon('Details', 'The project details page is currently under preparation.')">
          📌 Details
        </button>

        <button class="btn ghost" type="button"
          onclick="showComingSoon('Download Materials', 'There is currently no uploaded material.')">
          ⬇️ Download Materials
        </button>
      </div>
    </div>

    <div class="research-hero-media" onclick="openGallery('/assets/new_images/research/system.png')">
      <img src="/assets/new_images/research/system.png" alt="System Architecture Design">
    </div>
  </div>
</div>

<!-- ========================= Projects ========================= -->
<div class="section-container" id="projects">
  <h2 class="section-title">Projects</h2>

  <div class="uni-header"><h1>Seoul National University</h1></div>
  <div class="custom-grid">
    <div class="custom-card" onclick="openGallery('/assets/new_images/project5.jpg')">
      <div class="card-img-wrap">
        <img src="/assets/new_images/project5.jpg" alt="PCB">
        <div class="card-corner">Hardware</div>
        <div class="card-hint">🔍 Zoom</div>
      </div>
      <div class="card-content">
        <span class="card-tag">Hardware</span>
        <div class="card-title">PCB Circuit Design</div>
        <p class="card-desc">PPG measurement PCB, ACE Lab, 2024</p>
      </div>
      <div class="card-footer">
        <span style="font-weight:700; color: rgba(31,42,55,0.62); font-size:0.86rem;">ACE Lab</span>
        <span style="font-weight:700; color: rgba(31,42,55,0.52); font-size:0.86rem;">2024</span>
      </div>
    </div>

    <div class="custom-card" onclick="openGallery('/assets/new_images/project4_original.jpg')">
      <div class="card-img-wrap">
        <img src="/assets/new_images/project4.jpg" alt="Internship">
        <div class="card-corner">Sensor</div>
        <div class="card-hint">🔍 Zoom</div>
      </div>
      <div class="card-content">
        <span class="card-tag">Sensor</span>
        <div class="card-title">Winter Internship</div>
        <p class="card-desc">Piezo based Stiffness Sensor, Hero Lab, 2022</p>
      </div>
      <div class="card-footer">
        <span style="font-weight:700; color: rgba(31,42,55,0.62); font-size:0.86rem;">Hero Lab</span>
        <span style="font-weight:700; color: rgba(31,42,55,0.52); font-size:0.86rem;">2022</span>
      </div>
    </div>
  </div>

  <div class="uni-header"><h1>Hanyang University</h1></div>
  <div class="custom-grid">

    <a href="https://www.youtube.com/watch?v=OespY0dTNjA" target="_blank" rel="noopener" class="custom-card">
      <div class="card-img-wrap">
        <img src="/assets/new_images/project3.jpg" alt="3D map">
        <div class="card-corner">Robotics</div>
        <div class="card-hint">▶ YouTube</div>
      </div>
      <div class="card-content">
        <span class="card-tag">Robotics</span>
        <div class="card-title">2023 Academic Town</div>
        <p class="card-desc">Indoor 3D Mapping for convenience technology</p>
      </div>
      <div class="card-footer">
        <div class="youtube-label">📺 Watch on YouTube</div>
        <span style="font-weight:700; color: rgba(31,42,55,0.52); font-size:0.86rem;">2023</span>
      </div>
    </a>

    <a href="https://www.youtube.com/watch?v=2-kjNgfCKaI&t=18s" target="_blank" rel="noopener" class="custom-card">
      <div class="card-img-wrap">
        <img src="/assets/new_images/project2.jpg" alt="robot">
        <div class="card-corner">Deep Learning</div>
        <div class="card-hint">▶ YouTube</div>
      </div>
      <div class="card-content">
        <span class="card-tag">Deep Learning</span>
        <div class="card-title">Capstone Design II</div>
        <p class="card-desc">Solar-powered Cigarette Butts Collection Robot Using Deep-learning</p>
      </div>
      <div class="card-footer">
        <div class="youtube-label">📺 Watch on YouTube</div>
        <span style="font-weight:700; color: rgba(31,42,55,0.52); font-size:0.86rem;">2023</span>
      </div>
    </a>

    <div class="custom-card" onclick="openGallery('/assets/new_images/project1_original.jpg')">
      <div class="card-img-wrap">
        <img src="/assets/new_images/project1.jpg" alt="wearable body">
        <div class="card-corner">Robotics</div>
        <div class="card-hint">🔍 Zoom</div>
      </div>
      <div class="card-content">
        <span class="card-tag">Robotics</span>
        <div class="card-title">ME Capstone Design I</div>
        <p class="card-desc">Smart Key Using Gesture Recognition (Body)</p>
      </div>
      <div class="card-footer">
        <span style="font-weight:700; color: rgba(31,42,55,0.62); font-size:0.86rem;">Hanyang</span>
        <span style="font-weight:700; color: rgba(31,42,55,0.52); font-size:0.86rem;">2023</span>
      </div>
    </div>

    <div class="custom-card" onclick="openVideo('/assets/new_images/research/Final.mp4')">
      <div class="card-img-wrap">
        <img src="/assets/new_images/project0.jpg" alt="controller wearable">
        <div class="card-corner">Wearable</div>
        <div class="card-hint">▶ Video</div>
      </div>
      <div class="card-content">
        <span class="card-tag">Wearable</span>
        <div class="card-title">EE Capstone Design</div>
        <p class="card-desc">Wearable Smart Key Using Gesture Recognition (Controller)</p>
      </div>
      <div class="card-footer">
        <div class="youtube-label">📺 Watch on Video</div>
        <span style="font-weight:700; color: rgba(31,42,55,0.52); font-size:0.86rem;">2022</span>
      </div>
    </div>

    <a href="https://www.youtube.com/watch?v=pfUYDsK3Zlc" target="_blank" rel="noopener" class="custom-card">
      <div class="card-img-wrap">
        <img src="/assets/new_images/project00.jpg" alt="2022 academic town">
        <div class="card-corner">Robotics</div>
        <div class="card-hint">▶ YouTube</div>
      </div>
      <div class="card-content">
        <span class="card-tag">Robotics</span>
        <div class="card-title">2022 Academic Town</div>
        <p class="card-desc">ASAP system (Automatic Secondary Accident Prevention system)</p>
      </div>
      <div class="card-footer">
        <div class="youtube-label">📺 Watch on YouTube</div>
        <span style="font-weight:700; color: rgba(31,42,55,0.52); font-size:0.86rem;">2022</span>
      </div>
    </a>

  </div>
</div>

<!-- ========================= Lightbox Image Zoom ========================= -->
<div class="gallery-container" id="galleryContainer" onclick="closeGallery()">
  <span class="close-btn" onclick="event.stopPropagation(); closeGallery()">&times;</span>
  <img class="gallery-image" id="galleryImage" src="" alt="Gallery Image">
</div>

<!-- ========================= Video Modal ========================= -->
<div class="video-overlay" id="videoOverlay" onclick="closeVideo()">
  <div class="video-modal" id="videoModal" onclick="event.stopPropagation()">
    <span class="video-close" onclick="closeVideo()">&times;</span>
    <video id="videoPlayer" controls playsinline>
      <source id="videoSource" src="" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
</div>

<!-- ========================= Coming Soon Modal ========================= -->
<div class="comingsoon-overlay" id="comingSoonOverlay" onclick="closeComingSoon()">
  <div class="comingsoon-modal" onclick="event.stopPropagation()">
    <div class="comingsoon-top">
      <h3 class="comingsoon-title" id="comingSoonTitle">준비중입니다</h3>
      <button class="comingsoon-close" type="button" onclick="closeComingSoon()">&times;</button>
    </div>
    <div class="comingsoon-body" id="comingSoonBody">
      현재 기능을 준비 중입니다.
    </div>
    <div class="comingsoon-actions">
      <button class="comingsoon-btn" type="button" onclick="closeComingSoon()">OK</button>
    </div>
  </div>
</div>

<script>
  /* ===== Image Zoom Lightbox ===== */
  function openGallery(imageSrc) {
    const container = document.getElementById("galleryContainer");
    const img = document.getElementById("galleryImage");
    img.src = imageSrc;
    container.style.display = "flex";
    document.body.style.overflow = "hidden";
  }

  function closeGallery() {
    const container = document.getElementById("galleryContainer");
    container.style.display = "none";
    document.body.style.overflow = "auto";
  }

  /* ===== Coming Soon Modal ===== */
  function showComingSoon(title, message){
    const overlay = document.getElementById('comingSoonOverlay');
    const t = document.getElementById('comingSoonTitle');
    const b = document.getElementById('comingSoonBody');

    t.textContent = title || '준비중입니다';
    b.textContent = message || '현재 기능을 준비 중입니다.';

    overlay.style.display = 'flex';
    document.body.style.overflow = 'hidden';
  }

  function closeComingSoon(){
    const overlay = document.getElementById('comingSoonOverlay');
    overlay.style.display = 'none';
    document.body.style.overflow = 'auto';
  }

  /* ===== Video Modal ===== */
  function openVideo(videoSrc){
    const overlay = document.getElementById('videoOverlay');
    const player = document.getElementById('videoPlayer');
    const source = document.getElementById('videoSource');

    source.src = videoSrc;
    player.load();

    overlay.style.display = 'flex';
    document.body.style.overflow = 'hidden';

    const playPromise = player.play();
    if (playPromise !== undefined) {
      playPromise.catch(() => {});
    }
  }

  function closeVideo(){
    const overlay = document.getElementById('videoOverlay');
    const player = document.getElementById('videoPlayer');
    const source = document.getElementById('videoSource');

    player.pause();
    player.currentTime = 0;
    source.src = "";
    player.load();

    overlay.style.display = 'none';
    document.body.style.overflow = 'auto';
  }

  /* ===== ESC Handling ===== */
  document.addEventListener("keydown", (e) => {
    if (e.key === "Escape") {
      closeGallery();
      closeComingSoon();
      closeVideo();
    }
  });
</script>