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

<!-- 🔽 hidden by default; becomes visible when page reloads with #sent -->
<div id="sent" style="display:none; margin-top:1rem; color:green;">
  ✅ Thanks! Your message has been sent.
</div>

<script>
  /* If the URL ends in #sent, un‑hide the success banner */
  if (location.hash === '#sent') {
    document.getElementById('sent').style.display = 'block';
    /* optional: scroll to it */
    document.getElementById('sent').scrollIntoView({behavior:'smooth'});
  }
</script>
