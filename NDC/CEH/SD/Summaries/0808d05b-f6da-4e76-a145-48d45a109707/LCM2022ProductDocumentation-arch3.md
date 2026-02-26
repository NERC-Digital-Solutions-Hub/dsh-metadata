# The UKCEH Land Cover Map for 2022

- Purpose and scope
  - User guide for UKCEH Land Cover Map 2022 (LCM2022), detailing data production, validation, accuracy, and appropriate use.
  - LCM2022 comprises seven geospatial data holdings for Great Britain and Northern Ireland: three 10 m datasets (classified pixels, land parcels, and rasterised land parcels, the latter two at 25 m), plus a 1 km summary raster product covering GB and NI.
  - Aim is to enable informed decision-making, change detection, and monitoring of environmental objectives through an annual, comparable land-cover time series.

- Data products and structure
  - 10 m Classified Pixel datasets (GB and NI): classified per-pixel land-cover class with a second band indicating classification confidence; preserves fine spatial detail (no parcel-wide generalisation).
  - Land Parcel datasets (GB and NI): derive parcel attributes by intersecting 10 m pixels with the UKCEH Land Parcel Spatial Framework (minimum parcel size ~0.5 ha).
  - 25 m Rasterised Land Parcel datasets (GB and NI): three-band rasters carrying per-parcel dominant class (mode), confidence (conf), and purity (purity).
  - 1 km raster products: dominant class per 1 km pixel (for both classes and aggregates) and percentage cover per class/aggregate (rounded integers; coastal areas may sum to slightly less or more than 100% due to rounding).
  - Seasonal Composite Images: derived from Sentinel-2 data (four seasonal periods) and combined with Context Rasters to form Classification Scenes.
  - Context Rasters (GB and NI): 10 m layers including terrain attributes, proximity to buildings/roads/water, foreshore and binary masks (woodland, saltmarsh, urban).
  - Classification Scenes: GB classified in 32 tiles; NI uses a single 49-band Scene combining Seasonal Composite with Context Rasters.
  - Coordinate systems and coverage: GB (OSGB 27700), NI (TM75 Irish Grid 29903); datasets include metadata on extent, pixel size (10 m and 25 m), and band structure.
  - Dataset metadata and DOIs are provided; datasets are cited via DOIs in the product table.

- Production methods and workflow
  - Land cover mapping via automatic classification using Bootstrap Training and Random Forest (RF).
  - Bootstrap Training: uses historic LCM observations (LCM2019–LCM2021) with >80% probability and consistent class across years to train RF for the current map, enabling use of wall-to-wall historical data without new field collection.
  - Random Forest classifier: balanced training by drawing 10,000 samples per bag to ensure equal representation of classes; proprietary UKCEH software integrates WEKA with PostGIS and GDAL (open-source components used).
  - Seasonal Composite Images: produced from Google Earth Engine; Sentinel-2 bands across four seasons (10 bands used) with gaps handled through classifier tolerance to incomplete spectral information.
  - Context Rasters: mitigate spectral confusion (e.g., rocks, urban areas) by incorporating terrain, urban proximity, water proximity, foreshore and vegetation masks.
  - UK Land Parcel Spatial Framework: used to structure 10 m pixels into parcels; framework ensures discrete real-world units (approx. 0.5 ha MMU) and supports change-detection, though parcel identifiers may differ from LCM2015 for comparability.
  - Validation approach: formal validation using 33,107 reference points across all 21 classes; overall accuracy reported at 86.1%.

- Validation, accuracy and limitations
  - Overall accuracy: 86.1% at full thematic detail (LCM2022).
  - Validation data: composite dataset from GB Countryside Survey, National Forest Inventory, Rural Payments Agency, and bespoke LCM validation points; intersected with 25 m rasterised parcel data for accuracy assessment.
  - Known issues:
    - A small number of polygons missing from vector land parcel products (affects 25 m rasterised parcels modestly; 10 m classified pixels unaffected).
    - Some inter-class confusion remains among fine-scale habitat types (notably Bog, Heather/Heather Grassland, fen/marsh/swamp) due to spectral similarities and the nature of BAP Broad Habitats.
  - Disclaimer: minor methodological changes between annual maps may produce real changes in land cover alongside changes due to updated methods.

- Accessibility, governance, and citation
  - Each LCM2022 dataset has a DOI; users are encouraged to cite the dataset and related publications (e.g., Marston et al. 2023/2024 series) when using the data.
  - Data are deposited at NERC EDS Environmental Information Data Centre; DOIs are provided for 10 m Classified Pixels, 25 m Rasterised Land Parcels, Land Parcel products, and 1 km summary rasters.
  - Metadata considerations and data-sharing practices are discussed, including the balance between openness and data governance; public sharing of underlying data is a factor in data usage decisions.

- Practical considerations for monitoring frameworks
  - Annual production supports monitoring state and change with improved temporal consistency, enabling differentiation of real change from random classification noise (random errors expected to flicker over time).
  - High spatial detail (10 m) preserves narrow features and small patches relevant for fine-scale monitoring, while 25 m parcel data and 1 km summaries enable scalable, multi-resolution analyses.
  - Bootstrap Training enhances efficiency by leveraging recent maps to train current classifications, reducing the need for fresh field data—though some crop-rotation changes may reduce suitability for certain classes (e.g., arable vs. improved grassland).
  - Crosswalks with Biodiversity Action Plan Broad Habitats are included to aid interpretation and compatibility with historical habitat classifications, with explicit notes on where equivalence is approximate.
  - Users should heed known issues (e.g., occasional missing parcels, potential coastal misclassifications) and refer to the appendices for detailed classification notes, color palettes, and metadata guidance.

- Appendices and ancillary resources
  - Appendix 1 & 2: notes on UKCEH Land Cover Classes and BAP Broad Habitats, including guidance on interpretation and potential spectral confusions.
  - Appendix 3–4: full dataset lists and validation correspondence matrices (Producer’s and User’s accuracies by class).
  - Appendix 5 & 6: recommended color and color-blind-friendly color schemes for displaying land cover classes; accompanying QGIS symbology files provided.
  - Cross-references and citations to foundational methods (e.g., Breiman 2001 on RF) and prior UK LCM reports.

- Endnotes
  - Formal validation is reported; methodological changes are acknowledged as part of the continuous development of the LCM series.
  - The document emphasizes the goal of enabling informed decision-making and robust monitoring of the UK countryside through an annually updated, well-documented land cover data product.