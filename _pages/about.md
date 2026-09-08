---
layout: about
title: about
permalink: /
subtitle: Georgia Tech. School of Electrical and Computer Engineering

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>TSRB 419</p>
    <p>Technology Square Research Building, 85 5th St NW</p>
    <p> Atlanta, GA 30332</p>

selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: true # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: true
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---
<div style="font-size:1.1rem;margin-bottom:1.5rem;color:#2c5f7c;">
  <span id="tw"></span><span id="cursor">|</span>
</div>

<script>
(function () {
  const words = ["Biomedical Engineering", "Wearable Sensing", "Neuromodulation"];
  const el = document.getElementById("tw");
  const cur = document.getElementById("cursor");
  if (window.matchMedia("(prefers-reduced-motion: reduce)").matches) {
    el.textContent = words[0];
    return;
  }
  setInterval(() => { cur.style.opacity = cur.style.opacity === "0" ? "1" : "0"; }, 530);
  let w = 0, c = 0, deleting = false;
  (function tick() {
    const word = words[w];
    c = deleting ? c - 1 : c + 1;
    el.textContent = word.slice(0, c);
    let wait = deleting ? 50 : 110;
    if (!deleting && c === word.length) { deleting = true; wait = 1600; }
    else if (deleting && c === 0) { deleting = false; w = (w + 1) % words.length; wait = 350; }
    setTimeout(tick, wait);
  })();
})();
</script>
Hi, I am a postdoctoral fellow at the [Inan Research Lab](https://irl.gatech.edu/) at Georgia Tech, advised by [Prof. Omer T. Inan](https://ece.gatech.edu/directory/omer-t-inan).

