# Soil data from the South Fork McKenzie River in Oregon, USA

## Overview
- Data Type: Monitoring
- Size: 22KB
- Interpreted by: All authors
- Collection purpose: To assess soil variable response to wildfire in restored and unrestored sites

## Dataset scope and purpose
- Location: South Fork McKenzie River, Oregon, USA
- Dataset contains soil properties from multiple depths and sites (restored, unrestored, reference)
- Core variables include moisture, grain size (sand, silt, clay; USGS texture), organic carbon, total carbon, total nitrogen, nitrate, and nitrite
- Data file: SFMR_Soil_Data.csv
- Sample coverage: 53 samples (July 2020), 27 samples (February 2021), 34 samples (June 2021)

## Data structure and fields
- Key columns:
  - Sampling_Date, FieldID, SampleID, SampNum
  - Site_Type (restored, unrestored, or reference)
  - Depth, moisture, Microtopography
  - Sand, Silt, Clay, Clay_Silt_Pct, Texture
  - Longitude, Latitude
  - OrganicCarbon_pct, TotalCarbon_pct
  - DateRecd, DateRept
  - Total_N_ppm, Nitrite_N_ppm, Nitrate_N_ppm
- Additional context:
  - Sampling_Date = collection date
  - FieldID = field campaign ID
  - SampleID = specific sample ID
  - Site_Pairs indicates duplicate samples; Microtopography indicates high/low areas
  - Texture uses USGS classification
- Notable data nuances:
  - Moisture data may be missing for some samples (wet/dry locations chosen by eye using wetland vegetation)

## Collection methodology and timeline
- 2021 field campaign:
  - 0–30 cm bulk samples collected with a T-bar probe
  - Samples bagged, frozen, and shipped to Ward Lab or Colorado collaborators for analyses (total carbon, organic carbon, and grain size)
  - Additional samples planned for 30–60 cm and 60–90 cm depths if feasible
- 2020 field campaign:
  - Targeted 22 soil samples per site (11 wet, 11 dry) in floodplain
  - Sites:
    - A: Restored floodplain area (SFMR monitoring transects 1–3)
    - B: Unrestored degraded floodplain (SFMR monitoring transects 9–10)
    - C: Reference area near Horse Creek
  - July 2020 sampling; used standard T-bar soil sampling probe
  - Depths: 0–30 cm; deeper if feasible
  - Sample counts: 53 (July 2020), 27 (Feb 2021), 34 (June 2021)

## Quality control and provenance
- Quality Control: Conducted by Moffett lab, Washington State University
- Procedures:
  - Duplicate samples retained where possible
  - Cross-check of selective parameters (e.g., texture) to ensure accuracy

## Data governance and sharing considerations
- Data carrier: SFMR_Soil_Data.csv with geolocated samples (Longitude/Latitude) and detailed metadata
- Metadata captured includes sampling dates, site types, depths, moisture, microtopography, grain-size distribution, texture, and processing dates (DateRecd, DateRept)
- Processing and provenance are documented through collection notes and QC routines, supporting traceability and reuse

## Limitations and challenges
- Moisture data are not consistently available across all samples
- Some depths beyond 0–30 cm depend on feasibility; deeper samples were attempted only if possible
- Multi-year, multi-site collection and cross-lab analyses may require harmonization of methods and metadata for interoperability