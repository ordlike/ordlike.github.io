---
layout: single
permalink: /contact/
author_profile: true
sidebar_main: false
---
# ***| Direct Message System***
<head>
    <script type="text/javascript" src="https://cdn.jsdelivr.net/npm/emailjs-com@3/dist/email.min.js"></script>
    <script type="text/javascript">
        (function() {
            // https://dashboard.emailjs.com/admin/account
            emailjs.init('6NrA1NVH-yQj6Nas4');
        })();
    </script>
    <script type="text/javascript">
        window.onload = function() {
            document.getElementById('contact-form').addEventListener('submit', function(event) {
                event.preventDefault();
                // generate a five digit number for the contact_number variable
                this.contact_number.value = Math.random() * 100000 | 0;

                // 유효성 검사: 제목, 이메일 주소, 메시지가 모두 입력되었는지 확인
                var title = this.title.value;
                var email = this.email.value;
                var message = this.message.value;
                if (!title || !email || !message) {
                    window.alert('Please fill in all blanks.');
                    return;
                }
    
                // these IDs from the previous steps
                emailjs.sendForm('service_ybo0xbb', 'template_fz0bb1f', this)
                    .then(function(response) {
                        window.alert('Message sent successfully!');
                    }, function(error) {
                        window.alert('Failed to send message. Please try again later.');
                    });
            });
        }
    </script>
</head>
<body>
    <form id="contact-form">
        <input type="hidden" name="contact_number">
        <label>Your Name</label>
        <input type="text" name="name">
        <label>Message Title</label>
        <input type="text" name="title">
        <label>Your Email address</label>
        <input type="email" name="email">
        <label>Message</label>
        <textarea name="message"></textarea>
        <input type="submit" value="Send">
    </form>
</body>





