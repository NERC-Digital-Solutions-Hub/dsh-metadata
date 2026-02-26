# Experimental design/collection method: Life history data

## Overview
- Study of life history, reproductive output, and wing morphology across four laboratory populations from two Belgian landscape types (woodland and agricultural).
- Populations: Lauzelle, St. Hubert (woodland); Lillois, Hoegaarden (agricultural).
- Larvae reared on Potentilla trivialis under control or drought-stressed conditions in climate room; random allocation with equal representation from each source population.

## Experimental design and sampling
- Newly hatched larvae randomly selected and assigned (three per plant) to treatments; total of 178 control and 390 drought-stressed larvae.
- Each population contributed equally to both treatment groups.
- Monitored from hatching to adult eclosion; eclosion date recorded; development time computed.
- F1 adults weighed and sexed at eclosion.

## Data collected and measurements

- Life history data
  - Population, Landscape, Treatment, ID, Adult_mass, Total_development_time, Square_root_Total_devtime, sex
  - Development time from egg hatching to adult eclosion; mass at eclosion; sex
- Female reproductive output
  - Population, Landscape, Treatment, ID, Adult_mass
  - Mean_egg_size, Longevity, Days_until_first_egg, Fecundity (total eggs laid), Arcsine square root of % eggs hatched, % eggs hatched
- Wing data
  - Population, Landscape, Treatment, ID, Adult_mass
  - Total_development_time, Wing_loading, Mean_forewing_Melanin, Mean_FW_aspect_ratio, Total_Wing_area

## Data format and storage
- Stored as CSV spreadsheets:
  - Life_history_data.csv
  - Female_reproductive_output_data.csv
  - Wing_data.csv
- Headers described for each file; examples include:
  - Life_history_data.csv: Description, Population, Landscape, Treatment, ID, Adult_mass, Total_development_time, Square_root_Total_devtime, sex
  - Female_reproductive_output_data.csv: Population, Description, Landscape, Description, ID, Adult_mass, Mean_egg_size, Longevity, Number_days_until_1st_egg_la id, Fecundity, Arcsine square root_% Eggs hatched, %Eggs hatched
  - Wing_data.csv: Population, Description, Landscape, Description, ID, Adult_mass, Total_development_time, sex, Wing_loading, Mean_forewing_Melanin, Mean_FW_aspect_ratio, Total_Wing_area
- Missing data indicated by empty cells (e.g., due to death).

## Metadata and header details
- Key fields link population origin to landscape and treatment, enabling cross-study analyses.
- Derived fields included: Square_root_Total_devtime (for normalization) and Arcsine square root transformed hatch rate.

## Data quality and handling
- Mortality and missing observations are recorded as empty cells.
- Data are distributed across three interrelated files; integration requires cross-referencing by ID and Population.

## Potential uses and applications
- Assess effects of drought stress and landscape origin on development time, survival, adult mass, fecundity, hatch success, and wing morphology.
- Multi-trait analyses linking life-history with reproductive output and morphology.
- Cross-file analyses to explore relationships among growth, reproduction, and wing traits.

## Practical considerations for data leaders
- This dataset exemplifies modular data storage (separate files by trait) with explicit header metadata for discoverability and reuse.
- Highlights need for clear cross-file linking (via Population and ID) to enable holistic analyses.
- Demonstrates explicit handling of missing data and data transformations (e.g., square root, arcsine) to support statistical analyses.