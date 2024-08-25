# Rename wp-content folder

First, back up your site, then make this modification to the wp-config.php file.

For example, you can use 'assets', 'files', or 'media'. This example uses 'assets'.

Next, add the below line before require_once(ABSPATH . 'wp-settings.php'); (usually located at the very bottom) to tell WordPress that the wp-content has been renamed.

```define ('WP_CONTENT_FOLDERNAME', 'assets');```

Then, add these lines below to direct WordPress to the new directory path.

```define ('WP_CONTENT_DIR', ABSPATH . WP_CONTENT_FOLDERNAME) ;
define('WP_SITEURL', 'https://' . $_SERVER['HTTP_HOST'] . '/');
define('WP_CONTENT_URL', WP_SITEURL . WP_CONTENT_FOLDERNAME);```
