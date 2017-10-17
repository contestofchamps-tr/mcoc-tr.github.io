---
layout: page
icon: docpad.png
title: "For-Schleife um durch Array zu iterieren"
teaser: "Mit dieser For-Schleife generiert man aus einem Array aus den Frontmatter-Metadaten eine Gallery"
tags:
  - docpad
  - "multiple images"
  - gallery
---

<pre><code class="lang-html">
image:
    - image1.jpg
    - image2.jpg
    - image3.jpg
    - image4.jpg
    - image5.jpg
</code></pre>

Der Code der For-Schleife, um aus den Bilddateien eine Gallerie zu erzeugen.

<pre><code class="lang-ruby">
<ul>
  <% for image, i in @document.image: %>
    <li>
      <img src="<%- "#{image}" %>" />
    </li>
  <% end %>
</ul>
</code></pre>


