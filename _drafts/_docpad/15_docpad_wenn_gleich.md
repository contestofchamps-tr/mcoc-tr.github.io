---
layout: page
icon: docpad.png
title: "Gib keinen Inhalt aus, wenn gleich..."
teaser: "Der Inhalt innerhalb der IF-Anweisung wird *nicht* ausgegeben, wenn der Dokumententitel auf »Phlow UX Design«"
tags:
  - docpad
---
<pre><code class="lang-ruby">
<%= if @document.title is "Phlow UX Design" then "" else "#{@document.title}" %>
</code></pre>
