# Time series of microbial carbon release from soil as carbon dioxide under different nitrogen and phosphorus treatments with a high glucose concentration added as a carbon source in the Conwy catchment, North Wales, UK (2015)

## Overview
- A soil carbon mineralization dataset measuring 14CO2 evolution after adding 14C-labelled glucose across different nutrient treatments (control with glucose, nitrogen, phosphorus, and nitrogen+phosphorus) in the Conwy catchment, North Wales, UK, collected in 2015.
- Incubation at 10°C to reflect mean annual temperature; NaOH traps capture evolved 14CO2 and are analyzed by liquid scintillation counting.
- Data intended to support studies of microbial respiration responses to carbon inputs and nutrient amendments.

## Data and measurements
- Primary data file: High_glucose_C_release_data.csv
- Supporting metadata: High_glucose_C_release_data_metadata.csv clarifies column names and data descriptions; Quality control references in the associated QC/metadata files.
- Abbreviations: HWMC (high molecular weight carbon), N (nitrogen), P (phosphorus).
- Measurement details:
  - 5 g soil per sample (dry weight basis adjusted for moisture)
  - 50 µL of 14C-glucose nutrient solution added per sample
  - NaOH traps (1 M) capture evolving 14CO2; traps replaced at multiple time points and analyzed with a scintillation counter
  - Time series coverage: measurements taken at 0.5, 1, 2, 4, 6, 24, 48, 72, 96, 120, 144, 168, 192, 336, 504, 672, 840, and 1008 hours, with weekly collections up to 6 weeks
  - DPM (disintegrations per minute) counts provided for each time point
- Plot/borehole data:
  - Plot locations specified in Plot_locations.csv
  - Plot_locations_metadata.rtf provides description of arrangement and metadata fields
- Data quality indicators:
  - QC-related columns and standard controls (e.g., STD1_HMWC, STD2_HMWC+N, STD3_HMWC+N+P, STD4_HMWC+P)
  - Blank DPM counts documented (BLANK)
  - Quality control and reference data are contained in High_glucose_C_release_data_metadata.csv

## Experimental design and treatments
- Soil depth sampling and grouping:
  - Depth intervals: 0–15, 15–30, 50–100, 100–150, 150–200, 250–300 cm
  - Grouped into topsoil (0–30 cm), midsoil (50–100 cm), subsoil (100–300 cm) for manuscript interpretation
  - Cores passed through a 5 mm sieve to remove stones/materials and ensure homogeneity
- Treatments:
  - Control (high concentration glucose with no N or P additions)
  - N addition
  - P addition
  - N and P addition
- Replicates and sampling:
  - Each treatment comprises 42 samples
  - 5 g soil per sample, 300 mM glucose added (C addition)
  - N and P additions set according to treatment (e.g., N addition ~33.3 units; P addition ~3.53 units)
- Transects and spatial reference:
  - Each sample linked to a Transect and Row referencing Plot_locations.csv

## Data structure and metadata
- Columns:
  - Transect, Row: spatial identifiers tied to Plot_locations.csv
  - Depth: sampling depth in cm
  - Time interval columns: 0.5 hr, 1 hr, 2 hr, 4 hr, 6 hr, 24 hr, 48 hr, 72 hr, 96 hr, 120 hr, 144 hr, 168 hr, 192 hr, 336 hr, 504 hr, 672 hr, 840 hr, 1008 hr (DPM counts)
- Data notes:
  - Empty cells indicate missing data
  - Units: DPM counts from NaOH-trapped 14CO2
- Related documentation:
  - Plot_locations.csv and its metadata provide site layout
  - Plot_locations_metadata.rtf explains the structure of the location data

## Data quality, provenance, and standards
- Metadata quality:
  - Metadata files explain column meanings and data provenance
  - Blank controls and standard measurements included to assess measurement reliability
- Provenance:
  - Sample collection and laboratory measurement procedures are described (soil preparation, incubation conditions, trapping, and counting)
- Potential limitations:
  - Data gaps indicated by empty cells
  - Varied depth and spatial coverage may affect cross-site comparability
  - Detailed metadata necessary to ensure correct interpretation of units and treatment codes

## Access, reuse, and governance
- Data assets and supporting files:
  - High_glucose_C_release_data.csv (primary data)
  - High_glucose_C_release_data_metadata.csv (column-level definitions)
  - Plot_locations.csv and Plot_locations_metadata.rtf (spatial context)
  - Miscellaneous QC and reference data (as referenced in metadata)
- Use cases for data leaders:
  - Integrating this time-series with other soil carbon flux datasets
  - Assessing how glucose addition and nutrient amendments alter microbial CO2 release across soil depths
  - Evaluating data management practices: metadata clarity, data discoverability, and standardization across datasets
- Accessibility considerations:
  - Data are structured with explicit time-point columns and clear treatment designations, aiding discoverability and re-use
  - Ensure alignment with metadata standards and data sharing policies to maximize interoperability across datasets and networks