OpenTopoMap
===========
OpenTopoMap is a topographic map style out of data from OpenStreetMap and SRTM. If you are interested in building your own OpenTopoMap, see the beginner's guides for [a tile server](mapnik/README.md).

As of 2025-09-25 2 world wide instances exists that I know of : 
* The "main one" is at https://opentopomap.org
* A secondary backup one, whose git repo and README is the one you are reading right now, visible at https://openmaps.fr/?layers=0B0 

This instance of OpenTopoMap can be included into other applications (Well, as of now 2025-09-25, the tile.openmaps.fr server isn't powerfull enough, so please don't use it for high tile usage).
There isn't any written Usage policy right now, so in the mean time, use the same as the OpenStreetMap Tile usage policy :  https://operations.osmfoundation.org/policies/tiles/
+ be warn that in case of high usage slowing the server, I might block your accesses

The online renderer is based on Mapnik. All necessary files are available to build your own OpenTopoMap server.


OpenTopoMap-Revived
===================
This instance, that I'd like to call OTM-R (for OpenTopoMap-Revived or OpenTopoMap-Raster) for the time beeing, aims to be identical to the main instance's map for now and act as a failover/clone/in place replacement. While hoping to get help or time someday to improve the map itself. 
Except for a few adjustements :
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

In the process hillshading was made brighter to help readability of contours alitude

* tiff files (color and shade) were merge into a single tiff with overviews to reduce the xml code and files
* the "contours" table in it's own database was move to the gis database
* the lowzooms tables were put back into the gis database
* the "parking" relevance to hiking trails was abandonned for now (so all parking icons are shown)
* saddle icons orientation was abondonned for now due to lack of quick disk drives

