# Soil metrics and vegetation data from pasture fed livestock farms across Great Britain, 2018

- Overview
  - Dataset from UK Centre for Ecology & Hydrology, funded by BBSRC, to evidence impacts of pasture-fed livestock on grassland parameters (vegetation, soil quality).
  - Focuses on Pasture Fed Livestock Association (PFLA) farms, with data intended to support biodiversity, soil health and resilience considerations.
  - Enables comparison with Countryside Survey data; samples a single field per farm with vegetation and soil measurements.

- Experimental design and sampling
  - 56 farms across Great Britain, members or prospective members of PFLA; recruited via PFLA contact.
  - Field visits conducted May–September 2018.
  - Plot framework: one large 200 m2 plot per field, with a randomly positioned sub-plot for vegetation and soil sampling.
  - Farm participation included varying certification status (fully certified, provisionally certified, or member-only with future certification plans).
  - Plant and soil data collected following Countryside Survey (CS) methodologies to enable cross-study comparability.
  - Farm locations anonymised with site codes to protect landowner confidentiality.

- Data collected
  - Vegetation
    - All species recorded within the 200 m2 plot; species presence and cover in nested sub-plots; vegetation height categories.
    - Data captured electronically; plot-level and nest-level cover estimates.
  - Field management
    - On-site confirmation of current and historic field management practices via a purpose-built questionnaire (grazing, sward longevity, inputs, etc.).
  - Soils
    - One soil core per sampling plot (15 cm depth, 7 cm diameter).
    - Measured properties included: bulk density, soil carbon (SOC) and total carbon after inorganic carbon removal, total nitrogen, pH (in water and CaCl2), Olsen P, total P, soil moisture, EC, particle size distribution, aggregate stability, CaCO3, and LOI (for organic matter estimation).
    - LOI used to derive carbon concentration with a standard equation; LOI quality controlled with internal standards.
    - Additional CS-aligned measures included, where applicable, soil moisture and soil macro-fauna counts for comparative contexts.
  - Documentation of sampling specifics
    - Pre-visit plot location determination where possible; on-site validation to ensure representative field selection.

- Laboratory analyses and data processing
  - LOI and C concentration
    - LOI measured on 10 g sub-samples; C calculated as LOI × 0.55 × 10; LOI QC with internal standards.
  - Carbon and nitrogen
    - SOC measured after removing inorganic carbon using a standardized elemental analyzer with quality controls.
  - Phosphorus
    - TOT_P measured after acid digestion; Olsen-P measured in arable/improved grassland samples using standard colorimetric methods with quality controls.
  - pH and electrical conductivity
    - pH measured in deionised water and CaCl2; EC measured in soil suspensions; QA via internal standards.
  - Physical soil properties
    - Bulk density (BD) and fine-earth moisture content calculations; particle size distribution by laser diffraction with replication checks and organics adjustment notes.
    - Aggregate stability assessed via wet sieving protocol; expressed as (A−B)×100/(IW).
    - CaCO3 content determined by thermogravimetric analysis.
  - Data quality and calibration
    - Internal standards and duplicates used across batches; periodic calibration and cross-checks against established CS protocols to ensure data compatibility.

- Data structure and access
  - Four CSV data files, anonymised by farm/site:
    - SEEGSLIP_PLOTS_2018.csv: basic plot attributes, vegetation sampling details, site codes, habitat classifications, slope, aspect, shade, canopy/shrub/ground height descriptors, soil sampling info, and Ordnance Survey grid reference.
    - SEEGSLIP_SPECIES_2018.csv: plot-level species data, including BRC names and codes, nest-level and total cover metrics.
    - SEEGSLIP_SOIL_2018.csv: soil properties by plot/rep, including dry content, conductivity, total carbon and nitrogen, LOI, phosphorus forms, bulk density, particle size fractions, aggregate stability, pH (water and CaCl2), CaCO3, and related metrics.
    - SEEGSLIP_FIELD_MGT_2018.csv: field management and grazing-related data (PFLA membership/certification details, pasture type, grazing timings, stocking, cutting, fertilisation, lime/herbicide use, and other management inputs).
  - Farm data are anonymised; fields include site codes, rep IDs, dates, habitat classifications, and reference IDs for traceability.
  - Prepared to support data merging across sheets for self-serve analyses and cross-study comparisons with Countryside Survey data.

- Context and references
  - Builds on established CS soil and vegetation methodologies (Emmett et al.; Wood et al.; CS technical reports).
  - Aligns with PFLA certification standards and farmer-led environmental outcomes, enabling interpretation of pasture-fed systems’ impacts on biodiversity, soil organic matter, and nutrient cycling.
  - Data are suitable for analyses of relationships between pasture management practices, vegetation structure, and soil quality across UK grassland systems, with potential policy and practice implications.