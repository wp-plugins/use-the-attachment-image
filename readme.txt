=== Plugin Name ===
Contributors: tomthewebmaster
Tags: image, attachment image, thumbnail, magazine
Requires at least: 2.7
Tested up to: 2.9.1
Stable tag: trunk

Allows the first attachment image associated with a post to be used in different locations throughout a blog.

== Description ==

This plugin allows the first attachment image associated with a post to be used in different locations throughout a blog, a perfect compliment for magazine themes.

This plugin can include images of nearly any size, simply by using the included `<?php special_get_post_photo(); ?> function. See the installation page for more details regarding usage.


== Installation ==

1. Upload `use_attachment_image.php` to the `/wp-content/plugins/` directory on your web server.
1. Activate the plugin through the 'Plugins' menu in WordPress.
1. Place `<?php use_the_attachment_image() ?>` (will include a link to the post), or `<?php use_the_attachment_image() ?>` (will NOT include a link to the post) in your template to include a thumbnail of the first attachment image. Note the function must be inside of a WordPress loop.

By default, this function will include a thumbnail image. To include images of different sizes, use the respective functions below.

<strong>Thumbnail</strong> `<?php special_get_post_photo('thumbnail'); ?>`
<strong>Medium</strong> `<?php special_get_post_photo('medium'); ?></p>`
<strong>Large</strong> `<?php special_get_post_photo('large'); ?></p>`
<strong>Full</strong> `<?php special_get_post_photo('full'); ?>`
<strong>20 pox</strong> `<?php special_get_post_photo(array(20,20)); ?>`
Feel free to replace 20 with another specific size to best meet your needs.

1. This plugin also includes the capability to include a thumbnail image from each post to your RSS feed. To activate this feature, simply add this code to your functions.php file.

`<?php add_filter('the_excerpt_rss', 'insertAttachmentRSS'); ?>`
`<?php add_filter('the_content_feed', 'insertAttachmentRSS'); ?>`

== Changelog ==

= 1.0 =
* Initial release.