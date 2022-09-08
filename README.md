# SHIRA_climate_hazards_report

Integrates SHIRA and NPVuln climate change hazards for list of parks & assets

## How to run

Files needed to run this hazards report are located in the [CCRP Collaborate! Sharepoint](https://doimspp.sharepoint.com/sites/nps-waso-ccrp/Shared%20Documents/Forms/AllItems.aspx?FolderCTID=0x0120006B8FB33F4A9AB343A7A8653D56FAD402&OR=Teams%2DHL&CT=1662666857851&clickparams=eyJBcHBOYW1lIjoiVGVhbXMtRGVza3RvcCIsIkFwcFZlcnNpb24iOiIyNy8yMjA3MzEwMTAwNSIsIkhhc0ZlZGVyYXRlZFVzZXIiOmZhbHNlfQ%3D%3D&id=%2Fsites%2Fnps%2Dwaso%2Dccrp%2FShared%20Documents%2F01%20PROJECT%20Collaboration%2FFacilities%2FGAOA%5FSHIRA%20Reviewing&viewid=a459d1c3%2Dd72a%2D4fec%2D9adc%2D0cc2a4094eba)

To run, you will need to:

1.  Identify the list of potential projects and format a csv with the following headers:

2.  Load "PAM_Owned Buildings and Structures.csv" from the [Shira Sharepoint](https://doimspp.sharepoint.com/sites/usgs-shira_home?CT=1662061010120&OR=OWA-NT&CID=0ee76a98-796e-fb71-9009-9b62065909ef)  
    *Always check for an updated version as variables are often modified*

3.  Subset PAM dataframe to the coordinates closest to the coordinates of assets. If FMBS ID\#s are provided, the hazards of the asset can be identified. If only the park is identified the asset closest to the centroid will be used.

4.  New dataframe should have the following fields:

    | Park | Lat | Long | State | Hazard | Risk | Raw |
    |------|-----|------|-------|--------|------|-----|

5.  Read in shapefiles from the [Shira Sharepoint](https://doimspp.sharepoint.com/sites/nps-waso-ccrp/Shared%20Documents/Forms/AllItems.aspx?FolderCTID=0x0120006B8FB33F4A9AB343A7A8653D56FAD402&OR=Teams%2DHL&CT=1662666857851&clickparams=eyJBcHBOYW1lIjoiVGVhbXMtRGVza3RvcCIsIkFwcFZlcnNpb24iOiIyNy8yMjA3MzEwMTAwNSIsIkhhc0ZlZGVyYXRlZFVzZXIiOmZhbHNlfQ%3D%3D&id=%2Fsites%2Fnps%2Dwaso%2Dccrp%2FShared%20Documents%2F01%20PROJECT%20Collaboration%2FFacilities%2FGAOA%5FSHIRA%20Reviewing%2FGIS%5Ffiles&viewid=a459d1c3%2Dd72a%2D4fec%2D9adc%2D0cc2a4094eba)

6.  From this the report should knit
