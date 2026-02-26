# Soil data from the South Fork McKenzie River in Oregon, USA. Lat/Long: 44.17, -122.30.

## Overview
- Purpose: Assess soil variable response to wildfire in restored and unrestored sites, with a reference site nearby, to support environmental monitoring and policy performance over time.
- Location: South Fork McKenzie River, Oregon (lat/long 44.17, -122.30).
- Data type and size: Monitoring data; 22 KB; 1 CSV file (SFMR_Soil_Data).
- Use case for analysts: Standardized, traceable soil data enabling cross-site comparisons and temporal monitoring.

## Data Contents
- File: SFMR_Soil_Data.csv with columns:
  Sampling_Date, FieldID, SampleID, SampNum, Site_Type, Depth, moisture, Microtopography, Sand, Silt, Clay, Clay_Silt_Pct, Texture, Longitude, Latitude, OrganicCarbon_pct, TotalCarbon_pct, DateRecd, DateRept, Total_N_ppm, Nitrite_N_ppm, Nitrate_N_ppm.
- Site types: restored, unrestored, reference (Horse Creek near East).
- Depths: 0-30 cm, 30-60 cm, 60-90 cm (where feasible).
- Moisture: wet/dry status (not always available; selected by eye using wetland vegetation cues).
- Grain size and texture: Sand, Silt, Clay, Clay_Silt_Pct; Texture classified by USGS system.
- Carbon and nitrogen: OrganicCarbon_pct, TotalCarbon_pct, Total_N_ppm, Nitrite_N_ppm, Nitrate_N_ppm.
- Spatial and temporal coverage: samples collected across three campaigns.

## Collection Methodology
- Field campaigns: 2020 and 2021.
- Sampling method: 0-30 cm bulk samples collected with a T-bar, bagged, frozen, and shipped to labs; additional deeper samples (30-60, 60-90 cm) if feasible.
- 2020 design: targeted 22 locations per site in floodplain (SFMR) across three sites:
  A) restored floodplain, SFMR transects 1-3
  B) unrestored degraded floodplain, SFMR transects 9-10
  C) undegraded reference at Horse Creek
  - Sampling included 11 wet and 11 dry locations per site when possible; July 2020 sampling with plans for 2021 resampling.
- Sample handling: samples placed in sealed bags, frozen, and mailed to Ward Lab for analyses.
- Labs and QA: Ward Lab for total and organic carbon and grain size; Quality Control by Moffett Lab (Washington State University).

## Dataset Structure & Metadata
- Single dataset: SFMR_Soil_Data.
- Key field definitions:
  - Sampling_Date: collection date
  - Site_Type: treatment category (restored/unrestored/reference)
  - Depth: sampling depth interval
  - Site_Pairs: duplicate sample design (a/b)
  - Microtopography: high/low microtopography
  - Texture: USGS texture classification
  - DateRecd / DateRept: processing and reporting dates
- Geospatial and temporal context supports trend analysis and site comparisons over time.

## Quality Control
- QA performed by Moffett Lab (WSU).
- Duplicates retained where possible; cross-checks for parameters like texture to ensure accuracy.
- Provenance: samples shipped to Ward Lab; processing dates recorded (DateRecd, DateRept).

## Data Management & Accessibility
- Data are organized for traceability (FieldID, SampleID, SampNum, Site_Type, Depth).
- Emphasis on enabling access to underlying data for wider monitoring use and reproducibility.
- Data management aims to store and upload datasets to appropriate data portals to support sharing and scrutiny.

## Relevance to Environmental Monitoring Goals
- Provides standardized soil metrics (texture, moisture, carbon, nitrogen) across restored, unrestored, and reference sites.
- Enables spatial (site-level) and temporal (campaign-level) comparisons to evaluate wildfire impacts and restoration outcomes.
- Supports data-driven assessments and policy performance over time through consistent formats and documented QA.

## Notable Notes and Limitations
- Moisture data gaps: not all samples have wet/dry status.
- 2020 sampling faced limited wet locations at degraded site, affecting the intended 22-sample-per-site design; planned repeat sampling in 2021 to address coverage.
- Underlying data are linked to specific campaigns and site contexts, with explicit sampling depths and duplicate sampling design. 

## References / Data Source
- Ward Lab: https://www.wardlab.com/