---
layout: default
title: Blog
permalink: /blog/
---
<!-- Page Header -->
<header class="masthead-page text-white text-center" style="background: linear-gradient(rgba(13, 71, 161, 0.8), rgba(38, 50, 56, 0.8)), url('https://images.unsplash.com/photo-1503694978374-8a2fa686963a?auto=format&fit=crop&w=1920&q=80'); background-size: cover; background-position: center; padding: 180px 0 100px;">
  <div class="container">
    <h1 class="display-3 fw-bold mb-3 text-uppercase">Blog</h1>
    <p class="lead fw-light mb-0 opacity-75">Asansör dünyasından en güncel haberler, teknik bilgiler ve güvenlik tavsiyeleri.</p>
  </div>
</header>

<section class="py-5 bg-light">
  <div class="container py-5">
    <div class="row g-4">
      {% for post in site.posts %}
        <div class="col-md-4">
          <div class="card h-100 border-0 shadow-sm rounded-4 overflow-hidden">
            <div class="card-body p-4">
              <div class="text-primary small fw-bold mb-2">{{ post.date | date: "%d.%m.%Y" }}</div>
              <h4 class="card-title fw-bold mb-3"><a href="{{ post.url | prepend: site.baseurl }}" class="text-decoration-none text-dark">{{ post.title }}</a></h4>
              <p class="card-text text-muted mb-4 small">{{ post.description | truncate: 150 }}</p>
              <a href="{{ post.url | prepend: site.baseurl }}" class="btn btn-outline-primary rounded-pill btn-sm fw-bold">Devamını Oku</a>
            </div>
          </div>
        </div>
      {% endfor %}
    </div>
  </div>
</section>
