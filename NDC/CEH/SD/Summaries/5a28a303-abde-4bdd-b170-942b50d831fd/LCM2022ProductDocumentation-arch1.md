# The UKCEH Land Cover Map for 2022

- LCM2022 comprises seven datasets (three GB/NI each for 10 m classified pixels, land parcels, and 25 m rasterised land parcels) plus a 1 km summary raster for Great Britain and Northern Ireland.
- 21 UKCEH Land Cover Classes are defined, linked to Biodiversity Action Plan (BAP) Broad Habitats; classifications are based on UKCEH-defined classes with careful mapping to BAP concepts.
- Formal validation reports an overall accuracy of 86.1% across all classes; validation used 33,107 reference points from GB and NI.

## Data products and structure

- 10 m Classified Pixel datasets
  - Separate GB and NI products; first band = most likely UKCEH Land Cover Class, second band = classification confidence for that class.
  - No generalisation with the UKCEH Land Parcel Spatial Framework to preserve fine landscape details.
- Land Parcel datasets
  - Intersect 10 m Classified Pixels with the UKCEH Land Parcel Spatial Framework to create parcel attributes (land parcels as analysis units).
- 25 m Rasterised Land Parcel datasets
  - Rasterised version of parcels (GB and NI) with three bands: dominant land cover (mode), confidence (conf), and purity (purity).
- 1 km summary rasters
  - Summaries of 25 m data to 1 km resolution: dominant class per 1 km pixel, and percentage cover (for 21 classes) plus aggregate classes (10 bands).
  - Rounding can cause the 1 km percentage sums to deviate from 100; coastal areas may sum to less than 100 due to partial coastal mapping.
- Coordinate systems and extents
  - GB: British National Grid (EPSG 27700); NI: Irish Grid (TM75; EPSG 29903).
  - GB and NI parcel counts and extents are documented (e.g., GB ~6.7 million parcels; NI ~0.9 million parcels).
- Software and formats
  - Uses a bespoke RF classification pipeline integrating Weka, PostGIS, and GDAL; all tools are open source.

## Data production and methodology

- Seasonal Composite Images
  - Derived from Google Earth Engine using Sentinel-2 data; four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) with 10-band spectral information plus contextual data.
  - 60 m and 10–20 m band resolutions per band; occasional data gaps exist due to cloud, but classification tolerates incomplete spectra.
- Context Rasters
  - 10 m context rasters to reduce spectral confusion (e.g., terrain, proximity to buildings/roads, water, foreshore, woodland, saltmarsh).
  - GB and NI use tailored context rasters to address regional differences in landscape and data availability.
- Classification Scenes and Tile Layout
  - GB: grid of 32 Classification Scenes (~100 x 100 km tiles); NI: single 49-band scene for Northern Ireland (40 Sentinel-2 bands + NI-specific context rasters).
- Bootstrap Training
  - Automatic training set created without fresh field data by sampling historic LCM data (LCM2019–LCM2021) with >80% probability and consistent class across years.
  - Large bootstrap training sets emphasize the dominant signal; minority class signals are balanced via sampling.
  - Visual example shows Bootstrap Training data feeding into the RF classifier to produce the LCM2022 classification.
- Random Forest classification
  - 10,000 samples per bag, balancing classes to strengthen learning for rarer classes.
  - RF classifier outputs the most probable class per 10 m pixel and an associated probability/confidence measure.
- UK Land Parcel Spatial Framework
  - Frame used to generalise 10 m pixels into parcels, with a 0.5 ha minimum mapping unit (MMU).
  - Parcels help reduce noise and enable consistent temporal comparisons; parcel identifiers (gid) differ from LCM2015 identifiers due to framework updates.
- Validation and quality assurance
  - Validation dataset (33,107 points) spans all 21 classes; overall accuracy = 86.1% (producer’s and user’s accuracies vary by class).
  - Validation used 25 m rasterised parcels for accuracy assessment; 10 m classified pixels remain uncoupled from those validation results.

## Known issues and cautions

- Some polygons are missing from the vector land parcel products, causing nodata areas in the 25 m rasterised land parcels; impact on 1 km products is negligible.
- The annual production method can introduce minor methodological differences year to year; observed changes may reflect method changes as well as real land-cover change.
- Some spectral confusions persist among Complex habitats (notably between Bog, Heather/Heather Grassland, Fen/Marsh/Swamp, and acid-neutral grassland blends); context rasters help mitigate but do not eliminate all misclassifications.
- Saltwater and Freshwater distinctions near coasts can be ambiguous in tidal areas.

## Accessibility, citations, and data lineage

- Each LCM2022 dataset has a DOI; table of DOIs provided for 10 m classified pixels, land parcels, 25 m rasterised land parcels, land parcels (vector), and 1 km summary rasters.
- Key references include Marston et al. (2024a–g) for GB/NI datasets and Marston et al. (2023) for LCM2021 methodology; previous UKCEH/Land Cover Map lineage from 1990 onwards is noted.
- A formal disclaimer notes that recent maps may reflect methodological changes in addition to real land-cover changes.

## Appendices and classification details

- Appendix 1: Notes on UKCEH Land Cover Classes (and how they relate to BAP Broad Habitats), including nuanced definitions and potential confusion between closely related classes.
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats glossary with detailed class definitions and mapping notes.
- Appendix 3: Full list of datasets for UKCEH LCM2022 with dataset names, DOIs, and citations.
- Appendix 4: Correspondence matrices showing observed vs. predicted per-class accuracies and user/producer accuracies.
- Appendix 5 & 6: Recommended color recipes for displaying UKCEH Land Cover Classes, including color-blind friendly variants and accompanying QGIS symbol files.
- Appendix 4 also provides per-class accuracy metrics (producer’s and user’s accuracy) and overall confusion patterns.

## Usage notes and recommendations

- The LCM2022 dataset suite is designed to monitor state and change in the UK countryside and to support environmental objectives, with annual updates intended to improve temporal consistency and change-detection capabilities.
- Users should cite the appropriate DOIs when using each data product and consider the 1 km percentage sums and potential coastal rounding effects in area calculations.
- For practical use, refer to the color schemes and QGIS files in appendices to ensure consistent visualization and interpretation across platforms.