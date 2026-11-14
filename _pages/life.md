---
layout: page
permalink: /life/
title: life journey
description: Life is fleeting, and I am but a traveler.
nav: true
nav_title: life # shorter label for the navbar; the page keeps the full title
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

<div class="life-trail" aria-hidden="true">
  <svg width="300" height="52" viewBox="0 0 300 52">
    <defs>
      <mask id="life-trail-mask" maskUnits="userSpaceOnUse" x="0" y="0" width="300" height="52">
        <path class="life-trail-reveal" d="M 4 40 C 24 40, 34 24, 56 24 S 86 44, 108 44 S 140 22, 164 22 S 196 40, 218 40 S 252 28, 276 30" pathLength="1"></path>
      </mask>
    </defs>
    <path class="life-trail-path" d="M 4 40 C 24 40, 34 24, 56 24 S 86 44, 108 44 S 140 22, 164 22 S 196 40, 218 40 S 252 28, 276 30" mask="url(#life-trail-mask)"></path>
    <!-- feet at the origin, facing right, a small pack on the back -->
    <g class="life-trail-traveler" transform="translate(276 30)">
      <circle cx="0.8" cy="-15" r="2.3"></circle>
      <rect x="-3.6" y="-12" width="2.6" height="4.8" rx="0.9"></rect>
      <line x1="0" y1="-12.2" x2="0" y2="-6.4"></line>
      <line data-swing="-18" x1="0" y1="-11.4" x2="0" y2="-7.2"></line>
      <line data-swing="18" x1="0" y1="-11.4" x2="0" y2="-7.2"></line>
      <line data-swing="28" x1="0" y1="-6.4" x2="0" y2="0"></line>
      <line data-swing="-28" x1="0" y1="-6.4" x2="0" y2="0"></line>
    </g>
  </svg>
</div>

Outside of research, I find joy in hiking and basketball, and in the ordinary hours a life is mostly made of.

**Hiking:** :sunrise_over_mountains: chasing lakes, sunsets, and sunrises.

**Basketball:** :basketball: a James Harden fan for the past <span data-since="2015">{{ site.time | date: "%Y" | minus: 2015 }}</span> years.

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

<p class="life-coda">And the road goes on.</p>

<style>
/* the epigraph, its trail, and the closing line share one quiet voice: the
   title's serif in its true italic, in a grey softer than the body text
   (one per theme, both comfortably legible) */
.post-description,
.life-trail,
.life-coda {
  font-family: "Crimson Pro", Georgia, "Times New Roman", serif;
  font-style: italic;
  font-weight: 400;
  letter-spacing: 0.01em;
  color: #6b6b6b;
}
html[data-theme="dark"] .post-description,
html[data-theme="dark"] .life-trail,
html[data-theme="dark"] .life-coda {
  color: #a0a0a0;
}
.post-description {
  font-size: 1.3rem;
  line-height: 1.45;
  margin-top: 0.3rem;
  margin-bottom: 0.4rem;
}
.life-trail {
  line-height: 0;
  margin-bottom: 1.2rem;
}
.life-trail svg {
  display: block;
  width: 100%;
  max-width: 300px;
  height: auto;
  overflow: visible;
}
.life-trail-path {
  fill: none;
  stroke: currentColor;
  stroke-width: 2;
  stroke-linecap: round;
  /* round caps on near-zero dashes: a line of footprints */
  stroke-dasharray: 0.1 7;
}
/* the trail shows only where this solid stroke is drawn; animating its
   dash offset unrolls the footprints along the path */
.life-trail-reveal {
  fill: none;
  stroke: #fff;
  stroke-width: 8;
  stroke-dasharray: 1;
}
.life-trail-traveler {
  color: var(--global-theme-color);
}
.life-trail-traveler line {
  stroke: currentColor;
  stroke-width: 1.6;
  stroke-linecap: round;
}
.life-trail-traveler circle,
.life-trail-traveler rect {
  fill: currentColor;
}
/* limbs are vertical lines, so the top of their box is the hip/shoulder */
.life-trail-traveler [data-swing] {
  transform-box: fill-box;
  transform-origin: 50% 0%;
}
.life-coda {
  font-size: 1.15rem;
  text-align: center;
  margin: 2.5rem 0 0.5rem;
}
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
/* the wide lake photo drifts very slowly, like time passing while you look.
   The motion is on <picture>, not the img: medium-zoom and the hover lift
   both transform the img, and an animation would override them. The
   figure clips the drift and carries the frame the img normally has. */
