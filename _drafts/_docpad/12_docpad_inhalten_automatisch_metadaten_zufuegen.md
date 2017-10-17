---
layout: page
icon: docpad.png
title: "Inhalten automatisch Metadaten hinzufügen"
tags:
  - docpad
---
Quelle: http://takitapart.com/posts/organizing-docpad

## In Konfigurationsdatei einfügen

Erklärung: Jedem Dokument, das im Ordner `posts` liegt, werden automatisch die Metadaten `layout:"post"` hinzugefügt. Dadurch spart man sich Arbeit und mus den Dokumenten im Ordner `posts` kein Layout zuweisen.

<pre><code class="lang-ruby">
posts: ->
    @getCollection("html").findAllLive({relativeOutDirPath: 'posts'},[{date:-1}]).on "add", (model) ->
        model.setMetaDefaults({layout:"post"})
</code></pre>

## Weitere Beispiele

<pre><code class="lang-ruby">
collections:
    posts: ->
        @getCollection("html").findAllLive({relativeOutDirPath: 'posts'},[{date: -1}]).on "add", (model) ->
            model.setMetaDefaults({layout: "post"})
    projects: ->
        @getCollection("html").findAllLive({relativeOutDirPath: 'projects'},[{title: 1}]).on "add", (model) ->
            model.setMetaDefaults({layout: "project"})
    pages: ->
        @getCollection("html").findAllLive({relativeOutDirPath: 'pages'}).on "add", (model) ->
            model.setMetaDefaults({layout: "page"})
    pictures: ->
        @getCollection("html").findAllLive({relativeOutDirPath: 'pictures'},[{date: -1}]).on "add", (model) ->
            model.setMetaDefaults({layout: "picture"})</code></pre>
</code></pre>

## Spezifiziere mehrere Ordner in die geschaut werden sollen

<pre><code class="lang-ruby">
frontpage: ->
    @getCollection("html").findAllLive({relativeOutDirPath: $in: ['posts','projects','pictures']},[{date: -1}])
</code></pre>




