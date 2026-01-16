---
layout: page
title: Write a new blog post ✍️
---

<style>
  /* Your existing styles here – keep or copy from before */
  .form-container { max-width: 600px; margin: 40px auto; padding: 30px; background: rgba(255,255,255,0.9); border-radius: 12px; box-shadow: 0 4px 20px rgba(0,0,0,0.15); }
  input, textarea { width: 100%; padding: 12px; margin: 12px 0; border: 1px solid #ccc; border-radius: 6px; font-size: 16px; }
  textarea { height: 180px; resize: vertical; }
  button { background: #6c5ce7; color: white; padding: 14px 28px; border: none; border-radius: 6px; font-size: 18px; cursor: pointer; }
  button:hover { background: #5649c0; }
  .success { color: green; font-weight: bold; display: none; }
</style>

<div class="form-container">
  <h1>Write a new blog post ✍️</h1>
  <p>Send me your draft / idea — I'll review and publish it on the blog!</p>

  <form action="https://formspree.io/f/mykykrvk" method="POST">  <!-- ← Paste your REAL endpoint here (no brackets!) -->

    <input type="email" name="_replyto" placeholder="Your email:" value="pal.somil@gmail.com" required>  <!-- _replyto makes it clickable in email -->

    <input type="text" name="title" placeholder="Post Title" value="first one" required>

    <textarea name="message" placeholder="Your Message / Full post content" required>first seminar after joining mecon wait and see</textarea>

    <!-- Hidden fields for better control -->
    <input type="hidden" name="_subject" value="New Blog Post Idea from Website">
    <input type="hidden" name="_next" value="https://100myl.github.io/perspective/write?success=1">  <!-- Redirect back or to a thanks page -->
    <input type="text" name="_gotcha" style="display:none">  <!-- Spam trap -->

    <button type="submit">Send Post Idea →</button>
  </form>

  <p class="success" id="success-msg">Thank you! I'll check it soon and add to the blog if suitable.</p>
</div>

<script>
  // Simple success message (no reload needed if you want AJAX later)
  document.querySelector('form').addEventListener('submit', function() {
    setTimeout(() => {
      document.getElementById('success-msg').style.display = 'block';
    }, 1000);
  });
</script>
