# Land Cover mapping using Landsat 8 OLI data for Shivamogga, Sindhudurg and Wayanad

## Overview
- A remote sensing study to map land cover and land use (LCLU) across three districts in India (Shivamogga, Sindhudurg, Wayanad) using Landsat 8 OLI data.
- Emphasizes robust data processing, accuracy assessment, and reproducible workflow suitable for governance and dataset stewardship.
- Outputs include district-level LCLU rasters and accompanying LCLU signature vectors, with detailed method documentation and quality metrics.

## Data and processing workflow
- Data sources and corrections
  - USGS Landsat 8 OLI Surface Reflectance Tier 1 imagery, atmospherically corrected with LaSRC.
  - Cloud, shadow, water, and snow masking using CFMASK; per-pixel saturation mask; illumination correction to address topographic shading.
  - Dry-season scenes (Nov–Feb) from 2016–2018 used to minimize cloud impact.
- Image preparation
  - Median composite image created from low-cloud (<2%) scenes to represent the target dry-season period, avoiding the limitations of maximum NDVI during dry seasons.
  - Extra information layers: Enhanced Vegetation Index (EVI) computed from the composite; SRTM elevation data added as an ancillary physical layer.
- Classification approach
  - Land cover classification implemented as multiple realizations to quantify pixel-level stability; 50 realizations generated with random, weighted sampling of reference polygons.
  - Reference data: 20% held out for validation; remaining 80% subdivided per realization into training (70%) and validation (30%), using caTools in R.
  - Model: Support Vector Machine (SVM) with radial-basis-function kernel; tuned hyperparameters for the RBF kernel (cost C = 1000, gamma = 1e-6).
  - Realization selection: compared accuracy across sets of 10, 20, 30, 40, and 50 realizations to identify the mode solution with highest accuracy.
- Data and tools
  - Processing and accuracy assessment performed in Google Earth Engine (GEE).
  - Outputs documented with per-district error matrices and metadata on processing steps.

## Land cover definitions and study areas
- Classification schemes
  - Shivamogga: 11 LCLU classes (e.g., wet evergreen forest, moist deciduous forest, dry deciduous forest, grassland, plantation, cropland, fallow land, waterbody, built-up, grass/shola combinations, etc.).
  - Sindhudurg and Wayanad: 9–11 LCLU classes each, including evergreen/mixed forests, moist/grassland types, plantations (mango, cashew, tea, teak, etc.), cropland, fallow land, waterbody, built-up, and related categories.
- Study areas and extents
  - Shivamogga, Karnataka: tropical climate; flat east with western mountains; wide forest types and patches of shola grasslands.
  - Sindhudurg, Maharashtra: moist/humid climate; undulating landscape from coast to Western Ghats; mix of semi-evergreen, moist deciduous, and grassland.
  - Wayanad, Kerala: tropical monsoon climate; mountainous Western Ghats plateau; diverse forest types and high-elevation shola grassland.

## Accuracy assessment and results
- Validation framework
  - Accuracy metrics used: overall accuracy (OA), user’s accuracy (UA), producer’s accuracy (PA) with area-weighted post-sampling stratified sampling.
  - Kappa coefficient not reported in line with cited methodology.
- Results by district (example OA)
  - Shivamogga: OA 89.50% (SE 1.2%)
  - Sindhudurg: OA 88.32% (SE 2.0%)
  - Wayanad: OA 94.62% (SE 1.2%)
- Class-level performance highlights
  - Waterbody and certain water-related classes generally show high UA/PA (often near 100% UA in some classes).
  - Grassland and plantation classes vary by district, with some classes achieving high UA/PA (e.g., grassland 98.8% UA in Sindhudurg) and others showing lower accuracies due to spectral similarity with adjacent land covers.
  - Overall, high accuracy achieved across all three districts, with Wayanad achieving the highest OA among them.
- Outputs and documentation
  - District-specific error matrices accompany the outputs, detailing per-class UA/PA and area proportions, including standard errors.
  - Final products include district LCLU raster files and vector LCLU signature files for transparency and reproducibility.

## Data products and provenance
- Ingested/described files
  - Raster LCLU products:
    - Shivamogga_lclu.tif (11 classes)
    - Sindhudurg_lclu.tif (9 classes)
    - Wayanad_lclu.tif (11 classes)
  - Vector LCLU signature files (gpkg) for each district:
    - Shivamogga_signature.gpkg
    - Sindhudurg_signature.gpkg
    - Wayanad_signature.gpkg
- Metadata and reproducibility
  - Detailed description of imagery sources, preprocessing steps, compositing approach, and classification workflow to enable auditability and reuse.
  - References and methodological justifications for parameter choices (e.g., SVM tuning, realisations approach, accuracy assessment framework) are provided to support governance and standards compliance.

## Implications for data governance and stewardship
- Transparency and reproducibility
  - Full documentation of data sources, preprocessing, models, and validation enables traceability and audit trails for datasets.
- Metadata and versioning
  - Clear artifact naming and per-district documentation support versioning, updates, and discoverability of LCLU products.
- Data quality and usability
  - Use of multi-realization mode solution and explicit per-class accuracy metrics provide measurable quality indicators for dataset consumers.
- Interoperability and standards
  - Adoption of well-established correction (LaSRC), cloud masking (CFMASK), and standard LCLU class schemes facilitates interoperability with other datasets and portals.
- Data sharing and stewardship considerations
  - Outputs are packaged with both raster and vector representations and accompanying accuracy metadata, enabling responsible sharing, re-use, and integration into broader data governance frameworks.