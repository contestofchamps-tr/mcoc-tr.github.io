---
published: false
layout: page
subheadline: WordPress Programmierung
title: Schrittweise ein eigenes WordPress Theme programmieren
meta_description: ""
teaser: ""
permalink: /wordpress/theme-programmierung/
categories:
    - webdesign
tags:
    - wordpress
    - theme
    - programmierung
    - anleitung
image:
    thumb: icon/icon-wordpress.svg
header:
    image: icon/wordpress-logo-498x113.png
    background-color: "#82cbd0"
style: "#navigation > nav > section > ul.left > li:nth-child(5) > a { background: #82cbd0; color: #fff; }"
---


## Über das »Feeling Responsive Theme«

Theme-Name: Feeling Responsive
Demo-URL: <http://responsive.phlow.de>
Beschreibung:
Schlagworte: responsive webdesign, suchmaschinenoptimiert




## Planung

## WordPress installieren

### Download
* Download Original
* Download Deutsche Version

### Datenbank erstellen

### Entpacken

### Hochladen

### Installieren

### Testinhalte hochladen
- [XML-Datei mit Daten runterladen](http://codex.wordpress.org/Theme_Unit_Test)
- Daten importieren

#### Theme Unit Test eingeben und einstellen
- Testdaten runterladen unter: <http://codex.wordpress.org/Theme_Unit_Test>
- Testdaten über das Menu *Tools › Import importieren*



## Theme anlegen

### Theme-Ordner anlegen
`feelingresponsive`

### style.css-Datei anlegen

{% highlight css %}
/*
Theme Name: Feeling Responsive
Theme URI: http://responsive.phlow.de
Description: A minimal and elegant responsive webdesign theme for WordPress
Author: Moritz »mo.« Sauer
Author URI: Moritz »mo.« Sauer
Version: 0.1
Tags: black, white, responsive webdesign, exo font, 

License:
License URI:

General comments (optional).
*/
{% endhighlight %}

## Screenshot PNG erstellen
Größe 300x225 Pixel

## Leere PHP-Dateien anlegen
* index.php
* header.php
* sidebar.php
* footer.php
* page.php
* single.php

### Plugin API Hooks
{% highlight php startinline=true %}
<?php wp_header(); ?> 
<?php wp_header(); ?> 
</head>
<?php wp_footer(); ?> 
<?php wp_footer(); ?> 
</html>
{% endhighlight %}

## Theme Unit Test eingeben und einstellen


## WordPress Settings
Adjust WordPress settings as follows:
* Settings -> General: set the Site Title to something fairly long, and set the Tagline to something even longer. These settings will facilitate testing how the Theme handles these values.
* Settings -> Reading: set "Blog pages show at most" to 5. This setting will ensure that index/archive pagination is triggered.
* Settings -> Discussion: enable Threaded Comments, at least 3 levels deep. This setting will facilitate testing of Theme comment list styling.
* Settings -> Discussion: enable Break comments into pages, and set 5 comments per page. This setting will facilitate testing of Theme paginating link markup/styling.
* Settings -> Media: ensure that no values are set for max width or height of Embedded media. This setting will facilitate testing of the Theme $content_width setting/implementation.
* Settings -> Permalinks: ensure that a non-default permalink setting is selected, e.g. "Month and name". This setting will facilitate stepping through the Theme Unit Tests.

Create at least two Custom Menus:

Long Menu: all included Pages
Short Menu: a menu of 2-3 Pages


## Theme auf Herz und Nieren checken

## Theme testen mit Plugins
* [Theme Check](https://wordpress.org/plugins/theme-check/)


## Hilfreiche Tutorials

### ElmaStudio Tutorial Serie

* [Teil 1: Inspiration und Materialsammlung](http://www.elmastudio.de/tutorials/webseite-entsteht-teil-1-inspiration-materialsammlung/)
* [Teil 2: Die Layout-Vorlage (Mockup)](http://www.elmastudio.de/tutorials/eine-neue-webseite-entsteht-teil-2-die-layout-vorlage-mockup/)
* [Teil 3: Webdesign mit Illustrator und Photoshop](http://www.elmastudio.de/tutorials/webseite-entsteht-teil-3-webdesign-illustrator-photoshop/)
* [Teil 4: Das Webdesign-Styling](http://www.elmastudio.de/tutorials/eine-neue-webseite-entsteht-teil-4-das-webdesign-styling/)
* [Teil 5: Vorbereitungen für die Programmierung](http://www.elmastudio.de/tutorials/eine-neue-webseite-entsteht-teil-5-vorbereitungen-programmierung/)
* [Teil 6: WordPress lokal Installation und Blank-Theme](http://www.elmastudio.de/wordpress/webseite-entsteht-teil-6-wordpress-lokal-installation-blank-theme/)
* [Teil 7: Die Datei-Struktur des WordPress-Themes](http://www.elmastudio.de/wordpress/eine-neue-webseite-entsteht-teil-7-die-datei-struktur-des-wordpress-themes/)
* [Teil 8: Der WordPress-Theme Header](http://www.elmastudio.de/wordpress/neue-webseite-entsteht-teil8-wordpress-theme-header/)
* [Teil 9: Eine indi­vi­du­elle Startseite in WordPress](http://www.elmastudio.de/wordpress/neue-webseite-entsteht-teil-9-individuelle-startseite-wordpress/)
* [Teil 10: WordPress Footer-Widgets nutzen](http://www.elmastudio.de/wordpress/neue-webseite-entsteht-teil-10-footer-widgets/)
* [Teil 11: Einen jQuery Bilder-Slider integrieren](http://www.elmastudio.de/wordpress/eine-neue-webseite-entsteht-teil-11-jquery-bilder-slider/)
* [Teil 12: Der WordPress-Blog](http://www.elmastudio.de/wordpress/neue-webseite-entsteht-teil-12-wordpress-blog/)

