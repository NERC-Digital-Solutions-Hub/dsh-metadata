# The UKCEH Land Cover Map for 2020

- The LCM2020 is UKCEH’s land cover map product for 2020, delivered as a set of six geospatial datasets (three per region, GB and Northern Ireland): 10 m classified pixel datasets, a dataset of classified land parcels, and a 25 m pixel rasterised land parcel dataset. A full suite also includes 1 km summary rasters. Outputs cover Great Britain and Northern Ireland, with corresponding coordinate systems and extents.
- The product provides 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan Broad Habitats, mapped from Sentinel-2 Seasonal Composite Images plus 10 Context Layers, using Bootstrap Training and Random Forest classification.
- Validation indicates an overall accuracy of just over 79% (79.2% reported for full thematic detail). The validation draws on GB countryside survey data (2019/2020), open data (National Forest Inventory, IACS), and bespoke validation points (34,715 locations).

- LCM2020 aims to support informed decision-making on land cover and change monitoring, with annual production to improve temporal consistency and enable change detection. Manual corrections from earlier maps are no longer performed at scale; the annual series helps distinguish real change from classification errors, which are expected to be random in space/time.

## Data Products and Datasets

- 10 m Classified Pixel datasets
  - Separate for Great Britain and Northern Ireland.
  - Each pixel’s first band indicates the most likely UKCEH Land Cover Class; the second band provides the associated class membership probability (confidence).
  - These pixels preserve fine landscape detail (no generalisation via the Land Parcel Spatial Framework) intended for specialist use.
- Land Parcel datasets
  - Intersect the 10 m Classified Pixels with the UKCEH Land Parcel Spatial Framework to create parcel-level attributes.
- 25 m Rasterised Land Parcel datasets
  - Raster products derived from the Land Parcel framework, carrying three attributes per parcel: dominant land cover (_mode), mean confidence (_conf), and parcel purity (_purity).
- 1 km Raster products (summary rasters)
  - Summaries of 25 m rasters to provide dominant and percentage cover per 1 km pixel, for both class and aggregate class levels.
- UK coordinate systems and extents
  - Great Britain: EPSG 27700 (British National Grid)
  - Northern Ireland: EPSG 29903 (TM75 Irish Grid)
  - Detailed extent information and product naming provided in the dataset catalog (Table 2 and Appendix 6).

## Methodology: How LCM2020 Was Built

- Classification approach
  - 21 UKCEH Land Cover Classes defined from BAP Broad Habitats.
  - Classification scenes built from Sentinel-2 Seasonal Composite Images (winter, spring, summer, autumn) combined with 10 Context Rasters to reduce spectral confusion.
  - Bootstrap Training: automatic, non-field data–driven training using historic UKCEH maps (LCM2017–2019) to generate training observations; training sets filtered to >99% purity across three years.
  - Random Forest classifier used to classify classification scenes; 10,000 samples per land parcel bag with replacement ensure balanced learning across classes.
- Imagery and context
  - Seasonal composites created from Google Earth Engine; 9 Sentinel-2 bands used (B2, B3, B4, B5, B6, B7, B8, B11, B12); cloud gaps represented as nulls; classifier tolerates partial spectral information.
  - Context rasters include terrain metrics (Height, Aspect, Slope), proximity measures (distance to buildings, roads, sea, freshwater), coastal/foreshore masks, and woodland masks.
- Classification scale and processing
  - Great Britain used 100 x 100 km overlapping tiles to assemble 36-band Seasonal Composite Images and 46-band Classification Scenes (36 + 10 contexts); 74 overlapping GB Classification Scenes classified independently, with visual precedence rules used to resolve overlaps.
  - Northern Ireland used a single 43-band Classification Scene (36-band seasonal + NI context rasters) for the year.
- Land Parcel Framework
  - UK Land Parcel Spatial Framework stems from LCM2007 and is retained with minor internal changes for processing efficiency; unique parcel identifiers (gid) differ from LCM2015 for overlap-based comparisons.
  - Minimum mappable unit (MMU) is ~0.5 ha; parcels are designed to be dominated by a single land cover type when possible.

## UKCEH Land Cover Classes and BAP Broad Habitats

- The 21 UKCEH Land Cover Classes map to BAP Broad Habitats, with some one-to-one relationships and a few nuanced distinctions. Appendices explain the mappings and highlight spectral and contextual considerations (e.g., Saltwater vs. Freshwater, Bracken, Heather vs. Heather Grassland, and upland peatland complexities).
- The classification notes emphasize spectral confusion among some habitat types and the role of context rasters and training data in improving discrimination.

## Data Validation and Quality

- Validation methodology
  - Compared LCM2020 outputs with UK countryside survey data (2019/2020), National Forest Inventory, IACS, and bespoke interpretation points (34715 points total).
  - The overall accuracy achieved is 79.2% for full thematic detail.
- Appendix 5 provides confusion matrices and class-specific performance indicators, including producer’s and user’s accuracy metrics for each class.

## Practical Use and Considerations

- Pixel-level vs. parcel-level data
  - 10 m Classified Pixels provide fine-grained detail useful to specialists; 25 m Land Parcel rasters offer a more generalized parcel-level interpretation.
- Temporal dynamics and change detection
  - Annual production facilitates differentiation between real land cover changes and random classification noise; flickering changes across years indicate less stable transitions.
- Data interpretation notes
  - Some coastal, upland, and spectral-confusion areas are highlighted in appendices; users should refer to the mapping notes when interpreting edge cases.
- Accessibility and metadata
  - Dataset names, coordinate systems, extents, and attributes are documented; Appendix 3–4 provide colour ramps (standard and colour-blind friendly) for visualisation; Appendix 6 lists the full dataset catalog.

## Appendices and Additional Resources

- Appendix 1–2: Notes on UKCEH Land Cover Classes and their relation to BAP Broad Habitats, including class-specific training and interpretation guidance.
- Appendix 3–4: Colour recipes for displaying land cover classes (standard and colour-blind friendly) and associated QGIS symbology files.
- Appendix 5: Correspondence/confusion matrices for LCM2020 classifications.
- Appendix 6: Full list of datasets for UKCEH LCM2020, including dataset naming and scope.
- References: foundational works on Random Forests, training data, and related UK CEH methodology.