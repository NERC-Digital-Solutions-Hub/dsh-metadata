# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

## Purpose and Scope
- User guide for three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Each map provides a suite of geospatial datasets describing land cover across Great Britain and Northern Ireland.
- Emphasizes understanding production, validation, and planning for informed use, beyond mere structure and content.

## Data Content and Structure
- 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitat framework; aim to match earlier maps (LCM2015/2007/2000) for comparability.
- Dataset package (42 total datasets, GB and NI per year):
  - 20m Classified Pixels: new RF-based pixel classifications with per-pixel class and a second band indicating confidence (0–100).
  - Land Parcels: polygons from the UKCEH Land Parcel Spatial Framework with parcel-level attributes related to class composition, confidence, and dominance.
  - 25m Rasterised Land Parcels: three-band rasters (dominant class, confidence, purity) derived from the Land Parcels.
  - 1km Raster Datasets: Percent Cover (21 bands), Percent Aggregate Cover (10 bands), Dominant Cover (1 band), and Dominant Aggregate Cover (1 band).
- Geographic scope and formats:
  - GB data: Great Britain extents in British National Grid (EPSG:27700); NI data: Northern Ireland in Irish Grid (EPSG:29903).
  - Pixel sizes: 20m (classified pixels), 25m (land parcels rasterised), 1km grids for summary products.
- Data lineage and documentation: Clear dataset descriptions, including minor attribute changes from LCM2015 and notes on projection, extents, and pixel geometry.

## Production and Methodology
- Bootstrap Training and Random Forest (RF) classification:
  - Bootstrap Training uses historic UKCEH LCMs (primarily 2015) to automatically generate spectral training observations for current Sentinel-2 seasonal composites.
  - RF classifier trained with balanced sampling (10,000 samples per class per training bag) to derive 20m Classified Pixels.
- Seasonal imagery and context:
  - Sentinel-2 seasonal composites (TOA reflectance) created for winter, spring, summer, and autumn using certain bands; up to four-season data per location.
  - Production uses 10 Context Rasters (terrain, proximity to features) added to Seasonal Composite Images to form Classification Scenes and reduce spectral confusion.
- Classification Scenes and tiling:
  - Great Britain classified using 100x100 km overlapping tiles (36-band seasonal composites plus 10 context layers, total ~46 bands per scene); 74 GB Classification Scenes classified independently with overlaps to ensure robust training variation.
  - Northern Ireland classified with a single 43-band scene per year.
- Land Parcel Spatial Framework:
  - Framework retained from LCM2007/2015 lineage; 0.5 ha MMU; parcels designed to reflect discrete land units (fields, urban areas, woodlands, etc.).
  - gid identifiers are new across years; direct parcel-id comparisons to LCM2015 are not possible, but gid-based comparisons across 2017–2019 are valid.
- Data refinement and validation:
  - No manual corrections applied in this release to maintain automation; however, extensive visual checks and formal validation were performed.
  - Validation involved 22,325 points against GB countryside survey, National Forest Inventory, IACS, and bespoke LCM validation points.
- Future data and monitoring:
  - Ongoing evaluation of input data (TOA vs SR) and exploring use of Sentinel-1 SAR to fill gaps.
  - Plans to potentially broaden input data types and update strategies over time.

## Data Quality, Validation, and Limitations
- Overall accuracy:
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation notes:
  - Validation points derived from multiple data sources with some legacy-class mapping (not exact, requiring subjective schema conversions).
  - Validation data currency varies by product; the same validation points were used for all three products, influencing per-product currency.
  - Approximately 80% correspondence across products is considered strong for an automatically produced 21-class map; higher accuracy may be achieved with future methodological refinements.
- Class-level considerations and known issues:
  - Some spectral confusion persists among upland vegetation types, bracken vs acid grassland, bog vs other peatland components.
  - Saltwater vs Freshwater and coastal dynamics rely heavily on context rasters and can suffer in tidal regions.
  - Linear features (e.g., hedgerows, walls) are not systematically classified as explicit UKCEH Land Cover Classes; their detection may improve with finer resolution in future iterations.
  - The 21-class scheme is designed to maintain compatibility with prior maps for change detection, even if new classes could be more separable with richer training data.
- Data accuracy indicators:
  - Per-class producer’s and user’s accuracies are provided in Appendix 4 confusion matrices, highlighting strengths in some classes (e.g., Urban, Saltmarsh, Freshwater) and weaknesses in others (e.g., Heather Grassland, Acid Grassland).

## Accessibility, Usage, and Data Governance
- Data products and release lifecycle:
  - Yearly updates (LCM2017, LCM2018, LCM2019) with a consistent production pipeline designed to enable rapid generation of UK-wide maps.
  - 42 datasets across years and regions enable both detailed analysis at fine scale (20m Classified Pixels, Land Parcels) and broad summaries (1km rasters).
- Metadata and interpretation:
  - Appendices provide essential metadata, including a mapping between UKCEH Land Cover Classes and UK BAP Broad Habitats, with detailed notes on detection limitations and context improvements.
  - Appendix 3 provides recommended RGB color recipes for visualization of all 21 classes.
- Data stewardship considerations:
  - gid identifiers are year-specific due to the UKCEH Land Parcel Spatial Framework changes; users must rely on gid for cross-year parcel comparisons (LCM2017–LCM2019) rather than historical parcel IDs.
  - Clear documentation of data structure, attribute definitions, and changes from LCM2015 supports reproducibility and governance.
- Dataset naming and organization:
  - Full list of datasets and their GB/NI scope is provided (Appendix 5), including the 20m Classified Pixels, Land Parcels, 25m Rasterised Parcels, and 1km summary rasters.

## Appendix Highlights (Relevance to Data Stewards)
- Appendix 1–2: UKCEH Land Cover Classes and Biodiversity Action Plan Broad Habitats; detailed notes on class derivation, detection limitations, and contextual considerations for key habitats.
- Appendix 3: RGB color recipes for displaying each UKCEH Land Cover Class, facilitating consistent visualization across platforms.
- Appendix 4: Validation confusion matrices by year; per-class accuracy measures and summary producer’s/user’s accuracies to inform quality assurance and future improvements.
- Appendix 5: Full listing of datasets per LCM2017/2018/2019, detailing dataset types and geographic scope for governance and access control.

## Practical Takeaways for Data Stewards
- The LCM2017–LCM2019 suite provides a robust, automated, well-documented set of land cover datasets at multiple spatial scales, suitable for change detection and national-scale analysis, with clear governance through consistent metadata, versioning, and provenance.
- The 20m Classified Pixels dataset offers rich per-pixel classification confidence, while Land Parcels provide a structured, parcel-based summary with lineage preserved through the Land Parcel Spatial Framework.
- Be mindful of gid changes across years and the limitations of cross-year parcel comparisons; use gid-based cross-year alignment within 2017–2019 for change assessment.
- Validation results show strong overall performance but class-specific caveats exist; leverage Appendix 4 for targeted quality assurance and consider ongoing improvements in response to identified confusions.
- Practical use requires attention to visualization mappings (Appendix 3) and an understanding of the 21-class structure and its relation to BAP Broad Habitats (Appendices 1–2).