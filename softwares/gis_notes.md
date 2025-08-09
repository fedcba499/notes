## File formats
- Shp - points, lines and polygon
- Shx - index for each feature in shp files
- Dbf - database file, details about each feature in table form
- Tiff - image format
- Fly - Binary file, proprietary format of terraexplorer, settings and properties of terraexplorer file
- Mpt - map terrain database, proprietary formats of terraexplorer, represent terrain and satellite image
- li.mpu - multi resolution map terrain database, proprietary formats of terraexplorer
- Kml - key markup line, open-source, text file by Google


## What is DEM?
DEM stands for Digital Elevation Model. Can be downloaded from JAXA - Japanese Aerospace Exploration Agency, NASA Earth Science, SRTM - Shuttle Radar Topography Mission 1 arc resolution or 30 m resolution and from Bhoonidhi Portal.

## Plugins in QGIS
| Library | Functionality |
| --- | --- |
| Terrain profile | profile section of any location with respect to DEM file |
| Least cost path | best path using slope file( created from DEM file) |
| QuickOSM | convert OSM files into shp files |
| Plugin-Builder | To create custom plugin for QGIS |
| Reloader | Instead of reopening qgis, reloader eases work to see changed effects to plugin |
| Qt Designer | Can be used to create UI elements for plugins we build. Extension is qt |

## Bhoonidhi portal 
Latest Optical image data can downloaded for free using LISS 4 (Linear Imaging self scanning  sensor) of resolution of 5m of vintage of 4 - 5 days.
- satelite - resourcesat - 2.
- sensor type - LISS4.
- rotation - 22 days.

## optical image

- EOS - 06 (enhanced oceansat series - low res but regular cover)
- OCM-3 - Ocean Color Monitor is useful sensor for us
- LAC - Local Area Coverage - 366m res
- like LISS 4 Sensor of resoursesat
- AWiFS  - Advanced wide field sensor (res - 54m revisit 5 days)
- IRS (30 m res - discontinued) < Resourcesat(liss 4 - 5m res) < cartosat(1m res)
- Landsat 8/9 (res 15, 30, 100m res) revisit 8 days
- OLI Sensor - Operational Land Imager 
- TIRS Sensor - Thermal Infrared Sensor
- DEM - Cartosat DEM 30 m res ( 1 arc sec res ) free download ver 3
- Thematic maps incl - DEM, Land Cover maps etc

## Landsat Dataset
band 2 - Blue
band 3 - green
band 4 - red

## LISS 4 dataset
band 2 - green
band 3 - red
band 4 - NIR (Near Infrared)

## Landsat 8-9 Level-1
The data from this collection is available within 4-6 hours of acquisition for Landsat 9, and within 4-11 days for Landsat 8. 

## Landsat 8-9 Level-2
The data from this collection includes: 
Surface reflectance: Derived from Level-1 data, this product is atmospherically corrected 
Surface temperature: This product measures the Earth's surface temperature in Kelvin. It's useful for monitoring crop health, extreme heat events, and more

## Tips & Tricks
- bbbike.com for vector files of a particular location, files are from open street maps platform. In bbbike vector files are classified into roads, building etc
- SAS Planet - sasgis.org
