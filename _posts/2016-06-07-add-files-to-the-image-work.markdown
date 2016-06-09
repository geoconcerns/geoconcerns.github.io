---
layout: walkthrough
title:  "Add Files to the Image Work - Part 5 - Walkthrough of GeoConcerns"
date:   2016-06-07 14:52:00
categories: tutorial
author: 'Eliot Jordan'
author_link: 'https://github.com/eliotjordan'
snippet: 'Creating a Hydra PCDM scanned map work. Created as part of a tutorial series given as Walkthrough of GeoConcerns'
---

## Add files to the image work
  - Add an image file
  - Add an external metadata file
  - Add a child raster work

### Add an image file

1. Back on the Image Work show page you'll see a section for related objects. An Image Work can contain image files (in TIFF or JPEG format), external metadata files (MODS, ISO19139, FGDC), and one or more child Raster Works. These sections are empty because we haven't linked any other files or works to our image yet.

   ![members](/images/members.png)

1. On the bottom of the page, find the **Attach File** button and select **Attach Image** from the drop-down menu.

   ![add_image_file](/images/add_image_file.png)
1. On the next page, fill in a *Title* and *Visibility* for the new file.
1. From the **Type** drop-down, choose **TIFF**.
1. Click the **Choose File** button (ignoring the notice about PDFs).
1. Navigate to the files that you copied from the thumb drive and find the **data** directory.
1. Inside **data** there should be a directory called **geoconcerns-demo-data**. You can also download the data [here](https://github.com/geoconcerns/geoconcerns-demo-data/archive/master.zip).
1. In that directory navigate to **McKay** / **Original_Scan** / **N030031.tif** and click **Open**.

   ![orginial_tiff_path](/images/orginial_tiff_path.png)
1. Click the **Attach to Image Work** button, and after some time, you will be redirected to the Image Work show page.
1. The scanned map was uploaded, deposited in Fedora, and a thumbnail derivative was created.

   ![image_file](/images/image_file.png)
1. The orginal image file can now be versioned, deleted, or downloaded.

### Add an external metadata file

1. Attaching an external metadata file is very similar to the process for attaching an image file.
1. Click **Attach File** and then select **Attach Metadata**.
1. Select **MODS** from the **Type** drop-down.
1. Click the **Choose File** button.
1. Navigate to **McKay** / **Original_Scan** / **N030031_mods.xml** and click **Open**.

   ![mods_path](/images/mods_path.png)
1. Click the **Attach to Image Work**.
1. We now have a mods metadata file attached to our image work

   ![mods_file](/images/mods_file.png)

### Add a child raster work

An important component of GeoConcern models are parent-child relationships between different work types. In our example, we've' created an Image Work for a scanned map. At some point we might want to georectify this map and create a raster image from it. It turns out that we already went through that process and we now want to link that GeoTiff to it's parent image. 

1. On the bottom of the page, find the **Attach Child** button and select **Attach Raster Work** from the drop-down menu.

   ![add_child_raster](/images/add_child_raster.png)

1. This will redirect you to a form for creating a new Raster Work.
   
   ![new_raster_page](/images/new_raster_page.png)
1. Fill in only the minimum amount of required metadata - *Title* - and click the **Create Raster Work** button at the bottom of the page.

   ![create_raster_work](/images/create_raster_work.png)
1. You will be redirected to the Raster Work show page. If youk look at the breadcrumb bar below the raster title, you'll see a link to the parent Image Work.

   ![child_raster_work](/images/child_raster_work.png)

1. Click on that link and you will return to the scanned map image page. At the bottom of the page you'll see a link to that child Raster Work.

   ![all_child_raster_works](/images/all_child_raster_works.png)
1. Click on the raster work icon and proceed to the next tutorial section.

<div class='flash-notice'>
  <a href="{% post_url 2016-06-07-create-a-raster-work %}">Next → Create a raster work</a>
</div>
