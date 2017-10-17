---
layout: page
icon: docpad.png
title: "RSS-Feeds mit DocPad RSS Plugin erzeugen"
tags:
  - docpad
  - rss plugin
---
## Schritt 1: [DocPad RSS Plugin][1] installieren

`npm install --save docpad-plugin-rss`


## Schritt 2: Eine Collection anlegen

<pre><code class="lang-ruby">
aktuelles: ->
	@getCollection("html").findAllLive({relativeOutDirPath: 'aktuelles'})
</code></pre>

## Schritt 3: Das DocPad RSS Plugin konfigurieren

<pre><code class="lang-ruby">
# Important: You have to generate a collection first to use it (here: aktuelles)
rss:
	collection: 'aktuelles'
	url: '/rss.xml' # optional, this is the default
</code></pre>




[1]: https://github.com/hurrymaplelad/docpad-plugin-rss