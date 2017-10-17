---
layout: page
icon: docpad.png
title: "RSS-Feeds mit Feedr-Plugin parsen und ausgeben"
teaser: "Um mit dem DocPad-Plugin namens Feedr RSS-Feeds auszugeben, benutzt man das untere Code-Schnipsel."
tags:
  - docpad
  - feedr plugin
---
## Schritt 1 – Installieren und konfigurieren

Zuerst muss man das [DocPad-Plugin Feedr][1] mit `docpad install feedr` installieren. Anschließend fügt man z.B. das untere Code-Schnipsel in die *Konfigurationsdatei (docpad.coffee)* ein, um den RSS-Feed zu definieren...

<pre><code class="lang-ruby">
    plugins:
        feedr:
            feeds:
                phlow:
                    url: "http://mo.phlow.de/feed/"
</code></pre>

## Schritt 2 In Layout-Dokument einfügen

...und anschließend in einem Layout-Dokument über den folgenden Code auszugeben.

<pre><code class="lang-ruby">
<h1><a href="<%- @feedr.feeds.phlow.channel.link %>"><%= @feedr.feeds.phlow.channel.title %></a></h1>
<p><%= @feedr.feeds.phlow.channel.description %></p>

<ul>
    <% for item in @feedr.feeds.phlow.channel.item: %>
        <li><a href="<%= item.link %>"><%= item.title %></a> - <%- item.description %></li>
    <% end %>
</ul>
</code></pre>




[1]: https://github.com/docpad/docpad-plugin-feedr/