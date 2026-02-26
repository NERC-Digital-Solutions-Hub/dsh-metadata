# Land Cover mapping using Landsat 8 OLI data for Shivamogga, Sindhudurg and Wayanad

## Objective
- Map land cover and land use (LCLU) across three districts in India (Shivamogga, Sindhudurg, Wayanad) using Landsat 8 OLI data.
- Produce robust, comparable LCLU maps to inform environmental monitoring and policy evaluation.

## Data and pre-processing
- Satellite data: USGS Landsat 8 OLI Surface Reflectance Tier 1 imagery, atmospherically corrected with LaSRC; cloud/shadow/water/snow masking with CFMask; per-pixel illumination correction.
- Image selection and compositing: Cloud-heavy region; created a median image for 2017 from dry-season images (Nov–Feb) acquired 2016–2018 to minimize cloud impact and maximize seasonal spectral separation. EVI added as an information layer.
- Ancillary layer: SRTM elevation data included to reflect elevation-related vegetation patterns.
- Classification preparation: Produced 50 realizations (classifications) to quantify per-pixel stability; used 20% of reference polygons for validation and 80% for training/validation, with a 70/30 split within realizations.
- Tools and approach: Image classifications and accuracy assessments performed in Google Earth Engine (GEE); variable selection and model tuning conducted in R.

## Image classification methodology
- Algorithm: Support Vector Machine (SVM) with radial-basis-function (RBF) kernel; optimized kernel parameters at C = 10^3 and γ = 10^-6.
- Realization strategy: Each realization re-sampled training/validation polygons (weighted by class reference proportions); mode solution across realizations used as final map, with validation ensures accuracy.
- Realization count: Evaluated sets of 10, 20, 30, 40, and 50 realizations to determine the optimum balance of accuracy and effort.

## Land Cover and Land Use Class Definitions
- Shivamogga: 11 LCLU classes including Wet evergreen forest, Moist deciduous forest, Dry deciduous forest, Grassland/Shola, Mixed plantation, Cropland, Fallow land, Waterbody, Built-up, Tea plantation, Teak plantation.
- Sindhudurg: 9 LCLU classes including Evergreen & semi-evergreen, Moist deciduous forest, Grassland, Fallow land, Waterbody, Built-up, Mango plantation, Cashew plantation, Mixed plantation.
- Wayanad: 11 LCLU classes including Wet evergreen forest, Moist deciduous forest, Dry deciduous forest, Grassland, Mixed plantation, Fallow land, Waterbody, Built-up, Cropland, Tea plantation, Teak plantation.
- Training data: LCLU signatures provided as vector gpkg files per district (Sindhudurg_signature.gpkg, Shivamogga_signature.gpkg, Wayanad_signature.gpkg) to define class signatures.

## Accuracy assessment and area estimation
- Metrics: Overall accuracy (OA) and class-specific User’s and Producer’s accuracies (UA, PA); no Kappa coefficient used.
- Assessment design: Post-stratified, area-weighted sampling; 50 realizations evaluated to identify the optimum set for the mode solution.
- Processing environment: Accuracy assessments conducted within Google Earth Engine; results summarized per district.

## Study areas and key results
- Shivamogga
  - OA: 89.5% (SE 1.2%)
  - Representative class performance: Wet evergreen forest ~89%, Moist deciduous ~83%, Dry deciduous ~97%, Grassland ~96%, Fallow ~90%, Cropland ~76%, Waterbody 100%, Built-up ~88%, Grassland/Shola high accuracy.
- Sindhudurg
  - OA: 88.32% (SE 2.0%)
  - Representative class performance: Evergreen & semi-evergreen ~95%, Moist deciduous ~90%, Grassland ~99%, Fallow ~94%, Waterbody 100%, Built-up ~90%, Cropland ~96%, Cashew ~77%, Mango ~77%, Mixed plantation ~93%.
- Wayanad
  - OA: 94.62% (SE 1.2%)
  - Representative class performance: Wet evergreen ~97%, Moist deciduous ~88%, Mixed plantation ~94%, Fallow ~100%, Waterbody 100%, Grassland 100%, Dry deciduous ~100%, Built-up ~100%, Cropland 100%, Tea/Teak plantations ~100%.

## Outputs and data products
- LCLU raster maps:
  - Shivamogga_lclu.tif
  - Sindhudurg_lclu.tif
  - Wayanad_lclu.tif
- Training and validation signatures:
  - Sindhudurg_signature.gpkg, Shivamogga_signature.gpkg, Wayanad_signature.gpkg
- Ingested data descriptions:
  - LCLU rasters (9–11 classes per district) and polygon vector signatures for signature-based classification.
- All processing and accuracy assessments were conducted in an open, reproducible workflow (Landsat 8 data, EVI, SRTM, and SVM-based classification with multiple realizations).

## Relevance to Monitoring Frameworks
- Demonstrates a transparent, repeatable workflow suitable for policy monitoring: open data sources, robust preprocessing (cloud masking, illumination correction), inclusion of elevation as an ecological driver, and rigorous accuracy assessment without reliance on Kappa.
- Uses multiple realizations to quantify classification stability and determine robust mode solutions, aligning with best practices for monitoring framework outputs.
- Generates district-level, policy-relevant LCLU products with accompanying metadata and signatures, facilitating data governance, sharing, and downstream environmental health monitoring.

## Key takeaways
- A robust, transparent methodology can produce high-quality LCLU maps in cloud-prone tropical regions by using dry-season median composites and SVM-based classification.
- District-level OA ranges from ~88% to ~95%, with high accuracy for critical classes like waterbodies, grasslands, and evergreen forests.
- The workflow emphasizes openness, data provenance, and stakeholder-relevant outputs, supporting ongoing environmental health monitoring and decision-making.