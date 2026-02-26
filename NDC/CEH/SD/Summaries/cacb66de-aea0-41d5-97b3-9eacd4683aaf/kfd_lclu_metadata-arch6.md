# Land Cover mapping using Landsat 8 OLI data for Shivamogga, Sindhudurg and Wayanad

- Objective: Develop land cover and land use (LCLU) maps for three districts in India (Shivamogga, Sindhudurg, Wayanad) using Landsat 8 OLI imagery, produce data products for end users, and assess classification accuracy to support data-driven decision making.

- Data sources and preprocessing:
  - Satellite imagery: USGS Landsat 8 OLI Surface Reflectance Tier 1, atmospherically corrected with LaSRC; clouds, shadows, water, snow masked with CFMask; per-pixel saturation mask; illumination correction applied.
  - Temporal strategy: Images acquired in the dry season (Nov–Feb) from 2016–2018 were combined to form a median composite to minimize cloud effects and reflect seasonality.
  - Extra layers: Calculated EVI added as an information layer; SRTM elevation data included as an ancillary physical layer to reflect elevation-related land cover patterns.
  - Image selection: For each district, a set of scenes with low cloud cover (<2%) was used to build a representative 2017 image through a compositing approach.

- Classification methodology:
  - Realizations: The study produced 50 independent classifications (realizations) per district to quantify classification stability and produce a mode solution (most frequent class per pixel).
  - Training/validation design: For each realization, 80% of reference polygons were used for training and 20% for validation, with a weighted allocation by class proportions. Training/validation split performed with caTools in R.
  - Model: Support Vector Machine (SVM) with a radial basis function (RBF) kernel; kernel parameters tuned to optimize performance (C = 10^3, gamma = 10^-6).
  - Validation and accuracy: The mode solution's accuracy was evaluated across sets of 10, 20, 30, 40, and 50 realizations to determine the optimum number of realizations. Accuracy metrics used were overall accuracy (OA), user’s accuracy (UA), and producer’s accuracy (PA); kappa was not used. Assessments employed post-sampling area-weighted stratification and were conducted in Google Earth Engine (GEE).

- Land cover and land use classes (definitions by district):
  - Shared classes across districts include: Wet evergreen forest, Moist deciduous forest, Dry deciduous forest, Grassland, Plantation (Mixed plantation, Mango plantation, Cashew plantation, Tea plantation, Teak plantation, etc.), Cropland, Fallow land, Waterbody, Built-up.
  - Wayanad also includes specific plantation classes (Tea, Teak) as part of the LCLU scheme.
  - Each district’s class definitions align with local vegetation structure and land use patterns (e.g., evergreen vs. deciduous forests, plantation monocultures, agricultural crops, and urban areas).

- Study areas and accuracy results:
  - Shivamogga
    - Overall accuracy: 89.50% (standard error ~1.2%).
    - Notable class-level performance (UA): Wet evergreen forest ~89.5%, Moist deciduous ~82.7%, Dry deciduous ~96.6%, Plantation/Mixed plantation ~91.0%, Fallow ~90.1%, Cropland ~76.2%, Waterbody ~100%, Built-up ~87.9%, Grassland/Shola ~96.1%.
  - Sindhudurg
    - Overall accuracy: 88.32% (standard error ~2.0%).
    - Notable class-level performance (UA): Evergreen & semi-evergreen ~95.5%, Moist deciduous ~90.0%, Grassland ~98.8%, Fallow ~94.1%, Waterbody ~100%, Cropland ~96.4%, Built-up ~90%, Mixed Plantation ~93.6%, Mango ~77.3%, Cashew ~77.1%, Sand/Barren ~100%.
  - Wayanad
    - Overall accuracy: 94.62% (standard error ~1.2%).
    - Notable class-level performance (UA): Wet evergreen forest ~97.2%, Moist deciduous ~87.7%, Mixed Plantation ~93.6%, Fallow ~100%, Waterbody ~100%, Grassland ~100%, Dry deciduous ~100%, Built-up ~100%, Cropland ~100%, Tea plantation ~100%, Teak plantation ~100%.
  - Across all districts, the majority of key natural and agricultural classes achieved high UA, with some plantation classes (e.g., specific crop monocultures) showing comparatively lower UA in certain districts.

- Outputs and data products:
  - Raster LCLU maps for each district:
    - Shivamogga_lclu.tif
    - Sindhudurg_lclu.tif
    - Wayanad_lclu.tif
  - Associated vector signatures (for LCLU classes) in geopackage format:
    - Shivamogga_signature.gpkg
    - Sindhudurg_signature.gpkg
    - Wayanad_signature.gpkg
  - All classifications and accuracy assessments were conducted in Google Earth Engine, enabling end-user access and self-serve exploration.

- Ingested files (data catalog):
  - Sindhudurg_lclu.tif, Shivamogga_lclu.tif, Wayanad_lclu.tif (raster LCLU maps)
  - Sindhudurg_signature.gpkg, Shivamogga_signature.gpkg, Wayanad_signature.gpkg (vector LCLU signatures)

- Practical considerations for Data Support:
  - Strengths: Robust multi-realization approach provides a measure of pixel-wise classification stability; high OA and class-specific accuracies, particularly for forested and water classes; self-serve data products suitable for policy, planning, and environmental monitoring.
  - Data quality/limitations: Cloud/shadow prevalence in the Western Ghats necessitated composite median imagery; some crop/plantation classes show moderate UA due to spectral similarity with other land covers; results depend on quality of reference polygons and sample sizes.
  - Reproducibility and reuse: Clear preprocessing and classification workflow (Landsat 8 SR, median compositing, EVI, SRTM; SVM with defined parameters; 50 realizations) supports replication and adaptation to other regions or timeframes.
  - Potential applications: Baseline LCLU maps for land use planning, forest management, biodiversity monitoring, and policy-support dashboards; data products can be integrated with other regional datasets for multi-topic analyses.

- References and methodological anchors (core ideas used):
  - SVM-based classification effectiveness with RBF kernel; tuned parameters (C, gamma) for optimal boundary fitting.
  - Median compositing in dry-season Landsat imagery to mitigate cloud effects and reflective differences.
  - Use of multiple realizations to quantify stability and derive a mode solution for robust LCLU mapping.
  - Accuracy assessment framework emphasizing OA, UA, and PA with area-weighted sampling, excluding kappa.

- Overall takeaway for data-driven support:
  - The study delivers high-quality, district-scale LCLU maps and accompanying accuracy metrics derived from a rigorous, reproducible workflow. The data products and signatures provide ready-to-use resources for exploring land cover dynamics, informing planning decisions, and communicating data-driven insights to stakeholders.