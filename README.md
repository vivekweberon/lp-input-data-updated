# YAML Data Files Documentation

This repository contains three main directories that hold the configuration and content for your websites. These files work together to provide property-specific details, global settings, and homepage configurations. They are organized in a modular way using **default** values and **siteOverrides** to allow for site-specific customization.

## Directory Structure Overview

- **Property Data** (`/data/111/data.yaml`)
  - Contains property-specific details such as pricing, features, media, and more.
  - Uses a `default` section for standard property details.
  - Uses a `siteOverrides` section to override default values for specific sites.
  - Includes a `siteName` list that specifies the sites where the property should appear.

- **Global Data** (`/data/global/data.yaml`)
  - Contains settings that appear across the website (e.g., realtor details, footer text, contact information).
  - Uses a `default` section for common global settings.
  - Uses a `siteOverrides` section to customize settings for particular sites.
  - Includes a `siteName` list to determine which sites will use these global settings.

- **Home Data** (`/data/home/data.yaml`)
  - Contains the configuration and content for the homepage, including section order and showcase properties.
  - Uses a `default` section for homepage content.
  - Uses a `siteOverrides` section for site-specific adjustments.
  - Includes a `siteName` list to specify the sites using this homepage configuration.

---

## 1. Property File (`/data/111/data.yaml`)

### Structure Overview

- **`default`**:  
  Contains the base property details, for example:
  - **`home`**: YouTube video IDs and menu labels.
  - **`priceAndFeatures`**: Property title, price, bed count, bath count, home type, square footage, year built, etc.
  - **`photos`, `video`, `virtualTour`, `showcase`**: Media and tour details.
  - **`homePageData`**: Details that appear on the homepage (image, address, etc.).
  - **`chatbot` & `footertext`**: Additional settings.

- **`siteOverrides`**:  
  Allows you to override the default values for specific sites. For example, if the property should have different pricing details on `lp-bestbuys`, you can set them here.

- **`siteName`**:  
  A list that specifies on which sites the property should appear (e.g., `lp-showcase`, `lp-bestbuys`, `lp-bayrentals`).

### How to Update

- **Changing Property Details**:  
  Modify the values under the `default` section to update standard property information.

- **Overriding Defaults for Specific Sites**:  
  Add or update values under the `siteOverrides` section for the desired site.  
  _Example:_
  ```yaml
  siteOverrides:
    lp-bestbuys:
      priceAndFeatures:
        title1: 'Tracy Hills Residence-2'
        title2: '$892,880'
        beds: '4 Beds'
        baths: '3.5 Baths'
        homeType: 'Single-Home'
        sqft: 'Building 2,914 sq/ft'
        yearBuilt: 'Year Built: 2021'
        price: 'HOA: $77/mo'
        menu: 'Price & Features'
