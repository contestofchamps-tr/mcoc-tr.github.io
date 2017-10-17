---
layout: page
icon: docpad.png
title: "Inhalt filtern nach Tags"
teaser: "Code-Schnipsel für DocPad, das sämtliche Dokumente durchsucht und die Dokumente zurückgibt, die mit dem Tag Journalismus versehen wurden."
tags:
  - docpad
---
<pre><code class="lang-ruby">
<ul>
<% for doc in @getCollection('documents').findAll({tags: '$in': 'journalismus'}).toJSON(): %>
    <li><a href="<%= doc.url %>"><%= doc.title %></a></li>
<% end %>
</ul>
</code></pre>