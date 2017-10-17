---
layout: page
icon: docpad.png
title: "Navigation aufbauen"
tags:
  - docpad
---
Damit der untere Code funktioniert, muss in der Konfigurationsdatei erst einmal die Collection erstellt werden. Das geschieht mit:

<pre><code class="lang-javascript">
    collections:

        sortpages: ->
            @getCollection("html").findAllLive()
</code></pre>

Der folgende Code gehört dann in ein Template oder ein Dokument, dass durch den ECO-Filter fließt.

<pre><code class="lang-ruby">
<% for page in @getCollection("sortpages").toJSON(): %>
    <li class="<%= if page.id is @document.id then 'active' else 'inactive' %>"><a href="<%= page.url %>"><% if page.menutitle: %><%= page.menutitle %><% else: %><%= page.title %><% end %></a></li>
<% end %>
</code></pre>