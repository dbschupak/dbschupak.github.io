---
layout: default   # tells Jekyll to wrap this file with _layouts/default.html
title: Home
---

# **David Schupak Analytics**
**Data services that make your life easier** <br>
[linkedin.com/in/davidschupak](linkedin.com/in/davidschupak )

### **Summary**
David has {{ site.time | date: "%Y" | minus: 2019 }} years years of data experience.

<form action="https://formspree.io/f/xkgzwaar" method="POST">
  <input type="hidden" name="_next" value="#sent">
  <input type="hidden" name="_subject" value="Inquiry from webite form">

  <label>
    Your name:<br>
    <input type="text" name="name" required>
  </label><br><br>

  <label>
    Your email:<br>
    <input type="email" name="email" required>
  </label><br><br>

  <label>
    Your message:<br>
    <textarea name="message" rows="5" required></textarea>
  </label><br><br>

  <button type="submit">Send</button>
</form>

<div id="success-message" style="display: none; color: green; margin-top: 1em;">
  ✅ Thanks! Your message has been sent.
</div>

<script>
  const form = document.getElementById("contact-form");
  const success = document.getElementById("success-message");

  form.addEventListener("submit", async function (e) {
    e.preventDefault(); // prevent default page reload

    const data = new FormData(form);
    const action = "https://formspree.io/f/xyzabc"; // replace with your Formspree endpoint

    const response = await fetch(action, {
      method: "POST",
      body: data,
      headers: {
        'Accept': 'application/json'
      }
    });

    if (response.ok) {
      form.reset();                    // clear the form
      success.style.display = "block" // show success message
    } else {
      alert("Something went wrong. Please try again later.");
    }
  });
</script>
