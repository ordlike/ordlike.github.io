---
title: "Welcome to ORDLIKE!"
layout: splash
permalink: /main/
date: 2025-02-02    
header:
  overlay_color: "#000"
  overlay_filter: "0.3"
  overlay_image: /assets/new_images/main.gif
  
  actions:
  - label: "Download CV"
    url: "https://raw.githubusercontent.com/ordlike/ordlike.github.io/master/Files/C.V_Chaehwan%20Park.pdf" 
  - label: "Direct Contact"
    url: "/contact/"
  
  caption: #"Photo credit: [****](https://unsplash.com)"
excerpt: "Hello! I'm Chaehwan Park. <br> ORDLIKE Website is My personal homepage. "

feature_row2:
  - image_path: /assets/new_images/news2.jpg
    alt: "placeholder image 2"
    title: "Playing the drums at the Band Club Hanwoollim Performance!"
    excerpt: "On October 6, 2023, I played the drums for 'Buzz - Journey For Myself' at the Hanwoollim Freshman Performance, a band club at Hanyang University's College of Engineering."
    url: "/third/"
    btn_label: "Read More"
    btn_class: "btn--primary"
---

<style>
  body {
    margin: 0;
    padding: 0;
  }

  .department-info {
    font-size: 10px;
    text-align: center;
    margin-top: 10px;
    border-bottom: 1px solid #DCDCDC;
    padding-bottom: 10px;
  }

  .feature-container {
    text-align: center;
    display: flex;
    justify-content: space-between; /* Update this line */
    flex-wrap: wrap;
  }

  .feature-container a {
    text-decoration: none;
    color: black;
    width: 30%; /* Update this line */
    box-sizing: border-box; /* Add this line to include padding and border in the width */
    margin-bottom: 20px; /* Add some margin to create space between images */
  }

  .feature-container img {
    width: 100%;
    max-width: 100%;
    height: auto;
    border-radius: 5px;
    cursor: pointer;
    transition: transform 0.2s ease-in-out;
  }

    
  .feature-container img:hover {
    transform: scale(1.05);
  }

  .feature-container h1,
  .feature-container p {
    margin: 15px 0; /* Add margin to the top and bottom */
    color: #000000;
    
  }
  .custom-feature-row img {
            width: 100%;
            max-width: 100%;
            height: auto;
            border-radius: 5px;
            cursor: pointer;
            transition: transform 0.2s ease-in-out;
        }

  .custom-feature-row img:hover {
            transform: scale(1.05);
        }

  .custom-feature-row h1,
  .custom-feature-row p {
            margin: 10px 0;
            color: #000000;
        }
        
  .hot-news-header {
            font-weight: bold;
            font-size: 35px;
            margin-bottom: 10px;
            margin-top: 10px; /* Add this line for spacing above */
            border-top: 1px solid #DCDCDC; /* Add this line for the border above */
            padding-top: 20px; /* Add this line for spacing */
            padding-bottom: 5px; /* Add this line for spacing */
            color: #000000;
        }

  .hot-news-container {
        text-align: center;
        margin-top: 20px;
    }

  .hot-news-item {
    display: flex;
    align-items: center;
    justify-content: space-between;
    text-decoration: none;
    color: black;
    box-sizing: border-box;
    margin-bottom: 20px;
}

.text-container {
    width: 60%;
    padding: 0 20px;
    box-sizing: border-box;
    text-align: left;
    color: rgb(15, 15, 112); /* 텍스트 색상을 변경합니다. */
}

.btn--primary-container {
    display: flex;
    justify-content: flex-end; /* 버튼을 컨테이너의 오른쪽에 정렬합니다. */
}

.btn--primary {
    display: inline-block;
    padding: 10px 20px;
    font-size: 16px;
    font-weight: bold;
    text-align: center;
    text-decoration: none;
    background-color: #0E4A84; /* 초기 색상을 #0E4A84로 설정합니다. */
    color: #fff;
    border-radius: 5px;
    transition: background-color 0.3s ease-in-out;
}

.btn--primary:hover {
    background-color: rgb(15, 15, 112); /* 호버 시 색상을 RGB(15, 15, 112)로 변경합니다. */
}


.hot-news-item img {
        width: 40%;
        max-width: 100%;
        height: auto;
        border-radius: 5px;
        cursor: pointer;
        transition: transform 0.2s ease-in-out;
    }

.hot-news-item img:hover {
        transform: scale(1.05);
    }

.text-container {
        width: 60%; /* 텍스트 컨테이너의 너비를 조절하세요 */
        padding: 0 40px; /* 더 나은 간격을 위해 패딩을 추가하세요 */
        box-sizing: border-box;
        text-align: left;
    }

    /* 모바일 화면 크기에 대한 미디어 쿼리 추가 */
        @media screen and (max-width: 600px) {
            .feature-container a {
                width: 100%;
            }

            .hot-news-item {
                flex-direction: column;
            }

            .text-container {
                width: 100%;
                padding: 0 10px;
            }

            .hot-news-item img {
                width: 100%;
                margin-bottom: 10px;
            }
        }



</style>

<p class="department-info">
  Dept. of <em>Electrical and Computer Engineering</em> at Seoul National University, Seoul.<br>
  If you have any questions, please feel free to contact me.
</p>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome to ORDLIKE!</title>
</head>
<body>
    <section class="feature-container">
        <a href="/about">
            <img src="/assets/new_images/aboutme_final.gif" alt="About me">
            <h1>About me</h1>
            <p>If you want more information <strong>About me</strong>, please come in!</p>
        </a>
        <a href="/team">
            <img src="/assets/new_images/Team_2_final.jpg" alt="Team">
            <h1>Team</h1>
            <p>Introducing the <strong>Team members</strong> who worked with me.</p>
        </a>
        <a href="/research">
            <img src="/assets/new_images/project2_original.jpg" alt="research">
            <h1>Research</h1>
            <p>Let me introduce the <strong>Research</strong> I've been working on!</p>
        </a>
 </section>
    <h1 class="hot-news-header">:: HOT News ::</h1>
    <div class="hot-news-container">
        <a href="/fifth/" class="hot-news-item">
            <img src="/assets/new_images/news4.png" alt="hot 1">
            <div class="text-container">
                <h1>Completed the full marathon course!</h1>
                <p>On November 3rd, 2024, I completed the 42.195km full course of the Seoul Marathon hosted by JTBC in 5 hours, 39 minutes and 29 seconds. Please congratulate me!</p>
            </div>
            <div class="btn--primary-container">
                <a class="btn--primary" href="/fifth/">Read More</a>
            </div>
        </a>
    </div>
</body>

</html>


