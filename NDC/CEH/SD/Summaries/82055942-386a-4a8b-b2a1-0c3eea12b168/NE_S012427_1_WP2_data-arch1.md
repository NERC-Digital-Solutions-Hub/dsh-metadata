# Flood risk assessment of the Luanhe river basin under different development strategies and climate scenarios

## Overview
- Describes data needed for and results produced by a flood risk assessment framework applied to the Luanhe river basin under changing climate and development strategies.
- Location: Luanhe river basin in northeast North China Plain; significance for socio-economic development of the Beijing-Tianjin-Hebei region.
- Purpose: enable near-future flood risk assessment (to 2030) under multiple development and climate scenarios.

## Data included
- Uplifts of future climate scenarios to 2030 (dimensionless numbers describing climate impact for the 100-year design rainfall).
- Validation results for a historical flood event in 2012 (HiPIMS model; remote sensing data and inundation outputs).
- Flood inundation predictions to 2030 under different development strategies and climate scenarios (HiPIMS outputs; units in meters).
- Spatial resident density map for Luanhe basin to 2030 (GPWv4; units in persons per square kilometer).

## Data generation and inputs
- Climate uplifts generated from NASA Earth Exchange Global Daily Downscaled Projections (NEX-GDDP) and applied to future design rainfall.
- 2012 flood event used to validate the flood model (HiPIMS); remote sensing data provide real-world observations.
- HiPIMS applied to produce inundation predictions across various development strategies and climate scenarios to 2030.
- Inundation results overlaid with GPWv4 population data to derive flood risk maps for local residents.

## Data structure and formats
- Climate uplifts: CSV files (rcp45.csv, rcp85.csv). First column: city; second column: uplift value.
- Other data: TIFF files (inundation maps, validation data, etc.).
- Documentation notes reference Tabular data (Tab 1 and Tab 2) detailing datasets, formats, and licensing.

## Datasets and development scenarios
- Land use (2015) combined with 100-year design rainfall under various conditions:
  - Baseline
  - RCP4.5 and RCP8.5 variants
  - Trend (2030) with RCP4.5 and RCP8.5 variants
  - Expansion (2030) with RCP4.5 and RCP8.5 variants
  - Sustainability (2030) with RCP4.5 and RCP8.5 variants
  - Conservation (2030) with RCP4.5 and RCP8.5 variants
- Reservoir considerations:
  - P = Panjiakou Reservoir (including Daheiting)
  - S = Shuangfengsi Reservoir
- Population and land-use changes are integrated to assess flood risk to residents under different future scenarios.

## Quality control and validation
- HiPIMS model has supported flood risk assessment in prior projects (Xia et al., 2019; Xing et al., 2019).
- The flood risk dataset is well documented, peer-reviewed (revised/resubmitted) and shown to provide robust estimates (Zhao et al., 2021).
- NEX-GDDP and GPWv4 are widely used open datasets (cited in the documentation).

## Licensing and availability
- Licensing: Open Government Licence for all datasets.
- Data are mainly open data or authored/openly produced datasets.

## References and data provenance
- Doxsey-Whitfield et al. 2015; Thrasher & Nemani 2015 (GPWv4 and NEX-GDDP)
- Xia et al. 2019; Xing et al. 2019 (HiPIMS and city-scale hydrodynamic modelling)
- Zhao et al. 2021 (large-scale flood risk assessment in Luanhe River Basin)