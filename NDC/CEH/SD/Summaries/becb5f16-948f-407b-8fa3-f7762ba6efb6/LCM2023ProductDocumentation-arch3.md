# The UKCEH Land Cover Map for 2023

- LCM2023 is the UKCEH land cover map produced for 2023, the eleventh in the series, designed to monitor state and change of the UK countryside and inform policy and decision-making.
- The product consists of seven datasets (three for Great Britain and Northern Ireland each) plus a 1 km summary raster, plus accompanying documentation to support use and interpretation.
- The publication emphasises data production, validation, accuracy, and guidance for appropriate application.

## Data products and structure

- 10 m Classified Pixel datasets (GB and NI): per-pixel land cover class with a second band indicating the classifier confidence. The classification is produced from Classification Scenes using Bootstrap Training and a Random Forest classifier; 10 m data preserve fine landscape detail.
- 25 m Rasterised Land Parcel datasets (GB and NI): rasterised versions of land parcels, created by overlaying 10 m pixels with the UKCEH Land Parcel Spatial Framework; three-band rasters provide dominant class (mode), mean confidence, and mean purity per parcel.
- Land Parcel vector datasets (GB and NI): parcel geometries with attributes (e.g., gid, hist, mode, conf, purity) used for spatial analysis and change detection.
- 1 km summary rasters (GB and NI): summary products that give dominant class and percentage cover per 1 km pixel, derived from the 25 m raster data.
- Seasonal Composite Images and Classification Scenes: four-season Sentinel-2 reflectance composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) combined with Context Rasters to form multi-band Classification Scenes (GB tiled into 100 x 100 km tiles; NI uses a single scene).
- Context Rasters (GB and NI): 10 m layers that help resolve spectral confusion (e.g., height, aspect, slope, distances to buildings/roads/water, foreshore and masks for woodland, saltmarsh).
- Classification methodology: automated Bootstrap Training with a Random Forest classifier; outputs include a probability/confidence band for each pixel (and, for NI, additional dataset variants).
- Coordinate systems: Great Britain uses British National Grid (EPSG: 27700); Northern Ireland uses Irish Grid (TM75, EPSG: 29903).

## Production methodology

- Bootstrap Training: uses historical LCM maps (LCM2020–LCM2022) to automatically generate training data, selecting high-confidence pixels (over 80% probability) consistent across years, to train the classifier without fresh field-collected data.
- Random Forest classification: trained with balanced sampling across classes to avoid dominance by common classes; produces the 10 m Classified Pixel product and associated confidence.
- Classification Scenes: GB is divided into about 32 tiles for processing; NI is a single 49-band scene; scenes combine Sentinel-2 bands with Context Rasters and Seasonal Composite information.
- UKCEH Land Parcel Spatial Framework: 0.5 ha minimum parcel size (MMU); parcels created by generalising national cartography to form discrete land units; parcels aid change detection and reduce classification noise.
- Validation: 33,107 validation points across all 21 LCM classes; overall accuracy reported at 83%.

## Relationship to biodiversity classifications and class detail

- LCM2023 uses 21 UKCEH Land Cover Classes aligned with Biodiversity Action Plan (BAP) Broad Habitats, but not identical to BAP; some mappings are adapted for remote sensing.
- Appendices provide notes on class definitions, mapping nuances, and guidance for interpreting overlaps between UKCEH classes and BAP Broad Habitats.
- The document includes extensive guidance on classification challenges and expected confusions (e.g., between arable and improved grassland, various grassland types, bogs, heather, and aquatic/coastal classes).

## Data quality, governance, and access

- Validation indicates an overall accuracy of 83% at full thematic detail; per-class producer and user accuracies are provided in the documentation (Appendix 4).
- Known issues: a small number of land parcel polygons are missing in the vector parcel products, causing nodata gaps in the 25 m rasterised parcel data; impact on 1 km products is negligible; 10 m classified pixels are unaffected.
- Data and DOIs: each LCM2023 dataset has a DOI; citations and overview references are provided (Table 5 and accompanying references).
- Publication notes: occasional methodological changes between years reflect ongoing improvements; users should be aware that some inter-map differences may reflect method changes as well as real land cover change.
- Data presentation: recommended color recipes and color-blind-friendly variants are provided (Appendices 5 and 6), with companion QGIS symbology files.

## End-user guidance and interpretation

- Use cases: annual maps support temporal change detection, change-based monitoring, and policy-relevant environmental assessments; the annual series helps distinguish random errors from real change due to the persistence of real land-cover transitions.
- Cautions: be mindful of spectral confusion among habitat types, coastal and aquatic features, and peat/peatland classes; refer to Appendix 1–2 for detailed definitions, and Appendix 4 for per-class accuracy and confusion matrices.
- Data governance and sharing: while the document prioritises openness and reproducibility, some data and metadata considerations are noted (e.g., CI/SHARING constraints and the need to manage metadata).

## Appendices (highlights)

- Appendix 1: Notes on UKCEH Land Cover Classes (descriptions and potential spectral confusions for each class).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats (definitions and mapping considerations).
- Appendix 3: Full list of LCM2023 datasets with DOIs and citations.
- Appendix 4: Detailed correspondence/confusion matrices and accuracy statistics by class.
- Appendix 5: Recommended color recipe for displaying UKCEH Land Cover Classes.
- Appendix 6: Color-blind-friendly display recipe for the same classes.
- Supporting materials include a QGIS symbology file (lcm_raster.qml) and a color-blind-friendly version (lcm_raster_cb_friendly.qml).