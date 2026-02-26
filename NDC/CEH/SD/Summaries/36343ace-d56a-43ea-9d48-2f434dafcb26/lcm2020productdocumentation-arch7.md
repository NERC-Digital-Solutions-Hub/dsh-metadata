# The UKCEH Land Cover Map for 2020

- LCM2020 is UKCEH’s annual land cover map, produced with automated methods and no manual region-wide corrections.
- Product scope: six datasets in total, three for Great Britain (GB) and Northern Ireland (NI) each—10m Classified Pixels, Land Parcel Product, and 25m Rasterised Land Parcel Product.
- Aim for GIS use: map-based data products designed to support change detection, temporal consistency, and decision-making for environmental objectives.

## Product suite and datasets

- 10m Classified Pixel datasets (GB and NI)
  - Pixel-level land cover class (UKCEH Land Cover Class) in band 1
  - Band 2 provides the classification probability/confidence
  - No generalisation to the Land Parcel Spatial Framework to preserve detailed features
- Land Parcel datasets (GB and NI)
  - Derived by intersecting 10m pixels with the UKCEH Land Parcel Spatial Framework
  - Includes parcel-level attributes (see Table 3 in the source for fields)
- 25m Rasterised Land Parcel datasets (GB and NI)
  - Raster representation of parcels at 25m resolution
  - Three bands per parcel: dominant class (_mode), mean confidence (_conf), and parcel purity (_purity)
- Coordinate systems and extents
  - GB: EPSG 27700 (British National Grid)
  - NI: EPSG 29903 (Irish Grid)
  - Extents covered as described in dataset specifications

## Data production and workflow

- Classification Scenes
  - GB: 100x100 km tiles; 74 overlapping scenes used to select 36-band Seasonal Composite Images (Sentinel-2) plus 10 Context Rasters to create 46-band Classification Scenes
  - NI: single 43-band Classification Scene per year
  - Overlaps allow ensuring diverse training observations; a manual precedence rule resolves conflicts in GB
- Seasonal Composite Images
  - Derived from Sentinel-2 reflectance bands (bands 2,3,4,5,6,7,8,11,12) across four seasons
  - Median reflectance per season; some gaps due to cloud are allowed and handled by classifier
- Context Rasters (10m)
  - GB: terrain (Height, Aspect, Slope), proximity masks (buildings, roads, sea, freshwater), foreshore and tidal water masks, woodland mask
  - NI: terrain plus urban mask and distances to coast, freshwater, and roads
- UK Land Parcel Spatial Framework
  - Generalised parcel framework with MMU ~0.5 ha
  - Parcels represent discrete real-world units (fields, parks, urban areas, etc.)
  - Some identifiers (gid) do not match LCM2015 due to framework updates
- Bootstrap Training and Random Forest
  - Bootstrap Training automatically samples from historic LCM data (2017–2019) to train a Random Forest
  - Training samples drawn from land parcels; 10,000 pixel samples per class per bag; balanced sampling to avoid dominance by common classes
  - RF classifier yields the 10m Classified Pixel product and associated class probability
- Validation and accuracy
  - Validation against GB countryside survey (2019/2020), open data from National Forest Inventory, IACS, and bespoke validation points
  - Total validation points: 34,715
  - Overall accuracy: 79.2–79.2% (full thematic detail)

## UKCEH Land Cover Classes and mapping relationships

- LCM2020 uses 21 UKCEH Land Cover Classes, linked to Biodiversity Action Plan (BAP) Broad Habitats, with careful distinctions and occasional redefinitions to align with remote sensing capabilities.
- Class naming conventions
  - UKCEH Land Cover Classes use capitalised terms
  - UK BAP Broad Habitats are italicised when explicitly referenced
- Generalised Land Parcel (Aggregate) classes are provided for users who require coarser thematic detail
- Some BAP Broad Habitats are represented by single UKCEH classes or split into multiple UKCEH classes (e.g., Freshwater vs. River/Canal distinctions, Dwarf Shrub and Heath split into Heather and Heather Grassland)

## Data usage notes for GIS work

- The 10m Classified Pixels retain fine landscape detail (e.g., narrow features) because they are not Generalised to the Land Parcel Spatial Framework.
- The Land Parcel products provide a stable basis for change detection and time-series analysis, but parcel identifiers may not align with LCM2015 for direct crosswalks.
- Classification accuracy is validated and suitable for a wide range of environmental monitoring and planning tasks, though some inter-class confusion is acknowledged (Appendix 4 matrices provide detailed accuracy and producer’s/user’s accuracy per class).
- The datasets are designed to support annual mapping, enabling users to distinguish real change from random noise over time.

## Practical implications for GIS specialists

- High-resolution (10m) pixel data enables detailed mapping of land cover and small features; use with care in areas with known spectral confusion.
- 25m rasterised parcel data provides a cleaner, parcel-based time series suitable for change detection and thematic aggregation.
- Context rasters and seasonal composites improve discrimination between spectrally similar classes, especially in complex landscapes.
- Use the GB and NI coordinate systems appropriately when integrating with other spatial layers; ensure alignment of projections and extents.

## Validation and reliability

- Overall accuracy: 79.2% at full thematic detail (Appendix 4)
- Validation data sources include countryside survey, National Forest Inventory, IACS, and bespoke validation points
- The product emphasizes temporal consistency and change detection capabilities across the annual series, with random classification errors expected to flicker over time

## References and appendices (high-level)

- Bootstrap Training description and Random Forest approach
- Appendix 1–3: Notes on UKCEH Land Cover Classes, BAP Broad Habitats, and color recipes for display
- Appendix 4: Detailed confusion matrices and accuracy metrics
- Appendix 5: Full dataset list and naming conventions