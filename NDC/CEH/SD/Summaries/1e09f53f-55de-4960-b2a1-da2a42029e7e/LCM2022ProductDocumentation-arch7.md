# The UKCEH Land Cover Map for 2022

- Overview: UKCEH’s LCM2022 is the tenth UK land cover map, produced annually using automated methods. It delivers 21 UKCEH Land Cover Classes linked to Biodiversity Action Plan (BAP) Broad Habitats, across Great Britain (GB) and Northern Ireland (NI) in multiple data formats and resolutions.
- Purpose for GIS users: Provide map-based data products and validation details to support informed decision-making and change detection in UK landscapes.

## Data products and formats

- 10 m Classified Pixel datasets
  - GB and NI versions; each pixel records:
    - Primary band: most likely UKCEH Land Cover Class (integer)
    - Second band: probability/confidence for that class
  - Maintains high detail (no aggregation to Land Parcel framework) to preserve fine features and narrow habitats.
- Land Parcel datasets (derived from 10 m pixels)
  - GB and NI versions; intersect 10 m pixels with the UKCEH Land Parcel Spatial Framework
  - Produce parcel-level attributes (e.g., per-parcel composition, mode, purity, confidence)
- 25 m Rasterised Land Parcel datasets
  - GB and NI versions; rasterise parcel data to 25 m grid
  - Three attributes carried per parcel: dominant land cover (mode), mean confidence (conf), and purity (purity)
- 1 km Summary rasters
  - GB and NI combined; include dominant class per 1 km pixel and percentage cover by class/aggregate class
  - Percentage values are integer-rounded; coastal areas may sum to below 100 due to coastal mapping extents
- Classification Scene and context
  - Seasonal Composite Images (Sentinel-2) combined with Context Rasters to produce Classification Scenes
  - 32 GB Classification Scenes (tile-based grid); 1 NI Classification Scene (single scene)
- Context rasters (10 m)
  - GB: height, aspect, slope; distance to buildings/roads/tidal water/freshwater; foreshore mask; woodland mask; saltmarsh mask
  - NI: height, aspect, slope; urban mask; distance to coast/road/freshwater; foreshore and tidal water masks
- Seasonal composites
  - Derived from Sentinel-2 (four seasons) with gaps handled automatically
  - Bands used: 2,3,4,5,6,7,8,8a,11,12 (plus coastal bands where relevant)
- Output data details
  - 10 m classified pixels: 2 bands (class ID; confidence)
  - 25 m rasterised parcels: 3 bands (dominant class; conf; purity)
  - 1 km rasters: multiple bands for class and aggregate-class percentages

## Methodology and production

- Classification approach
  - Bootstrap Training: automatic generation of training data using historic land map observations; selects training samples with high consistency across multiple years
  - Random Forest classifier: trained on bootstrap samples to produce pixel-level classifications
  - Classifier is designed to balance learning across all classes to avoid dominance by common classes
- Data sources and training
  - Bootstrap Training uses LCM2019, LCM2020, LCM2021 classified pixels; filtered for >80% probability and consistent class across years
  - Some classes (e.g., arable and improved grassland) may rely on alternative training data (e.g., UKCEH Land Cover plus: Crops data) due to rotation-related changes
- Software and workflow
  - Custom UKCEH software integrating WEKA, PostGIS, and GDAL
  - Emphasis on automation to support annual production and enable change-detection capabilities

## Validation and accuracy

- Validation dataset: 33,107 reference points across all 21 classes
- Overall validation accuracy: 86.1% at full thematic detail
- Validation supports assessment of per-class user’s and producer’s accuracies, with detailed matrices provided in accompanying appendices

## Classification scope and structure

- UKCEH Land Cover Classes
  - 21 classes aligned with BAP Broad Habitats (not always identical to BAP definitions)
  - Appendix notes explain nuanced mappings and where divergences occur (e.g., separate Urban vs Suburban, Saltwater vs Freshwater distinctions)
- Relationship to BAP Broad Habitats
  - Generally one-to-one mapping, with some exceptions; italics used to denote BAP references when discussing non-UKCEH classes
- Geospatial framework
  - GB: British National Grid (EPSG:27700)
  - NI: Irish TM75 Grid (EPSG:29903)
  - Land Parcel Spatial Framework used to aggregate 10 m pixels into parcels (MMU ~ 0.5 ha; parcels designed to represent discrete land units)

## Seasonal and contextual detail

- Seasonal Composite Images
  - Four-season Sentinel-2 composites provide temporal differentiation to improve vegetation discrimination
  - Spectral bands used cover visible to shortwave IR with appropriate spatial resolutions
- Context Rasters
  - Added to Classification Scenes to reduce spectral confusion (e.g., distinguishing vegetation from rock, urban, coastal features)

## Citing and data accessibility

- DOIs and citations are provided for each LCM2022 dataset (10 m classified, land parcels, 25 m parcels, 1 km rasters, and related products)
- Users are encouraged to cite the corresponding Marston et al. 2023/2024 papers for production methods and data product descriptions

## Known issues and limitations

- Minor gaps: a small number of polygons missing from vector land parcel products; negligible effect on 1 km rasters, but 10 m classified pixels are unaffected
- Method changes: slight differences in production methods compared with prior years; differences reflect ongoing methodological improvements and may affect cross-year comparisons
- Bootstrap Training limitations: some land-cover transitions (e.g., crop rotations) may be less well captured; alternative training data used for certain classes

## Practical guidance for GIS specialists

- Use the 10 m Classified Pixels for high-resolution mapping and detection of small patches; consult the accompanying confidence band for classification certainty
- Use the 25 m Rasterised Land Parcels for stable parcel-based change detection and integration with vector workflows
- Use the 1 km Summary rasters for broad-scale analyses and rapid visualization over large extents
- Leverage Context Rasters and Seasonal Composite Information to improve classification of spectrally similar land covers
- Consider the given color recipes (Appendix 5 and 6) for displaying Land Cover Classes, including color-blind friendly palettes
- When comparing across years, account for slight methodological differences and MMU-related changes in parcel boundaries

## Appendices and additional references

- Appendix 1–2: Notes on UKCEH Land Cover Classes and relationship to BAP Broad Habitats
- Appendix 3: Full list of LCM2022 datasets and DOIs
- Appendix 4: Correspondence matrices for class-by-class validation
- Appendix 5–6: Recommended colour schemes (standard and color-blind friendly) with QGIS symbology files
- References: Key methodological and historical sources (Breiman 2001; Carrasco et al. 2019; Jackson 2000; Morton et al. 2011; Smith et al. 2007; Marston et al. 2023/2024)