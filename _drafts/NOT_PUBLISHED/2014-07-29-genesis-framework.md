---
title: Genesis Framework
layout: post
permalink: /genesis-framework/
categories:
  - Ah...!
tags:
  - theme
  - webentwicklung
  - wordpress
---
[<img class="size-full wp-image-3337 alignnone" src="{{ site.url }}/images/genesis-framework.png" alt="genesis-framework" width="470" height="446" />][1]

Das <a href="http://www.studiopress.com/" target="_blank">Genesis Framework</a>, ist das Framework für WordPress-Websites und hochoptimiert für Suchmaschinen. Bei Kunden wie <a href="http://Tarnkappe.info" target="_blank">Tarnkappe.info</a> und <a href="http://Nixdorf-Internatsberatung.de" target="_blank">Nixdorf-Internatsberatung.de</a> setze ich es bereits ein. Damit ich mit dem Framework noch besser umgehen kann, habe ich mein altes Theme gewechselt. Lernen am lebenden Objekt, dass hilft mir am Besten. Also nicht erschrecken, dass Design hier wir schrittweise verbessert.<!--more-->

## Credits im Footer anpassen

<pre>//* Customize the credits
add_filter( 'genesis_footer_creds_text', 'sp_footer_creds_text' );
function sp_footer_creds_text() {
        echo '<div class="creds">
  <p>
    ';
            echo 'Copyright &copy;';
            echo date('Y');
            echo ' by <a href="http://phlow.de/" title="WordPress Webdesign SEO Suchmaschinenoptimierung">Phlow – Agentur für WordPress, Webdesign & Suchmaschinenoptimierung</a>';
            echo '
  </p>
</div>';
}
</pre>

## Textbausteine anpassen

<pre>//* Customize the post meta function
add_filter( 'genesis_post_meta', 'sp_post_meta_filter' );
function sp_post_meta_filter($post_meta) {
if ( !is_page() ) {
    $post_meta = '[post_categories before="Abgelegt unter: "] [post_tags before="Schlagwort: "]';
    return $post_meta;
}}



add_filter( 'genesis_search_title_text', 'wpse_101947_search_title_text' );

function wpse_101947_search_title_text() {
    return 'Suchresultate für: ';
}


//* Modify the WordPress read more link
add_filter( 'the_content_more_link', 'sp_read_more_link' );
function sp_read_more_link() {
    return '<a class="more-link" href="' . get_permalink() . '">Weiterlesen »</a>';
}


//* Customize search form input button text
add_filter( 'genesis_search_button_text', 'sp_search_button_text' );
function sp_search_button_text( $text ) {
    return esc_attr( 'Suchen' );
}

//* Customize search form input box text
add_filter( 'genesis_search_text', 'sp_search_text' );
function sp_search_text( $text ) {
    return esc_attr( 'Suchbegriff' );
}

</pre>

 [1]: {{ site.url }}/images/genesis-framework.png