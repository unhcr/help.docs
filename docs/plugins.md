# Plugins

help.unhcr.org uses a variety of plugins. This will go over the ones that are being used by the site and how they are used in the site.

### Advanced Custom Fields Pro (ACF)

This is the main plugin you will deal with when working with help.unhcr.org. You can find the docs here: [http://www.advancedcustomfields.com/resources](http://www.advancedcustomfields.com/resources)

There are a few gotchas when using ACF and multisites. The important thing to be able to do is have the custom fields that you make available for all sites. In order to do this you can follow these instructions:

1. Create new fields in the main help.unhcr.org blog (not the network) admin.
2. Sync those fields with the rest of the sites. This is only available on the help.unhcr.org blog which is why you should create your fields there.

To upload these to the production server, it's a similar process:

1. Export the fields you'd like from the help.unhcr.org blog.
2. Import the fields you just export to the production site on the help.unhcr.org blog.
3. Sync the fields with the rest of the sites using the multisite sync.


### WPML Multilingual CMS

This [plugin](http://wpml.org/) allows for posts and different fields to be translated. We use it in conjunction with ACF. It also provides String translations for static strings.

### WP-RTL

This [plugin](https://wordpress.org/plugins/wp-rtl/) allows users to write left-to-right and right-to-left in the same post.

