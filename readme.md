# Google Tag Manager Plugin for Crafter CMS

This is a plugin to add Google Tag Manager to your site.

# Installation

The plugin can be installed to your site from the Crafter CMS Marketplace

# Setup

After the plugin has been installed you can enable it by adding the following snippet in your site configuration:

```xml
<plugins>
  <googleTagManager>
    <enabled>...</enabled>
    <id>GTM-XXXX</id>
  </googleTagManager>
</plugins>
```

# Configuration

- `enabled`: Indicates if the Google Tag Manager plugin should be added to all pages, defaults to `false` if the site
- `id`: The container id that starts with `GTM-`

Example:

```xml
<plugins>
  <googleTagManager>
    <id>GTM-XXXX</id>
  </googleTagManager>
</plugins>
```

# Page Override

If the plugin is enabled in the site configuration but some pages should not include the Google Tag Manager markup it
is possible to override the configuration using a field in the content-type:

| Field Type |  Field Name                 |
|------------|-----------------------------|
| `checkbox` | `disableGoogleTagManager_b` |

When the property is added to a content-type authors can use it do control which pages are excluded.
