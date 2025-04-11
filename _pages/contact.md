---
author_profile: true
layout: single
title: "Get in touch!"
permalink: /contact/
---

If you'd like to get in touch, feel free to send me a message using the form below.

<form action="https://formspree.io/f/xnnplrzp" method="POST">
  

  <label for="name">Name:</label><br>
    <input type="text" name="Name:" id="name" required><br><br>

  <label for="email">Email:</label><br>
    <input type="email" name="Reply to:" id="_replyto" required><br><br>

  <label for="message">Message:</label><br>
    <textarea name="message" id="message" rows="5" required></textarea><br><br>
    
  <input name="Subject:" id="form-subject" type="hidden" value="none" />
  <input type="submit" value="Send">
</form>
<script>
  const nameInput = document.getElementById("name");
  const subjectInput = document.getElementById("form-subject");

  nameInput.addEventListener("input", function () {
    subjectInput.value = `Message from ${nameInput.value}!`;
  });
</script>


