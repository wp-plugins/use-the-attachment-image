=== Plugin Name ===
Contributors: tomthewebmaster
Tags: image, attachment image, thumbnail, magazine
Requires at least: 2.7
Tested up to: 3.0.2
Stable tag: trunk

Allows the first attachment image associated with a post to be used in different locations throughout a blog.

== Description ==

Use the Attachment Image! allows the first attachment image associated with a post to be displayed nearly anywhere on a blog, simply by adding a special function to a loop. This plugin is a perfect compliment for magazine themes.

This plugin can include images of nearly any size, simply by using the included `<?php use_the_attachment_image(); ?>` function. See the installation page for more details regarding usage.

== Installation ==

To utilize this plugin, you will first need to upload `use_attachment_image.php` to the `/wp-content/plugins/` directory on your web server; and activate the plugin through the 'Plugins' menu in WordPress.

Next, place `<?php use_the_attachment_image() ?>` (will include a link to the post), or `<?php use_the_attachment_image_nolink() ?>` (will NOT include a link to the post) in your template to include a thumbnail of the first attachment image. Note the function must be inside of a WordPress loop.

By default, this function will include a thumbnail image. To include images of different sizes, use the respective functions below. You may also use `<?php use_the_attachment_image_nolink() ?>` in place of `<?php use_the_attachment_image() ?>` here.

<strong>Thumbnail</strong> `<?php use_the_attachment_image('thumbnail'); ?>`<br />
<strong>Medium</strong> `<?php use_the_attachment_image('medium'); ?></p>`<br />
<strong>Large</strong> `<?php use_the_attachment_image('large'); ?></p>`<br />
<strong>Full</strong> `<?php use_the_attachment_image('full'); ?>`<br />
<strong>20 px</strong> `<?php use_the_attachment_image(array(20,20)); ?>`<br />
Feel free to replace 20px with another specific size to best meet your needs. Note that WordPress will scale a larger image down to give you the size you desire here.

This plugin also includes the capability to include a thumbnail image from each post to your RSS feed. To activate this feature, simply add this code to your functions.php file.

`<?php add_filter('the_excerpt_rss', 'insertAttachmentRSS'); ?>`
`<?php add_filter('the_content_feed', 'insertAttachmentRSS'); ?>`

See <a href="http://tomlany.net/use-the-attachment-image/image-test/">an example of how this plugin can be used</a>.

If you have any questions about this plugin, <a href="http://tomlany.net/use-the-attachment-image/">feel free to ask on my website</a>, and I will respond as my time allows.

== Changelog ==

= 1.01 =
* Fixed the function name in the documentation. In a few cases, a function that did not exist was referenced. Thanks, <a href="http://www.taringacs.net/">Matias</a> for the report. The actual plugin was not changed.

= 1.0 =
* Initial release.