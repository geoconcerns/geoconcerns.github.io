---
layout: walkthrough
title:  "Create an Image Work - Part 4 - Walkthrough of GeoConcerns"
date:   2016-06-07 14:52:00
categories: tutorial
author: 'Eliot Jordan'
author_link: 'https://github.com/eliotjordan'
snippet: 'Creating a Hydra PCDM scanned map work. Created as part of a tutorial series given as Walkthrough of GeoConcerns'
---

## Create an image work
  - What's an image work?
  - Add a new image
  - Add basic metadata
  - Add add a location
  - Set visibility
  - Choose a license
  - Create the work
  - Inspect the work in Fedora
  - Inspect the work in Solr

### What's an image work?

A scanned map.

### Add a new image

1. Click the **+** symbol in the upper-right corner.
1. Select **New Image Work** from the drop-down menu.
   
   ![image_work_add](/images/image_work_add.png)

### Add basic metadata

1. Fill out fields on the **Describe Your Image Work** form.
1. Required fields are noted with an icon. In this case only *Title* is required.
1. Fields with the **More** button are multivalued. Simply click the button and add another value.

   ![image_work_title](/images/image_work_title.png)

### Metadata field definitions

Many of the fields on the work description form are basic metadata properties inherited from CurationConcerns. Below is a list of fields and simple descriptions of what they mean in the context of a geospatial object.

Name | Definition
---- | -------------
Creator | Author(s). Example: George Washington, Thomas Jefferson.
Contributor | An entity (person, organization) responsible for making contributions to the resource.
Description | 	Description of the work.
Subject | Subjects, preferrably in a controlled vocabulary. Examples: Census, Human settlements.
Publisher | Publisher. Example: ML InfoMap.
Source | A related resource from which the described resource is derived.
Language | Language for the work. Example: English.
Spatial | Spatial coverage and place names, perferrably in a controlled vocabulary. Example: "Paris, France".
Temporal | Temporal coverage, typically years or dates. Example: 1989, circa 2010, 2007-2009.
Issued | Issued date for the work.
Provenance | Institution that holds the work.

### Add a location

All GeoConcerns works have a location property that can be set using a Leaflet-based map widget. The location property is a bounding box represented as coordinates in a WGS84 projection.

1. You can search for specific locations on the map by using the search widget on the left side. 
	- Click the search icon (magnifying glass).
	- Type a place name and press enter.
	- Select a location from the dropdown menu.

	  ![map_widget_search_icon](/images/map_widget_search_icon.png)
1. Once you have identified a location, you can re-center the bounding box by clicking the **Select Area** button on the upper right.
1. The bounding box appears on the map widget as a rectangle with a light interior.
1. The extent of the bounding box can be changed by clicking and dragging the white squares at the corners of the rectangle.
	
	![map_widget_corners](/images/map_widget_corners.png)

1. Clicking and dragging the grid icon on the upper left hand corner of the bounding box will move the rectangle without moving the underlying map.

   ![map_widget_grid](/images/map_widget_grid.png)

1. You can zoom in and out on the map by clicking on the plus **+** and minus **-** icons in the upper left corner.
1. You can move the geographic extents can by clicking and dragging anywhere on the map canvas besides the bounding box corners.

   ![map_widget_demo](/images/map_widget_demo.gif)

### Set visibility

The visibility settings control who can view your work and it's files. 

![visibility](/images/visibility.png)

1. The **Open Access**, **Your Institution**, and **Private** options are the most common settings you will  use. For this tutorial, select one of these three.
1. An **Embargo** allows you to restrict content until a specific date.
1. A **Lease** does the inverse, allowing you to open up access for a specific time period.

### Choose a license

In this last step you can choose a license for your data. You can choose multiple licenses, or none at all. These options are configurable.

![licenses](/images/licenses.png)

### Create the work

1. Click **Create image work** button.

   ![create_image_work](/images/create_image_work.png)
1. You'll be directed to the Image Work show page.
1. On the show page, you'll see a list of list of the attributes that you entered in the previous steps.

   ![attributes](/images/attributes.png)

### Inspect the work in Fedora

1. Open the Fedora Repository dev containter web interface in a new browser tab or window.
  - [http://127.0.0.1:8984/rest/dev](http://127.0.0.1:8984/rest/dev)
1. You'll see a resource with at least three children. The child with the shortest URL will (probably) be your Image Work reource.
1. Click on that link (you might have to copy and paste it into another tab).
   
   ![fedora_resource](/images/fedora_resource.png)

1. You'll see the metadata for the Image Work you created earlier as a Fedora resource.
   
   ![fedora_resource_full](/images/fedora_resource_full.png)

### Inspect the work in Solr

1. Open the Solr web interface in a new browser tab or window. 
  - [http://127.0.0.1:8983/solr/#/hydra-development](http://127.0.0.1:8983/solr/#/hydra-development)
1. Click the **Query** button on the lower left.

   ![solr_query_button](/images/solr_query_button.png)

1. Then click **Execute Query** to search all documents.

   ![execute_query](/images/execute_query.png)
1. This returns a JSON formatted list of documents. If you scroll around, you'll find metadata from your Image Work and see that it was fully indexed into Solr.
   ![solr_query_results](/images/solr_query_results.png)


<div class='flash-notice'>
  <a href="{% post_url 2016-06-07-add-files-to-the-image-work %}">Next → Add files to the image work</a>
</div>




