---
layout: splash
permalink: /secret/
author_profile: true
sidebar_main: false
---
**Secret Gallery**
<!DOCTYPE html>
<html>
<head>
    <title>Gallery</title>
    <link rel="stylesheet" href="style.css"> <!-- 별도의 CSS 파일을 링크합니다 -->
    <style>
        .gallery {
            display: grid;
            grid-template-columns: repeat(4, 1fr); /* 4개의 열로 그리드를 생성 */
            grid-gap: 20px; /* 이미지 간 간격 설정 */
        }
        .image-container {
            position: relative;
            width: 100%;
            overflow: hidden;
            border-radius: 8px;
        }
        .image-container img {
            width: 100%;
            height: auto;
            transition: transform 0.3s ease;
        }
        .image-container:hover img {
            transform: scale(1.1); /* 마우스를 올리면 이미지 확대 */
        }
        .overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            background-color: rgba(0, 0, 0, 0.7);
            transition: opacity 0.3s ease;
        }
        .image-container:hover .overlay {
            opacity: 1; /* 마우스를 올리면 투명도를 1로 변경하여 효과를 보여줌 */
        }
        .overlay h3 {
            color: white;
            font-size: 24px;
        }
    </style>
</head>
<body>
    <div class="gallery">
        <div class="image-container">
            <a href="./../assets/new_images/team/secret/beech.jpg">
                <img src="./../assets/new_images/team/secret/beech.jpg" alt="Image 1">
                <div class="overlay">
                    <h3>속초여행</h3>
                </div>
            </a>
        </div>
        <div class="image-container">
            <a href="./../assets/new_images/team/secret/baseball.jpg">
                <img src="./../assets/new_images/team/secret/baseball.jpg" alt="Image 2">
                <div class="overlay">
                    <h3>롯데 VS LG</h3>
                </div>
            </a>
        </div>
        <div class="image-container">
            <a href="./../assets/new_images/team/secret/youngme.jpg">
                <img src="./../assets/new_images/team/secret/youngme.jpg" alt="Image 3">
                <div class="overlay">
                    <h3>어린시절</h3>
                </div>
            </a>
        </div>
        <div class="image-container">
            <a href="./../assets/new_images/team/secret/event.jpg">
                <img src="./../assets/new_images/team/secret/event.jpg" alt="Image 4">
                <div class="overlay">
                    <h3>오잉??</h3>
                </div>
            </a>
        </div>
        <div class="image-container">
            <a href="./../assets/new_images/team/secret/event.jpg">
                <img src="./../assets/new_images/team/secret/event.jpg" alt="Image 5">
                <div class="overlay">
                    <h3>누구지?</h3>
                </div>
            </a>
        </div>
        <!-- 나머지 이미지를 동일한 방식으로 추가 -->
    </div>
</body>
</html>
