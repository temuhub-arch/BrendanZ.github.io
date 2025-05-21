📁 _config.yml
--------------------------------------------------
title: My Custom Jekyll Theme
description: A minimalist theme for GitHub Pages
baseurl: ""
url: "https://your-username.github.io"
theme: null
markdown: kramdown

📁 index.md
--------------------------------------------------
---
layout: default
title: Home
---

# Welcome to My GitHub Page

This is a clean and custom theme built with Jekyll for GitHub Pages.

📁 _layouts/default.html
--------------------------------------------------
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>{{ page.title }} - {{ site.title }}</title>
  <link rel="stylesheet" href="/assets/style.css">
</head>
<body>
  {% include header.html %}
  <main>
    {{ content }}
  </main>
  {% include footer.html %}
</body>
</html>

📁 _includes/header.html
--------------------------------------------------
<header>
  <h1><a href="/">{{ site.title }}</a></h1>
  <nav>
    <a href="/">Home</a>
    <a href="/about">About</a>
  </nav>
</header>

📁 _includes/footer.html
--------------------------------------------------
<footer>
  <p>© {{ site.title }} {{ site.time | date: "%Y" }}</p>
</footer>

📁 assets/style.css
--------------------------------------------------
body {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  margin: 0;
  padding: 0;
  background: #f8f9fa;
  color: #212529;
}

header, footer {
  background: #343a40;
  color: white;
  padding: 1rem;
  text-align: center;
}

header a, footer a {
  color: #f8f9fa;
  text-decoration: none;
}

nav a {
  margin: 0 1rem;
}

main {
  padding: 2rem;
  max-width: 800px;
  margin: auto;
  background: white;
  box-shadow: 0 0 10px rgba(0,0,0,0.05);
}
