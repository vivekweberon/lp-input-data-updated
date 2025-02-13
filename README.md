# Overview of Key YAML Configuration Elements

This guide provides a brief overview of the primary keys used in our YAML configuration files and explains how to update values.

## Key Components

- **default**  
  Contains the baseline configuration values (e.g., property details, global settings, or homepage content). These values serve as the standard setup for your data.

- **siteOverrides**  
  Allows you to specify modifications to the default values for specific sites. Use this key when you need to customize details (such as property features or homepage sections) for particular websites without affecting the overall configuration.

- **siteName**  
  A list of site identifiers where the configuration should apply. Add or remove site keys here to control which sites display the corresponding content.

## How to Update Values

1. **Update Default Values**:  
   Modify the values under the `default` key to change the standard configuration. These changes apply across all sites unless a site-specific override is provided.

2. **Apply Site-Specific Overrides**:  
   To customize settings for a particular site, update or add the necessary values under the `siteOverrides` key for that site. For example, to change the property title for `lp-bestbuys`, update its `priceAndFeatures` section within `siteOverrides`.

3. **Manage Site Visibility**:  
   Adjust the `siteName` list to determine which sites should use this configuration. To add a site, include its identifier in the list; to remove a site, simply delete its identifier.

By following these steps, you can efficiently manage and customize your configurations using the `default`, `siteOverrides`, and `siteName` keys.
