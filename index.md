---
layout: default
title: "Marco Rosario Capodiferro"
permalink: /
---

<section class="intro">
  <img src="/images/profile.jpg" alt="Profile Photo" class="profile-pic">
</section>

<section class="content-box">
  <div class="intro">
    <h2>Research Fellow in Population Genomics</h2>
    <p>Smurfit Institute of Genomics, Trinity College Dublin, Ireland</p>
  </div>
  <div class="section-content">
    <p class="big-space">I am a postdoctoral researcher specializing in population genomics, ancient DNA analysis, and human evolution.</p>
    <p class="big-space">My initial research experience in population genetics was gained in the laboratory of Prof. Alessandro Achilli at the University of Perugia (Italy), where I focused on mitochondrial DNA studies in both humans and animals.</p>
    <p class="big-space">During my PhD at the University of Pavia (Italy), I shifted my focus toward the study of autosomal markers, particularly investigating present-day and ancient Indigenous groups from the Americas.</p>
    <p class="big-space">Since 2022, I have been a member of Prof. Emilia Huerta-Sánchez's research group at the Smurfit Institute of Genetics, Trinity College Dublin (Ireland), where we study archaic introgression in ancient genomes.</p>
  </div>
</section>

<section class="content-box">
  <div class="intro">
    <h2>Latest News</h2>
  </div>
  <div class="news-item">
    <h3><a>New Talk Accepted</a></h3>
    <p>I will be giving a talk on archaic introgression at the ISBA11 conference in August in Turin, Italy. For more information, visit <a href="https://www.isba11.com/" target="_blank">ISBA11 Website</a>.</p>
  </div>
  <a href="/all-news/" class="view-all-news">View All News</a>
</section>

<section class="image-carousel">
  <h2>Who said science can’t be fun?</h2>
  <div class="carousel-container">
    <button class="prev" onclick="moveSlide(-1)">&#10094;</button>
    <div class="carousel-images">
      {% for image in site.data.carousel_images %}
        <img src="{{ image.url }}" alt="{{ image.alt }}">
      {% endfor %}
    </div>
    <button class="next" onclick="moveSlide(1)">&#10095;</button>
  </div>
</section>

<script>
let currentIndex = 0;
const images = document.querySelectorAll(".carousel-images img");
const totalImages = images.length;

function moveSlide(step) {
  currentIndex += step;
  if (currentIndex < 0) currentIndex = totalImages - 1;
  else if (currentIndex >= totalImages) currentIndex = 0;
  const newTransformValue = -100 * currentIndex + '%';
  document.querySelector(".carousel-images").style.transform = `translateX(${newTransformValue})`;
}
setInterval(() => moveSlide(1), 10000);
</script>
