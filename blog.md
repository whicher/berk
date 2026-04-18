---
layout: default
title: Blog
permalink: /blog/
---
<section class="py-5 mt-5">
  <div class="container py-5">
    <div class="row mb-5 text-center">
      <div class="col-lg-12">
        <h1 class="display-4 fw-bold mb-3" style="color: #{{ site.data.template.color.primary }};">Blog</h1>
        <p class="lead text-muted">Asansör dünyasından en güncel haberler, teknik bilgiler ve güvenlik tavsiyeleri.</p>
      </div>
    </div>
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
