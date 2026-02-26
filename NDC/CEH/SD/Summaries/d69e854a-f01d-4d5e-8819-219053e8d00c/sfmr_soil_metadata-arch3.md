# Soil data from the South Fork McKenzie River in Oregon, USA.

## Overview
- Data type: Monitoring
- Size: 22KB
- Interpreted by: All authors
- Collection purpose: To assess soil variable response to wildfire in restored and unrestored sites
- Study sites: Restored, unrestored floodplain sites, plus a nearby unburned reference site at Horse Creek (east)

## Dataset contents
- Single data file: SFMR_Soil_Data.csv
- Key fields and what they represent:
  - Sampling_Date: date of sample collection
  - FieldID: field campaign identifier
  - SampleID: unique sample identifier
  - SampNum: sampling number
  - Site_Type: treatment category (restored, unrestored, or reference)
  - Depth: soil depth sampled (0-30 cm, 30-60 cm, 60-90 cm when feasible)
  - moisture: sample moisture status (wet or dry)
  - Microtopography: site microtopography (high or low)
  - Sand, Silt, Clay: percent grain-size fractions
  - Clay_Silt_Pct: combined clay or silt percentage
  - Texture: USGS soil texture classification
  - Longitude, Latitude: sampling coordinates
  - OrganicCarbon_pct, TotalCarbon_pct: carbon content by percentage
  - DateRecd, DateRept: dates samples were received and results reported
  - Total_N_ppm, Nitrite_N_ppm, Nitrate_N_ppm: nitrogen measurements in ppm
- Additional notes:
  - Site_Pairs denote duplicate samples for a site
  - Metadata includes field campaign context and how microtopography and moisture were recorded

## Sampling and collection methods
- 2021 field campaign:
  - 0–30 cm bulk samples collected with a T-bar probe; placed in Ziploc bags, frozen, and shipped to Ward Labs or to Colorado collaborators
  - Additional 30–60 cm and 60–90 cm depths collected if feasible
- 2020 field campaign:
  - Targeted 22 soil samples per site in floodplain area, randomly sampled; 11 in wet locations and 11 in dry locations
  - Sites:
    - (A) Restored floodplain area around monitoring transects 1–3 (SFMR)
    - (B) Unrestored degraded floodplain area around transects 9–10 (SFMR)
    - (C) undegraded reference area at Horse Creek
  - Protocol: ~3/4 inch diameter T-bar probe; 0–30 cm horizon with potential deeper samples if possible; samples bagged and frozen for shipment to Ward Lab

## Samples and collection dates
- 53 samples collected in July 2020
- 27 samples collected in February 2021
- 34 samples collected in June 2021

## Dataset structure and column definitions
- File: SFMR_Soil_Data.csv
- Columns and meanings (at-a-glance):
  - Sampling_Date: collection date
  - FieldID: field campaign ID
  - SampleID: unique sample ID
  - SampNum: sampling number
  - Site_Type: restored, unrestored, or reference
  - Depth: sampling depth (0-30, 30-60, 60-90 cm)
  - moisture: wet or dry sampling condition
  - Microtopography: high or low microtopography area
  - Sand, Silt, Clay: percent grain-size fractions
  - Clay_Silt_Pct: combined clay and silt percentage
  - Texture: texture class (USGS system)
  - Longitude, Latitude: geographic coordinates
  - OrganicCarbon_pct, TotalCarbon_pct: carbon content percentages
  - DateRecd: date sample was received for processing
  - DateRept: date results were reported
  - Total_N_ppm, Nitrite_N_ppm, Nitrate_N_ppm: nitrogen species concentrations
- Notes on data structure:
  - Site_Pairs indicates duplicates from the same site
  - Samples may be linked to specific field campaigns via FieldID

## Quality control
- Quality control conducted by Moffett lab (Washington State University)
- Duplicates retained where possible; cross-checks performed for select parameters (e.g., texture) to ensure accuracy