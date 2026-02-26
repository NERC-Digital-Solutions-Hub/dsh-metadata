# Land Cover mapping using Landsat 8 OLI data for Shivamogga, Sindhudurg and Wayanad

- Objective: Develop high-accuracy land cover and land use (LCLU) maps for three Indian districts using Landsat 8 imagery, addressing cloud contamination and terrain effects to support data-driven decision making.

## Data sources and preparation

- Satellite data: USGS Landsat 8 OLI Surface Reflectance Tier 1 imagery, atmospherically corrected with LaSRC; cloud/shadow/water/snow masks created with CFMask; per-pixel saturation masks; illumination correction applied to reduce topographic shading.
- Image selection and compositing: Cloud cover is a major challenge; created a median composite for 2017 from dry-season images (Nov–Feb) with low cloud (<2%) acquired 2016–2018. Median chosen over maximum NDVI to better represent dry-season conditions.
- Additional layers: Added EVI as an information layer; included SRTM elevation data as an ancillary physical layer to reflect elevation-driven vegetation patterns.
- Data products and resources: For each district, LCLU rasters are produced (Shivamogga_lclu.tif, Sindhudurg_lclu.tif, Wayanad_lclu.tif) and associated ingested signatures (Shivamogga_signature.gpkg, Sindhudurg_signature.gpkg, Wayanad_signature.gpkg) detailing class names and IDs.

## Methodology

- Classification approach:
  - Land cover classification executed 50 realizations to quantify pixel-wise class stability.
  - Training/validation split: 20% reference polygons for validation; remaining 80% split into 70% training and 30% validation per realization; sampling weighted by class reference polygon proportions.
  - Determined the optimal number of realizations by evaluating mode solution accuracy across sets of 10, 20, 30, 40 and 50 realizations.
- Classification model:
  - Support Vector Machine (SVM) with Radial Basis Function (RBF) kernel.
  - Hyperparameters tuned: C = 10^3, gamma = 10^-6 (based on prior literature for robust boundary fitting).
- Validation and accuracy assessment:
  - Metrics used: overall accuracy (OA), user’s accuracy (UA), producer’s accuracy (PA) with standard errors; no kappa coefficient.
  - Accuracy assessment employed a post-sampling area-weighted stratification approach to reflect area proportions.
  - Process and accuracy assessments conducted in Google Earth Engine (GEE).

## Land Cover Class Definitions

- Shivamogga (9 classes): Wet evergreen forest, Evergreen & semi-evergreen, Moist deciduous forest, Dry deciduous forest, Grassland/Shola forest, Mixed plantation, Fallow land, Cropland, Waterbody, Built-up.
- Sindhudurg and Wayanad (11 classes each): Similar suite with additional plantation and crop distinctions (e.g., Mango plantation, Cashew plantation, Tea/Teak plantations, Sand/Barren, etc.), reflecting regional variability in land use types.
- Class descriptions emphasize vegetation types (evergreen, moist/dry deciduous), plantation crops, croplands, fallow areas, water bodies, built-up areas, and specialty plantations.

## Accuracy and area estimation

- Shivamogga: Estimated overall accuracy (OA) 89.50% (SE 1.2%) with detailed per-class UA/PA figures and standard errors; total area accuracy summarized in the provided error matrix.
- Sindhudurg: OA 88.32% (SE 2.0%) with per-class UA/PA detailed in the district’s error matrix.
- Wayanad: OA 94.62% (SE 1.2%) with per-class UA/PA detailed in the district’s error matrix.
- The study reports the error matrices and class-specific accuracies for each district, including total percentages, user’s accuracy, producer’s accuracy, and sample sizes used in validation.
- Processing and accuracy assessment workflow performed in Google Earth Engine; outputs include district-specific LCLU maps and accompanying accuracy statistics.

## Study areas and geographic context

- Shivamogga: Tropical climate; flat eastern parts with western mountains; vegetation gradients from dry-deciduous to wet evergreen forests.
- Sindhudurg: Moist and humid climate; undulating topography from Arabian Sea to Western Ghats; vegetation includes semi-evergreen and moist deciduous forests with grasslands.
- Wayanad: Tropical monsoon climate in a Western Ghats plateau; vegetation includes wet evergreen, moist deciduous, dry deciduous forests, and high-elevation shola grasslands.

## Data quality, limitations, and practices

- Cloud cover remains a core challenge in the Western Ghats; median compositing helps mitigate cloud/shadow effects and preserves a coherent dry-season representation.
- The multi-realization approach provides a measure of per-pixel classification stability, supporting more robust map products.
- The study emphasizes area-weighted accuracy assessment and avoids relying on a single global metric (kappa), aligning with current best practices for land cover validation.
- Deliverables are designed for reuse and scalability, with explicit data assets (lclu.tif rasters and signatures gpkg) and documentation on data sources and methods.

## Reuse and implications for Data Leaders

- Data assets and workflow offer a scalable template for data-led land cover mapping across other regions:
  - Use of median/dry-season image composites to minimize cloud impact in tropical regions.
  - Incorporation of EVI and elevation as auxiliary layers to improve discrimination among land cover types.
  - Stability assessment via multiple realizations to quantify per-pixel reliability.
  - Transparent validation framework with per-class accuracy reporting and SEs, enabling risk-aware decision making.
- Governance considerations:
  - Documentation of data sources, processing steps, and class definitions enhances discoverability and discoverable metadata for cross-network collaboration.
  - The publication of district-specific LCLU maps and corresponding signatures supports reproducibility and potential integration with broader data ecosystems.

## Deliverables

- LCLU maps:
  - Shivamogga_lclu.tif
  - Sindhudurg_lclu.tif
  - Wayanad_lclu.tif
- Signatures:
  - Shivamogga_signature.gpkg
  - Sindhudurg_signature.gpkg
  - Wayanad_signature.gpkg
- Supporting materials: Tables of acquisition dates and paths for Landsat scenes, LCLU class definitions, accuracy matrices (per district), and study-area extents.