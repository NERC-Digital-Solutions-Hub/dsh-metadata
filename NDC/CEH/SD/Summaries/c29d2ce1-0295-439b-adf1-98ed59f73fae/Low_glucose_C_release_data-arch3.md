# Time series of microbial carbon release from soil as carbon dioxide under different nitrogen and phosphorus treatments with a low glucose concentration added as a carbon source in the Conwy catchment, North Wales, UK (2015)

## Overview
- Longitudinal measurements of microbial carbon mineralization to CO2 in soil under varying nitrogen (N) and phosphorus (P) treatments with a low concentration glucose carbon source.
- Location: Conwy catchment, North Wales, UK; study year: 2015.
- Data capture through 14C-labeled glucose and NaOH CO2 traps to quantify 14CO2 evolution over time.

## Experimental design and treatments
- Treatments: four conditions – Control (low glucose only), N addition, P addition, and N&P addition.
- Carbon source: low concentration glucose added at 0.006 mM.
- Nutrient additions: N and P added as specified per treatment (e.g., N addition 33.33; P addition 3.53; combinations reflect N, P, or both).
- Replication: 42 samples per treatment.
- Sample size: 5 g of dry-weight soil per sample.

## Soil sampling and preparation
- Depth intervals: 0-15 cm, 15-30 cm, 50-100 cm, 100-150 cm, 150-200 cm, 250-300 cm.
- Grouping by depth: topsoil (0-30 cm), midsoil (50-100 cm), subsoil (100-300 cm).
- Processing: soils were divided and passed through a 5 mm sieve to remove stones/plant material and improve homogeneity, minimizing microbial community disturbance.

## Carbon mineralization measurement
- Procedure: 5 g soil placed in sterile tubes; 14C-glucose solution added to the surface; NaOH trap (1 M, 1 mL) placed in each tube to capture evolved 14CO2.
- Incubation: 10°C to reflect mean annual catchment temperature.
- Timepoints for trap changes: 0.5, 1, 2, 4, 6, 24, 48, 72, 96, 120, 144, 168, 192, 288, 336, 504, 672, 840, and 1008 hours, then weekly up to 6 weeks.
- Measurement: trapped CO2 quantified by mixing NaOH trap contents with Optiphase HiSafe 3 and counting with a Wallac 1404 liquid scintillation counter.
- Output units: disintegrations per minute (DPM).

## Data structure and accompanying files
- Data file: Low_glucose_C_release_data.csv
- Metadata file: Low_glucose_C_release_data_metadata.csv (quality control and reference data)
- Plot locations: Plot_locations.csv; description of fields in Plot_locations.csv provided in Plot_locations_metadata.rtf
- Column definitions (examples): 
  - Transect, Row (locations referencing Plot_locations.csv)
  - Depth (cm)
  - Time-series DPM columns: 0.5, 1, 2, 4, 6, 24, 48, 72, 96, 120, 144, 168, 192, 288, 336, 504, 672, 840, 1008 (hours)
  - Additional fields: Blank DPM counts for blanks; STD1_HMWC, STD2_HMWC+N, STD3_HMWC+N+P, STD4_HMWC+P (quality control standards)
- Application data details:
  - Each treatment’s number of samples, soil weight per sample (5 g), carbon addition (0.006 mM), and specific N and P additions per treatment
  - Treatment labels: Control, N, P, N&P
- Data completeness: Empty cells indicate no data

## Data quality, governance, and access
- Metadata provided to document data structure, QC references, and field meanings.
- Data are intended to be quality-assured, cleaned, transformed, and clearly presented (e.g., in reports or dashboards) with appropriate data governance.
- Underlying data sharing and openness are considered as part of governance, with metadata detailing usage and data provenance.