# Time series of microbial carbon release from soil as carbon dioxide under different nitrogen and phosphorus treatments with a low glucose concentration added as a carbon source in the Conwy catchment, North Wales, UK (2015)

## Overview
- Presents time-series measurements of microbial carbon mineralization from soil as CO2, using 14C-labeled glucose as a carbon source.
- Experimental context: Conwy catchment, North Wales, UK, 2015.
- Examines effects of varying nitrogen (N) and phosphorus (P) amendments on cumulative 14CO2 evolution across multiple soil depths.
- Data are organized with accompanying metadata and location information to support data discovery and reuse.

## Treatments and sampling design
- Treatments (low concentration glucose with nutrient amendments):
  - Control (glucose only)
  - Nitrogen addition (N)
  - Phosphorus addition (P)
  - Nitrogen and Phosphorus addition (N&P)
- Glucose addition: 0.006 mM
- Dry soil per assay: 5 g (fresh weight adjusted to dry weight)
- Number of samples per treatment: 42
- Total sampling framework integrates soil depth, transects, and rows.

## Soil sampling and depth stratification
- Soil cores divided into depth intervals:
  - 0–15 cm, 15–30 cm, 50–100 cm, 100–150 cm, 150–200 cm, and 250–300 cm
- Depths grouped for analysis:
  - Topsoil: 0–30 cm
  - Midsoil: 50–100 cm
  - Subsoil: 100–300 cm
- Sample homogenization achieved by passing through a 5 mm sieve to remove stones and plant material.

## Mineralization measurement protocol
- 14C-glucose labeled nutrient solution (50 µL) added to the soil surface.
- NaOH trap (1 M) placed in each tube to capture evolved 14CO2.
- Incubation temperature: 10°C (representing mean annual catchment temperature).
- NaOH traps were replaced at multiple time points and then weekly for up to 6 weeks after labeling.
- 14CO2 captured in the NaOH trap quantified by mixing with liquid scintillation fluid and counting with a scintillation counter.

## Data files and metadata
- Primary data file: Low_glucose_C_release_data.csv
- Metadata files:
  - Low_glucose_C_release_data_metadata.csv (column names and descriptions)
  - Plot_locations.csv (borehole locations)
  - Plot_locations_metadata.rtf (description of fields in Plot_locations.csv)
  - Quality control and reference data described in Low_glucose_C_release_data_metadata.csv
- Abbreviations:
  - HWMC: high molecular weight carbon
  - N: nitrogen
  - P: phosphorus

## Data structure and time series details
- Key columns in data:
  - Transect: transect number (refers to cage location in Plot_locations.csv)
  - Row: row number (refers to cage location in Plot_locations.csv)
  - Depth: soil depth sampled (cm)
  - Time-series DPM counts for each time interval:
    - 0.5, 1, 2, 4, 6, 24, 48, 72, 96, 120, 144, 168, 192, 288, 336, 504, 672, 840, 1008 hours
- DPM counts correspond to 14C-CO2 captured in the NaOH traps at each specified time interval.
- Empty cells indicate no data for that sample/time point.

## Spatial and measurement context
- Borehole locations detailed in Plot_locations.csv; description of fields available in Plot_locations_metadata.rtf.
- Depth categories allow comparisons across topsoil, midsoil, and subsoil responses to nutrient amendments.

## Data quality, caveats, and use
- Metadata provides descriptions of columns and QC/reference considerations.
- The dataset enables analyses of how N and P amendments influence microbial carbon mineralization across depth and time, under a controlled low-glucose carbon source.
- Limitations to consider:
  - Incubation conditions (10°C) and low glucose regime may not reflect all in-situ field conditions.
  - Data represent 14C-labeled substrate mineralization under specified treatment combinations and sampling schedule.
- Suitable analytical approaches include time-series analyses, mixed-effects models across depth and transects, and cross-treatment comparisons of mineralization rates.

## Potential analyses and applications
- Assess treatment effects (N, P, N&P) on cumulative 14CO2 evolution over time.
- Compare mineralization dynamics across soil depths (topsoil vs. midsoil vs. subsoil).
- Explore correlations between depth, time, and mineralization rate under different nutrient amendments.
- Integrate with Plot_locations metadata to relate microbial responses to spatial context within the Conwy catchment.