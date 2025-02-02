---
layout: splash
permalink: /research/
author_profile: true
sidebar_main: false
---
> # Conference
<ul style="list-style-type: disc; font-size: 1.1em;">
  <li>
    <sub>
      박채환, 안수빈, 신승윤, 이지호, 최현진, 이수연,  
      "고성능 디스플레이 화소 회로 설계를 위한 TFT 인버터 특성 비교",  
      Korean Meeting on Information Display 2025 (KMID 2025),  
      Gangneung, Korea, January 2025 (Poster)
    </sub>
  </li>
  <li>
    <sub>
      Chae-Hwan Park, Kyeong-Soo Kang, Ji-Hwan Park, Chanjin Park, Soo-Yeon Lee,  
      "μLED pixel circuit based on Low-Temperature Polysilicon and Oxide Thin Film Transistors for  
      pulse width modulation with extremely short falling time",  
      International Conference on Electro-physics & Information Technology Applications 2024 (ICEP-ITA 2024),  
      Tashkent, Uzbekistan, June 2024 (Oral)
    </sub>
  </li>
</ul>





> # Projects
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Projects</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Arial', sans-serif;
        }
        .top-section header {
            background-color: #0E4A84;
            color: #fff;
            text-align: center;
            padding: 5px;
        }
        .bottom-section header {
            background-color: rgb(15, 15, 112);
            color: #fff;
            text-align: center;
            padding: 5px;
        }
        section {
            padding: 20px;
        }
        .project-container {
            display: flex;
            flex-wrap: wrap;
        }
        .project-card {
            width: 30%;
            margin-right: 10px;
            margin-bottom: 20px;
            border: 1px solid #ddd;
            border-radius: 5px;
            overflow: hidden;
            transition: transform 0.3s ease-in-out;
            cursor: pointer;
            text-decoration: none; /* 변경된 부분: 링크의 기본 양식 제거 */
            color: inherit; /* 변경된 부분: 기본 링크 색상 상속 */
            display: block; /* 변경된 부분: 링크를 블록 레벨로 설정 */
            text-align: center; /* 가운데 정렬 추가 */
        }
        .project-card:hover {
            transform: scale(1.05);
        }
        .project-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        .project-details {
            padding: 15px;
        }
        .project-title {
            font-size: 18px;
            font-weight: bold;
            margin-bottom: 10px;
        }
        .project-description {
            font-size: 14px;
            color: #555;
        }
        /* 갤러리 스타일 */
        .gallery-container {
            display: none;
            position: fixed;
            z-index: 2;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            max-width: 80%;
            max-height: 80%;
            overflow: hidden;
            background-color: #fff;
            box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.5);
        }
        .gallery-content {
            width: 100%;
            height: 100%;
        }
        .gallery-image {
            width: 100%;
            height: auto;
            object-fit: contain;
        }
        .close {
            color: #000;
            position: absolute;
            top: 10px;
            right: 10px;
            font-size: 20px;
            cursor: pointer;
        }

        @media (max-width: 600px) {
            .project-card {
                width: 100%;
                margin-right: 0;
            }
        }
    </style>
</head>
<body>
    <div class="bottom-section">
        <header>
            <h1>Seoul National University</h1>
        </header>
    </div>
    <section>
        <div class="project-container">
            <div class="project-card" onclick="openGallery('/assets/new_images/project5.jpg')">
                <img src="/assets/new_images/project5.jpg" alt="Project 3">
                <div class="project-details">
                    <div class="project-title">PCB circuit design</div>
                    <div class="project-description">PPG(Photoplethysmogram) measurement PCB, ACE Lab, 2024</div>
                </div>
            </div>
             <div class="project-card" onclick="openGallery('/assets/new_images/project4_original.jpg')">
                <img src="/assets/new_images/project4.jpg" alt="Project 3">
                <div class="project-details">
                    <div class="project-title">2022 Winter vacation Intern</div>
                    <div class="project-description">Piezo based Stiffness Sensor, Hero Lab, 2022</div>
                </div>
            </div>           
            <!-- 다른 프로젝트 카드들도 같은 방식으로 수정 -->
        </div>
    </section>
    <div class="top-section">
        <header>
            <h1>Hanyang University</h1>
        </header>
    </div>
    <section>
        <div class="project-container">
            <a href="https://www.youtube.com/watch?v=OespY0dTNjA" class="project-card" onclick="openGallery('/assets/new_images/project3_original.jpg')">
                <img src="/assets/new_images/project3.jpg" alt="Project 3">
                <div class="project-details">
                    <div class="project-title">2023 Hanyang Academic Town</div>
                    <div class="project-description">실내 3D Map 생성을 통한 미래 편의 기술 확충<br><br>▶ YouTube link ◀</div>
                </div>
            </a>
            <a href="https://www.youtube.com/watch?v=2-kjNgfCKaI&t=18s" class="project-card" onclick="openGallery('/assets/new_images/project2_original.jpg')">
                <img src="/assets/new_images/project2.jpg" alt="Project 2">
                <div class="project-details">
                    <div class="project-title">ME Capstone Design Project 2</div>
                    <div class="project-description">Solar-powered Cigarette Butts Collection Robot Using Deep Learning, 2023<br><br>▶ YouTube link ◀</div>
                </div>
            </a>
            <div class="project-card" onclick="openGallery('/assets/new_images/project1_original.jpg')">
                <img src="/assets/new_images/project1.jpg" alt="Project 1">
                <div class="project-details">
                    <div class="project-title">ME Capstone Design Project 1</div>
                    <div class="project-description">Wearable Smart Key Using Gesture Recognition (car body), 2023</div>
                </div>
            </div>
            <div class="project-card" onclick="openGallery('/assets/new_images/project0_original.jpg')">
                <img src="/assets/new_images/project0.jpg" alt="Project 1">
                <div class="project-details">
                    <div class="project-title">EE Capstone Design Project</div>
                    <div class="project-description">Wearable Smart Key Using Gesture Recognition (Controller), 2023</div>
                </div>
            </div>
            <a href="https://www.youtube.com/watch?v=pfUYDsK3Zlc" class="project-card" onclick="openGallery('/assets/new_images/project00_original.jpg')">
                <img src="/assets/new_images/project00.jpg" alt="Project 2">
                <div class="project-details">
                    <div class="project-title">2022 Hanyang Academic Town</div>
                    <div class="project-description">ASAP system (Automatic Secondary Accident Prevention system), 2022<br><br>▶ YouTube link ◀</div>
                </div>
            </a>
        </div>
    </section>
    <div class="gallery-container" id="galleryContainer" onclick="closeGallery()">
        <span class="close" onclick="closeGallery()">&times;</span>
        <div class="gallery-content">
            <img class="gallery-image" id="galleryImage" src="" alt="Gallery Image">
        </div>
    </div>
    <script>
        function openGallery(imageSrc) {
            var galleryContainer = document.getElementById("galleryContainer");
            var galleryImage = document.getElementById("galleryImage");
            galleryImage.src = imageSrc;
            galleryContainer.style.display = "flex";
        }

        function closeGallery() {
            var galleryContainer = document.getElementById("galleryContainer");
            galleryContainer.style.display = "none";
        }
    </script>
</body>
</html>
