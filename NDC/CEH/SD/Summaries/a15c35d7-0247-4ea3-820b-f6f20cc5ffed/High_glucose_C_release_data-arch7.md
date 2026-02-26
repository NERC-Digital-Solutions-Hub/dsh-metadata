# Time series of microbial carbon release from soil as carbon dioxide under different nitrogen and phosphorus treatments with a high glucose concentration added as a carbon source in the Conwy catchment, North Wales, UK (2015)

## Overview
- Study measuring 14C-labeled glucose mineralization to CO2 in soils from boreholes in the Conwy catchment, North Wales.
- Four nutrient treatments combined with high glucose addition: Control, N, P, and N&P.
- Time-series data collected over up to 1008 hours (~6 weeks) at multiple depths to assess microbial carbon release dynamics.
- Spatial context provided via Plot_locations.csv (borehole/transect locations); description file Plot_locations_metadata.rtf.
- Data intended for GIS-based visualization and analysis of spatial patterns in soil carbon mineralization across depths and treatments.

## Dataset contents and structure
- High_glucose_C_release_data.csv: time-series DPM (disintegrations per minute) measurements for each sample, across multiple time points.
- High_glucose_C_release_data_metadata.csv: metadata describing each column, including abbreviations (e.g., HWMC) and data definitions.
- Plot_locations.csv: borehole/plot locations referenced by Transect and Row identifiers.
- Plot_locations_metadata.rtf: description of Plot_locations.csv fields.
- Quality control and reference data: included in High_glucose_C_release_data_metadata.csv.

## Sampling context and soil preparation
- Soil cores collected and stored with depth intervals:
  - 0-15 cm, 15-30 cm, 50-100 cm, 100-150 cm, 150-200 cm, 250-300 cm.
  - Grouped for analysis as topsoil (0-30 cm), midsoil (50-100 cm), subsoil (100-300 cm).
- Samples processed by sieving to 5 mm to ensure homogeneity and minimize microbial community shifts.
- For each sample, 5 g of dry soil used in sterile tubes.

## Carbon mineralization assay (14C-glucose)
- 5 g soil incubated with 50 µl of 14C-glucose labeled nutrient solution on soil surface.
- NaOH trap (1 M) added to capture evolved 14CO2; traps changed at multiple time points and then weekly to 6 weeks.
- Incubations conducted at 10°C to reflect mean annual catchment temperature.
- 14CO2 quantified by mixing NaOH trap with scintillation fluid and counting with a Wallac 1404 counter.

## Treatments and data scope
- Application data per treatment at high glucose concentration (300 mM glucose):
  - Control: N=0, P=0
  - N: N=33.3, P=0
  - P: N=0, P=3.53
  - N&P: N=33.3, P=3.53
- Number of samples: 42 per treatment (total dataset includes multiple transects/ depths per treatment).
- Measurements: DPM counts at time intervals in hours:
  0.5, 1, 2, 4, 6, 24, 48, 72, 96, 120, 144, 168, 192, 288, 336, 504, 672, 840, 1008 hours.
- Empty cells indicate missing data.

## Data fields and GIS-ready structure
- Sample identifiers:
  - Transect: referencing the cage location in Plot_locations.csv
  - Row: sub-location within the cage
  - Depth: sampling depth in cm
- Time-series measurements:
  - Columns labeled with hours (e.g., 0.5, 1, 2, 4, ..., 1008)
  - Each cell contains DPM counts (or missing if data not collected)
- Depth grouping:
  - Topsoil (0-30 cm)
  - Midsoil (50-100 cm)
  - Subsoil (100-300 cm)
- Abbreviations:
  - HWMC: high molecular weight carbon
  - N: nitrogen
  - P: phosphorus

## How this helps GIS specialists
- Spatial visualization:
  - Map borehole locations (Plot_locations.csv) and link to depth-resolved mineralization time-series.
  - Create layers for each treatment and depth band to compare spatial patterns.
- Temporal analysis:
  - Visualize DPM counts over time for each sample, treatment, and depth; support trend analysis and rate calculations.
- Data integration:
  - Join plot locations with metadata to enrich GIS attributes (treatment, C addition, N/P additions) and quality flags.
- Data preparation:
  - Use the provided metadata to interpret column meanings, units (DPM counts), and sampling design (depth, transect, row).

## Quality, metadata, and caveats
- Metadata and column descriptions are provided in separate CSV file (High_glucose_C_release_data_metadata.csv).
- Quality control and reference data are documented within the same metadata file.
- Data gaps exist (empty cells) where measurements are unavailable.
- Spatial accuracy relies on Plot_locations.csv reference; consult Plot_locations_metadata.rtf for field definitions.

## Files to consult
- High_glucose_C_release_data.csv
- High_glucose_C_release_data_metadata.csv
- Plot_locations.csv
- Plot_locations_metadata.rtf
- Miscellaneous supporting documents (as referenced in metadata)