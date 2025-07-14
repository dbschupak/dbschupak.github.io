---
layout: default   # tells Jekyll to wrap this file with _layouts/default.html
title: Home
---

# **David Schupak Analytics**
**Data services that make your life easier** <br>
[linkedin.com/in/davidschupak](linkedin.com/in/davidschupak )

### **Summary**
David has {{ site.time | date: "%Y" | minus: 2019 }} years years of data experience.

<!-- Contact section (Markdown is fine; the HTML below passes through Jekyll) -->
## Get in touch

<form id="contact-form" action="https://submit-form.com/Efk4WA1KC" method="POST">
  <!-- ✨ optional: customise e‑mail subject for yourself -->
  <input type="hidden" name="_email.subject" value="New message from website">

  <label for="name">Name</label>
  <input type="text" id="name" name="name" placeholder="Name" required>

  <label for="email">Email</label>
  <input type="email" id="email" name="email" placeholder="Email" required>

  <label for="message">Message</label>
  <textarea id="message" name="message" placeholder="Message" required></textarea>

  <button type="submit">Send</button>
</form>

<!-- Hidden success banner -->
<p id="contact-success"
   style="display:none; margin-top:1rem; color:green;">
  ✅ Thanks! Your message has been sent.
</p>

<script>
/* ----- stay‑on‑page AJAX submit for Formspark ----- */
document.getElementById('contact-form').addEventListener('submit', async (e) => {
  e.preventDefault();                                // stop the normal redirect
  const form   = e.target;
  const data   = Object.fromEntries(new FormData(form).entries());

  try {
    const res = await fetch(form.action, {
      method: 'POST',
      headers: {
        'Accept':       'application/json',          // ← Formspark needs both
        'Content-Type': 'application/json'
      },
      body: JSON.stringify(data)
    });

    if (res.ok) {
      form.reset();                                  // clear the fields
      document.getElementById('contact-success').style.display = 'block';
    } else {
      alert('Submission failed – please try again later.');
    }
  } catch {
    alert('Network error – please check your connection.');
  }
});
</script>

