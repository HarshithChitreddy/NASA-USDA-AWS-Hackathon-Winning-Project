## Watershed Folder Contents
- Lidar_DEM_Hillshade
    - [Watershed name]_BareEarth_DEM_1m.tif
        - Lidar-derived bare earth digital elevation model. Elevation of the earth's surface. Resolution of these data is 1 meter. This file and its metadata can be read with Python packages like Rasterio, Rioxarray, and gdal among others.
    - [Watershed name]_BareEarth_Hillshade_1m.tif
        - Transformation of the bare earth digital elevation model that assuming a lighting source at a specific altitude and azumuth. When visualized, this shows the terrain as if its being illuminated by the sun. Very useful in identifying the location of roads. Resolution of these data is 1 meter. This file and its metadata can be read with Python packages like Rasterio, Rioxarray, and gdal among others.
    - *.json
        - Metadata about the GeoTIFF including coordinate system. 
    - *.tif.aux.xml
        - More GeoTIFF metadata including band statistics. (useful for visualizing in GIS)
- NAIP
    - [Watershed name]_2023_NAIP_1m.tif
        - Aerial imagery collected by the National Agricultural Imagery Program with 3 channels: blue, green, red, and near-infrared (nir). These data are exactly aligned with the lidar-derived dem's and can be stacked for analysis. Resolution of these data is 1 meter. Visualization of RGB channels will show true color representation. Visualization where the red band is replaced with nir, the green band is replaced with red, and the blue band is replaced with green will highlight areas with vegetation. This file and its metadata can be read with Python packages like Rasterio, Rioxarray, and gdal among others.
    - [Watershed name]_2023_NAIP_06m.tif
        - Aerial imagery collected by the National Agricultural Imagery Program with 3 channels: blue, green, red, and near-infrared (nir). These data are not aligned with the dem's and cannot be stacked for analysis without additional image warping. This file and its metadata can be read with Python packages like Rasterio, Rioxarray, and gdal among others.
    - *.json
        - Metadata about the GeoTIFF including coordinate system. 
    - *.tif.aux.xml
        - More GeoRIFF metadata including band statistics. (useful for visualizing in GIS)
- Roads_Boundary
    - [Watershed name]_Bounds.shp
        - ESRI shapefile (vector data) delineating the bounds of the watershed. This file can be read with Python packages like GeoPandas.
    - [Watershed name]_Roads.shp
        - ESRI shapefile (vector data) delineating the road network within the watershed. This file can be read with Python packages like GeoPandas.
    - [Watershed name]_Roads_Mask.tif
        - Rasterized verion of the Roads.shp shapefile. Values of 1 indicate roads, values of 0 are not roads. These data are exactly aligned with the lidar-derived dem's and can be stacked for analysis. Resolution of these data is 1 meter. This file and its metadata can be read with Python packages like Rasterio, Rioxarray, and gdal among others.
    - [Watershed name]_*.cpg
        - ESRI shapefile support file that allows for interpreation of test characters in the shapefile's tabular data (dataframe). This file can be read with Python packages like GeoPandas.
    - [Watershed name]_*.dbf
        - ESRI shapefile support file that stores the tabular data (dataframe) associated with the shapefile's geometries (lines, points, polygons). This file can be read with Python packages like GeoPandas.
    - [Watershed name]_*.prj
        - ESRI shapefile support file that stores information about the coordinate reference system used for the geometries (lines, points, polygons) in the shapefile. This file can be read with Python packages like GeoPandas.
    - [Watershed name]_*.sbn
        - ESRI shapefile support file that stores binary spatial index for the shapefile. This file can be read with Python packages like GeoPandas.
    - [Watershed name]_*.sbx
        - ESRI shapefile support file that stores the spatial index for the shapefile and is used to speed up spatial queries. This file can be read with Python packages like GeoPandas.
    - [Watershed name]_*.shp.xml
        - ESRI shapefile support file that stores additional metadata about the shapefile. This file can be read with Python packages like GeoPandas.
    - *.json
        - Metadata about the GeoTIFF including coordinate system. 
    - *.tif.aux.xml
        - More GeoTIFF metadata including band statistics. (useful for visualizing in GIS)

    