.life-gallery .life-feature figure:first-child {
  overflow: hidden;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
}
html[data-theme="dark"] .life-gallery .life-feature figure:first-child {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.4);
}
.life-feature figure:first-child picture {
  display: block;
  transform-origin: 60% 55%;
  will-change: transform;
  animation: lake-drift 36s ease-in-out infinite alternate;
}
.life-gallery .life-feature figure:first-child img,
.life-gallery .life-feature figure:first-child img:hover {
  box-shadow: none;
  transform: none;
}
@keyframes lake-drift {
  from {
    transform: scale(1);
  }
  to {
    transform: scale(1.07) translate(-1.2%, 0.6%);
  }
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
/* "Life is fleeting, and I am but a traveler": the epigraph surfaces word
   by word, and photos drift into place as they come into view, like scenery
   passing on a journey. The script below adds these classes only when motion
   is welcome, so without it everything simply shows. */
.epigraph-word {
  /* the theme colours every span directly; keep the epigraph's grey */
  color: inherit;
  display: inline-block;
  opacity: 0;
  filter: blur(4px);
  transform: translateY(0.3em);
  animation: epigraph-word 1.2s ease-out forwards;
}
@keyframes epigraph-word {
  to {
    opacity: 1;
    filter: blur(0);
    transform: none;
  }
}
.life-gallery figure.life-reveal {
  opacity: 0;
  transform: translateY(1.25rem);
  transition:
    opacity 1s ease,
    transform 1s ease;
}
.life-gallery figure.life-reveal.is-visible {
  opacity: 1;
  transform: none;
}
.life-coda {
  transition:
    opacity 1.8s ease,
    transform 1.8s ease,
    filter 1.8s ease;
}
.life-coda.is-waiting {
  opacity: 0;
  transform: translateY(0.5rem);
  filter: blur(3px);
}
@media (prefers-reduced-motion: reduce) {
  .life-gallery img,
  .life-gallery img:hover {
    transition: none;
    transform: none;
  }
  .life-feature figure:first-child picture {
    animation: none;
  }
}
</style>

<script>
  (function () {
    /* years counted from data-since, so the count stays current between
       deploys (the build already filled in the value as of its own date) */
    document.querySelectorAll("[data-since]").forEach(function (el) {
      el.textContent = new Date().getFullYear() - Number(el.getAttribute("data-since"));
    });

    if (window.matchMedia("(prefers-reduced-motion: reduce)").matches) return;

    /* the epigraph surfaces one word at a time */
    var epigraph = document.querySelector(".post-description");
    if (epigraph) {
      var words = epigraph.textContent.trim().split(/\s+/);
      epigraph.textContent = "";
      words.forEach(function (word, i) {
        var span = document.createElement("span");
        span.className = "epigraph-word";
        span.textContent = word;
        span.style.animationDelay = 0.3 + i * 0.16 + "s";
        epigraph.appendChild(span);
        if (i < words.length - 1) epigraph.appendChild(document.createTextNode(" "));
      });
    }

    /* a traveler walks the trail beneath the epigraph, leaving footprints.
       Driven by the Web Animations API so the browser runs it like the CSS
       animations: the traveler follows points sampled evenly along the path,
       and the footprints unroll in step under the same timing. */
    var trail = document.querySelector(".life-trail");
    if (trail && trail.animate) {
      var path = trail.querySelector(".life-trail-path");
      var reveal = trail.querySelector(".life-trail-reveal");
      var traveler = trail.querySelector(".life-trail-traveler");
      var length = path.getTotalLength();
      var steps = [];
      for (var n = 0; n <= 40; n++) {
        var point = path.getPointAtLength((length * n) / 40);
        steps.push({ transform: "translate(" + point.x + "px, " + point.y + "px)" });
      }
      var walk = { duration: 5200, delay: 1900, easing: "ease-in-out", fill: "both" };
      traveler.animate(steps, walk);
      traveler.animate([{ opacity: 0 }, { opacity: 1 }], { duration: 600, delay: 1900, fill: "both" });
      reveal.animate([{ strokeDashoffset: 1 }, { strokeDashoffset: 0 }], walk);
      /* arms and legs swing for exactly the length of the walk, then the
         traveler stands still where the trail ends */
      var stride = { duration: 520, delay: 1900, iterations: 10, direction: "alternate", easing: "ease-in-out" };
      trail.querySelectorAll("[data-swing]").forEach(function (limb) {
        var angle = Number(limb.getAttribute("data-swing"));
        limb.animate([{ transform: "rotate(" + angle + "deg)" }, { transform: "rotate(" + -angle + "deg)" }], stride);
      });
    }

    /* photos drift into place as they scroll into view, a few at a time */
    if (!("IntersectionObserver" in window)) return;
    var observer = new IntersectionObserver(
      function (entries) {
        var shown = 0;
        entries.forEach(function (entry) {
          if (!entry.isIntersecting) return;
          entry.target.style.transitionDelay = shown++ * 90 + "ms";
          entry.target.classList.add("is-visible");
          observer.unobserve(entry.target);
        });
      },
      { rootMargin: "0px 0px -8% 0px" }
    );
    document.querySelectorAll(".life-gallery figure").forEach(function (figure) {
      figure.classList.add("life-reveal");
      observer.observe(figure);
    });

    /* the closing line lingers into view once the reader reaches the end */
    var coda = document.querySelector(".life-coda");
    if (coda) {
      coda.classList.add("is-waiting");
      var codaObserver = new IntersectionObserver(
        function (entries) {
          if (!entries[0].isIntersecting) return;
          setTimeout(function () {
            coda.classList.remove("is-waiting");
          }, 300);
          codaObserver.unobserve(coda);
        },
        { threshold: 1 }
      );
      codaObserver.observe(coda);
    }
  })();
</script>
