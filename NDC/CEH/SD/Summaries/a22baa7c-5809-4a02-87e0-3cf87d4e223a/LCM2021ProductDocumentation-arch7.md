# The UKCEH Land Cover Map for 2021

## Overview
- The ninth UK land cover map produced by UKCEH, containing 21 UKCEH Land Cover Classes derived from Biodiversity Broad Habitats (BAP) and mapped annually.
- Product comprises six geospatial datasets: three for Great Britain and three for Northern Ireland (GB and NI) including a 10 m classified pixel dataset, a land parcel dataset, and a 25 m pixel rasterised land parcel dataset.
- Created from Classification Scenes that combine Sentinel-2 Seasonal Composite Images with 10 Context Rasters; classification uses Bootstrap Training and a Random Forest classifier.
- Aims for high temporal consistency and change detection capability; annual updates help separate real change from random classification errors.
- Formal validation reports an overall accuracy of 82.6%.

## Product suite and dataset details
- Dataset structure ( appendix references official dataset names in Appendix 3 ):
  - 10 m Classified Pixel datasets (GB and NI): each pixel carries two bands—Band 1 = most likely UKCEH Land Cover Class (integer), Band 2 = class probability/confidence. These preserve fine landscape features and are not generalised by the Land Parcel Spatial Framework.
  - Land Parcel datasets (GB and NI): polygons representing land parcels created by intersecting 10 m Classified Pixels with the UKCEH Land Parcel Spatial Framework; include parcel-level attributes (see Table 3: gid, hist, mode, purity, conf, stdev, agg, n).
  - 25 m Rasterised Land Parcel datasets (GB and NI): three-band rasters per parcel carrying per-parcel Land Cover (mode), conf, and purity.
- 1 km raster products (summary outputs derived from 25 m data): Dominant cover at 1 km (1-band), Percentage cover at 1 km for classes (21 bands) and aggregates (10 bands); values are rounded integers; coastal areas may sum to less than 100% due to coarse resolution and patch sizes.
- Coordinate systems and extents:
  - Great Britain: British National Grid, EPSG 27700; extent 0–700000 m E, 0–1300000 m N.
  - Northern Ireland: TM75 Irish Grid, EPSG 29903; extent truncated to Northern Ireland landmass.

## Data production, inputs and methodology
- Seasonal Composite Images:
  - Derived from Google Earth Engine; Sentinel-2 reflectance, resampled to 10 m; four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) using bands 2, 3, 4, 5, 6, 7, 8, 8A, 11, 12; occasional gaps due to cloud are accommodated by the classifier.
- Context Rasters:
  - Great Britain: height, aspect, slope (NEXTMap); distance to buildings, roads, sea, freshwater; foreshore and tidal masks; woodland mask.
  - Northern Ireland: height, aspect, slope; urban mask; distance to coast, freshwater, roads; foreshore and tidal masks.
- Classification Scenes:
  - GB: 32 Classification Scenes covering GB using a modified Ordnance Survey 100 x 100 km tile system; NI: single 49-band  Sentinel-2 Seasonal Composite Image plus NI context rasters.
  - Each Classification Scene is trained and classified independently, producing 50-band outputs (seasonal + context information) for RF classification.
- Bootstrap Training and Random Forest:
  - Bootstrap Training uses historic land cover maps (LCM2018–LCM2020), filtered to parcels with >80% purity and consistent class across years.
  - Random Forest trained with balanced sampling (10,000 samples per bag) to ensure rare classes are learned; the classifier outputs the 10 m pixel class and associated probability.

## The UKCEH Land Parcel Spatial Framework
- A fixed framework with a minimum parcel area of ~0.5 ha (MMU) used to generalise pixel data into discrete land parcels for stable temporal comparisons.
- Parceled data reduce classification noise and support change detection; note that parcel identifiers (gid) do not match LCM2015 due to framework updates.

## Practical notes for GIS specialists
- 10 m Classified Pixels vs 25 m Rasterised Parcels:
  - 10 m data retain detailed features (e.g., narrow linear features) but have not been generalised to the Land Parcel Spatial Framework; validation has been performed against the 25 m parcel dataset, so users should be aware of scale and validation scope.
- Data use and interpretation:
  - The classifier is designed to distinguish 21 UKCEH Land Cover Classes, with some known inter-class spectral confusion (e.g., various grasslands, bogs, and peatland categories).
  - Saltwater vs Freshwater distinctions rely on context rasters and can exhibit some confusion in tidal rivers and near-coastal zones.
  - Temporal comparisons across years require careful handling of parcel identifiers due to the updated spatial framework.
- Data access and scales:
  - The suite supports detailed analyses at 10 m and aggregated analysis at 25 m parcel level; 1 km summaries provide broader-scale overviews for policy and planning.
- Validation and reliability:
  - Validation points cover all 21 classes; overall accuracy 82.6% with a 95% confidence interval of 82.19%–82.99%.

## Appendices and supplementary information
- Appendix 1–2: Notes on UKCEH Land Cover Classes and BAP Broad Habitat definitions to aid interpretation and cross-walks.
- Appendix 3–4: Full dataset lists and detailed accuracy/confusion matrices; overall accuracy reiterated.
- Appendix 5–6: Colour recipes for displaying UKCEH Land Cover Classes, including color-blind friendly options.
- References: Key sources on Random Forests, Sentinel-2 combinations, and historical LCM methodology.