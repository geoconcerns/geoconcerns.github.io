---
layout: walkthrough
title:  "Create a Vector Work - Part 7 - Walkthrough of GeoConcerns"
date:   2016-06-07 15:08:00
categories: tutorial
author: 'Eliot Jordan'
author_link: 'https://github.com/eliotjordan'
snippet: 'Creating a GeoConcerns vector work. Created as part of a tutorial series given as Walkthrough of GeoConcerns'
---

## Create a vector work
  1. What's a vector work?
  1. Create the vector work
  1. Attach a shapefile
  1. Attach an external metadata file
  1. Build a Geoblacklight Solr document

### What's a vector work?

A vector work represents a geospatial vector dataset. Points, lines, polygons. Common formats include the shapefile and GeoJSON. In this case, the vector work represents the output of a feature extraction process that was run on the parent raster work.

### Create the vector work

1. On the show page of your Raster Work, create a child Vector Work.
1. Click **Attach Child** and select **Attach Vector Work**
1. On the new vector work form add a basic **Title** and fill in the **Provenance** field.

   ![provenance](/images/provenance.png)
1. Click **Create Vector Work**.

### Attach a shapefile

1. Attach a vector file to the work using the same process as the other works.
1. This time the **Type** should be **ESRI Shapefile**.
1. The file can be found at **McKay** / **Geospatial_Data** / **S_566_1914_lines.zip**

   ![shapefile_path](/images/shapefile_path.png)

1. The shapefile is now attached to the vector work.

   ![shapefile](/images/shapefile.png)

   In GeoConcerns, file formats that are composed of multiple files (as in the Shapefile) must be  zipped into a single file before uploading.
   {: .flash-alert}

### Attach an external metadata file

1. Now, attach an FGDC external metadata to the work.
1. The file can be found at **McKay** / **Geospatial_Data** / **S_566_1914_lines_fgdc.xml**

   ![vector_fgdc_path](/images/vector_fgdc_path.png)

1. Once the file is attached, use it to populate the vector work attributes like you did with the raster work.

   ![populate_metadata](/images/populate_metadata.png)

### Build a Geoblacklight Solr document

GeoConcerns has the ability to generate documents for use in external discovery systems like Geoblacklight.

1. In the address bar for the vector work, append `/geoblacklight` to the end of the URL.

   ![address_bar](/images/address_bar.png)
1. The application will build a JSON formatted document that can be indexed into a Geoblacklight Solr instance.

   ![geoblacklight_solr](/images/geoblacklight_solr.png)

<div class='flash-notice'>
  <a href="{% post_url 2016-09-14-viewing-derivatives %}">Next → Viewing derivatives</a>
</div>
