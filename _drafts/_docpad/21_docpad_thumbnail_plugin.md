---
layout: page
icon: docpad.png
title: "Bilder automatisch vergrößern und verkleinern mit dem Thumbnail Plugin"
tags:
  - docpad
  - thumbnail plugin
---
<div class="alert-box alert radius">
<p>Damit dieser Code-Schnipsel funktioniert, muss zuerst das [DocPad-Thumbnails-Plugin][1] installiert werden. Dazu reicht leider nicht ein Kommando, da auf der Maschine für die automatische Bearbeitung der Bilder entweder das Software-Paket [ImageMagick][2] oder [GraphicsMagick][3]. Mehr dazu in der [Anleitung zum Thumbnails Plugin][1].</p>
</div>

Wie man Bilder mit dem Thumbnails Plugin vergrößert oder verkleinert, erklärt die Anleitung des Plugins. Was fehlt ist die Syntax für die Bearbeitung eines Bildes, dessen Namen man in den Metadaten im Dokument abgespeichert hat.

## Metadaten des Beispieldokumentes

<pre><code class="lang-html">
&ndash;&ndash;&ndash;
layout: page
icon: docpad.png
title: "Bilder bearbeiten"
&ndash;&ndash;&ndash;
</code></pre>

## Aufruf des Thumbnail Plugins samt Zugriff auf die Metadaten

Damit das Thumbnail Plugin auf das Bild `docpad.png` zugreift, muss man den Aufruf des Plugins wie folgt gestalten: 

<pre><code class="lang-ruby">
<img style="margin: 0px 0 0 0px;" src="<%= @getThumbnail('images/' + @document.icon,  { w: 100, h: 100 }) %>" alt=""> 
</code></pre>

Der Teil `'images/' + @document.icon` setzt die URL zum Bild zusammen.


 [1]: https://github.com/rantecki/docpad-plugin-thumbnails
 [2]: http://www.imagemagick.org/script/index.php
 [3]: http://www.graphicsmagick.org/