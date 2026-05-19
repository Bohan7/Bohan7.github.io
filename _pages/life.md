---
layout: page
permalink: /life/
title: life
nav: true
nav_order: 4
---

Outside of research, I find joy in hiking and basketball, and in the small moments in between.

**Hiking:** :sunrise_over_mountains: chasing lakes, sunsets, and sunrises.

**Basketball:** :basketball: a James Harden fan for the past 10 years.

<div class="life-gallery">
  <img src="{{ '/assets/img/life/photo_1.jpg' | relative_url }}" alt="Life moment 1" loading="lazy">
  <img src="{{ '/assets/img/life/photo_2.jpg' | relative_url }}" alt="Life moment 2" loading="lazy">
  <img src="{{ '/assets/img/life/photo_3.jpg' | relative_url }}" alt="Life moment 3" loading="lazy">
  <img src="{{ '/assets/img/life/photo_4.jpg' | relative_url }}" alt="Life moment 4" loading="lazy">
  <img src="{{ '/assets/img/life/photo_5.jpg' | relative_url }}" alt="Life moment 5" loading="lazy">
  <img src="{{ '/assets/img/life/photo_6.jpg' | relative_url }}" alt="Life moment 6" loading="lazy">
  <img src="{{ '/assets/img/life/photo_7.jpg' | relative_url }}" alt="Life moment 7" loading="lazy">
  <img src="{{ '/assets/img/life/photo_8.jpg' | relative_url }}" alt="Life moment 8" loading="lazy">
  <img src="{{ '/assets/img/life/photo_9.jpg' | relative_url }}" alt="Life moment 9" loading="lazy">
  <img src="{{ '/assets/img/life/photo_10.jpg' | relative_url }}" alt="Life moment 10" loading="lazy">
  <img src="{{ '/assets/img/life/photo_11.jpg' | relative_url }}" alt="Life moment 11" loading="lazy">
  <img src="{{ '/assets/img/life/photo_12.jpg' | relative_url }}" alt="Life moment 12" loading="lazy">
  <img src="{{ '/assets/img/life/photo_13.jpg' | relative_url }}" alt="Life moment 13" loading="lazy">
</div>

<style>
.life-gallery {
  column-count: 3;
  column-gap: 0.7rem;
  margin-top: 2.5rem;
}
.life-gallery img {
  width: 100%;
  margin-bottom: 0.7rem;
  border-radius: 8px;
  break-inside: avoid;
  display: block;
  cursor: zoom-in;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
  transition: transform 0.4s ease, box-shadow 0.4s ease;
}
.life-gallery img:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 18px rgba(0, 0, 0, 0.15);
}
@media (max-width: 768px) {
  .life-gallery { column-count: 2; column-gap: 0.5rem; }
  .life-gallery img { margin-bottom: 0.5rem; }
}
@media (max-width: 480px) {
  .life-gallery { column-count: 1; }
}
</style>
