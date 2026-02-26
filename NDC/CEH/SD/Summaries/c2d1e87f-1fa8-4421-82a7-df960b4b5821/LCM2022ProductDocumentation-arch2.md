The UKCEH Land Cover Map for 2022

## Purpose and scope
- Annual UK land cover map (LCM2022) created by UKCEH to support monitoring of environmental health, state, and change over time.
- Produces 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) across Great Britain and Northern Ireland.
- Aims to maximise temporal consistency for change detection and to differentiate real change from method-related variation.
- Formal validation reports an overall accuracy of 86.1% at full thematic detail.

## What the LCM2022 comprises
- Seven datasets total, three for Great Britain and three for Northern Ireland, plus a 1 km summary raster product covering GB and NI.
  - 10 m Classified Pixels (GB and NI)
  - 25 m Rasterised Land Parcels (GB and NI)
  - Land Parcel Spatial Framework (used to derive parcel-level attributes)
  - 1 km summary rasters (dominant class and percentage cover)
- Appendix and tables provide data names, coordinate systems, and validation details.

## Data production and processing workflow
- Classification Scenes
  - GB: 32 Classification Scenes created on a modified OS tile grid; NI: a single Scene using the minimum bounding rectangle of NI land mass.
  - Each scene is trained and classified independently to manage regional phenology and processing.
- Seasonal Composite Images
  - Sentinel-2 data resampled to 10 m; four seasonal composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) used to provide temporal information.
- Context Rasters
  - 10 m context layers to reduce spectral confusion (terrain, proximity to buildings/roads, coastal/flood-related masks, etc.).
  - GB and NI contexts differ in some layers (e.g., urban masks for NI; coastal and water-related masks for GB).
- Bootstrap Training and Random Forest
  - Bootstrap Training uses historical LCMs (2019–2021) to automatically generate training data, reducing need for new field data.
  - Random Forest classifier derives class membership with a probability for each pixel; the highest probability class is chosen.
  - Training samples are balanced to prevent dominance by common classes.
- Land Parcel Framework
  - 0.5 ha minimum parcel size; parcels aggregate 10 m pixels to reduce noise and enable change detection over time.
  - Parcel datasets used to produce 25 m rasterised land parcels (band 1: dominant class, band 2: mean confidence, band 3: purity).

## Data structure and formats
- 10 m Classified Pixel datasets (GB and NI)
  - Two bands: class (UKCEH Land Cover Class) and associated confidence/probability.
  - No generalisation to land parcel framework to preserve fine-scale details (e.g., small patches, narrow features).
- Land Parcel datasets
  - Vector parcels (gids and attributes) and 25 m rasterised parcels (three bands: mode, conf, purity).
  - Extent and projection: GB uses British National Grid (EPSG: 27700); NI uses Irish Grid (TM75, EPSG:29903).
  - GB parcel count ≈ 6.74 million; NI parcel count ≈ 902k.
- 1 km raster products
  - Dominant class per 1 km cell (for both GB and NI).
  - Percentage cover per class per 1 km cell (21 class layers; 10 aggregate layers).
  - Rounding can cause sums to differ slightly from 100%.
- Seasonal, Context, and Classification details
  - Context rasters provide terrain and proximity information to help disambiguate spectrally similar classes.
  - Seasonal composites provide four-season reflectance signals used in classification.

## Data accuracy and validation
- Validation dataset: 33,107 reference points across all 21 classes.
- Overall thematic accuracy: 86.1%.
- Producer’s accuracy and user’s accuracy matrices provided (detailed per-class performance).

## Relationship to UK BAP Broad Habitats
- The UKCEH Land Cover Classes map directly extends the UK BAP Broad Habitat framework but is not identical to BAP categories.
- Appendices describe mappings and the nuances of translating between UKCEH classes and BAP Broad Habitats; some BAP classes are split or combined to suit spectral separability and mapping goals.
- Special notes on ambiguous or spectrally similar classes (e.g., acid vs. neutral grassland, bog vs. heath, freshwater vs. saltwater near coast).

## Practical implications for monitoring and analysis
- Annual maps support change detection and separation of real land cover change from classification noise.
- Rich time-series potential due to the annual cadence and automated Bootstrap Training approach.
- Provides datasets at multiple spatial resolutions (10 m; 25 m parcel-level; 1 km summaries) and parcel-based analytics for change analysis.
- Users should treat the 10 m Classified Pixels as high-detail but not fully validated against the 25 m parcel dataset; validation focuses on the 25 m raster dataset.

## Known issues and caveats
- Minor polygons missing in the vector Land Parcel products; negligible effect on 1 km raster products; 10 m pixels unaffected.
- Parcel identifiers (gid) do not match LCM2015 identifiers due to Framework reordering; cross-year parcel comparisons may require spatial overlap rather than id matching.
- Some spectral confusions persist among certain habitat types (notably bog, heath, acid/calcareous grasslands, and mixed habitats in complex mosaics).
- Differences in methodology across the annual series may introduce small discrepancies; changes reflect both real land cover change and methodological updates.

## Access, citation, and metadata
- Each LCM2022 dataset has a DOI; recommended citations provided (Marston et al. 2024a–g; specific to GB/NI, 10 m, 25 m, land parcels, and 1 km rasters).
- Users should cite the appropriate dataset DOI and consider Marston et al. (2023/2024) for production method context.
- Appendix 5 and 6 provide recommended color recipes for mapping, including color-blind friendly options.

## Appendix highlights (for reference)
- Appendix 1: Notes on UKCEH Land Cover Classes and interpretation with BAP Broad Habitats.
- Appendix 2: Summary of BAP Broad Habitats definitions and how they relate to UKCEH classes.
- Appendix 3: Full list of LCM2022 datasets and DOIs.
- Appendix 4: Detailed correspondence/accuracy matrices by class (confusion, user, and producer accuracies).
- Appendix 5 & 6: Color schemes for displaying UKCEH classes (standard and color-blind friendly).
- Data and methods are supported by references to foundational works on RF classification, Bootstrap Training, Sentinel-2 seasonal composites, and prior LCM editions.