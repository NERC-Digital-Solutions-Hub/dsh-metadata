# Land Cover mapping using Landsat 8 OLI data for Shivamogga, Sindhudurg and Wayanad

- Purpose: Produce land cover and land use (LCLU) maps for three Indian districts (Shivamogga, Sindhudurg, Wayanad) using Landsat 8 OLI imagery; deliver map-based data products suitable for GIS analysis and policy/communication needs.

## Data and preprocessing

- Satellite data: USGS Landsat 8 OLI Surface Reflectance Tier 1 images, atmospherically corrected with LaSRC; cloud/shadow/water/snow masks via CFMask; per-pixel saturation mask; illumination correction to offset topographic shading.
- Image selection and compositing: Cloud-prone region (Western Ghats) necessitated a median composite of low-cloud scenes (cloud cover < 2%) captured in the dry season (Nov–Feb) from 2016–2018 to reflect a consistent time period.
- Indices and ancillary data: Calculated EVI from the composite; included SRTM elevation data as an ancillary layer to leverage elevation–vegetation associations.
- Rationale for methods: Median composite preferred over max-NDVI for dry-season imagery to better reflect actual condition; elevation data assists interpretation of forest types and land covers.

## Image classification approach

- Realizations for accuracy: Classified 50 times with different training samples to quantify pixel-level stability; determined the mode as the final class per pixel, with an associated stability measure.
- Reference data handling: Allocated 20% of reference polygons to a validation set; the remaining 80% split into 70% training and 30% validation samples (weighted by class representation). Splits performed in R using caTools.
- Realization testing: Assessed accuracy across sets of 10, 20, 30, 40 and 50 realizations to identify the optimum number of realizations delivering the highest accuracy.
- Classifier: Support Vector Machine (SVM) with an RBF kernel; tuned parameters with C = 1000 and gamma = 1e-6 (based on prior guidance for remote sensing classification).

## Land Cover and Land Use Class Definitions

- Classes defined for Shivamogga, Sindhudurg, and Wayanad include:
  - Wet evergreen forest
  - Evergreen & semi-evergreen forest
  - Moist deciduous forest
  - Dry deciduous forest
  - Grassland (including shola grassland in some contexts)
  - Mixed plantation (e.g., areca nut, coconut, eucalyptus)
  - Fallow land
  - Cropland
  - Waterbody
  - Built-up
  - Tea plantation and Teak plantation (noted in Wayanad)
  - Cashew plantation and Mango plantation (in some districts)
  - Sand/Barren
- Each class is accompanied by descriptive definitions reflecting forest types, plantation monocultures, or land-use categories to support map interpretation.

## Accuracy and area estimation

- Evaluation framework: OA (overall accuracy) and class-specific User’s Accuracy (UA) and Producer’s Accuracy (PA); area-weighted post-sampling stratified accuracy assessment following established practices; avoided using kappa.
- Overall accuracy by district:
  - Shivamogga: 89.50% OA (SE ≈ 1.2%)
  - Sindhudurg: 88.32% OA (SE ≈ 2.0%)
  - Wayanad: 94.62% OA (SE ≈ 1.2%)
- Validation approach: Assessed omission and commission errors per class and across realizations to determine the stability and reliability of the mode solution.
- Processing platform: All image classifications and accuracy assessments were performed in Google Earth Engine (GEE).

## Study areas and results (error matrices overview)

- Shivamogga: Tropical climate with flat eastern terrain and western mountains; major natural vegetation gradients correspond to evergreen, moist deciduous, and dry deciduous forests; error matrix indicates high accuracy for key forest classes and substantial accuracy for waterbody, cropland, and built-up classes.
- Sindhudurg: Moist and humid climate with coastal to hilly landscape; natural vegetation includes semi-evergreen and moisture forests plus grasslands; error matrix shows high user/producer accuracy for evergreen and semi-evergreen, grassland, and waterbody; overall OA around 88%.
- Wayanad: Mountainous Western Ghats region with wet evergreen, moist deciduous, dry deciduous forests and shola grassland; highest overall accuracy among the three (OA ≈ 94.6%); strong performance for wet evergreen, mixed plantation, and forest-related classes.
- Ingested products: Sharable rasters and vector signatures include Shivamogga_lclu.tif (nine LCLU classes) and Sindhudurg_lclu.tif / Wayanad_lclu.tif (eleven classes each); corresponding signature gpkg files provide polygon-based LCLU signatures for each district.

## Ingested files and data products

- Raster LCLU products:
  - Shivamogga_lclu.tif (nine classes)
  - Sindhudurg_lclu.tif (nine classes)
  - Wayanad_lclu.tif (eleven classes)
- Vector/LCLU signatures:
  - Shivamogga_signature.gpkg (11 classes)
  - Sindhudurg_signature.gpkg (nine classes)
  - Wayanad_signature.gpkg (11 classes)
- Use: These data products are suitable for GIS-based visualization, analysis, and policy-oriented mapping within local planning contexts.

## Tools and references

- Software and tools: Google Earth Engine (classification and accuracy assessment); R (caTools package for data splitting; general statistical tasks).
- Classifier and data practices: SVM with RBF kernel; medoid-like approaches discussed for seasonal composites; use of NDVI/EVI; attention to data at multiple resolutions and harmonization via elevation data.
- Key references underpinning methods: SVM classification, cloud masking, terrain illumination correction, resampling and accuracy assessment methodologies, and standard remote-sensing practice for land cover mapping.