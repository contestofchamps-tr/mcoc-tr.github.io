---
layout: page
title: "DocPad Batch-Datei installiert nacheinander Plugins"
subheadline: "Batch-Datei für Plugin-Installationen"
teaser: "Diese DocPadd Batch-Datei installiert nacheinander Plugins, die wichtigsten und grundlegendsten Plugins, die man immer wieder braucht."
icon: docpad.png
tags:
  - docpad
  - batch
---
<div class="alert-box alert radius">
<p>Damit sämtliche Plugins funktionieren und korrekt konfiguriert sind, muss man die dazugehörigen Module – z.B. ImageMagick für das Thumbnail-Plugin – installiert haben und die Konfigurationsdatei aktualisieren – für das z.B. Sitemap-Plugin.</p>
</div>

<pre><code class="lang-html">
# This Batch-File installs all the important plugins
# and generates automatically the partials directory

# Make partials-directory
mkdir src/partials

# Install eco https://github.com/docpad/docpad-plugin-eco
npm install --save docpad-plugin-eco

# Install Markdown support
# https://github.com/docpad/docpad-plugin-marked
npm install --save docpad-plugin-marked

# Install partials support
# https://github.com/docpad/docpad-plugin-partials
docpad install partials

# Install related plugin
# https://github.com/docpad/docpad-plugin-related
npm install --save docpad-plugin-related

# Install sitemap plugin
# https://github.com/benjamind/docpad-plugin-sitemap
docpad install sitemap

# Install Thumbnails plugin
# https://github.com/rantecki/docpad-plugin-thumbnails
npm install --save docpad-plugin-thumbnails

# Install Highlight plugin
# https://github.com/docpad/docpad-plugin-highlightjs
docpad install highlightjs

# Start DocPad and server
docpad run
</code></pre>


## DocPad-Stapelverarbeitung für Mac erstellen

Will man eine Kette von Befehlen nacheinander vom Terminal abarbeiten lassen, legt man dazu am Besten eine so genannte *Batch-Datei* an. Hierbei handelt es sich um eine einfache Textdatei **ohne Dateiendung**.

In jede Zeile kopiert man einen Befehl, der abgearbeitet werden soll. Damit diese Datei ausgeführt werden kann, müssen die Rechte geändert werden.

Lautet die Batch-Datei z.B. *stapelverarbeitung* muss man die Rechte mit Hilfe des *chmod*-Befehls auf 755 stelle.

Der Befehl wäre dann <kbd>chmod 755 stapelverarbeitung</kbd>. Soll die Batch-Datei ausgeführt werden, springt man in das Verzeichnis, in welcher die Datei liegt und tippt vor dem Batch-Dateinamen noch <kbd>./</kbd> ein. In diesem Beispiel <kbd>./stapelverarbeitung</kbd>. Ohne <kbd>./</kbd> würde das Terminal den Befehl *stapelverarbeitung* suchen.