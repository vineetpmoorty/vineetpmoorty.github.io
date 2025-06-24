---
layout: about
title: about
permalink: /
subtitle: >
  <div style="font-size: 1em; color: #666;">🔊 <em>Vin-eet Poon-yuh-moor-tee</em></div><br>

profile:
  align: right
  image: vineet_photo.jpg
  image_circular: true # crops the image to make it circular
  more_info: >
    <p>West Lafayette, IN 47906 United States</p>
    <p id="email"></p>
    <script>
      const user = "vineetpmoorty";
      const domain = "gmail.com";
      const link = `mailto:${user}@${domain}`;
      document.getElementById("email").innerHTML = `<a href="${link}">${user}@${domain}</a>`;
    </script>
    <p>
      <a href="https://github.com/vineetpmoorty" target="_blank">
        <i class="fab fa-github"></i> GitHub
      </a><br>
      <a href="https://scholar.google.com/citations?user=JLH9zs8AAAAJ" target="_blank">
        <i class="ai ai-google-scholar"></i> Google Scholar
      </a>
    </p>

selected_papers: false # includes a list of papers marked as "selected={true}"
social: false # includes social icons at the bottom of the page

announcements:
  enabled: true # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

Hi, I'm Vineet. I am a PhD student in Machine Learning at <a href="https://engineering.purdue.edu/ECE">Purdue ECE</a>. My research broadly focuses on **multimodal learning**, **computer vision**, and **generative models**.

I’ve worked on contrastive learning for time-series data, adaptive planning with diffusion models, and multimodal learning for cardiac assessment. I'm excited by the transformative potential of AI in healthcare, targeted drug design, scientific discovery and a wide range of other fields.

Explore this site to learn more about my work, or take a look at my <a href="/cv/">resume</a>.