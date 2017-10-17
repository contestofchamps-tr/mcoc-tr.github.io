---
layout: page
icon: docpad.png
title: "Inhalte eines definierten Ordners ausgeben"
teaser: "Code-Schnipsel für DocPad, das sämtliche Dokumente eines Ordners – hier »Seminare« ausgibt."
tags:
  - docpad
---
<pre><code class="lang-ruby">
<dl>
<% for post in @getFilesAtPath("seminare").toJSON(): %>
    <dt><a href="<%= post.url %>"><%= post.title %></a></dt>
    <dd><%= post.subtitle %> // <%= post.description %></dd>
<% end %>
</dl>
</code></pre>