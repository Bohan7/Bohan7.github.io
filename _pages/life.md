---
layout: page
permalink: /life/
title: life
nav: true
nav_order: 4
featured:
  # One row above the columns, on the same three-column grid: the first
  # photo spans two columns, the second fills the third at the same
  # height (it is cropped to fit, so pick one of nearly that shape).
  - { file: photo_9.jpg, w: 1600, h: 736, alt: Life moment 9 }
  - { file: photo_6.jpg, w: 1600, h: 1521, alt: Life moment 6 }
photos:
  # Ordered as three height-balanced groups (see the gallery comment
  # below): column 1, then column 2, then column 3.
  # -- column 1
  - { file: photo_1.jpg, w: 1200, h: 1600, alt: Life moment 1 }
  - { file: photo_14.jpg, w: 1500, h: 2000, alt: Green coastal meadow under a wide blue sky }
  - { file: photo_7.jpg, w: 1200, h: 1600, alt: Life moment 7 }
  - { file: photo_8.jpg, w: 1200, h: 1600, alt: Life moment 8 }
  - { file: photo_18.jpg, w: 1500, h: 2000, alt: Lake under a clear blue sky framed by autumn foliage }
  # -- column 2
  - { file: photo_3.jpg, w: 1200, h: 1600, alt: Life moment 3 }
  - { file: photo_12.jpg, w: 1080, h: 1080, alt: Life moment 12 }
  - { file: photo_5.jpg, w: 1200, h: 1600, alt: Life moment 5 }
  - { file: photo_2.jpg, w: 1600, h: 1066, alt: Life moment 2 }
  - { file: photo_11.jpg, w: 1080, h: 1440, alt: Life moment 11 }
  - { file: photo_17.jpg, w: 1500, h: 2000, alt: Morning coffee overlooking autumn mountains }
  # -- column 3
  - { file: photo_4.jpg, w: 1200, h: 1600, alt: Life moment 4 }
  - { file: photo_10.jpg, w: 1440, h: 1080, alt: Life moment 10 }
  - { file: photo_15.jpg, w: 1500, h: 2000, alt: Sunset over the ocean from a coastal bluff }
  - { file: photo_13.jpg, w: 1440, h: 1080, alt: Life moment 13 }
  - { file: photo_16.jpg, w: 1500, h: 2000, alt: Late afternoon sun breaking through clouds above the sea }
  - { file: photo_19.jpg, w: 1500, h: 2000, alt: Sunlit forest with picnic tables }
---

Outside of research, I find joy in hiking and basketball, and in the ordinary hours a life is mostly made of.

**Hiking:** :sunrise_over_mountains: chasing lakes, sunsets, and sunrises.

**Basketball:** :basketball: a James Harden fan for the past 10 years.

<div class="life-gallery">
  <div class="life-feature">
    {% for photo in page.featured %}
      <figure style="--ratio: {{ photo.w }} / {{ photo.h }}">
        {% if forloop.first %}
          {% include life_photo.liquid photo=photo sizes="(max-width: 480px) 92vw, (max-width: 960px) 62vw, 600px" %}
        {% else %}
          {% include life_photo.liquid photo=photo sizes="(max-width: 480px) 92vw, 31vw" %}
        {% endif %}
      </figure>
    {% endfor %}
  </div>
  {% for photo in page.photos %}
    <figure>
      {% include life_photo.liquid photo=photo sizes="(max-width: 480px) 92vw, (max-width: 768px) 46vw, 31vw" %}
    </figure>
  {% endfor %}
</div>

<style>
.life-gallery {
  /* CSS multicol fills columns in document order and cannot split an
     image, so column bottoms only line up if the source order already
     balances. page.photos is grouped accordingly - reshuffle those
     groups, not just the list, when adding photos. */
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
/* the featured pair spans every column of the multicol, then lays itself
   out on a matching three-column grid so its edges line up with the
   columns below */
.life-feature {
  column-span: all;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 0.7rem;
  margin-bottom: 0.7rem;
}
.life-gallery .life-feature figure {
  display: block;
  margin: 0;
}
.life-feature figure:first-child {
  grid-column: span 2;
}
/* the partner takes the wide photo's height instead of its own */
.life-feature figure:last-child {
  position: relative;
}
.life-gallery .life-feature figure:last-child img {
  position: absolute;
  inset: 0;
  height: 100%;
  object-fit: cover;
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
  .life-feature {
    gap: 0.5rem;
    margin-bottom: 0.5rem;
  }
}
@media (max-width: 480px) {
  .life-gallery {
    column-count: 1;
  }
  /* single column: stack the pair, each at its own shape */
  .life-feature {
    grid-template-columns: 1fr;
  }
  .life-feature figure:first-child {
    grid-column: auto;
  }
  .life-feature figure:last-child {
    aspect-ratio: var(--ratio);
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
