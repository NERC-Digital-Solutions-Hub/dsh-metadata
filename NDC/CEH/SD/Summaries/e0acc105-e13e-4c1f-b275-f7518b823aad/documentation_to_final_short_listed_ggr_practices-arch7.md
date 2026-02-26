# Documentation of shortlist of soil-based greenhouse gas removal practices selected following consideration of biophysical, economic and social impacts

## Overview
- Documents a short list of soil-based greenhouse gas removal (GGR) practices aimed at enhancing soil carbon sequestration (SCS) in agricultural land.
- Shortlist results from a multidisciplinary analysis of practices already proposed to deliver SCS.
- Describes the data structure and assessment framework used to compile and justify the shortlisted measures.
- References key literature for methodological context.

## Data structure and fields
- Table 1: Key for data
  - Uses a priority scale: 1 = High importance, 2 = Medium importance, 3 = Low importance; n/a = Not applicable; ? = Further suggestions needed.
  - Justification for priority is provided in per-cell comments.
- Table 2: Header in file with a short description
- Core data fields (examples and purposes):
  - ID, description: crop type
  - IMAGE_region: specific region or country where measures are applied
  - Representative_of?: more specific crop type for the region
  - Rotated_with?: crop for rotation
  - Case_study_country: country where measures are applied
  - Area_harvested_ha: area in hectares
  - Erosion_control, Fire_management, Stocking_density, Pasture_renovation, Sward_management
  - Extend_perennial_phase, Reduce_bare_fallow, Cover_crops, Deep_rooted_plants, Nutrient_management
  - Organic_amendment_inc_grass_to_crops, Residue_management, Add_biochar, pH_management
  - Reduced_no_till, Water_managment, Wetland_management, Agroforestry, Hedges
  - Each measure field has a corresponding comment_n field with data source or data notes
- Notes on data structure:
  - Comments are dataset-specific for each grid cell
  - Data types and descriptors are designed to support GIS mapping and cross-dataset integration

## Method and data (how the shortlist was developed)
- Greenhouse gas removal technologies (GGRTs) include soil carbon sequestration (SCS) in agricultural land.
- Goal: address environmental heterogeneity and practice differences that affect practical SCS implementation.
- Shortlist derived from a multidisciplinary literature review and expert panel input.
- Assessment criteria:
  - Identify practices with potential positive SCS impact at the farm level and uptake compatible with global impact
  - Focus on: optimizing crop productivity (e.g., nutrient optimization, pH management, irrigation)
  - reducing soil disturbance and improving soil physical properties (e.g., rotations, minimum till)
  - minimizing removal of carbon or erosion-driven transport
  - adding carbon produced outside the system (e.g., organic amendments, biochar)
  - providing additional carbon inputs within the cropping system (e.g., agroforestry, cover cropping)
  - Based on Macleod et al. 2015
- Economic and non-cost barriers, incentives, and externalities considered
- Ability of existing scientific approaches to quantify potential and externalities, and barriers to implementation in global agricultural systems assessed
- Final shortlist results from the literature review and expert panel
- Detailed description referenced in:
  - Sykes AJ, Macleod M, Eory V, et al. Characterising the biophysical, economic and social impacts of soil carbon sequestration as a greenhouse gas removal technology. Glob Change Biol. 2020. DOI: 10.1111/gcb.14844
- Additional foundational references:
  - Macleod, M., Eory, V., Gruère, G., & Lankoski, J. (2015). Cost-effectiveness of greenhouse gas mitigation measures for agriculture: A literature review. OECD Publishing.

## Implications for GIS practice
- The data structure is designed to support spatial representation of soil-based GGR measures (regional and country coverage, area harvested, crop types, rotations).
- Fields such as IMAGE_region, Case_study_country, Area_harvested_ha enable creation of thematic maps and region-level analyses.
- Per-measure comments provide data provenance and sources, aiding traceability in map-based products.
- The multi-criteria nature (importance scores and various measures) supports layer-based prioritization and scenario mapping.
- Highlights core GIS needs: data integration across sources, data standards consistency, data cleaning and transformation, and collaboration with domain experts to maintain data quality.