---
layout: about
title: about
permalink: /
subtitle: PhD student at the <a href='https://computerscience.emory.edu/index.html'>Computer Science Department, Emory University</a>, advised by <a href='https://www.cs.emory.edu/~wjin30//lab/'>Prof. Wei Jin</a>

profile:
  align: right
  image: Bohan_Wang.jpg
  image_circular: false # crops the image to make it circular
  # more_info: >
  #   <p>Email: bohan.wang2@emory.edu</p>

selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: true # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

**Research Interests:** Graph Neural Networks (GNNs), Graph Generation, Time Series Analysis, and Foundation Models.

**Prior Experience:** I received my Master's degree from [École Polytechnique Fédérale de Lausanne (EPFL)](https://www.epfl.ch/en/), completing my thesis at [ETH Zurich](https://ethz.ch/en.html) under the co-supervision of [Prof. Pascal Frossard](https://people.epfl.ch/pascal.frossard) and [Prof. Roger Wattenhofer](https://disco.ethz.ch/members/wroger). I have also served as a research intern at EPFL's [Signal Processing Laboratory](https://www.epfl.ch/labs/lts4/) and as a research assistant at the [Pennsylvania State University](https://www.psu.edu/) with [Prof. Lu Lin](https://louise-lulin.github.io/).

**Research Journey:** My research has touched multiple data modalities: Computer Vision :framed_picture:, Audio ML :studio_microphone:, Graph Generation :dna:, and now Time Series :chart_with_upwards_trend:. I am always excited to learn new things.

<h2 style="clear: both">academic journey</h2>

<div class="study-journey">
  <div class="journey-track">
    <div class="journey-stop">
      <div class="journey-photo">
        <img src="{{ '/assets/img/china.jpg' | relative_url }}" alt="China">
      </div>
      <div class="journey-info">
        <div class="journey-country">China :cn:</div>
        <div class="journey-place">Hometown</div>
      </div>
    </div>

    <div class="journey-stop">
      <div class="journey-photo">
        <img src="{{ '/assets/img/england.jpg' | relative_url }}" alt="England">
      </div>
      <div class="journey-info">
        <div class="journey-country">England :gb:</div>
        <div class="journey-place">Nottingham, UK</div>
      </div>
    </div>

    <div class="journey-stop">
      <div class="journey-photo">
        <img src="{{ '/assets/img/switzerland.jpg' | relative_url }}" alt="Switzerland">
      </div>
      <div class="journey-info">
        <div class="journey-country">Switzerland :switzerland:</div>
        <div class="journey-place">EPFL · ETH Zurich</div>
      </div>
    </div>

    <div class="journey-stop">
      <div class="journey-photo">
        <img src="{{ '/assets/img/USA.jpg' | relative_url }}" alt="USA">
      </div>
      <div class="journey-info">
        <div class="journey-country">USA :us:</div>
        <div class="journey-place">Emory University</div>
      </div>
    </div>
  </div>
</div>

<style>
.study-journey { margin: 0 0 2rem; }

.journey-track {
  display: flex;
  align-items: stretch;
  justify-content: space-between;
  gap: 0.55rem;
}

.journey-stop {
  flex: 1 1 0;
  min-width: 0;
  display: flex;
  flex-direction: column;
  text-align: center;
  transition: transform 0.35s ease;
}

.journey-stop:hover { transform: translateY(-6px); }

.journey-photo {
  position: relative;
  width: 100%;
  aspect-ratio: 4 / 5;
  border-radius: 14px;
  overflow: hidden;
  box-shadow: 0 4px 14px rgba(0, 0, 0, 0.10);
  transition: box-shadow 0.35s ease;
}

.journey-stop:hover .journey-photo {
  box-shadow: 0 14px 28px rgba(0, 0, 0, 0.18);
}

.journey-photo::after {
  content: "";
  position: absolute;
  inset: 0;
  background: linear-gradient(to top, rgba(0, 0, 0, 0.20), transparent 45%);
  pointer-events: none;
}

.journey-photo img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
  transition: transform 0.6s ease;
}

