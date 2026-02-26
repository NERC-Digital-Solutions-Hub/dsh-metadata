# Soil data from the South Fork McKenzie River in Oregon, USA. Lat/Long: 44.17, -122.30.

## Overview
- Purpose: assess soil variable response to wildfire in restored and unrestored sites, with a reference site nearby.
- Location: South Fork McKenzie River, Oregon; sampling spans near 44.17°N, -122.30°W.
- Data format: a single CSV file containing soil analytical data collected across multiple field campaigns.

## Data Content
- File: SFMR_Soil_Data (1 CSV, approximately 22 KB).
- Core variables:
  - Sampling_Date, FieldID, SampleID, SampNum
  - Site_Type (restored, unrestored, reference)
  - Depth (cm), moisture (wet/dry), Microtopography (high/low)
  - Grain sizes: Sand, Silt, Clay (percentages); Clay_Silt_Pct
  - Texture (USGS classification), OrganicCarbon_pct, TotalCarbon_pct
  - Total_N_ppm, Nitrite_N_ppm, Nitrate_N_ppm
  - Longitude, Latitude
  - DateRecd, DateRept (processing receive and reporting dates)
  - Additional notes on Site_Pairs (duplicates) and sampling identifiers
- Data detail: includes both mineral soil properties and nutrient content (C/N, N-species) along with physical texture.

## Dataset Structure and Sampling Framework
- Structure: 1 dataset named SFMR_Soil_Data with 1 CSV file.
- Columns described as above; key categorical splits by Site_Type (restored, unrestored, reference) and Sampling_Date.
- Sampling design notes:
  - Depths targeted: primarily 0-30 cm; additional 30-60 cm and 60-90 cm possible if feasible.
  - 2020 field campaign: targeted 22 locations per site (11 wet, 11 dry); sites A (restored floodplain), B (unrestored degraded floodplain), C (reference near Horse Creek).
  - 2021 campaigns added to expand depth and site coverage.
  - Duplicates: Site_Pairs indicate paired samples (labels a/b for duplicates); Microtopography indicates sampling from high/low microtopographic areas.
- Sample counts by date: 53 samples (July 2020), 27 samples (February 2021), 34 samples (June 2021).

## Collection Methodology
- 2021 field campaign:
  - 0-30 cm bulk samples collected with a T-bar, sealed in ziplocs, frozen, and shipped to Ward Labs for analysis.
  - Deeper samples (30-60 cm, 60-90 cm) collected where feasible using the same method.
- 2020 field campaign:
  - 22 soil locations per site (11 wet, 11 dry) across three sites (A restored, B unrestored, C reference).
  - Sampling method: standard T-bar probe (~3/4 inch diameter); 0-30 cm horizon, with optional deeper increments if possible.
- Lab processing:
  - Primary analyses include total carbon, organic carbon, and grain-size (Ward Labs).
  - Some analyses cross-checked or quality-controlled via the Moffett lab (Washington State University).

## Quality Control
- Detailed QC performed by Moffett lab (WSU).
- Duplicate samples retained and texture data cross-checked to ensure accuracy where possible.

## Potential Analyses and Uses for Analysts
- Evaluate how soil carbon (OrganicCarbon_pct, TotalCarbon_pct) and total nitrogen (Total_N_ppm) vary by Site_Type (restored vs unrestored vs reference) and by depth.
- Examine relationships between texture (Sand, Silt, Clay, Clay_Silt_Pct) and carbon/nitrogen metrics.
- Assess potential wildfire/land-management effects by comparing 0-30 cm data to deeper horizons where available.
- Explore spatial patterns using Latitude/Longitude to identify geographic clusters of soil properties.
- Investigate temporal changes across sampling dates (2020 vs 2021 campaigns) in soil variables.
- Analyze the influence of moisture status (wet vs dry) and microtopography (high vs low) on measured soil properties.
- Consider data quality and limitations when modeling (e.g., missing moisture data for some samples, incomplete depth coverage, and site-specific conditions).

## Limitations and Considerations
- Moisture data not consistently available for all samples.
- Deeper depth samples are only available where feasible; depth coverage is uneven across sites.
- Some data gaps may exist due to field feasibility and sampling logistics.
- Site_Pairs and Microtopography metadata are important for mixed-effects or stratified analyses.

## Accessibility and Provenance
- Data collected as part of soil monitoring in restored/unrestored/wildfire-impacted habitats.
- Laboratory QC and processing documented; primary analyses performed by Ward Labs (grain size, carbon) and validated by Moffett Lab (WSU).