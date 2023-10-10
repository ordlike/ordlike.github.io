---
title: "Welcome to ORDLIKE!"
layout: splash
permalink: /main/
date: 2023-07-30     
header:
  overlay_color: "#000"
  overlay_filter: "0.3"
  overlay_image: /assets/new_images/mainprofile_HYU.jpg
  
  actions:
  - label: "Download CV"
    url: "https://raw.githubusercontent.com/ordlike/ordlike.github.io/master/Files/C.V_Chaehwan%20Park.pdf" 
  - label: "Direct Contact"
    url: "/contact/"

  caption: #"Photo credit: [****](https://unsplash.com)"
excerpt: "Hello! I'm Chaehwan Park. <br> ORDLIKE Website is My personal homepage. "
intro: 
  - excerpt: 'Dept. of *Mechanical Engineering* & *Electronic Engineering* at Hanyang University, Seoul. 
  If you have any questions, please feel free to contact me. ' 



feature_row:
  - image_path: /assets/new_images/aboutme_final.jpg
    url: "/about/"
    alt: Projects
    title: <center>About me</center>
    excerpt: "If you want more information **About me**, please come in!"
    btn_label: "Read More" 
    btn_class: "btn--primary"

  - image_path: /assets/new_images/Team_final.jpg 
    title: <center>Team</center>
    excerpt: "Introducing the **Team members** who worked with me."
    url: "/team/"
    btn_label: "Read More"
    btn_class: "btn--primary"
    #image_caption: "Image courtesy of [Unsplash](https://unsplash.com/)"

  - image_path: /assets/new_images/main_car.jpg
    title: <center>Projects</center>
    excerpt: "Let me introduce the **Projects** I've been working on!"
    url: "/projects/"
    btn_label: "Read More"
    btn_class: "btn--primary"
    
feature_row2:
  - image_path: /assets/new_images/news2.jpg
    alt: "placeholder image 2"
    title: "Playing the drums at the Band Club Hanullim Performance!"
    excerpt: "On October 6, 2023, I played the drums for 'Buzz - Journey For Myself' at the Hanwoollim Freshman Performance, a band club at Hanyang University's College of Engineering."
    url: "/third/"
    btn_label: "Read More"
    btn_class: "btn--primary"
# feature_row3:
#   - image_path: /assets/images/unsplash-gallery-image-2-th.jpg
#     alt: "placeholder image 2"
#     title: "Placeholder Image Right Aligned"
#     excerpt: 'This is some sample content that goes here with **Markdown** formatting. Right aligned with `type="right"`'
#     url: "#test-link"
#     btn_label: "Read More"
#     btn_class: "btn--primary"
# feature_row4:
#   - image_path: /assets/images/unsplash-gallery-image-2-th.jpg
#     alt: "placeholder image 2"
#     title: "Placeholder Image Center Aligned"
#     excerpt: 'This is some sample content that goes here with **Markdown** formatting. Centered with `type="center"`'
#     url: "#test-link"
#     btn_label: "Read More"
#     btn_class: "btn--primary"
---

{% include feature_row id="intro" type="center" %}

{% include feature_row %}

# :: HOT News ::


{% include feature_row id="feature_row2" type="left" %}

<!-- {% include feature_row id="feature_row3" type="right" %}

{% include feature_row id="feature_row4" type="center" %} -->
