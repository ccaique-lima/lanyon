---
layout: page
title: Contact Me
---

### Do you have a question? (Maybe) I have a answer. 😄

#### For questions, compliments, suggestions and complaints, send me a message using the form below. 
#### I will try to answer as soon as possible!




<html>  
  <head>    
    <title>reCAPTCHA demo: Simple page</title>    
    <script src="https://www.google.com/recaptcha/api.js" async defer></script>  
  </head>  
  <body>    
    <form action="https://formspree.io/f/xleznwww" method="POST">      
      <label for="full-name">Name</label>  <br>
      <input type="text" name="name" id="full-name" placeholder="First and last name." required=""> <br>
      <label for="email-address">E-mail</label> <br>
      <input type="email" name="_replyto" id="email-address" placeholder="youremail@domain.com" required=""> <br>
      <label for="message">Message</label> <br>
      <textarea rows="5" name="message" id="message" placeholder="Please, type your message here." required=""></textarea>
      <input type="hidden" name="_subject" id="email-subject" value="Contact Form Submission">      
      <div class="g-recaptcha" data-sitekey="6LeCXbQeAAAAAM6y7PfIyg1YBMsmwaqVbYECTHj3"></div> <!-- replace with your recaptcha SITE key not secret key -->      
      <br/>      
      <input type="submit" value="Submit">    
    </form>  
  </body>
</html>
