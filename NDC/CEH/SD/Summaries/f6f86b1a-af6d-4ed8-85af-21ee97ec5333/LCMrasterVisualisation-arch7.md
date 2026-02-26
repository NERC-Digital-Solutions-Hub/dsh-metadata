# Visualising UKCEH Land Cover Class using a GIS application

- This document explains how to visualize Land Cover Class data contained in band 1 of multi-band land cover rasters (2017–2020).  
- Datasets vary by resolution: 20 m and 10 m rasters have two bands (Band 1: class identifier; Band 2: classification confidence), while 25 m rasters have three bands (Band 1: dominant class identifier; Bands 2–3: confidence).  
- The guide focuses on visualizing band 1 in common GIS applications; refer to the product documentation for a full data description.  

## Visualising in QGIS

- Add the file to your project; it appears in the Layers panel.  
- Open Layer Properties for the layer, select Symbology.  
- Set Render type to Paletted/Unique values, choose Band 1.  
- Click the style button, choose Load style, and select the accompanying LCMcolours_QGIS.qml.  
- Click OK to redraw the map with the correct classification.  

## Visualising in ArcGIS Desktop

- In the Catalog, locate the data folder and expand the raster to show its bands.  
- Drag Band_1 into the Table of Contents.  
- Double-click the layer, open the Symbology tab, and select Unique Values (if prompted to calculate values, confirm).  
- Click the Import button and load the accompanying LCMcolours.lyr.  
- Click OK to redraw the map with the correct classification.  

## Visualising in ArcGIS Pro

- In the Project, open the Catalog, locate the data folder, and expand the raster bands.  
- Drag Band_1 into the Table of Contents.  
- Double-click the layer name to open Layer Properties, then go to Appearance > Symbology.  
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).  
- Use the hamburger menu in the Symbology panel and choose Import; load the LCMcolours.lyr file provided with these instructions.  
- The map will be redrawn with the correct classification.  

## Additional notes

- The color styles (LCMcolours_QGIS.qml and LCMcolours.lyr) accompany these instructions for consistent visualization.  
- The guide is designed for rapid visualization of band 1 classifications across the listed GIS applications; refer to the full product documentation for more detail.