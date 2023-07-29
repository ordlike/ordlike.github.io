---
layout: splash
permalink: /contact/
author_profile: true
sidebar_main: true
---

<!DOCTYPE html>
<html>
<head>
    <title>Contact Form</title>
    <script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@emailjs/browser@3/dist/email.min.js"></script>
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
                // these IDs from the previous steps
                emailjs.sendForm('service_ybo0xbb', 'template_fz0bb1f', this)
                    .then(function() {
                        console.log('SUCCESS!');
                    }, function(error) {
                        console.log('FAILED...', error);
                    });
            });
        }
    </script>
</head>
<body>
    <form id="contact-form">
        <input type="hidden" name="contact_number">
        <label>Name</label>
        <input type="text" name="user_name">
        <label>Email</label>
        <input type="email" name="user_email">
        <label>Message</label>
        <textarea name="message"></textarea>
        <input type="submit" value="Send">
    </form>
</body>
</html>



<!-- #### Contact easily through below!
Everything is welcome :)
<br>
<input type="text" name="name" placeholder="Enter your name" style="width:100%">
<br>
<input type="text" name="email" placeholder="Enter your email address" style="width:100%">
<br>
<input type="text" name="phone" placeholder="Enter your phone number" style="width:100%">
<br>

<textarea name="message" rows="5" placeholder="Enter the contents" style="width:100%"></textarea>
<br>
<input type="button" name="submit" value="Send" style= "color:white; background:rgb(38, 124, 185); border-radius:5px"/>


<script type="text/javascript"
        src="https://cdn.jsdelivr.net/npm/emailjs-com@2/dist/email.min.js">
</script>

<script type="text/javascript">
	import{ init } from 'emailjs-com';
    init("user_6NrA1NVH-yQj6Nas4");
	$(document).ready(function() {
		emailjs.init("user_6NrA1NVH-yQj6Nas4");		

    $('input[name=submit]').click(function(){       	 
          
        var templateParams = {	
             name: $('input[name=name]').val(),
            phone: $('input[name=phone]').val(), 
            email : $('input[name=email]').val(),
            message : $('textarea[name=message]').val()
           				};


​                	
​         emailjs.send('service_ybo0xbb', 'template_fz0bb1f', templateParams)
​         	.then(function(response) {
​         	  console.log('SUCCESS!', response.status, response.text);
​         	}, function(error) {
​         	       console.log('FAILED...', error);
​         	});


​         	       


        });
        
      })();


	</script>
(Last Update: 09/28/2021)
 -->
