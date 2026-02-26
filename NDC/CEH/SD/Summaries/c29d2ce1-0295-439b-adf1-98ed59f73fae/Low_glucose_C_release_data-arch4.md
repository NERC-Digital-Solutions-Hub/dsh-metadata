# Time series of microbial carbon release from soil as carbon dioxide under different nitrogen and phosphorus treatments with a low glucose concentration added as a carbon source in the Conwy catchment, North Wales, UK (2015)

## Overview
- Describes an experiment measuring 14CO2 mineralization from soil under varying nitrogen (N) and phosphorus (P) additions with a low glucose carbon source.
- Study location: Conwy catchment, North Wales, UK; incubation at 10°C to reflect mean annual temperature.
- Data intended to support understanding of how nutrient amendments influence microbial carbon release from soil organic matter.

## Data assets and metadata
- Primary data: Low_glucose_C_release_data.csv (14C-CO2 release measurements)
- Metadata: Low_glucose_C_release_data_metadata.csv (column names and descriptions)
- Supporting location data: Plot_locations.csv (borehole/location coordinates)
- Plot metadata: Plot_locations_metadata.rtf (description of fields in Plot_locations.csv)
- Abbreviations and supplementary notes are included (e.g., HWMC, N, P)
- Quality control context: Indicates where to find data quality and reference information

## Experimental design and treatments
- Carbon source: Low concentration glucose added at 0.006 mM
- Treatments (per the application data):
  - Control (no N or P addition)
  - N addition (33.33 units)
  - P addition (3.53 units)
  - N & P addition (N 33.33, P 3.53)
- Each treatment has 42 samples
- Soil: 5 g per sample (dry weight), with 0-30 cm as topsoil, 50-100 cm midsoil, and 100-300 cm subsoil; samples later grouped into topsoil, midsoil, subsoil for analysis
- Study design includes replication across transects/plots

## Soil sampling and preparation
- Soil cores divided into depth intervals: 0-15 cm, 15-30 cm, 50-100 cm, 100-150 cm, 150-200 cm, 250-300 cm; grouped as topsoil, midsoil, subsoil
- Soil mixed and sieved through 5 mm to remove stones/plants and ensure homogeneity
- Sample handling minimizes disturbance to microbial communities

## Measurement protocol (carbon mineralization)
- 5 g dry soil placed in sterile 50 ml tubes
- 14C-glucose labelled nutrient solution (50 µl) added to soil surface
- NaOH trap (1 M) placed in each tube to capture evolved 14CO2
- Tubes sealed and incubated at 10°C
- NaOH traps replaced at multiple time points: 0.5, 1, 2, 4, 6, 24, 48, 72, 96, 120, 144, 168, 192, 336, 504, 672, 840, 1008 hours, then weekly up to 6 weeks
- 14CO2 quantified by mixing traps with Optiphase HiSafe 3 and measuring with a Wallac 1404 liquid scintillation counter

## Data structure and content
- Core identifiers: Transect (plot reference), Row (within-plot location), Depth (cm)
- Time-series data columns (DPM counts):
  - 0.5, 1, 2, 4, 6, 24, 48, 72, 96, 120, 144, 168, 192, 288, 336, 504, 672, 840, 1008 hours
- Additional columns indicate blanks (BLANK) and standard/reference measurements (STD1_HMWC, STD2_HMWC+N, STD3_HMWC + N + P, STD4_HMWC + P)
- Empty cells indicate no data
- Column naming convention reflects DPM counts after each specified time interval

## Plot locations and accessibility
- Borehole locations referenced in Plot_locations.csv
- Description and field definitions available in Plot_locations_metadata.rtf

## Abbreviations and terminology
- HWMC: High Molecular Weight Carbon
- N: Nitrogen
- P: Phosphorus

## Notes for data reuse and quality
- Metadata file provides column names and detailed descriptions; use to interpret data columns accurately
- QC/supporting data include blanks, standard references, and clear time-point labeling
- Data are structured for comparative analysis across treatments, depths, and time points to understand mineralization dynamics under nutrient amendments