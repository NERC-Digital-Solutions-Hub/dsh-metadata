# Flood risk assessment of the Luanhe river basin under different development strategies and climate scenarios

- Overview
  - Assess flood risk in the Luanhe river basin under multiple development strategies and climate scenarios up to 2030.
  - Uses a high-performance hydrodynamic model (HiPIMS) to generate inundation predictions and overlay with population data to produce local flood risk maps.
  - Data sources are primarily open datasets (NASA NEX-GDDP for climate uplifts, GPWv4 for population) and remote sensing observations for model validation.
  - The Luanhe basin is a key socio-economic area in Northeast China influencing the Beijing-Tianjin-Hebei region.

- Data inputs and generation
  - Climate uplifts to 2030: dimensionless numbers describing climate impact for the future 100-year design rainfall, derived from NASA Earth Exchange Global Daily Downscaled Projections (NEX-GDDP).
  - Historical validation: 2012 flood event validated using HiPIMS with remote sensing data.
  - Inundation predictions to 2030: HiPIMS outputs under varying development strategies and climate scenarios.
  - Population and exposure: Gridded Population of the World, Version 4 (GPWv4) overlaid with inundation results to compute local resident flood risk.

- Model and validation
  - HiPIMS used for flood risk assessment; validated against 2012 event with remote sensing observations.
  - Model and data are documented and prepared for peer-reviewed publication; HiPIMS performance supported by prior studies.

- Scenarios and development strategies
  - Scenarios combine land use data (2015 baseline) with 100-year design rainfall and climate pathways.
  - Climate pathways: RCP4.5 and RCP8.5.
  - Development strategies: Trend, Expansion, Sustainability, and Conservation.
  - Reservoir references: P denotes Panjiakou Reservoir (including Daheiting); S denotes Shuangfengsi Reservoir.
  - Results include scenario-specific inundation maps and, where applicable, P/S partitions (e.g., Trend_RCP4.5_P, Expansion_RCP8.5_S).

- Data formats and structure
  - Climate uplifts: CSV (first column: city; second column: uplift value).
  - Inundation maps and validation: TIFF files (units for inundation: meters; remote sensing validation data units: dimensionless or as provided).
  - Population data: resampled GPWv4 (units: persons/km^2).
  - Data are organized into two tabs (Tab 1 and Tab 2) and described in Dataset sections.

- Datasets and documentation
  - Flood model validation: Validation.tif; RemoteSensing_validation.tif; contributed by Loughborough University; Open Government Licence.
  - Climate change uplifts: rcp45.csv, rcp85.csv; first column city, second uplift; contributed by Loughborough University; Open Government Licence.
  - Inundation map: flood simulation results for different climate and infrastructure scenarios; Open Government Licence.
  - Population data: resampled GPWv4; Open Government Licence.
  - Flood scenarios and land use combinations (including P and S reservoir considerations) are documented in Tab. 2 and associated descriptions.

- Quality control and provenance
  - HiPIMS has been used in multiple flood risk projects and cited in related literature.
  - The dataset is well documented, peer-reviewed, and shown to provide robust estimates.
  - NEX-GDDP and GPWv4 are widely used open datasets, supporting transparency and reproducibility.

- Outputs and intended GIS use
  - Produces flood risk maps by overlaying inundation outputs with population density to assess resident exposure.
  - Facilitates visualization and exploration of spatial flood risk under various development and climate scenarios for policymakers, planners, and the public.
  - Open data licensing supports reuse and integration into GIS workflows.