---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage_mcoc
title: "Marvels Contest of Champions"
header:
    image_fullwidth: other/all-champs.jpg
    background-color: "#29aebc"
style: "#masthead-with-background-color { padding: 10px; }"
homepage: true
---
<br><br>
<div class="row">

     <div class="medium-6 columns">
    <h4 class="b05"><a href="{{ site.url }}/haber/">Son Haberler</a></h4>
    {% include list-collection.html collection='haber' limit='5' %}
    <p class="sans text-right"><a class="button tiny radius" href="{{ site.url }}/haber/"><strong>Tümü›››</strong></a></p>
  </div><!-- /.medium-6.columns -->

  <div class="medium-6 columns">
    <h4 class="b05"><a href="{{ site.url }}/taktik/">Oynama taktikleri</a></h4>
    {% include list-collection.html collection='taktik' limit='5' %}
    <p class="sans text-right"><a class="button tiny radius" href="{{ site.url }}/taktik/"><strong>Tümü›››</strong></a></p>
  </div><!-- /.medium-6.columns -->
  
</div><!-- /.row -->

<div class="t0 b15" style="padding: 30px 0; background: #82cbd0;">
  <div class="row">
    <div class="small-12 text-center medium-12 columns">
      <a href="{{ site.url }}/indir-download/"><img class="left" src="{{ site.urlimg }}other/down-logo.png" width="200" height="200" alt="Newsletter"></a>
      <h2 class="shadow-black" style="margin: 10px 0; color: #fff;" >Oyunu oynamaya karar verdiysenız sizi aşağıdaki indirme sayfasına davet ediyoruz.</h2>
      <a class="radius button info shadow-black" href="{{ site.url }}/indir-download/">indirme sayfası / download page</a>
    </div><!-- /.small-12 medium-8.columns -->
  </div><!-- /.row -->
</div>

