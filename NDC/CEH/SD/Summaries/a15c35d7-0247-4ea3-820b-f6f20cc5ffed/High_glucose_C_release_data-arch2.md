# Time series of microbial carbon release from soil as carbon dioxide under different nitrogen and phosphorus treatments with a high glucose concentration added as a carbon source in the Conwy catchment, North Wales, UK (2015)

## Overview
- Describes time-series measurements of soil microbial respiration (14CO2 release) under varying nitrogen and phosphorus treatments with high glucose as the carbon source.
- Location and context: Conwy catchment, North Wales, UK; study year 2015.
- Purpose aligned with environmental monitoring: standardised data collection to assess environmental health and carbon mineralization responses to nutrient amendments.
- Data outputs include DPM counts, 14CO2 capture, and accompanying metadata and quality-control resources.

## Data and treatments
- Substrate and carbon source: high concentration glucose (C addition = 300 mM).
- Treatments (N and P additions): Control (no N/P), N addition, P addition, N and P addition.
- Replication: 42 samples per treatment.
- Soil mass: 5 g dry weight per sample.
- Variable additions (from application data): N addition = 33.3 (units not specified), P addition = 3.53 (units not specified); C addition constant at 300 mM.
- Abbreviations: HWMC = high molecular weight carbon; N = nitrogen; P = phosphorus.
- Plot and borehole context: locations described in Plot_locations.csv with corresponding borehole data in Plot_locations_metadata.rtf.

## Experimental design and soil sampling
- Depth intervals: 0-15 cm, 15-30 cm, 50-100 cm, 100-150 cm, 150-200 cm, 250-300 cm; grouped as topsoil (0-30 cm), midsoil (50-100 cm), and subsoil (100-300 cm).
- Sample processing: soils sieved to 5 mm to remove stones and plant material, ensuring sample homogeneity and minimal microbial community disturbance.

## Carbon mineralization method
- 14C-substrate mineralization assessed by trapping evolved 14CO2.
- Procedure: 5 g soil placed in 50 mL tubes; 50 µL of 14C-glucose labelled nutrient solution added; NaOH trap (1 M) placed to capture 14CO2; tubes sealed and incubated at 10°C.
- Trap handling: NaOH traps replaced at specific time points and later combined with scintillation fluid for counting.
- Measurement: 14CO2 quantified using a liquid scintillation counter (Wallac 1404).

## Data structure and metadata
- Primary data columns include Transect and Row (referencing Plot_locations.csv), Depth (cm), and time-interval DPM counts (e.g., 0.5, 1, 2, 4, 6, 24, 48, 72, 96, 120, 144, 168, 192, 288, 336, 504, 672, 840, 1008 hours).
- Blank and standard/reference data included (e.g., BLANK, STD1_HMWC, STD2_HMWC+ N, STD3_HMWC + N + P, STD4_HMWC + P) for quality control.
- Data structure notes: Empty cells indicate missing data.
- Metadata resources: High_glucose_C_release_data_metadata.csv provides column names and descriptions; additional quality-control and reference data are available in related documents.

## Quality control and data quality resources
- Quality control and reference datasets accompany the application data to support verification and standardization of measurements.
- Metadata documentation aligns column definitions with data structure to facilitate reproducibility and data integration.

## Data access, storage, and reuse
- Data are organized in CSV format with explicit metadata and plot-location references.
- Plot_locations.csv and Plot_locations_metadata.rtf provide spatial context for transects, rows, and boreholes.
- Designed to be stored in appropriate data portals and made accessible to others, supporting broader data reuse and integration for environmental monitoring and policy evaluation.

## Relevance for environmental monitoring and the analyst role
- Provides a standardized, time-resolved dataset to evaluate soil carbon mineralization under nutrient amendments, enabling tracking of environmental health indicators over time.
- Includes detailed methods, sampling design, and quality-control resources to support data verification, comparability across studies, and integration with other environmental datasets.
- Supports generation of outputs such as charts and maps for policy performance assessment and environmental health monitoring, while ensuring underlying data remain accessible to researchers and practitioners.