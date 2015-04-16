.. _wp_settings:

********
Settings
********

Permission settings
===================

The detailed official explanation for the permission setting is http://codex.wordpress.org/Changing_File_Permissions

The mediafile stored in /wordpress/wp-content/ and required for writable permission, reset the owner to apache server::

  sudo chown -R www-data:www-data wp-content/

the media uploading will work well.

Plugins
=======

Disable google fonts

https://wordpress.org/plugins/disable-google-fonts/

Using Themes
============



