# Time series of microbial carbon release from soil as carbon dioxide under different nitrogen and phosphorus treatments with a high glucose concentration added as a carbon source in the Conwy catchment, North Wales, UK (2015)

- Provides a detailed data record of soil carbon mineralization (14CO2 evolution) under controlled nutrient amendments with added glucose, in the Conwy catchment, North Wales.
- Designed as a time-series monitoring dataset to evaluate how nitrogen and phosphorus additions influence microbial carbon release from soil carbon pools.

## Overview of the dataset and study design

- Treatments and replication:
  - Four treatment conditions: Control (no added N or P with high glucose), N addition, P addition, and N&P addition.
  - Each treatment has 42 samples, enabling robust comparisons across treatments.
- Substrate and conditions:
  - High concentration glucose (C addition = 300 mM) used as a carbon source.
  - No nitrogen or phosphorus addition in control; nutrient additions varied per treatment as specified.
  - Incubation performed at 10°C to reflect mean annual catchment temperature.
- Soil sampling and preparation:
  - Soil cores sieved to 5 mm to remove stones and plant material, ensuring homogeneity.
  - Depths profiled and grouped into: topsoil (0–30 cm), midsoil (50–100 cm), subsoil (100–300 cm); samples taken from multiple transects/rows.
- CO2 capture and measurement:
  - 5 g dry-weight soil aliquots incubated with 14C-glucose; CO2 captured in NaOH traps (1 M) at multiple time points.
  - NaOH traps collected and analyzed with a liquid scintillation counter to quantify 14CO2 evolution.
  - Time points span from 0.5 hours to 1008 hours (weekly beyond initial 6 weeks), with trap changes at 0.5, 1, 2, 4, 6, 24, 48, 72, 96, 120, 144, 168, 192, 336, 504, 672, 840, and 1008 hours.
- Data collection timing and replication:
  - Data recorded as disintegrations per minute (DPM) per time interval for each soil depth and transect/row.

## Data and metadata organization

- Core data files:
  - High_glucose_C_release_data.csv: Time-series DPM measurements for each sample and time interval.
  - High_glucose_C_release_data_metadata.csv: Column names and descriptions, including sample metadata and measurement details.
- Supporting metadata and reference data:
  - Plot_locations.csv and Plot_locations_metadata.rtf: Geographic and spatial context for transects/plots.
  - Miscellaneous QC data and references stored to support data quality and traceability.
- Data structure details:
  - Columns include: Transect, Row, Depth, and a series of time-point columns labeled by hour intervals (e.g., 0.5, 1, 2, 4, 6, 24, 48, 72, 96, 120, 144, 168, 192, 288, 336, 504, 672, 840, 1008).
  - Empty cells indicate missing data.
- Data governance and quality:
  - Metadata files provide context for measurements and raw data quality checks.
  - The dataset emphasizes provenance (sampling depth, location, treatment, and time-stamped DPM counts) to support reproducibility and secondary use.

## Methods and measurement details

- Soil collection and processing:
  - Depth intervals: 0–15, 15–30, 50–100, 100–150, 150–200, 250–300 cm; grouped as topsoil, midsoil, and subsoil.
  - Soils passed through a 5 mm sieve to ensure homogeneity and minimal disturbance to microbial communities.
- Laboratory protocol:
  - 5 g soil samples placed in sterile tubes; 14C-glucose solution applied to soil surface.
  - NaOH (1 M) trap added to capture evolved 14CO2 immediately after nutrient addition.
  - Tubes sealed and incubated at 10°C; NaOH traps replaced at specified intervals and later analyzed via scintillation counting.
- Data mapping:
  - DPM counts are reported for each time interval, linked to transect, row, and depth locations to enable spatial-temporal analysis of mineralization responses.

## Relevance for monitoring frameworks

- Demonstrates an end-to-end approach to environmental health monitoring:
  - Clear linkage between nutrient management (N and P amendments) and microbial carbon mineralization under a defined carbon substrate.
  - Comprehensive time-series measurement framework capturing short- and long-term responses.
  - Emphasis on metadata quality, data provenance, and open reporting of measurement methods and data structures.
- Supports policy evaluation and decision-making by providing:
  - Quantitative measures of soil carbon turnover under different nutrient regimes.
  - Spatially resolved data across soil depths and transects enabling assessment of depth-dependent responses.
  - A replicable protocol that can be adapted for other catchments or monitoring programs.

## Practical considerations and potential challenges for monitoring teams

- Data accessibility and sharing:
  - Metadata and supporting files are essential for data reuse; ensure timely sharing of plots and location metadata alongside primary datasets.
- Metadata completeness:
  - The usefulness of time-series measurements depends on complete time-point documentation and clear column labeling.
- Data transformation and interpretation:
  - DPM counts must be consistently translated into CO2 release metrics; documentation of any calibration, background corrections, or blank adjustments is critical.
- Governance and data quality:
  - Establish data governance to maintain dataset integrity, update metadata as needed, and ensure long-term availability.

## Key takeaways for policy and implementation

- Time-series, depth-resolved soil carbon data under controlled nutrient treatments provide actionable insights into soil health and carbon cycling under nutrient management strategies.
- Robust metadata, transparent data structure, and reproducible laboratory methods are central to making such datasets usable for monitoring frameworks.
- The combination of replicated treatments, spatially explicit sampling, and multi-timepoint measurements supports nuanced assessments of how management actions influence environmental health outcomes over time.