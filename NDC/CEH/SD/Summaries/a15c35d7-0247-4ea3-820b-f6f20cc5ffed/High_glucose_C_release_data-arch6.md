# Time series of microbial carbon release from soil as carbon dioxide under different nitrogen and phosphorus treatments with a high glucose concentration added as a carbon source in the Conwy catchment, North Wales, UK (2015)

## Purpose and scope
- Document describes time-series data on microbial carbon release as CO2 from soil, using 14C-glucose as carbon source, under varying N and P treatments in the Conwy catchment, North Wales, UK (2015).
- Data support four treatments (Control, N, P, N&P) with high glucose (300 mM) and 42 samples per treatment, enabling analysis of carbon mineralization across depth and treatment.

## Data and files
- High_glucose_C_release_data.csv: application data containing 14C-CO2 release (DPM) over time for each soil sample.
- High_glucose_C_release_data_metadata.csv: quality control and reference data; column names and descriptions for the data file.
- Plot_locations.csv: borehole/plot locations referenced by Transect and Row.
- Plot_locations_metadata.rtf: description of Plot_locations.csv.
- Miscellaneous supporting documents: quality control and reference data files referenced in metadata.

## Sampling and laboratory methods
- Soil sampling and preparation:
  - Soil cores collected and divided into depth intervals: 0–15, 15–30, 50–100, 100–150, 150–200, 250–300 cm (grouped as topsoil 0–30 cm, midsoil 50–100 cm, subsoil 100–300 cm).
  - Cores passed through a 5 mm sieve to remove stones and ensure homogeneity.
- Carbon mineralization assay:
  - 5 g soil (dry weight equivalent) placed in sterile tubes.
  - 14C-glucose labeled nutrient solution added to the soil surface.
  - NaOH trap (1 M) placed in each tube to capture evolved 14CO2; tubes sealed and incubated at 10°C.
  - NaOH traps changed at 0.5, 1, 2, 4, 6, 24, 48, 72, 96, 120, 144, 168, 192, 336, 504, 672, 840, 1008 hours, then weekly up to 6 weeks.
  - Captured 14CO2 quantified by mixing traps with scintillation fluid and counting with a liquid scintillation counter (Wallac 1404).
- Data capture and measurement:
  - 14C-substrate mineralization tracked as disintegrations per minute (DPM) over time.

## Data structure and key fields
- Core identifiers:
  - Transect (Cage location) and Row (Cage location) reference Plot_locations.csv.
  - Depth (cm) of soil sample.
- Time-series measures:
  - DPM counts at listed time intervals: 0.5, 1, 2, 4, 6, 24, 48, 72, 96, 120, 144, 168, 192, 288, 336, 504, 672, 840, 1008 hours.
  - Empty cells indicate no data.
- Quality control fields (as described in metadata):
  - BLANK: DPM count for blank.
  - STD1_HMWC, STD2_HMWC+N, STD3_HMWC+N+P, STD4_HMWC+P: standard/reference measurements.
- Experimental design notes:
  - Application data includes four treatments with corresponding nutrient additions:
    - Control: N 0, P 0; N addition = 0, P addition = 0.
    - N: N addition = 33.3, P addition = 0.
    - P: N addition = 0, P addition = 3.53.
    - N&P: N addition = 33.3, P addition = 3.53.
  - Carbon addition (C addition) = 300 mM for all samples.
  - Number of samples per treatment = 42; Dry weight soil per sample = 5 g.

## Abbreviations and units
- HWMC: high molecular weight carbon.
- N: nitrogen.
- P: phosphorus.
- DPM: disintegrations per minute (radioactivity count).
- Depth: centimeters.
- Time: hours since nutrient addition.

## Data quality, provenance, and access notes
- Metadata file provides column descriptions and data provenance.
- Plot locations are linked to samples via Transect/Row references; exact locations described in Plot_locations.csv and its metadata.
- Data notes: empty cells indicate missing data; multiple time points require careful alignment when analyzing the time-series.

## Practical considerations for use
- Suitable for examining how C mineralization (14C-glucose-derived CO2) responds to N and/or P amendments across depth profiles.
- Can be used to compare topsoil, midsoil, and subsoil responses and to explore temporal dynamics of mineralization over the 1008-hour window (about 42 days).
- Consider using the QC fields (BLANK, STD*) to assess measurement quality and to calibrate or normalize DPM values.