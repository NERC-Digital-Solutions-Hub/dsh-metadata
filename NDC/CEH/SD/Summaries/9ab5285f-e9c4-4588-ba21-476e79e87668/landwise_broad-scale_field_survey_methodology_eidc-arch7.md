# Aim Quantify the impact of different land use and management strategies on key soil properties that affect infiltration and water storage across the main soils type in the West Thames catchment.

## Objective overview for GIS work
- Define a field-based sampling program to quantify how land use and management affect near-surface soil properties and vegetation in fields under Natural Flood Management (NFM) measures.
- Target properties: soil texture, soil organic matter (SOM), volumetric water content (VWC), bulk density (BD), vegetation type/height/cover, soil aggregate stability (slaking/dispersion), and soil structure (Visual Evaluation of Soil Structure; VESS).
- Produce spatially-resolved data to support map-based analyses and decision-making for flood management and land use planning.

## Sampling design: field scale and replication
- Factor structure (fixed effects to control):
  - Land use: Arable, Grassland (permanent, >5 years), Woodland (broadleaf, mature)
  - Management (sub-class for arable): Arable rotation with grass, Arable rotation without grass
- Covariates / random effects (to account for variability):
  - Management practices, Crop types, Rotation, Tillage (Organic, Conventional, Min Till, No Till), Cover Crops, Controlled Traffic, Field Drainage, Flooding History, etc.
- Soil type classification (principal soil types on carbonate and mudstone geology):
  - Shallow chalk/limestone (carbonate)
  - Free draining loamy (carbonate)
  - Impeded drainage loamy/clayey (carbonate)
  - Free draining sandy/loamy (sandstone)
  - Naturally wet or slowly permeable loamy/clayey (mudstone)
  - Floodplain or high groundwater loamy/clayey (mudstone)
- Target sampling plan:
  - Ideally 20 combinations (4 land use/management classes x 5 soil types)
  - Approximately 8 replicates per combination, totaling around 160 fields
  - Up to 2000 samples in total (subject to field availability)
  - Avoid pseudo-replication: at most one field/plot per farm per soil/land-use cell; multiple fields in same cell allowed if land-use/management differs
  - Practical adjustments may focus on particular soil types or sites

## Sampling strategy by field type
- Grassland
  - 15 sampling locations per field:
    - 5 infield
    - 5 trafficked (cropped headland or tramlines)
    - 5 untrafficked margin (uncultivated/uncropped, >1 m from stems/burrows)
  - 3 VESS samples across locations
- Woodland
  - Distinct WD sampling: mineral and organic layers (e.g., WD-M and WD-O as needed)
  - 6 mineral samples (1 VESS) and 6 organic samples (if >50 mm organic layer; otherwise skip)
- Arable
  - Similar 15-location framework as Grassland, with VESS sampling where applicable
- VESS (Visual Evaluation of Soil Structure)
  - One VESS location per Trafficked and one per Untrafficked subset (Grassland/Arable)
  - In Woodlands, VESS applied to appropriate soil layer(s) as per site

## Fixed-volume and additional samples per field
- Fixed-volume samples (0–51 mm bgl)
  - 6 samples per field in mineral layer (surface) + 6 if an organic layer is present (WD or field appropriate)
- Additional small samples per grid cell
  - 6 or 12 extra small samples (0–50 mm bgl) for SOM, slaking, texture assessment, bulked by grid cell
  - Bulk by grid cell to yield 6 or 12 additional samples per plot
- Total per field varies with soil/vegetation type and organic layer depth
  - VESS sampling integrated within the above locations

## Pre-survey and on-site actions ( GIS data integration)
- Landowner engagement and consent; identify potential fields/plots
- Gather base maps and contextual layers:
  - 1:10k or 1:25k OS field boundaries
  - Local soil maps (e.g., SoilScapes)
  - Defra MAGIC map for designated areas (lightly restricted sites)
- Exclude fields with multiple soil types or designated areas that complicate uniform sampling
- Coordinate survey date/time and field meet-ups; ensure access and safety
- Labeling and documentation plan for field codes, sample codes, and farm identifiers

## On-site data collection workflow
- Photos and field records:
  - Field ID card, general site photos, vegetation cover photos
  - GPS coordinates in British National Grid (to nearest metre or decimal degrees)
  - Vegetation height estimates (with ranges)
- Sampling execution:
  - Prepare ground, remove surface debris, insert a 50 mm diameter ring to 0 mm depth
  - Collect fixed-volume 0–51 mm sample (V) into pre-labeled bags; time-stamp
  - Collect 0–50 mm additional sample (A) adjacent to V location; document and bag
  - If surface organic layer >50 mm, collect WD-O samples first, then WD-M samples
  - If VESS sampling is designated, perform VESS per method sheet and record results
  - Mark and group samples by field; clean equipment between sites
- Post-sampling notes:
  - Record exact location details, sampling times, and environmental conditions
  - Note any potential risks or field modifications

## Post-survey data handling and transport
- Digitize field survey records and store electronic copies with consistent naming (e.g., Farm, Field, Date)
- Store photos and documents in organized folders per field and date
- Temporary storage of samples in a cool, dark place; batch deliveries to CEH/UoR coordinators
- Ship or deliver samples to CEH for long-term storage (e.g., in a fridge) and link to corresponding field data
- Share consent forms, field records, and photos with CEH for integration with GIS datasets
- Regularly clean equipment to prevent cross-site contamination

## Laboratory analysis and texture assessment
- Primary analyses (lab):
  - Particle Size Distribution (for texture classification)
  - Organic matter content (where available)
- Texture classification guidance:
  - Hand texture assessment to categorize soils into texture groups (sand, sandy loam, loam, silt loam, clayey, etc.)
  - Use texture triangle for final grouping; differentiate by aggregate or calcareous content as needed
- Calcareous content estimation (for calcareous soils):
  - Guidance on interpreting hydrogen chloride tests and related indicators is provided for context
- Output:
  - Quantitative texture fractions (sand/silt/clay), OM content
  - Texture group assignments aligned with Defra soil management frameworks

## Data and quality considerations for GIS specialists
- Harmonize data sources: field codes, soil type classifications (LANDWISE Soil.Type), land-use classes, and VESS scores
- Ensure consistent spatial referencing (BNG/OSGB 1936) and precise GPS coordinates
- Maintain explicit links between field plots and map layers (soil type, land use, NFM measures)
- Plan for non-uniform replication and document any deviations from the ideal 20 x 5 (soil type x land-use) matrix
- Use standardized sample labeling and metadata to facilitate GIS integration and reproducibility

## Equipment and logistics (highlights)
- Soil rings (50 mm ID), hand hammer, trowels/spades, knives, plastic sample bags
- Field maps, OS maps, SoilScapes, MAGIC maps
- PPE and safety gear, GPS-enabled devices, camera, data sheets or tablets
- Sample grouping materials and transport containers for CEH/UoR transfer
- Data management workflow: digitization, file naming, and organized storage of digital copies and photos

## Key notes and references
- Texture assessments and class definitions are guided by established soil science handbooks and RB209-related methods
- The protocol emphasizes avoiding pseudo-replication, capturing field-level variability, and aligning sampling with field-specific land-use and management practices
- The LANDWISE framework and related field method sheets drive the sampling and data collection processes, including VESS, grid-cell sampling, and field observations