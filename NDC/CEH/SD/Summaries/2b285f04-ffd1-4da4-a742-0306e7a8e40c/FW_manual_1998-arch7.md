# Countryside Survey 2000. Module 2: survey of freshwater habitats. Field handbook v.2.0

## Overview for GIS Specialists
- Purpose: produce map-based data products to understand and explore freshwater habitat features across Great Britain.
- Core outputs: spatial data layers from River Habitat Survey (RHS), vegetation and land-use data, substrate and channel morphology, and SERCON conservation assessments.
- GIS relevance: standardised field procedures enable comparable time-series analysis and integration with satellite/remote-sensed land-cover data.

## Spatial data structure and data layers
- Sampling units: 1 x 1 km squares (CS1990 baseline; CS2000 expands to 568 squares with 435 sampled in CS2000 CS1990 framework).
- Time series: repeat sampling to build timeseries; CS2000 aims to connect top-down remote sensing with bottom-up field data.
- Key spatial layers and attributes:
  - River Habitat Survey (RHS) components: 500 m central reach around macro-invertebrate sampling site; 50 m RHS sub-reach around the site; spot-checks along the 500 m.
  - Substratum and bed materials: bedrock, boulder, cobble, gravel/sand, silt, plant cover; percent cover estimates across the 500 m.
  - Channel features and flow types: riffles, pools, rapids, waterfalls, boiles, flats, pontoon-like features; flow types (FF, CH, BW, CF, RP, UP, SM, NO).
  - Banktop land-use and vegetation structure (within 5 m of banktop across 10 m transects) and channel vegetation types (within 10 m transect).
  - Land-use within 50 m of river: categories like woodland, pasture, arable, wetland, open water, urban, etc.
  - Channel dimensions and modifications: bankfull width, banktop height, bankfull height, embankments, revetments, fords, culverts, weirs, dams, etc.
  - Riparian vegetation naturalness and SERCON indicators: percentage natural/semi-natural vegetation along banks and in riparian zones; vegetation types typical of river corridors; presence of alien species.
  - Alders and alder disease indicators (Phytophthora-related data) and other features of special interest.
- Data outputs: structured field forms (RHS and SERCON components) and mapped coordinates (mid-site grid references, OS grid references, National Grid References).

## Sampling framework and spatial units (GIS-ready design)
- Core sampling plan:
  - Re-sampling of 1990 CS1990 squares (508 previously sampled, with replacements for Isle of Man sites).
  - Additional sites: up to 30 new squares for country-unit estimates; 568 total potential CS2000 sites.
  - Two square types: repeat 1990 squares and new 1998 CS2000 squares (with reserve sites MR for M-pref sampling if needed).
- Data capture points:
  - Macro-invertebrate sampling site marked as 'M'; reserve sites 'MR' if the primary site is dry.
  - RHS and chemical sampling tied to the 500 m RHS reach and the 50 m RHS reach around the M site.
- Geometry and coordinate data:
  - Mid-site grid references (OS grid) recorded for precise GIS placement.
  - 1:10,000 and 1:50,000 scale maps provided to field teams for spatial planning and location tagging.

## Data collection, metadata, and governance (GIS metadata alignment)
- Field forms and identifiers:
  - RHS form (Part Three) with spot-checks and sweep-up data; SERCON component forms for conservation assessment; accompanying spot-check key and guidance notes.
  - Each sample container labeled with site identifiers (land class/square number), date, sampler names, replicate status, and sample type.
- Spatial tagging and documentation:
  - Maps supplied for each square showing macro-invertebrate sampling site (M) and reserve sites (MR).
  - On-field marking of sampling locations on 1:10,000 maps; upper/lower RHS limits; D (diatoms) and C (chironomid pupal exuviae) sites marked on maps.
- Data quality and standardization:
  - Emphasis on consistent field procedures to minimise observer effects; approx. 60% of BMWP taxa captured in three-minute pond-net sampling, with replicates for quality control.
  - Accredited RHS surveyors; QA processes include 10% replicate sampling, inter-/intra-operator checks, and audit sampling.

## Data standards, quality control, and interoperability (GIS integration)
- Standardization and accreditation:
  - RHS surveyors must be accredited; training and testing ensure consistency across teams and regions.
  - SERCON components integrated with RHS data to support a standardized conservation scoring framework.
- Quality control mechanisms:
  - Replicate sampling, team member swapping, and auditing of RHS surveys.
  - Regular field training and calibration to harmonize data collection techniques.
- Data integration readiness:
  - Data designed to link with ITE Land Classification System, satellite imagery, and national datasets (e.g., land cover maps, hedgerow schemes).
  - Clear, consistent coding for land use, substrate, and vegetation types to support GIS analyses and cross-time comparisons.

## Practical GIS workflow and use-cases
- Workflow highlights:
  - Use 1 km square geometry as the spatial unit; build 500 m RHS reach polygons around sampling points for habitat analysis.
  - Create attribute tables for RHS, including substratum composition, flow types, channel features, and land-use categories.
  - Integrate SERCON scores with RHS attributes to generate conservation/value maps for river corridors.
  - Produce time-series layers by comparing CS1990, CS1998, and CS2000 data where squares repeat.
- Potential analyses:
  - Change detection in land use and river morphology; assessment of habitat quality and connectivity.
  - Spatial correlation of physical habitat features with biological indicators (RIVPACS macroinvertebrate data).
  - Mapping alder disease presence and protoxicity indicators for disease risk assessment.
  - Identification of priority areas for restoration (recreatable vs unrecreatable wetlands in floodplains).

## Challenges and considerations for GIS data management
- Data fragmentation:
  - Data held across multiple modules (RHS, SERCON, macroinvertebrate sampling, diatoms, chironomid exuviae, chemical data) and across organizations; integrating into a single GIS requires careful schema alignment.
- Multi-resolution data:
  - Field data at 1 km square and 500 m/50 m reach scales; aligning these with coarser satellite-based land cover and finer local site data requires robust generalization rules.
- Standardization and reproducibility:
  - Variability in field procedures historically; emphasis on standardized RHS procedures and accredited surveyors to maintain comparability across time and space.
- Timeseries and policy relevance:
  - Re-surveys (CS2000) intended to inform government policies; GIS outputs should support trend analyses and policy-relevant reporting (e.g., habitat change, hedgerow impacts, river conservation status).