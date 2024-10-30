=== Horizontal Image Gallery ===
Contributors: flashblue
Tags: flashblue, css, color, button, border, background, as3, arrow, multiple, loop, item, image, horizontal, grey, gallery, font, time, slideshow, second, saturation, reflection, product, path, xml, viewer, timer, wordpress, joomla, plugin, module
Requires at least: 2.8.0
Tested up to: 3.0.3
Stable tag: trunk

Dynamic XML controlled image gallery / product showcase.

== Description ==

Features included:

* XML driven Flash image gallery / product viewer
* Supports multiple items defined in XML file
* Title & description colors, font sizes
* Image/swf names/paths set in XML file
* URL links & targets for each item set in XML file
* Border & arrow buttons rollover, colors set in XML file
* Border, background size
* Item spacing set in XML file
* CSS file path set in XML file
* You can show/hide saturation, reflection of items
* You can change maximum visible items
* You can loop items by loop="true" parameter on XML
* You can create slideshow with global timer by slideShow="true" & slideShowTimer="_second_" parameters on XML
* Includes WordPress plugin & Joomla module

== Installation ==

Make sure your Wordpress version is greater than 2.8 and your hosting provider is using PHP5.

1. Create a new folder inside your **wp-content** folder called **flashdo**, inside this folder create a new one called **flashblue**, inside this folder create a new one called **horizontal-image-gallery** and copy files under **deploy** folder there
2. If you copied the **deploy** to a location different than the one above, go to **Horizontal Image Gallery** from the **Settings** tab in your **WordPress Dashboard** and update the path accordingly
3. Add `[horizontal-image-gallery][/horizontal-image-gallery]` where you want the Flash to show up in your post/page
4. If you want to make the Horizontal Image Gallery part of your theme, edit the template files and add `<?php horizontalimagegallery_echo_embed_code(); ?>` where you want it to show up
5. Modify the `gallery.xml` content and use it to overwrite `wp-content/flashdo/flashblue/horizontal-image-gallery/xml/gallery.xml`
6. To use your own images / swf, upload them to `wp-content/flashdo/flashblue/horizontal-image-gallery/images/`

= Additional settings file =

To embed the Horizontal Image Gallery more than once, you will need another settings file. Let's assume your new file is called `gallery2.xml`. Add `[horizontal-image-gallery xmlUrl="xml/gallery2.xml"][/horizontal-image-gallery]` where you want the Flash to show up in your post/page. If you made the Flash part of your theme, add the file name as **the first argument** of the `horizontalimagegallery_echo_embed_code()` function call (for example `<?php horizontalimagegallery_echo_embed_code("xml/gallery2.xml"); ?>`).

= No Flash support text =

To support visitors without Adobe Flash Player, you can provide alternative content by adding the text between `[horizontal-image-gallery]` and `[/horizontal-image-gallery]`. If you made the Flash part of your theme, add the text as **the second argument** of the `horizontalimagegallery_echo_embed_code()` function call (for example `<?php horizontalimagegallery_echo_embed_code("","Alternative content"); ?>`).

= If you have PHP4 =

To make it work with PHP4, add `[horizontal-image-gallery width="960" height="350"][/horizontal-image-gallery]` where you want the Flash to show up in your post/page. If you made the Flash part of your theme, add the width and height as **the third and fourth argument** of the `horizontalimagegallery_echo_embed_code()` function call. Don't forget to provide your own width and height values, since 960 and 350 are just examples.

== Screenshots ==

1. You can view the live demo on [flashdo.com](http://www.flashdo.com/item/horizontal-image-gallery/88 "Horizontal Image Gallery") for Horizontal Image Gallery.