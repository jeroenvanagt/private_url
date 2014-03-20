private_url
===========

Private URL Plugin for WordPress

Allows private posts to be shared through a special private url.

### Based on original plugin James Clarke ###

* Plugin Name: Private URL
* Plugin URI: http://jamesclarke.info/projects/private-url
* Description: Create publicly accessible URLs for your private posts
* Version: 1.0.2
* Author: James Clarke
* Author URI: http://jamesclarke.info
* License: GPL

### Version info ###

* Contributors: JamesClarke
* Tags: posts, private
* Requires at least: 2.3.1
* Tested up to: 2.5
* Stable tag: 1.0.2
 
This is original version, incompatible with Wordpress 3.8.1

### Planned Refactoring ###

* Planned refactoring by Jeroen van Agt to make the plugin compatible with Wordpress 3.8.1
* Author: Jeroen van Agt
* Author URI: https://github.com/jeroenvanagt 
* License: GPL

### Description ###

Private URL is a plugin for sharing private posts through a special
private url which is accessible without requiring readers to register or
enter a password.  Private URLs have a structure similar to
`/private/293/df8eb1583b052b59e2cafc4327214d0/`.

### Installation ###

1. Upload `private-url.php` to the `/wp-content/plugins/` directory
2. Activate the plugin through the 'Plugins' menu in WordPress
3. Configure the plugin in the 'Private URL' menu under 'Settings' in
   WordPress.
4. Create and save a private post.  A new options panel called 'Private
   URL' will show the private url for the post.

### Usage ###

When you edit a private post a new options panel will become available
called *Private URL*.  This provides the private url and a means for
changing the *salt* for the post.  The url is a publicly accessible
version of the private post and typically of the form:
`/private/293/df8eb1583b052b59e2cafc4327214d0/`

### What is the *salt*?

The salt is responsible to generating the private url for each post.  It
is similar to a passphrase.  By default all posts use the salt provided
in the settings page for Private URL.  However, you can specify a post
specific salt using the Private URL options panel while editing a post.

Modifying the salt for a post will cause it to have a new private url
and the post's old private url will no longer function.  This can be
used as a means to *expire* an old private url for the post.  Changing
the default salt in the options menu will cause all posts without their
own salt to have new private urls.
