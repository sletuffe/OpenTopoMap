OpenTopoMap
===========
OpenTopoMap is a topographic mapnik 3+ xml (non CartoCss) map style using data from OpenStreetMap contributors and various Data Elevation Model. Created by @der-stefan, @max-dn and others. If you are interested in building your own OpenTopoMap, see the beginner's guides for [a tile server](mapnik/README.md) (but this guide is quite outdated and was made for Ubuntu 16.04 but can be adapted to more modern Linux distributions).

As of 2025-09-25 2 world wide instances exists that I know of : 
* The "main one" is at https://opentopomap.org
* A secondary backup one, whose git repo and README is the one you are reading right now, [visible at openmaps.fr](https://openmaps.fr/#opentopomap-r/5/46.34693/9.27246)

This instance of OpenTopoMap can be used in other applications (Well, as of now 2025-09-25, the tile.openmaps.fr server isn't powerfull enough, so please don't use it for high tile usage).
If you include tiles from tile.openmaps.fr in your project, you must read and accept the [Tile usage policy](https://openmaps.fr/tile-usage-policy.html) where you will also find the URLs for
this map style.

The online renderer is based on Mapnik 3+. All necessary files and instructions are available to build your own OpenTopoMap server.


OpenTopoMap-Revived
===================
This instance, that I'd like to call OTM-R (for OpenTopoMap-Revived or OpenTopoMap-Raster) for the time beeing, aims to be identical to the main instance's map for now and act as a failover/clone/in place replacement. While hoping to get help or time someday to improve the map itself. 
Except for a few changes :
* Contours, hillshading and elevation color was composed and kindly provided by @Yvecai from https://www.opensnowmap.org and based on :
  * ASTER GDEM is a product of METI and NASA
  * SRTM 1 Arc-Second Global
  * EU-DEM: Prroduced using Copernicus data and information funded by the European Union
  * France – RGE ALTI® 5m © IGN
  * Switzerland – Alti3D © swisstopo
  * US & Canada – NED 1arcsec U.S. Geological Survey
  * Austria – DHM 10m - CC-BY-4.0: Land Kärnten - data.gv.at
  * Italy – Tinitaly 10m – CC BY 4.0 Tarquini S., I. Isola, M. Favalli, A. Battistini, G. Dotta (2023). Istituto Nazionale di Geofisica e Vulcanologia (INGV).
  * Norway - DTM 10 Terrengmodell (UTM33) – CC BY 4.0 Kartverket

As a collateral dammage hillshading is now brighter than the original, maybe too bright.

* tiff files (color and shade) were merge into a single tiff with overviews to reduce the xml code and files
* the "contours" table in it's own database was move to the gis database
* the lowzooms tables were put back into the gis database
* the "parking" relevance to hiking trails was abandonned for now (so all parking icons are shown)
* saddle icons orientation was abondonned for now due to lack of quick disk drives

