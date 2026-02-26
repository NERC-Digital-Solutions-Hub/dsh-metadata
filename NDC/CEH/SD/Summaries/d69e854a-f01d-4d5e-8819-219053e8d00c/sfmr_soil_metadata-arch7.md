# Soil data from the South Fork McKenzie River in Oregon, USA. Lat/Long: 44.17, -122.30.

## Overview
- Data Type: Monitoring
- Size: 22KB
- Collection purpose: Assess soil variable response to wildfire in restored and unrestored sites
- Interpreted by: All authors
- Geographic focus: South Fork McKenzie River area, Oregon; sampling near Horse Creek to the east

## Data Description
- Data file: SFMR_Soil_Data.csv
- Key columns:
  - Sampling_Date, FieldID, SampleID, SampNum
  - Site_Type (restored, unrestored, or reference)
  - Depth (cm)
  - moisture (wet/dry)
  - Microtopography
  - Sand, Silt, Clay (percentages)
  - Clay_Silt_Pct (percent clay or silt)
  - Texture (USGS classification)
  - Longitude, Latitude
  - OrganicCarbon_pct, TotalCarbon_pct
  - DateRecd, DateRept
  - Total_N_ppm, Nitrite_N_ppm, Nitrate_N_ppm

## Grain-size standards
- Clay ≤ 0.002 mm
- Silt > 0.002 to ≤ 0.05 mm
- Sand > 0.05 to ≤ 2.0 mm
- Grain-size data provided as percentages aligned with Ward Laboratories standards

## Collection Methodology
- 2021 field campaign: 0–30 cm bulk samples collected with a T-bar, bagged, frozen, and shipped to Ward Lab for total carbon, organic carbon, and grain size analysis
- Additional sampling at 30–60 cm and 60–90 cm if feasible
- 2020 field campaign: targeted 22 locations per site in the floodplain; random within floodplain with 11 wet and 11 dry per site
  - Sites:
    - A: Restored floodplain (SFMR transects 1–3)
    - B: Unrestored degraded floodplain (SFMR transects 9–10)
    - C: Reference area at Horse Creek
- Sampling method: T-bar soil sampling probe (~3/4 inch diameter); 0–30 cm horizon; deeper if possible; samples bagged and frozen for shipment to Ward Lab
- Sampling timeline: July 2020 (53 samples), February 2021 (27 samples), June 2021 (34 samples)

## Dataset Structure
- File: SFMR_Soil_Data.csv (1.csv)
- Columns include: Sampling_Date, FieldID, SampleID, SampNum, Site_Type, Depth, moisture, Microtopography, Sand, Silt, Clay, Clay_Silt_Pct, Texture, Longitude, Latitude, OrganicCarbon_pct, TotalCarbon_pct, DateRecd, DateRept, Total_N_ppm, Nitrite_N_ppm, Nitrate_N_ppm
- Descriptors:
  - Sampling_Date: date of collection
  - FieldID: field campaign identifier
  - SampleID: specific sample identifier
  - Site_Type: restored, unrestored, or reference
  - Depth: depth of sampling (cm)
  - moisture: sample moisture status
  - Microtopography: high or low microtopography
  - Location coordinates specify sample site
  - Carbon and nitrogen metrics provided as percentages or ppm

## Quality Control and Provenance
- Quality Control performed by Moffett Lab (Washington State University)
- Duplicates retained; cross-referenced parameters (e.g., texture) to ensure accuracy

## Location and Coverage
- Study area: South Fork McKenzie River, Oregon
- Reference site: near Horse Creek (east of SFMR)
- Focus on floodplain soils across restored, unrestored, and reference conditions
- Depth-led sampling to compare surface and sub-surface soil properties

## GIS and Data Use Applications
- Create map-based visualizations comparing soil properties across Site_Type and depths
- Analyze spatial patterns of organic carbon, total carbon, and nitrogen species
- Integrate with other GIS layers (e.g., wildfire impact, restoration status, microtopography) for policy and outreach
- Use coordinates to plot sample locations and generate spatial summaries

## Limitations and Considerations
- Some moisture measurements missing across sites
- Depth coverage limited to 0–90 cm where feasible; not always achieved
- Year-to-year sampling variability (2020–2021) may affect comparability
- Data includes duplicates and microtopography classifications that require careful handling in GIS analyses

## Access and Format
- Format: CSV
- File name: SFMR_Soil_Data.csv
- Size: 22KB
- Provides geospatial coordinates (Longitude, Latitude) and multiple soil chemistry metrics suitable for GIS mapping and analysis