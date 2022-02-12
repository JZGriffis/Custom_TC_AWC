# PR Indicator

This customization is adding a indicator on Item Revisions when it is used in PR using the CMHasProblem relation. This is done by using a custom TypeReference property on the Item Revision to the GnProblemItemRevision's. This property is created in BMIDE and will need ITK to pull the related PR's to the Item Revisions.

This customization was created and tested in AWC5.2.

![image](https://user-images.githubusercontent.com/42276263/153721596-ed32490a-19a1-4f9c-8e95-6718e8024e7f.png)


#Steps to create the indicator

You will need to already have a custom module created for AWC. That is not covered here.

In your custom module folder, create files called indicators.json and typeProperties.json. 

Create a 16x16 SVG icon with the naming convention indicatorCUSTOMNAME16.svg. Place this in the aws2\stage\scr\image folder.

