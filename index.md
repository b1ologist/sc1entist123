├── _config.yml
├── index.md
├── about.md
├── _posts/
│   └── 2025-04-14-welcome.md
├── _layouts/
│   └── default.html
├── _includes/
│   └── header.html
│   └── footer.html
└── assets/
    └── style.css

---

# _config.yml

title: My Jekyll Site
description: Добро пожаловать на мой сайт!
baseurl: ""
url: "https://USERNAME.github.io"
theme: minima

---

# index.md

---
layout: default
title: Главная
---

# Привет!

Добро пожаловать на мой сайт. Я делаю классные вещи. Ниже — мои посты 👇

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url }})
{% endfor %}

---

# about.md

---
layout: default
title: Обо мне
---

## Кто я?

Я — человек, который решил сделать свой сайт с нуля. 🚀  
Интересуюсь технологиями, кодом и творчеством.

---

# _posts/2025-04-14-welcome.md

---
layout: default
title: "Добро пожаловать в мой блог!"
date: 2025-04-14
---

Это мой первый пост на Jekyll!  
Здесь я буду писать мысли, проекты, и, может быть, мемы.

---

# _layouts/default.html

<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>{{ page.title }}</title>
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

---

# _includes/header.html

<header>
  <h1><a href="/">My Jekyll Site</a></h1>
  <nav>
    <a href="/">Главная</a> |
    <a href="/about">Обо мне</a>
  </nav>
</header>

---

# _includes/footer.html

<footer>
  <p>&copy; {{ site.time | date: "%Y" }} Все права защищены.</p>
</footer>

---

# assets/style.css

body {
  font-family: sans-serif;
  max-width: 800px;
  margin: auto;
  padding: 2rem;
  background: #f9f9f9;
  color: #333;
}

header, footer {
  text-align: center;
  margin: 2rem 0;
}
