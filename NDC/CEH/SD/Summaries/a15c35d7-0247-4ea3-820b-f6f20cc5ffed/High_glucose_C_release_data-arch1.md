# Time series of microbial carbon release from soil as carbon dioxide under different nitrogen and phosphorus treatments with a high glucose concentration added as a carbon source in the Conwy catchment, North Wales, UK (2015)

## Overview
- Study of microbial carbon mineralization to CO2 using 14C-glucose as a carbon source in soils from the Conwy catchment, North Wales, UK, 2015.
- Soils were subjected to four nutrient treatments: Control (glucose only), N (glucose + nitrogen), P (glucose + phosphorus), and N&P (glucose + nitrogen + phosphorus).
- 14CO2 evolved captured in 1 M NaOH traps over a long time course, with counts measured by liquid scintillation counting.
- Incubations performed at 10°C to reflect mean annual catchment temperature.
- Soil sampling depths grouped into topsoil (0–30 cm), midsoil (50–100 cm), and subsoil (100–300 cm) with multiple discrete depths within these ranges.

## Experimental design and treatments
- Treatments and samples
  - High concentration glucose (C addition = 300 mM) with:
    - Control: N addition = 0, P addition = 0
    - N: N addition = 33.3, P addition = 0
    - P: N addition = 0, P addition = 3.53
    - N&P: N addition = 33.3, P addition = 3.53
  - Dry soil per sample: 5 g
  - Number of samples per treatment: 42
- Substrates and labels
  - 14C-glucose labeled substrate solution added to soil surface
  - Abbreviations in metadata: HWMC = high molecular weight carbon; N = nitrogen; P = phosphorus

## Sampling and measurement protocol
- Soil core preparation
  - Cores divided into depth intervals: 0–15 cm, 15–30 cm, 50–100 cm, 100–150 cm, 150–200 cm, 250–300 cm
  - Samples sieved to 5 mm to remove stones and plant material
  - Grouped into topsoil (0–30 cm), midsoil (50–100 cm), subsoil (100–300 cm)
- 14CO2 measurement
  - 5 g soil placed in 50 mL tubes
  - 50 µL of 14C-glucose nutrient solution added
  - NaOH trap (1 M) added to capture evolving 14CO2
  - Tubes sealed and incubated at 10°C
  - NaOH traps replaced at 0.5, 1, 2, 4, 6, 24, 48, 72, 96, 120, 144, 168, 192, 336, 504, 672, 840, 1008 hours, then weekly for 6 weeks
  - 14CO2 quantified by mixing NaOH trap with scintillation fluid and counting with a Wallac 1404 counter

## Data structure and variables
- Data files
  - High_glucose_C_release_data.csv: time-series DPM (disintegrations per minute) counts
  - High_glucose_C_release_data_metadata.csv: quality control and column definitions; includes hours and blank/standard columns
  - Plot_locations.csv: borehole/plot locations
  - Plot_locations_metadata.rtf: description of Plot_locations.csv
- Column structure in time-series data
  - Identifier columns: Transect, Row, Depth (cm)
  - Timepoint columns (DPM counts in counts per minute)
    - 0.5, 1, 2, 4, 6, 24, 48, 72, 96, 120, 144, 168, 192, 288, 336, 504, 672, 840, 1008 hours
  - Empty cells indicate missing data
- Additional details
  - Columns include blanks for 0.5–1008 hour timepoints
  - Standard and blank DPM counts are included in QC metadata (STD1_HMWC, STD2_HMWC+N, STD3_HMWC+N+P, STD4_HMWC+P)

## Potential analyses and uses
- Analyze how nitrogen and phosphorus additions influence microbial carbon mineralization over time
- Compare depth-wise (topsoil vs midsoil vs subsoil) responses to nutrient additions
- Model decay/uptake kinetics and estimate mineralization rate constants under different treatments
- Assess cumulative CO2 production over the entire time course and identify peak emission periods
- Correlate mineralization patterns with soil properties if available, and compare against standard/control baselines

## Data quality, limitations, and provenance
- Data are structured as time-series DPM counts with multiple timepoints per sample; careful handling of missing data is required
- Data are specific to a single catchment (Conwy, North Wales) and incubation conditions (10°C, 300 mM glucose) and may not generalize without adjustment
- Depth grouping into topsoil/midsoil/subsoil provides a coarse vertical resolution; individual depth intervals are listed in sampling methodology
- Metadata and QC files accompany the data to facilitate interpretation and reproducibility

## Access and related materials
- Primary data: High_glucose_C_release_data.csv
- Metadata and QC definitions: High_glucose_C_release_data_metadata.csv
- Plot locations: Plot_locations.csv
- Plot locations description: Plot_locations_metadata.rtf