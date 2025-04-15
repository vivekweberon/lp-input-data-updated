
--------------------------------##################---------------------------------#####################--------------------------

This is a refactored, new data format which supports page title and mautic form configuration

This data format works only with the new listing page template, code and build tool from the following changeset
https://vcs.weberon.com/hg/branded_pages/rev/b0ecca0e8441

New Resources:
js/tracker_v1.js
js/generateUI_v1.js
js/ytvideo_v1.js
pages/lp-showcase_v1.html

--------------------------------##################---------------------------------#####################--------------------------

Showcase page Sections 
Default order of the sections
On Home page
description
showcase
contact
realtor
On Property page
virtualTour
priceAndFeatures
description
photos
video
contact
realtor

Reorder Sections:
To change the order of the sections, add the properties ‘homePageSectionsOrder’ and  ‘propertyPageSectionsOrder’ to the input YAML files of the home page and property page respectively.
If the order properties are not present in the input YAML files, sections are rendered as per the default order mentioned above
Examples:
In YAML file of Home page
homePageSectionsOrder: [realtor, contact, showcase, description]
In YAML file of Property page
propertyPageSectionsOrder: [priceAndFeatures, description, contact, photos, video, virtualTour, realtor]

Enable/Disable Sections:
By default all sections are enabled
To disable a section, add the order properties ‘homePageSectionsOrder’ and ‘propertyPageSectionsOrder’ to the input YAML files of the home page and property page respectively and do not specify the section name which is not required
Examples:
In YAML file of Home page
homePageSectionsOrder: [contact, showcase, description]
Here ‘realtor’ section is removed
In YAML file of Property page
propertyPageSectionsOrder: [priceAndFeatures, description, contact, virtualTour, realtor]
Here ‘photos’ and ‘video’ sections are removed

Note:
If all the property pages of the website have the same order then configure the property ‘‘propertyPageSectionsOrder’’ once in the Global input YAML file
The properties ‘‘homePageSectionsOrder” and “propertyPageSectionsOrder” configured in the Global input YAML file is automatically copied into the output YAML files of home page and properties page respectively by the build tool(only if home/property input YAML file does not have the sections order property).

