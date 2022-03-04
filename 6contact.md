---
layout: page
title: Contact Me
---

### Do you have a question? (Maybe) I have a answer. 😄

#### For questions, compliments, suggestions and complaints, send me a message using the form below. 
#### I will try to answer as soon as possible!


<head>
  <title>reCAPTCHA demo: Simple page</title>
  <script src="https://www.google.com/recaptcha/api.js" async defer></script>
</head>

<form id="fs-frm" name="simple-contact-form" accept-charset="utf-8" action="https://formspree.io/f/xleznwww" method="post">
  <fieldset id="fs-frm-inputs">
    <label for="full-name">Name</label>  <br>
    <input type="text" name="name" id="full-name" placeholder="First and last name." required=""> <br>
    <label for="email-address">E-mail</label> <br>
    <input type="email" name="_replyto" id="email-address" placeholder="youremail@domain.com" required=""> <br>
    <label for="message">Message</label> <br>
    <textarea rows="5" name="message" id="message" placeholder="Please, type your message here." required=""></textarea>
    <input type="hidden" name="_subject" id="email-subject" value="Contact Form Submission">
  </fieldset>
  <input type="submit" value="Submit">
</form>

