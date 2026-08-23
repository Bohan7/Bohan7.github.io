---
layout: page
permalink: /life/
title: life
nav: true
nav_order: 4
photos:
  - { file: photo_1.jpg, w: 1200, h: 1600, alt: Life moment 1 }
  - { file: photo_2.jpg, w: 1600, h: 1066, alt: Life moment 2 }
  - { file: photo_3.jpg, w: 1200, h: 1600, alt: Life moment 3 }
  - { file: photo_4.jpg, w: 1200, h: 1600, alt: Life moment 4 }
  - { file: photo_14.jpg, w: 1500, h: 2000, alt: Green coastal meadow under a wide blue sky }
  - { file: photo_5.jpg, w: 1200, h: 1600, alt: Life moment 5 }
  - { file: photo_6.jpg, w: 1600, h: 1521, alt: Life moment 6 }
  - { file: photo_7.jpg, w: 1200, h: 1600, alt: Life moment 7 }
  - { file: photo_8.jpg, w: 1200, h: 1600, alt: Life moment 8 }
  - { file: photo_9.jpg, w: 1600, h: 736, alt: Life moment 9 }
  - { file: photo_15.jpg, w: 1500, h: 2000, alt: Sunset over the ocean from a coastal bluff }
  - { file: photo_10.jpg, w: 1440, h: 1080, alt: Life moment 10 }
  - { file: photo_11.jpg, w: 1080, h: 1440, alt: Life moment 11 }
  - { file: photo_12.jpg, w: 1080, h: 1080, alt: Life moment 12 }
  - { file: photo_13.jpg, w: 1440, h: 1080, alt: Life moment 13 }
  - { file: photo_16.jpg, w: 1500, h: 2000, alt: Late afternoon sun breaking through clouds above the sea }
---

Outside of research, I find joy in hiking and basketball, and in the ordinary hours a life is mostly made of.

**Hiking:** :sunrise_over_mountains: chasing lakes, sunsets, and sunrises.

**Basketball:** :basketball: a James Harden fan for the past 10 years.

<div class="life-gallery">
  {% for photo in page.photos %}
    {% assign stem = photo.file | split: '.' | first %}
    {% capture base %}{{ '/assets/img/life/' | append: stem | relative_url }}{% endcapture %}
    <figure>
      <picture>
        <source
          type="image/webp"
          srcset="{% for w in site.imagemagick.widths %}{{ base }}-{{ w }}.webp {{ w }}w{% unless forloop.last %}, {% endunless %}{% endfor %}"
          sizes="(max-width: 480px) 92vw, (max-width: 768px) 46vw, 31vw"
        >
        <img
          src="{{ '/assets/img/life/' | append: photo.file | relative_url }}"
          width="{{ photo.w }}"
          height="{{ photo.h }}"
          alt="{{ photo.alt }}"
          loading="lazy"
          decoding="async"
          data-zoomable
        >
      </picture>
    </figure>
  {% endfor %}
</div>

<style>
.life-gallery {
  column-count: 3;
  column-gap: 0.7rem;
  column-fill: balance;
  margin-top: 2.5rem;
}
.life-gallery figure {
  break-inside: avoid;
  margin: 0 0 0.7rem;
  /* keeps the whole card, shadow included, from being sliced across columns */
  display: inline-block;
  width: 100%;
}
.life-gallery img {
  width: 100%;
  height: auto;
  border-radius: 8px;
  display: block;
  cursor: zoom-in;
  background-color: var(--global-bg-color);
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
  transition:
    transform 0.4s ease,
    box-shadow 0.4s ease;
}
.life-gallery img:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 18px rgba(0, 0, 0, 0.15);
}
html[data-theme="dark"] .life-gallery img {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.4);
}
html[data-theme="dark"] .life-gallery img:hover {
  box-shadow: 0 8px 18px rgba(0, 0, 0, 0.55);
}
@media (max-width: 768px) {
  .life-gallery {
    column-count: 2;
    column-gap: 0.5rem;
  }
  .life-gallery figure {
    margin-bottom: 0.5rem;
  }
}
@media (max-width: 480px) {
  .life-gallery {
    column-count: 1;
  }
}
@media (prefers-reduced-motion: reduce) {
  .life-gallery img,
  .life-gallery img:hover {
    transition: none;
    transform: none;
  }
}
</style>
