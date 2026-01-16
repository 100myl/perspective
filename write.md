---
layout: page  # or default / post — check your _config.yml or index
title: Write a new blog post ✍️
---

<style>
  .form-container {
    max-width: 600px;
    margin: 40px auto;
    padding: 30px;
    background: rgba(255,255,255,0.9);
    border-radius: 12px;
    box-shadow: 0 4px 20px rgba(0,0,0,0.15);
  }
  input, textarea {
    width: 100%;
    padding: 12px;
    margin: 12px 0;
    border: 1px solid #ccc;
    border-radius: 6px;
    font-size: 16px;
  }
  textarea { height: 180px; resize: vertical; }
  button {
    background: #6c5ce7;
    color: white;
    padding: 14px 28px;
    border: none;
    border-radius: 6px;
    font-size: 18px;
    cursor: pointer;
  }
  button:hover { background: #5649c0; }
  .success { color: green; font-weight: bold; display: none; }
</style>

<div class="form-container">
  <h1>Write a new blog post ✍️</h1>
  <p>Send me your draft / idea — I'll review and publish it on the blog!</p>

  <form action="[https://formspree.io/f/mykkyrvk]" method="POST">
    <!-- Replace YOUR_FORM_ID_HERE with your actual Formspree endpoint (e.g. xabcdeyz) -->

    <input type="email" name="email" placeholder="Your email:" required>

    <input type="text" name="title" placeholder="Post Title (optional but helpful)" required>

    <textarea name="message" placeholder="Your Message / Full post content (Markdown is great!)" required></textarea>

    <!-- Honeypot spam trap — leave empty, humans won't fill it -->
    <input type="text" name="_gotcha" style="display:none">

    <button type="submit">Send Post Idea →</button>
  </form>

  <p class="success" id="success-msg">Thank you! I'll check it soon and add to the blog if suitable.</p>
</div>

<script>
  document.querySelector('form').addEventListener('submit', function(e) {
    // Optional: show success message without reload (nice UX)
    setTimeout(() => {
      document.getElementById('success-msg').style.display = 'block';
    }, 800);
  });
</script>
