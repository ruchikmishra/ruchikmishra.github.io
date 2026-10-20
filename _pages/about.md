---
layout: about
title: About
permalink: /
subtitle: Postdoctoral Fellow, <a href='https://irl.gatech.edu/'>Inan Research Lab</a>, Georgia Institute of Technology

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  # Icon links and the typing line under the photo.
  # Icons: Font Awesome (fa-*) and Academicons (ai-*).
  # To change the typed words, edit the WORDS list in the script below.
  more_info: |
    <div style="display:flex; justify-content:center; gap:1rem; font-size:1.35rem; margin-top:0.5rem;">
      <a href="mailto:rmishra92@gatech.edu" title="Email" aria-label="Email"><i class="fa-solid fa-envelope"></i></a>
      <a href="https://scholar.google.com/citations?user=9buTD38AAAAJ&hl=en" title="Google Scholar" aria-label="Google Scholar" target="_blank" rel="noopener"><i class="ai ai-google-scholar"></i></a>
      <a href="/assets/pdf/Ruchik_CV.pdf" title="CV" aria-label="CV" target="_blank" rel="noopener"><i class="ai ai-cv"></i></a>
      <a href="https://github.com/ruchikmishra" title="GitHub" aria-label="GitHub" target="_blank" rel="noopener"><i class="fa-brands fa-github"></i></a>
      <a href="https://www.linkedin.com/in/ruchik-mishra-a3843a133/" title="LinkedIn" aria-label="LinkedIn" target="_blank" rel="noopener"><i class="fa-brands fa-linkedin"></i></a>
    </div>
    <style>
      .post h2::first-letter { text-transform: uppercase; }
      .typer { text-align: center; margin-top: 0.6rem; min-height: 1.5em; font-family: monospace; font-size: 0.95rem; }
      .typer-caret { display: inline-block; margin-left: 1px; animation: typer-blink 1s steps(1) infinite; }
      @keyframes typer-blink { 50% { opacity: 0; } }
      @media (prefers-reduced-motion: reduce) { .typer-caret { display: none; } }
    </style>
    <div class="typer">
      <span aria-hidden="true">Loves </span><span class="typer-word" aria-hidden="true"></span><span class="typer-caret" aria-hidden="true">|</span>
      <span class="typer-sr" style="position:absolute; width:1px; height:1px; overflow:hidden; clip:rect(0 0 0 0);"></span>
    </div>
    <script>
      (function () {
        var WORDS = ["Research", "Table Tennis", "Food", "Cooking"];
        var TYPE_MS = 90, DELETE_MS = 40, HOLD_MS = 1400, GAP_MS = 300;
        var box = document.currentScript.previousElementSibling;
        var out = box.querySelector(".typer-word");
        box.querySelector(".typer-sr").textContent = "Loves " + WORDS.join(", ");
        if (window.matchMedia && window.matchMedia("(prefers-reduced-motion: reduce)").matches) {
          out.textContent = WORDS.join(", ");
          return;
        }
        var w = 0, i = 0, deleting = false;
        function tick() {
          var word = WORDS[w];
          if (!deleting) {
            i++;
            out.textContent = word.slice(0, i);
            if (i === word.length) { deleting = true; return setTimeout(tick, HOLD_MS); }
            return setTimeout(tick, TYPE_MS);
          }
          i--;
          out.textContent = word.slice(0, i);
          if (i === 0) { deleting = false; w = (w + 1) % WORDS.length; return setTimeout(tick, GAP_MS); }
          setTimeout(tick, DELETE_MS);
        }
        tick();
      })();
    </script>

selected_papers: true # lists papers marked selected={true} in _bibliography/papers.bib
social: false # icons now sit under the photo; set true to also show them at the bottom

announcements:
  enabled: true # shows items from the _news folder
  scrollable: true # shows `visible` items, then a scroll bar for the rest
  visible: 4
  limit: # leave blank to include every news item in the scroll list

latest_posts:
  enabled: false
---

<!-- DRAFT: edit these paragraphs in your own words. -->

I am a postdoctoral fellow in the School of Electrical and Computer Engineering at the Georgia Institute of Technology, working with [Prof. Omer T. Inan](https://www.ece.gatech.edu/directory/omer-t-inan) in the [Inan Research Lab](https://irl.gatech.edu/).

I currently develop a translational pipeline for wearable joint acoustics, aimed at bringing joint-health assessment from the clinic into the home. My work focuses on children with juvenile idiopathic arthritis (JIA), where I use the sounds a knee makes as it moves, recorded by a wearable device, to predict disease activity. The goal is objective, at-home monitoring that can capture changes in joint health between clinic visits.

More broadly, my research aims to make health data collected outside the clinic reliable enough to act on. I combine multimodal wearable sensing and machine learning to turn physiological signals into interpretable information about a person's changing health, accounting for factors such as sensor placement and differences in anatomy that can mask true changes.

I received my Ph.D. in Electrical Engineering from the University of Louisville in 2025, advised by Dr. Dan O. Popa and Dr. Karla Conn Welch. My dissertation developed multimodal emotion recognition for human–robot interaction across neurodiverse populations, including children with autism. I earned my B.E. (Honors) in Manufacturing Engineering from BITS Pilani, Hyderabad.
