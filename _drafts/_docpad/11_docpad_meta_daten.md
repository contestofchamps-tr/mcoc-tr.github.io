---
layout: page
icon: docpad.png
title: "Metadaten ausgeben (Pfade, URL, Encoding)"
tags:
  - docpad
---
<pre><code class="lang-javascript">
            <ul>
                <li>Datum: <%= @document.date %></li>
                <li>Quelle: <%= @document.url %></li>
                <li>ID: <%= @document.id %></li>
                <li>Filename: <%= @document.filename %></li>
                <li>Path: <%= @document.path %></li>
                <li>dirPath: <%= @document.dirPath %></li>
                <li>outPath: <%= @document.outPath %></li>
                <li>outDirPath: <%= @document.outDirPath %></li>
                <li>encoding: <%= @document.encoding %></li>
            </ul>
</code></pre>
