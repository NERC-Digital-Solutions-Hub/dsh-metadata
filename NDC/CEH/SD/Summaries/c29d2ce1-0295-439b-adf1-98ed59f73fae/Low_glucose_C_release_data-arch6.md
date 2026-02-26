# Time series of microbial carbon release from soil as carbon dioxide under different nitrogen and phosphorus treatments with a low glucose concentration added as a carbon source in the Conwy catchment, North Wales, UK (2015)

## Overview
- Dataset documenting time-series of 14CO2 release from soil after adding 14C-glucose, under four nutrient treatments (Control, N, P, N&P) at low glucose concentration.
- Location: Conwy catchment, North Wales, UK; incubation at 10°C to reflect mean annual temperature.
- Measurements: disintegrations per minute (DPM) of 14CO2 captured in NaOH traps over many time points up to 1008 hours, with weekly follow-ups for up to 6 weeks.
- Data structure links to site and depth information via Plot_locations files; includes metadata and quality-control references.

## Experimental design and treatments
- Treatments (low glucose, carbon source): 
  - Control (0 N, 0 P)
  - N addition (33.33 N, 0 P)
  - P addition (0 N, 3.53 P)
  - N & P addition (33.33 N, 3.53 P)
- Replication: 42 samples per treatment condition.
- Substrate: low concentration glucose added at 0.006 mM.
- Soil mass: 5 g dry weight per tube.
- Depths: soil cores segmented into 0–15, 15–30, 50–100, 100–150, 150–200, 250–300 cm; analyzed collectively as topsoil (0–30 cm), midsoil (50–100 cm), and subsoil (100–300 cm).
- Transect/Row: references to Plot_locations.csv for location mapping.

## Soil sampling, preparation, and measurement
- Soil preparation: cores sieved to 5 mm to remove stones and plant material; aim to preserve microbial community.
- Mineralization assay: 5 g soil placed in 50 ml tubes; 50 µl of 14C-glucose labelled nutrient solution applied to soil surface.
- CO2 capture: 1 ml of 1 M NaOH trap added to each tube to capture evolved 14CO2.
- Incubation: tubes sealed and incubated at 10°C.
- Trap updates and counting: NaOH traps replaced at multiple time points (0.5, 1, 2, 4, 6, 24, 48, 72, 96, 120, 144, 168, 192, 336, 504, 672, 840, 1008 hours) and then weekly up to 6 weeks; 14CO2 quantified using a Wallac 1404 liquid scintillation counter with Optiphase HiSafe 3 scintillant.

## Data structure and key variables
- Core identifiers: Transect (location reference), Row (location reference).
- Depth: soil depth sampled (cm).
- Time-series measurements: DPM counts at designated hours:
  - 0.5, 1, 2, 4, 6, 24, 48, 72, 96, 120, 144, 168, 192, 288, 336, 504, 672, 840, 1008 hours.
- Data points may have blank entries to indicate missing data.
- Column naming notes:
  - 0.5 - DPM count after this time interval (hour)
  - - 1, - 2, - 4, - 6, - 24, etc., correspond to subsequent time intervals
- Abbreviations and context:
  - HWMC = high molecular weight carbon
  - N = nitrogen
  - P = phosphorus

## Metadata, quality control, and supporting documents
- Metadata file: Low_glucose_C_release_data_metadata.csv contains column names and descriptions for application data.
- Quality control and reference data reside in the same metadata file.
- Supporting files:
  - Plot_locations.csv (borehole locations)
  - Plot_locations_metadata.rtf (description of Plot_locations.csv fields)
  - Miscellaneous supporting documents (context and additional materials)

## Related data files and access
- Primary application data: Low_glucose_C_release_data.csv
- Metadata: Low_glucose_C_release_data_metadata.csv
- Location mapping: Plot_locations.csv
- Location documentation: Plot_locations_metadata.rtf
- Additional supporting documents and references in the miscellaneous folder

## Usage notes for data support and re-use
- Suitable for self-service analyses and dashboards; ensure correct interpretation of timepoint columns and unit (DPM).
- Data originate from a single 10°C incubation study in the Conwy catchment, with explicit treatment combos and depth stratification.
- Cross-reference Plot_locations.csv and metadata to align sample identifiers with spatial and depth context.
- Empty cells denote missing data; treat accordingly in analyses.