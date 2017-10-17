---
layout: page
icon: docpad.png
title: "Starter Konfigurations Datei"
teaser: "Für eigene Projekte nutzen wir bei Phlow diese Starter Konfigurations Datei"
tags:
  - docpad
---
<pre><code style="font-size: .8em;" class="lang-html">
# DocPad Configuration File
# http://docpad.org/docs/config

# Define the DocPad Configuration
docpadConfig = {

    # =================================
    # Template Configuration

    # Template Data
    # Use to define your own template data and helpers that will be accessible to your templates
    # Complete listing of default values can be found here: http://docpad.org/docs/template-data
    templateData:  # example

        # Specify some site properties
        site:
            # The production url of our website
            # url: "http://snippets.phlow.de"
            url: "http://localhost:9778"


            # The default title of our website
            title: "Phlow Snippets"


            # General website description (for SEO)
            teaser: """
                
                """


            # Favicons, Apple Touch Buttons
            # More information » http://j.mp/apple-touch-icons

            favicon:                         "favicon.ico"                              # iOS7 Size 32x32
            apple_touch_icon_iphone:         "phlow-touch-icon-iphone-60x.png"          # iOS7 Size 60x60
            apple_touch_icon_iphone_retina: "phlow-touch-icon-iphone-retina-120x.png"  # iOS7 Size 120x120
            apple_touch_icon_ipad:           "phlow-touch-icon-ipad-76x.png"            # iOS7 Size 76x76
            apple_touch_icon_ipad_retina:    "phlow-touch-icon-ipad-retina-152x.png"    # iOS7 Size 152x152
            apple_touch_icon_precomposed:    "phlow-touch-icon-android-152x.png"        # iOS7 Size 152x152



            # Verify Website to Webmaster Tools
            # google_webmastertools_id:         ""
            # bing_webmastertools_id:           ""
            # alexa_verify_id:                  ""


            # Facebook-Optimization
            # More information » https://developers.facebook.com/docs/opengraph/property-types/

            # og_locale:                        "de_DE"
            # og_type:                          "website"
            # og_title:                         ""
            # og_teaser:                   ""
            # og_url:                           ""
            # og_site_name:                     ""
            og_image:                         "phlow_de-logo-512x.png"



    # =================================
    # Plugin Configuration

        thumbnails:
            imageMagick: true
            extensions: ['jpg', 'JPG', 'jpeg', 'JPEG', 'png', 'PNG', 'gif', 'GIF']
            presets:
                'default':
                    w: 200
                    h: 200
                    q: 90
                '64x64':
                    w: 64
                    h: 64
                '96x96':
                    w: 96
                    h: 96
                '128x128':
                    w: 128
                    h: 128
                '256x256':
                    w: 256
                    h: 256
    sitemap:
        cachetime: 600000
        changefreq: 'weekly'
        priority: 0.5

    collections:

        pages: ->
            @getCollection("html").findAllLive({isMenu:true})
        sortpages: ->
            @getCollection("html").findAllLive()

    # =================================
    # Ignore Custom Patterns
    # Can be set to a regex of custom patterns to ignore from the scanning process
    
    ignoreCustomPatterns: /config.rb/



}

# Export the DocPad Configuration
module.exports = docpadConfig
</code></pre>