---
layout: page
icon: docpad.png
title: "Gib Inhalt aus, wenn vorhanden"
teaser: "Der Inhalt innerhalb der IF-Anweisung wird nur ausgegeben, wenn die jeweiligen Metadaten vorhanden sind. Der Inhalt zwischen if und end im unteren Beispiel, wird nur ausgegeben, wenn es Metadaten zum Wert thumbnail gibt."
tags:
  - docpad
---
<pre><code class="lang-ruby">
<% if @document.thumbnail: %>
    <img src="/images/<%= @document.thumbnail %>" alt="">
<% end %>
</code></pre>
