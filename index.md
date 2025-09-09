---
layout: default
title: Home
---

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>{{ page.title }} | {{ site.title }}</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <style>
    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
      line-height: 1.6;
      margin: 0;
      padding: 0;
      color: #333;
    }
    .container {
      max-width: 900px;
      margin: 0 auto;
      padding: 2rem;
    }
    h1, h2 {
      text-align: center;
    }
    img.profile {
      display: block;
      margin: 1rem auto;
      border-radius: 50%;
      width: 200px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
    }
    /* Carousel */
    .carousel {
      position: relative;
      width: 100%;
      max-width: 800px;
      margin: 2rem auto;
      overflow: hidden;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
    }
    .carousel .slides {
      display: flex;
      width: 300%;
      animation: slide 12s infinite;
    }
    .carousel img {
      width: 100%;
      flex: 1 0 100%;
      object-fit: cover;
    }
    @keyframes slide {
      0%, 30% { transform: translateX(0%); }
      33%, 63% { transform: translateX(-100%); }
      66%, 96% { transform: translateX(-200%); }
      100% { transform: translateX(0%); }
    }
    /* Blog list */
    .posts {
      margin-top: 3rem;
    }
    .posts ul {
      list-style: none;
      padding: 0;
    }
    .posts li {
      margin-bottom: 1rem;
    }
    .posts a {
      text-decoration: none;
      font-weight: bold;
      color: #0066cc;
    }
    .posts small {
      color: #666;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Hi, I’m Phoebe 👋</h1>
    <p>
      A PwC tech degree apprentice, avid supporter of Women in Tech, and part of the internal team of CyberWomen Groups C.I.C.
    </p>
    <p>
      I love cyber conferences, especially speaking at them – so my new blog is for me to research and share about topics that interest me, in between those conferences!
    </p>
    <img src="/assets/images/Phoebe-Farrelly.png" alt="Phoebe Farrelly" class="profile">

    <!-- Carousel -->
    <div class="carousel">
      <div class="slides">
        <img src="/assets/images/pic1.jpg" alt="Slide 1">
        <img src="/assets/images/pic2.jpg" alt="Slide 2">
        <img src="/assets/images/pic3.jpg" alt="Slide 3">
      </div>
    </div>

    <!-- Blog posts -->
    <div class="posts">
      <h2>Latest Posts</h2>
      <ul>
        {% for post in site.posts %}
          <li>
            <a href="{{ post.url }}">{{ post.title }}</a>
            <br><small>{{ post.date | date: "%B %d, %Y" }}</small>
          </li>
        {% endfor %}
      </ul>
    </div>
  </div>
</body>
</html>
