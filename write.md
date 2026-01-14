---
layout: default
title: Write a Post
---

<div class="write-container">
  <h2>Write a new blog post ✍️</h2>

  <form action="https://formspree.io/f/mykkyrvk" method="POST">

    <label>Post Title</label>
    <input type="text" name="title" placeholder="My awesome blog post" required>

    <label>Post Content</label>
    <textarea name="content" rows="10" placeholder="Start writing here..." required></textarea>

    <button type="submit">Submit Draft</button>

  </form>
</div>
