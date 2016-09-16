---
layout: walkthrough
title:  "Create a Raster Work - Part 6 - Walkthrough of GeoConcerns"
date:   2016-06-07 15:07:00
categories: tutorial
author: 'Eliot Jordan'
author_link: 'https://github.com/eliotjordan'
snippet: 'Creating a GeoConcerns raster work. Created as part of a tutorial series given as Walkthrough of GeoConcerns'
---

## Create a raster work
  - Find raster in my works
  - Add georeferenced map
  - Add an FGDC external metadata file
  - Populate metadata from FGDC

  
###  Find raster in my works
At the end of the last section, we created an child Raster Work. We'll need to locate that raster work before we start this section.

1. In the upper right-hand corner, click on your user email address and select **My Works** from the drop-down.

   ![my_works](/images/my_works.png)
1. On the catalog page, you can:
   - facet on work type, creator, and subject

     ![search_facet](/images/search_facet.png)
   - do a keyword search

   	 ![search_keyword](/images/search_keyword.png)
   - search for works or collections

     ![search_type](/images/search_type.png)
1. In this case, out raster work is very easy to find. Click on the Raster Work title to go to it's show page.
1. You'll notice that the parent image work appears in the **Parent Works** section.
   
   ![raster_parent_work](/images/raster_parent_work.png)

### Add georeferenced map

1. We need to add our georeferenced raster to our raster work.
1. Attach the raster file in the same way as you did with the image work.

   ![attach_raster_file](/images/attach_raster_file.png)
1. Select **GeoTIFF** as the file type.
1. Choose this file **McKay** / **Georeferenced_Image** / **S_566_1914_clip.tif**

   ![geotiff_path](/images/geotiff_path.png)
1. Attach the file to the Raster Work.

   ![raster_file](/images/raster_file.png)

### Add an FGDC external metadata file

1. Using the same process as before, attach an external metadata file. This time make sure to select the type as FGDC.
1. The metadata file can be found at **McKay** / **Georeferenced_Image** / **S_566_1914_clip_fgdc.xml**

   ![fgdc_path](/images/fgdc_path.png)

### Populate metadata from FGDC
We can now extract metadata from the FGDC document to populate attributes on our Raster Work.

1. Click on **Edit This Raster Work**
   
   ![edit_raster](/images/edit_raster.png)
1. Scroll to the bottom of the page to the **Automatically Populate Metadata** section.
1. Select the metadata file from the drop-down menu.
1. Click **Update Raster Work**.

   ![populate_metadata](/images/populate_metadata.png)
1. We now have a much more complete Raster Work.

   ![raster_work_populated](/images/raster_work_populated.png)

<div class='flash-notice'>
  <a href="{% post_url 2016-06-07-create-a-collection %}">Next → Create a collection</a>
</div>
