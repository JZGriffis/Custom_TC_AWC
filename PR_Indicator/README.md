# PR Indicator

This customization is adding a indicator in AWC on Item Revisions when that Item Revision is in a Problem Report's CMHasProblemItem relation. This mimic's the behavor of the OOTB Active Change (Authoring Change) in AWC. 

The custom indicator is placed on a custom property on ItemRevision. This property is created in BMIDE as a TypedReference property on ItemRevision referencing GnProblemItemRevision as an unlimited array. To populate this property will need ITK to pull the related PR's to the Item Revisions. That ITK is not covered here.

This customization was created and tested in AWC5.2.

![image](https://user-images.githubusercontent.com/42276263/153721596-ed32490a-19a1-4f9c-8e95-6718e8024e7f.png)



# Steps to create the indicator

You will need to already have a custom module created for AWC. That is not covered here.

* Create two files named indicators.json and typeProperties.json in your custom module folder.
  * Samples of these two files are in this repo.


* Create a 16x16 SVG icon with the naming convention indicatorCUSTOMNAME16.svg. 
  * Place this in the aws2\stage\scr\image folder.

* Once the files are completed and the icon is in the images folder, rebuild AWC.



# Notes for indicators.json file

* "iconname" = Icon name without the "indicator" or "16.svg"
    * File name in images folder: indicatorXY9_AuthoringPR16.svg

* "propNames" = the custom property from BMIDE that we use to show the indicator
  * xy9_AuthoringPR



# Notes for typeProperties.json

* Not all properties are loaded when the Item Revision is retrieved. To load pre-load properties to use with indicators, you need to create this typeProperties.json and define for the different types the properties that need pre-loaded. In this case it is our custom xy9_AuthoringPR property.
