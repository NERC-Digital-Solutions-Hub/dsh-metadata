# Land Cover mapping using Landsat 8 OLI data for Shivamogga, Sindhudurg and Wayanad

- Objective: Develop high-accuracy land cover and land use (LCLU) maps for three Indian districts using Landsat 8 OLI data, quantify classification accuracy, and provide data-ready outputs for decision-making and further analysis.

## Data sources and preprocessing

- Satellite data: USGS Landsat 8 OLI Surface Reflectance Tier 1 imagery, atmospherically corrected with LaSRC; cloud/shadow/water/snow mask via CFMASK; per-pixel saturation mask; illumination correction to counter topographic shading.
- Image selection: dry-season images (November–February) with low cloud (<2%), spanning 2016–2018; median composite used to represent the time period and reduce cloud effects.
- Extra layers: Added Enhanced Vegetation Index (EVI) and Shuttle Radar Topography Mission (SRTM) elevation as ancillary layer to reflect elevation–vegetation associations.
- Output formats: mode LCLU maps and associated accuracy assessments; file examples include Shivamogga_lclu.tif, Sindhudurg_lclu.tif, Wayanad_lclu.tif.

## Image processing and classification workflow

- Realization-based accuracy assessment:
  - Generated 50 realizations by repeatedly training and validating with different reference polygons.
  - Data split within realizations: 80% for training/validation (70% training, 30% validation) and 20% reserved for initial validation.
  - Training sample selection weighted by the proportion of reference polygons per cover class.
  - Determined the optimum number of realizations by comparing accuracy across sets of 10, 20, 30, 40, and 50 realizations; mode solution selected as final map.
- Classification method:
  - Support Vector Machine (SVM) with radial basis function (RBF) kernel; tuned parameters: C = 10^3, gamma = 10^-6.
  - Rationale: high accuracy and robust boundary fitting with relatively few parameters when adequate training data are available.
- Classes and definitions:
  - Shivamogga: 11 LCLU types (e.g., Wet evergreen forest, Moist deciduous forest, Dry deciduous forest, Grassland/Shola, Mixed plantation, Cropland, Fallow land, Waterbody, Built-up, Tea plantation, Teak plantation).
  - Sindhudurg: 9 LCLU types (e.g., evergreen & semi-evergreen, Moist deciduous forest, Grassland, Fallow land, Waterbody, Built-up, Mango/Cashew/Cashew/Mixed plantation variants, etc.).
  - Wayanad: 11 LCLU types (e.g., Wet evergreen forest, Moist deciduous forest, Mixed Plantation, Fallow land, Waterbody, Grassland, Dry deciduous forest, Built-up, Cropland, Tea plantation, Teak plantation).
- Accuracy assessment approach:
  - Metrics: overall accuracy (OA), user’s accuracy (UA), producer’s accuracy (PA) per class.
  - No kappa coefficient; post-sampling area-weighted stratified accuracy assessment following recent methodological guidance.
  - Assessments performed in Google Earth Engine (GEE).

## Study areas and LCLU definitions

- Shivamogga (Karnataka)
  - Natural vegetation: gradient from wet evergreen to dry deciduous forests; shola grasslands at higher elevations.
- Sindhudurg (Maharashtra)
  - Climate: moist and humid; undulating terrain from sea-level west to Western Ghats east.
  - Vegetation: semi-evergreen, moist-deciduous forest, and grassland.
- Wayanad (Kerala)
  - Climatic setting: tropical monsoon; mountainous Western Ghats plateau.
  - Vegetation: wet evergreen, moist deciduous, dry deciduous forests, plus high-elevation shola grasslands.
- LCLU class definitions summarized in Table 4 cover forest types, grasslands, plantations (mixed, tea, teak, mango, cashew, etc.), cropland, fallow land, water bodies, built-up areas.

## Key results

- Overall accuracy (OA) by district:
  - Shivamogga: 89.50% OA (SE ≈ 1.2%)
  - Sindhudurg: 88.32% OA (SE ≈ 2.0%)
  - Wayanad: 94.62% OA (SE ≈ 1.2%)
- Representative class-accuracy patterns:
  - Waterbody, Grassland/Shola forests, and evergreen forest classes generally show high user and producer accuracies.
  - Cropland and plantation-related classes vary; some monoculture plantations (e.g., teak, tea, mango, cashew) exhibit higher producer or user accuracies depending on district.
  - Some classes with mixed signatures (e.g., Mixed plantation) achieve high user accuracy but may show variability in producer accuracy across realizations.
- Validation outputs:
  - Detailed per-class confusion matrices are provided for each district (e.g., Shivamogga_lclu.tif, Sindhudurg_lclu.tif, Wayanad_lclu.tif), including percentages, standard errors, and sample sizes for reference elements.
- Data products:
  - Final LCLU maps for each district (e.g., Shivamogga_lclu.tif, Sindhudurg_lclu.tif, Wayanad_lclu.tif) and associated accuracy reports.
  - Ingested files include district-specific rasters and vector signature files (Shivamogga_signature.gpkg, etc.) detailing class names and IDs.

## Methodological highlights and implications

- Cloud handling strategy: median composite across multiple scenes during the dry season mitigates cloud/shadow effects and improves temporal consistency with the underlying land cover.
- Feature enrichment: including EVI and elevation data improves separation of cover types related to vegetation density and topography.
- Robust uncertainty handling: using multiple realizations and reporting per-pixel mode with an associated stability measure provides a transparent sense of classification confidence.
- Reproducibility and workflow:
  - Analyses executed in Google Earth Engine; sampling and validation steps implemented in R (caTools) for data splitting and training/validation management.
  - The approach balances data access and methodological rigor, aligning with data-driven decision-making needs and potential reproducibility in governmental or large institutional contexts.

## Practical considerations for analysts

- Data accessibility and scale: the methodology addresses typical challenges in accessing diverse datasets and achieving reliable local-scale classifications through careful sampling and validation.
- Design choices: the median dry-season composite, EVI, and elevation layers help in distinguishing forest types, grasslands, and plantations across heterogeneous terrains typical of the Western Ghats region.
- Applications: the resulting LCLU maps support land use planning, conservation prioritization, forest management, and agricultural policy research at district scales.
- Limitations and future work: while OA is high, some classes show lower producer or user accuracies depending on district; further refinement could involve expanding reference data, integrating additional spectral indices, or exploring alternative classifiers for specific class separations.