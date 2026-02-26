# Time series of microbial carbon release from soil as carbon dioxide under different nitrogen and phosphorus treatments with a high glucose concentration added as a carbon source in the Conwy catchment, North Wales, UK (2015)

## Scope and aim
- Time-series dataset measuring microbial carbon mineralization as CO2 (14C-labeled glucose) under four nutrient treatments (Control, N, P, N&P) with a high glucose carbon source.
- Study conducted in the Conwy catchment, North Wales, UK, 2015.
- Data intended to support discovery and reuse by others, with attention to data governance, metadata, and usability.

## Data described
- Application data: 4 treatments with 42 samples each (total 168 samples), all using high concentration glucose (300 mM C addition). Soil sample weight 5 g (dry weight). Treatments:
  - Control: N = 0, P = 0
  - N: N = 33.3, P = 0
  - P: N = 0, P = 3.53
  - N&P: N = 33.3, P = 3.53
- Measured variable: 14CO2 evolved captured in NaOH traps and quantified by liquid scintillation counting.
- Incubation: 10°C to reflect mean annual catchment temperature.
- Depth and location:
  - Depths: 0–15 cm, 15–30 cm (grouped as topsoil 0–30 cm), 50–100 cm (midsoil), 100–300 cm (subsoil).
  - Transects and rows reference Plot_locations.csv (locations within plots).
- Timepoints: DPM counts at multiple hours, including 0.5, 1, 2, 4, 6, 24, 48, 72, 96, 120, 144, 168, 192, 288, 336, 504, 672, 840, and 1008 hours. Empty cells indicate no data.

## Metadata and data structure
- Metadata files:
  - High_glucose_C_release_data_metadata.csv: column names and descriptions for data columns.
  - Abbreviations used: clarifies terms (e.g., HWMC = high molecular weight carbon; N = nitrogen; P = phosphorus).
  - Miscellaneous supporting documents note quality control and reference data.
- Data structure fields:
  - Core fields: Transect, Row, Depth.
  - Time-series fields: DPM counts labelled by time intervals (e.g., 0.5, 1, 2, 4, 6, 24, 48, …, 1008 hours).
  - Blank controls: BLANK DPM counts included as part of QC.
- Plot and location references:
  - Plot_locations.csv for borehole/location coordinates.
  - Plot_locations_metadata.rtf describing Plot_locations.csv contents.

## Methods and data collection
- Soil sampling and preparation:
  - Soils were divided into depth intervals (topsoil 0–30 cm, midsoil 50–100 cm, subsoil 100–300 cm) and sieved to 5 mm to remove stones and plant material and improve homogeneity.
- Mineralization assay:
  - 5 g soil (adjusted for moisture) placed in sterile tubes.
  - 50 µL of 14C-glucose labelled solution added to soil surface.
  - NaOH trap (1 M) placed to capture evolved 14CO2; tubes sealed and incubated at 10°C.
  - NaOH traps replaced at fixed intervals up through 1008 hours, then weekly for up to 6 weeks.
  - Captured 14CO2 quantified by mixing trap with scintillation fluid and counting on a liquid scintillation counter.
- Quality control:
  - Include blanks and standards (as indicated in metadata: STD1_HMWC, STD2_HMWC+N, STD3_HMWC+N+P, STD4_HMWC+P).
  - QC and reference data described in metadata file to accompany raw data.

## Data governance, quality, and usability
- Data are prepared for reuse with explicit metadata, data dictionaries, and measurement protocols.
- Units and measurements explicitly defined (DPM for 14CO2, hours for timepoints, cm for depths, mM for C addition).
- Documentation links plot locations, depth-based grouping, and experimental design to support traceability and provenance.
- Potential data stewardship considerations:
  - Ensure consistent mapping between Plot_locations.csv and Plot_locations_metadata.rtf.
  - Maintain alignment between application data (treatment definitions, sample counts, C/N/P additions) and metadata.
  - Monitor for any missing timepoints or depth records and clearly annotate gaps.
  - Confirm licensing, access rights, and versioning for updates or additions to the dataset.

## Access, storage, and sharing considerations
- Data are organized across multiple files:
  - High_glucose_C_release_data.csv (primary measurements)
  - High_glucose_C_release_data_metadata.csv (variable definitions)
  - Plot_locations.csv and Plot_locations_metadata.rtf (spatial context)
  - Abbreviations used (glossary for clarity)
  - Quality control/reference data (within the metadata context)
- Ensure stable storage with version control and clear citation guidance for reuse.

## Provenance and reuse considerations
- Provenance traceable from soil sampling through lab measurements to time-series DPM data.
- Reuse opportunities include comparing carbon mineralization rates across depths and nutrient additions, benchmarking microbial activity under high-carbon conditions, and informing soil carbon models.
- Users should reference the metadata to interpret each column accurately and to understand the experimental context (glucose concentration, incubation conditions, and treatment specifics).

## Known limitations and considerations for users
- Some data columns are timepoint-specific and may contain blanks where data were not collected.
- Depth grouping (topsoil, midsoil, subsoil) relies on defined intervals; users should respect grouping when aggregating results.
- A comprehensive understanding requires consulting the associated metadata (High_glucose_C_release_data_metadata.csv) and plot-location documentation (Plot_locations.csv and Plot_locations_metadata.rtf) to ensure proper spatial or transect-level analyses.