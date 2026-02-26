# Land Cover mapping using Landsat 8 OLI data for Shivamogga, Sindhudurg and Wayanad

- Purpose and scope
  - Demonstrates a data-driven land cover and land use (LCLU) mapping workflow for three Indian districts using Landsat 8 OLI imagery.
  - Focuses on producing standardized, monitorable outputs (LCLU maps) and rigorous accuracy assessments to support environmental monitoring and policy evaluation over time.

## Data and imagery

- Satellite data
  - USGS Landsat 8 OLI Surface Reflectance Tier 1 imagery, atmospherically corrected with LaSRC.
  - Cloud, shadow, water, and snow masking with CFMask; per-pixel saturation mask; illumination correction for topographic shading.
  - Median composite image ('2017') created from dry-season scenes (Nov–Feb, 2016–2018) with low cloud (<2%) to represent the period.
  - Extra information layer: EVI; ancillary layer: SRTM elevation data.
- Rationale for approach
  - Western Ghats region has frequent cloud cover; median composite during a low-cloud dry season provides stable representations of land cover for the period.
  - Dry-season imagery enhances spectral separation between forest types and other cover types.

## Processing and methodology

- Image classification approach
  - Land cover mapped via Support Vector Machine (SVM) classifiers with an RBF kernel.
  - Model robustness enhanced by producing 50 realizations (train/validation splits) to derive a mode (most frequent) class for each pixel and an associated stability measure.
  - Validation strategy: 20% of reference polygons held out for validation; remaining 80% used for training (70%) and validation (30%) for each realization. Weighted sampling by class proportions.
  - Determination of optimal realizations: compared overall accuracy across 10, 20, 30, 40, and 50 realizations.
  - SVM parameters: cost C = 10^3, gamma = 10^−6 (RBF kernel).
- Outputs and tools
  - Analyses and classifications conducted in Google Earth Engine (GEE).
  - Generated mode LCLU maps with pixel-level stability measures from the multiple realizations.

## LCLU class definitions (district variations)

- General classes used across districts
  - Wet evergreen forest
  - Evergreen & semi-evergreen forest
  - Moist deciduous forest
  - Dry deciduous forest
  - Grassland (including shola-type) 
  - Mixed plantation
  - Cropland
  - Fallow land
  - Waterbody
  - Built-up
  - Tea plantation
  - Teak plantation
  - Mango plantation
  - Cashew plantation
  - Sand/Barren
- District-specific configurations
  - Shivamogga (Karnataka): 11 classes
  - Sindhudurg (Maharashtra): 9 classes
  - Wayanad (Kerala): 11 classes
- Example class descriptions
  - Forests (evergreen, moist deciduous, dry deciduous) characterized by canopy structure and typical dominant species.
  - Plantations (mixed, tea, teak, mango, cashew) represent monoculture or mixed plantation areas.
  - Grassland and shola grasslands, cropland, fallow land, waterbodies, and built-up areas described by land cover and land use characteristics.

## Accuracy assessment and results

- Evaluation metrics and approach
  - Overall accuracy (OA) and class-specific user’s accuracy (UA) and producer’s accuracy (PA) with post-sampling area-weighted stratified accuracy assessments.
  - Kappa not used, following Foody and Stehman et al. recommendations for accuracy assessment in this context.
- District-level accuracy (mode solution)
  - Shivamogga: OA 89.50% (SE ≈ 1.2%)
    - Example class-level accuracies reported; UA/PA vary by class.
  - Sindhudurg: OA 88.32% (SE ≈ 2.0%)
    - Class-wise accuracies indicate high reliability for evergreen and related forest classes; other classes show varying accuracy.
  - Wayanad: OA 94.62% (SE ≈ 1.2%)
    - Highest district OA among the three; strong performance for forest classes and mixed plantation.
- Validation and realizations
  - Accuracy metrics calculated for each of the 50 realizations and for mode solutions across different realization counts to identify the optimum balance of accuracy and stability.
- Outputs
  - District-specific LCLU maps (Shivamogga_lclu.tif, Sindhudurg_lclu.tif, Wayanad_lclu.tif) with accompanying error matrices and standard errors.
  - Ingested packages include district LCLU rasters and polygon-based LCLU signatures (gpkg) for each district.

## Study area details

- Geographic extents (EPSG:4326)
  - Shivamogga: approximately 13.46°–14.65° N; 74.63°–75.88° E
  - Sindhudurg: approximately 15.60°–16.66° N; 73.31°–74.22° E
  - Wayanad: approximately 11.44°–11.97° N; 75.77°–76.44° E
- Descriptions
  - Shivamogga: tropical climate with flat eastern areas and western mountains; natural vegetation includes dry-deciduous, moist evergreen, and wet evergreen forests.
  - Sindhudurg: moist and humid climate with undulating terrain from the Arabian Sea to the Western Ghats; vegetation includes semi-evergreen and moist deciduous forests and grasslands.
  - Wayanad: tropical monsoon climate on a mountainous Western Ghats plateau; vegetation includes wet evergreen, moist deciduous, dry deciduous forests, and high-elevation shola grasslands.

## Ingested data and signatures

- Raster LCLU maps
  - Shivamogga_lclu.tif (11 classes)
  - Sindhudurg_lclu.tif (9 classes)
  - Wayanad_lclu.tif (11 classes)
- Signature data
  - Shivamogga_signature.gpkg
  - Sindhudurg_signature.gpkg
  - Wayanad_signature.gpkg
  - Each signature dataset includes fid, LCLU class name, and LCLU id for validation and training reference.

## Implications for environmental monitoring

- Provides standardized, reproducible LCLU maps and accuracy metrics suitable for monitoring habitat distribution, land-use change, and policy impact over time.
- Demonstrates a robust, scalable workflow the environment-monitoring community can adopt, including:
  - Consensus-driven quantification of mapping accuracy without reliance on a single model fit.
  - Transparent handling of cloud-dominated regions via median dry-season composites and stability-based outputs.
  - Availability of district-specific classification schemes and corresponding signature data for reproducibility and comparison.
- Challenges and considerations
  - Cloud cover remains a major limitation; the median-dry-season approach mitigates but does not eliminate data gaps.
  - The study emphasizes clarity and comparability over maximal, potentially overfitted accuracy, aligning with monitoring priorities and data-sharing needs.
  - Access to underlying data and outputs is supported by providing both raster LCLU maps and signature gpkg files for reuse and integration with other datasets.