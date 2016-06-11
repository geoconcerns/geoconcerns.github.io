---
layout: walkthrough
title:  "Display Derivatives - Part 8 - Walkthrough of GeoConcerns"
date:   2016-06-07 15:08:00
categories: tutorial
author: 'Eliot Jordan'
author_link: 'https://github.com/eliotjordan'
snippet: 'Creating a GeoConcerns vector work. Created as part of a tutorial series given as Walkthrough of GeoConcerns'
---

## Display derivatives
  - What's a display derivative?
  - Raster display derivative
  - Vector display derivative

### What's a display derivative?

A display derivative is a derivative produced by GeoConcerns for loading into external software such as Geoserver. These derivatives can be used to visualize the dataset in a web mapping applications like OpenLayers and Leaflet. Datasets are re-projected into WGS 84 and converted into a standard file format. Geoblacklight makes use of display derivatives for previewing data.

![geoblacklight_leaflet](/images/geoblacklight_leaflet.png)

### Raster display derivative

1. Create a new raster work with minimal metadata.
1. Attach a raster file to the work. 
1. The **Type** should be **Arc/Info Binary Grid**.
1. The file can be found at **Raster** / **Precipitation** / **arcgrid.zip**.
1. After you attach the file, find the **Download** button on the raster file and select **Display Raster**.
1. GeoConcerns reprojected the raster and converted it to GeoTIFF format.

![raster_display](/images/raster_display.png)

### Vector display derivative

1. Create a new vector work with minimal metadata.
1. Attach a vector file to the work. 
1. The **Type** should be **GeoJSON**.
1. The file can be found at **Vector** / **countries** / **countries.geo.json**.
1. After you attach the file, find the **Download** button on the vector file and select **Display Vector**.
1. GeoConcerns reprojected the vector and converted it to Shapefile format.

![vector_display](/images/vector_display.png)