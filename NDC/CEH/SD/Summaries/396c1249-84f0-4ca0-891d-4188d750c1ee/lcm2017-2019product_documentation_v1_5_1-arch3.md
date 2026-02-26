# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

- The document is a user guide accompanying three new UKCEH land cover maps: LCM2017, LCM2018, and LCM2019.
- It explains content, production methods, validation, terminology, and future plans to help users apply the data appropriately.

## Aim and scope

- Provide UK-wide land cover maps in 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) with rapid, automatic production.
- Emphasise understanding production decisions, data sources, validation, and planned improvements to inform current and future work.

## Data production approach

- Production is automatic (no manual corrections used this cycle) to enable annual updates.
- Bootstrap Training: uses historic LCM2015 data to seed training. Parcels with high purity (≥99%) from LCM2015 form the training set for a Random Forest (RF) classifier.
- Goal is to leverage the majority signal from historic maps to bootstrap new maps (2017–2019) and progressively improve with future updates.

## Core classification methodology

- Random Forest classification trained on Bootstrap Training data; 10,000 samples per class per 10000-pixel bag, balanced across classes.
- Production software integrates Weka, PostGIS, and GDAL; uses open-source tools.
- Seasonal information: Sentinel-2 Seasonal Composite Images (TOA reflectance) per season (winter, spring, summer, autumn) at 20 m resolution, combined with 20 m Context Rasters to form Classification Scenes.
- Google Earth Engine supplies 4-season composites and context layers; in GB, Classification Scenes are 100 x 100 km tiles (46-band scenes); in Northern Ireland, a single 43-band scene per year.

## Data inputs and contextual information

- Seasonal Composite Images: median TOA reflectance per season from Sentinel-2 (bands 2,3,4,5,6,7,8,11,12); cloud gaps exist but classification tolerates gaps.
- Context Rasters (20 m): terrain (Height, Aspect, Slope) plus proximities (distance to buildings, roads, sea, freshwater), foreshore, tidal water, woodland, etc., to reduce spectral confusion.
- Context examples help separate spectrally similar classes (e.g., coastal vs urban areas).

## UKCEH Land Parcel Spatial Framework

- Parcels: discrete land units (~0.5 ha MMU) used to summarize 20 m classified pixels into fixed units.
- gid remains the permanent identifier, but gid values do not match LCM2015 parcels; cross-year comparison by overlap is preferred.
- Land parcel attributes per parcel (Table 5): hist, mode, purity, conf, stdev, n.
- Framework supports downstream analyses and change detection; original framework may be refined as resolution increases.

## Output products and dataset structure

- 20 m Classified Pixels: new addition; RF classification results with per-pixel class and a per-pixel confidence (0–100 scale). Keeps detailed landscape features (e.g., narrow patches) not generalized by parcels.
- Land Parcels: 20 m classified pixels summarized within parcels; includes hist as a list of class counts, mode, purity, conf, stdev, and n.
- 25 m Rasterised Land Parcels: three-band raster (band 1 = modal class, band 2 = confidence, band 3 = purity).
- 1 km rasters (GB and NI): 
  - 1 km Percent Cover (21 bands)
  - 1 km Percent Aggregate Cover (10 bands)
  - 1 km Dominant Cover (1 band)
  - 1 km Dominant Aggregate Cover (1 band)
- Extents and formats:
  - Great Britain (GB) datasets use EPSG 27700 (British National Grid).
  - Northern Ireland (NI) datasets use EPSG 29903 (Irish Grid).
  - Pixel resolutions: 20 m (classified), 25 m (land parcels), 1 km grids.
- Annual product composition: GB and NI datasets per year yield a total of 42 datasets across three years (GB and NI, 21-class + parcel products).

## Classification workflow specifics

- GB classification uses 74 overlapping 100 x 100 km tiles; NI uses a single tile per year.
- Overlaps are resolved by visual inspection to select the best results; this is the only manual judgment in the GB production process.
- The Classification Scenes are designed to balance training observations and phenological variation across the landscape.

## Dataset references and metadata

- Dataset descriptions align with the 21 UKCEH Land Cover Classes and an aggregate class set; crosswalks with UK BAP Broad Habitats are provided (Appendices 1 and 2).
- The 20 m Classified Pixels dataset preserves detailed patterns not captured in parcel-aggregated products.
- Attributes for Land Parcels are adjusted to align with production software naming conventions (some renaming from LCM2015).

## Validation and accuracy

- Validation conducted against GB countryside survey (2019), National Forest Inventory, IACS, and bespoke LCM validation points (22,325 points).
- Reported overall accuracies at UK scale:
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation points are not perfect ground truth and are subject to cross-mapping adjustments; accuracy is a best available indicator and is expected to improve with method refinements.

## Practical notes, caveats, and interpretation

- The relationship between UKCEH Land Cover Classes and BAP Broad Habitats is nuanced; many BAP categories are not exactly detectable spectrally. The guide explains how UKCEH classes map to BAP Broad Habitats and where confusion may occur.
- The Land Parcel Spatial Framework is a fixed summary structure; cross-year parcel identifiers (gid) do not align with LCM2015, complicating direct parcel-level comparisons across years.
- Some classes (e.g., Saltwater vs Freshwater) show spectral similarity; context rasters help mitigate misclassifications but users should be aware of potential coastal misclassifications.
- The 20 m Classified Pixels dataset is preferred for high-detail mapping, while parcel-aggregated products support change detection and broader-scale analyses.
- Data governance and metadata considerations are acknowledged; sharing underlying data and ensuring metadata quality can be barriers for some datasets.

## Appendices and background information

- Appendix 1: Notes on UKCEH Land Cover Classes (class definitions, detection considerations, and typical confusions).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions and mappings to UKCEH classes.
- Appendix 3: Recommended RGB color recipe for displaying UKCEH Land Cover Classes.
- Appendix 4: Validation details, confusion matrices, and accuracy metrics per year and per class (illustrative but extensive).
- Appendix 5: Full list of datasets for LCM2017, LCM2018, and LCM2019 (dataset names and storage references).

## Future directions and planning

- The authors plan annual map releases and ongoing evaluation of bootstrap training strategies with the aim of improving accuracy and timeliness.
- Exploration of additional satellite data inputs (e.g., Sentinel-1 SAR) and alternate gap-filling strategies to handle seasonal/cloud gaps.
- Potential refinements to the UKCEH Land Parcel Spatial Framework as higher-resolution data become available and as new training data are generated.