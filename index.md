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
  <input type="hidden" name="_next" value="?success=1">
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

<div id="sent" style="display:none;">✅ Thanks! Your message has been sent.</div>
<script>
  if (new URLSearchParams(location.search).get('success')) {
    document.getElementById('sent').style.display = 'block';
  }
</script>