.journey-stop:hover .journey-photo img { transform: scale(1.06); }

.journey-info { margin-top: 0.7rem; }

.journey-country {
  font-size: 1.05rem;
  font-weight: 600;
  letter-spacing: 0.02em;
  color: var(--global-text-color);
}

.journey-place {
  font-size: 0.82rem;
  color: var(--global-text-color-light);
  margin-top: 0.2rem;
  line-height: 1.35;
}

@media (max-width: 768px) {
  .journey-track {
    flex-direction: column;
    gap: 0.85rem;
  }
  .journey-stop {
    flex-direction: row;
    text-align: left;
    align-items: center;
    gap: 1rem;
  }
  .journey-stop:hover { transform: translateX(4px); }
  .journey-photo {
    flex: 0 0 38%;
    aspect-ratio: 1 / 1;
  }
  .journey-info { flex: 1; margin-top: 0; }
  .journey-country { font-size: 1.1rem; }
  .journey-place { font-size: 0.88rem; }
}

/* Internship journey: stacked vertical layout */
.internship-journey .journey-track {
  flex-direction: column;
  gap: 1rem;
  align-items: flex-start;
}
.internship-journey .journey-stop {
  flex-direction: row;
  align-items: center;
  text-align: left;
  gap: 1.2rem;
  width: 100%;
  max-width: 480px;
}
.internship-journey .journey-stop:hover {
  transform: translateX(4px);
}
.internship-journey .journey-photo {
  flex: 0 0 110px;
  aspect-ratio: 1 / 1;
  background: transparent;
  display: flex;
  align-items: center;
  justify-content: center;
}
.internship-journey .journey-photo::after { display: none; }
.internship-journey .journey-photo img {
  width: 100%;
  height: 100%;
  object-fit: contain;
  transition: transform 0.6s ease;
}
.internship-journey .journey-stop:hover .journey-photo img {
  transform: scale(1.06);
}
.internship-journey .journey-info {
  flex: 1;
  margin-top: 0;
  text-align: left;
}
.internship-journey .journey-years {
  font-size: 0.78rem;
  color: var(--global-text-color-light);
  margin-top: 0.2rem;
  letter-spacing: 0.03em;
}
</style>

<h2 style="clear: both">internship journey</h2>

<div class="study-journey internship-journey">
  <div class="journey-track">
    <div class="journey-stop">
      <div class="journey-photo">
        <img src="{{ '/assets/img/tiktok.png' | relative_url }}" alt="TikTok">
      </div>
      <div class="journey-info">
        <div class="journey-country">TikTok</div>
        <div class="journey-place">Machine Learning Engineer · San Jose, CA, USA</div>
        <div class="journey-years">May 2026 – Present</div>
      </div>
    </div>

    <div class="journey-stop">
      <div class="journey-photo">
        <img src="{{ '/assets/img/logitech.png' | relative_url }}" alt="Logitech">
      </div>
      <div class="journey-info">
        <div class="journey-country">Logitech</div>
        <div class="journey-place">Machine Learning Intern (Audio) · Lausanne, Switzerland</div>
        <div class="journey-years">Sep 2022 – Mar 2023</div>
      </div>
    </div>
  </div>
</div>

<h2>services</h2>

- **Web Chair**, [KDD'26 Workshop on SciSoc Agents & LLMs](https://kdd26scisocllm.github.io/)


<!-- Write your biography here. Tell the world about yourself. Link to your favorite [subreddit](http://reddit.com). You can put a picture in, too. The code is already in, just name your picture `prof_pic.jpg` and put it in the `img/` folder.

Put your address / P.O. box / other info right below your picture. You can also disable any of these elements by editing `profile` property of the YAML header of your `_pages/about.md`. Edit `_bibliography/papers.bib` and Jekyll will render your [publications page](/al-folio/publications/) automatically.

Link to your social media connections, too. This theme is set up to use [Font Awesome icons](https://fontawesome.com/) and [Academicons](https://jpswalsh.github.io/academicons/), like the ones below. Add your Facebook, Twitter, LinkedIn, Google Scholar, or just disable all of them. -->
