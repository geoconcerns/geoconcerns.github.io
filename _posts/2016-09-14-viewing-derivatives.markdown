---
layout: walkthrough
title:  "Viewing Derivatives - Part 9 - Walkthrough of GeoConcerns"
date:   2016-09-14 15:08:00
categories: tutorial
author: 'Darren Hardy'
author_link: 'https://github.com/drh-stanford'
snippet: 'Creating a GeoConcerns vector work automatically creates a variety of deriviative files. Created as part of a tutorial series given as Walkthrough of GeoConcerns'
---

## View Derivatives
  1. Thumbnail
  1. Display Vector
  1. GeoServer
  1. GeoBlacklight Metadata


### Thumbnail

Once you create a Vector Work and add a Shapefile to it, the thumbnail for the vector data is automatically created. It's viewable in the Summary page and directly downloadable from Fedora.

![Summary with thumbnail](/images/VectorFileSet_Summary.png)

![Direct access to thumbnail](/images/VectorFileSet_Thumbnail.png)


## Display Vector

A display derivative is a derivative produced by GeoConcerns for loading into external software such as Geoserver. These derivatives can be used to visualize the dataset in a web mapping applications like OpenLayers and Leaflet. Datasets are re-projected into WGS 84 and converted into a standard file format. Geoblacklight makes use of display derivatives for previewing data.

The vector data are also projected into a standard projection (EPSG:4326) and saved as a Shapefile.

![Direct download to Display Vector](/images/VectorFileSet_DisplayVector.png)

## GeoServer

This Display Vector is then uploaded and registered into your GeoServer catalog.

![GeoServer Workspaces](/images/GeoServer_DataMenu.png)

You will need to create two workspaces: "public" and "restricted". Login as `admin` with password `geoserver` to [http://localhost:8181/geoserver](http://localhost:8181/geoserver)

![GeoServer Workspaces](/images/GeoServer_Workspaces.png)

There's a new Data Store that holds your Display Vector Shapefile:

![GeoServer Workspaces](/images/GeoServer_DataStores.png)

There's a new Layer that renders the Vector data in your Data Store:

![GeoServer Workspaces](/images/GeoServer_Layers.png)

You can also preview your Vector data:

![GeoServer Workspaces](/images/GeoServer_VectorView.png)

## GeoBlacklight Metadata

Finally, if you modify the Vector Work URL by adding `/geoblacklight` to it, you will
receive your metadata as a GeoBlacklight Schema document that you can ingest into your GeoBlacklight instance.

![GeoBlacklight Export](/images/VectorWork_GeoBlacklight.png)

## Geoblacklight

The works you created in GeoConcerns should now be available to view in the included Geoblacklight application. [http://localhost:3001](http://localhost:3001)

![Geoblacklight](/images/geoblacklight.png)


