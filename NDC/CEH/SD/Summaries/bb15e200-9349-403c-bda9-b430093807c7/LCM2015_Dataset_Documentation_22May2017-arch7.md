# Dataset documentation

- Land Cover Map 2015 (LCM2015) documentation describing the data products, classification methodology, and usage notes for UK-wide land cover mapping.
- Key products: core vector, 25m raster, and 1km raster derivative products.
- Class framework: 21 target land cover classes based on UK Biodiversity Action Plan Broad Habitats (JNCC/Jackson, 2000).
- Data sources: two-date composite satellite imagery primarily from Landsat-8 (30 m) with AWIFS (60 m) as required.

## Introduction and background
- LCM2015 is a parcel-based land cover map of the UK created by classifying satellite data into 21 classes.
- Built on per-pixel classification with a stable spatial framework derived from standard topographic/cartography layers, refined with rural boundary data.
- Designed to support diverse user needs with map-based data products; intended for viewing and exploration by policy colleagues, clients, and the public.

## Differences from LCM2007 (output data and methodology)
- Output data differences:
  - Montane class removed; upland areas reclassified using spectral data (not altitude thresholds) as Inland Rock or other upland habitats.
  - Rough grassland class removed; grassland types re-aligned with JNCC Broad Habitats; no soil data used in LCM2015.
  - 25m raster now two-band (classification in band 1, mean per-polygon probability in band 2).
  - Probability data simplified: vector stores mean polygon probability; 25m raster band 2 stores mean probability; 1km products have no probability data.
  - No spectral sub-classes with Random Forest; grouping into sub-classes deemed unnecessary.
  - Spatial framework: no segmentation-based polygons; per-pixel, segmentation-free approach; segmentation removal reduces complexity for change mapping.
  - Mixed woodland training uses pure stands; training data assembled from stable areas plus coastal/previously mapped areas.
- Methodology differences:
  - New classifier: Random Forest replaces Maximum Likelihood Classifier.
  - Ancillary data (e.g., altitude, soil) are integrated as input data rather than post-classification enhancements.
  - Training data selection emphasizes stable areas and targeted coastal and poorly mapped classes.

## Data products and formats
- Core vector data set (parcel polygons with attributes).
- 25m raster product (two bands).
- 1km raster products (percentage and dominant cover) for both 21-class target set and 10 aggregate classes.
- Spatial separation: Great Britain and Northern Ireland datasets provided separately due to different projections.

## Spatial framework and data structure
- Vector data: polygons with rich metadata per polygon (dominant class, pixel counts per class, uncertainties, and per-polygon probability).
- 25m raster: two bands per pixel (band 1 = dominant class; band 2 = mean per-polygon probability).
- 1km raster: derived by summarising 25m data into dominant class and percentage cover per 1km cell (GB and NI datasets with respective projections).
- Minimum mappable unit: >0.5 ha; parcels smaller than 0.5 ha or linears < 20 m dissolved into surrounding landscape.

## Classes and labeling
- 21 target classes derived from Broad Habitats; some Broad Habitats are subdivided in specific ways (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral categories split as applicable).
- Each parcel receives a unique gid (Geometry ID) in the vector product.
- Colour mapping and class definitions are provided in Appendices (color recipe and class definitions).

## Data access, licensing and DOIs
- 1km raster data accessible via the CEH Environmental Information Platform (eip.ceh.ac.uk).
- Full vector and 25m products available under licence on request from CEH; licensing fees may apply.
- Each LCM2015 product has a DOI for citation (GB and NI products listed with specific DOIs).
- Data citation guidelines emphasize including DOIs in publications (author list, year) and providing full DOI references.

## Projections and data structure details
- Projections:
  - Great Britain: British National Grid (EPSG 27700).
  - Northern Ireland: Irish Grid (TM75 / EPSG 29903).
- Metadata:
  - 25m and 1km raster metadata (extent, pixel size, data type, coordinate system, etc.) provided, with per-product details for GB and NI.

## Cautions, usage guidance and limitations
- Do not use the LCM series for change mapping in their current state due to differences across time and classification errors influencing apparent changes.
- Differences between LCM products reflect real change plus classification and methodological differences; users should validate changes carefully.
- LCM2015 maps land cover, not necessarily land use; some land uses may be spectrally indistinguishable from other cover types.
- Uncertainty information is provided for vector and 25m raster products; 1km products do not include uncertainty data.

## Access to further information
- Project and data information: CEH websites and the CEH Environmental Information Platform.
- Contact: spatialdata@ceh.ac.uk for questions and licensing.
- The LCM2015 dataset paper and additional documentation are available via CEH portals.

## Appendix and technical details
- Appendix 1-3 include class definitions, color mappings, and detailed labeling explanations.
- Appendix 4 describes composite images used in LCM2015 (selection of Landsat 8 and AWIFS images across dates).

- Summary visuals:
  - Figure and table references illustrate data product relationships, with figure comparisons of vector vs. raster detail and the distribution of 1km aggregate products.
  - Table 1 links LCM2015 target classes to aggregate classes and Broad Habitats; Tables 3-5 provide detailed metadata and DOIs for GB and NI products.