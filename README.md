Workaround For XSS Vulnerability on WordPress Up To Version 4.6.1

While waiting for WordPress Team to release the fix. You should disable the caption of the media by adding the below script to your functions.php of your theme.

function no_caption($deprecated, $attr, $content) { return $content; };
add_filter('img_caption_shortcode', 'no_caption', 10, 3);
