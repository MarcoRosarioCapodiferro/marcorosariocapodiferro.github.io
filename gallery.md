---
layout: default
title: "Gallery"
permalink: /gallery/
---

<section class="gallery">
  <h2>Image Gallery</h2>
  <div class="gallery-grid">
    {% assign photos = site.data.carousel_images %}
    {% for image in photos %}
      <img src="{{ image.url }}" alt="{{ image.alt }}" class="gallery-img">
    {% endfor %}
  </div>

  <!-- Lightbox -->
  <div id="lightbox" class="lightbox">
    <span class="close-btn">&times;</span>
    <img id="lightbox-img" src="" alt="Enlarged Image">
  </div>
</section>

<script>
  const galleryImages = document.querySelectorAll('.gallery-img');
  const lightbox = document.getElementById('lightbox');
  const lightboxImg = document.getElementById('lightbox-img');
  const closeBtn = document.querySelector('.close-btn');

  galleryImages.forEach(img => {
    img.addEventListener('click', () => {
      lightbox.style.display = 'flex';
      lightboxImg.src = img.src;
    });
  });

  closeBtn.addEventListener('click', () => {
    lightbox.style.display = 'none';
  });

  lightbox.addEventListener('click', (e) => {
    if (e.target === lightbox) {
      lightbox.style.display = 'none';
    }
  });
</script>
