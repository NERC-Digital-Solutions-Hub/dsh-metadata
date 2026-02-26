# The energy and mass balance of Peruvian glaciers

## Overview
- Data and modeling outputs linked to the Peru GROWS and PEGASUS projects, funded by NERC and CONCYTEC.
- Focus on understanding glacier energy and mass balance in Peru, informing glacierized region hydrology and climate impact assessments.
- WRF model runs (bias-corrected) used to generate long-term climate forcing data for two major glacierized catchments: Rio Santa (Cordillera Blanca) and Vilcanota-Urubamba.
- Five on-glacier weather stations used for bias correction; outputs presented as averaged and monthly datasets suitable for analysis and visualization.

## Data generation and quality control
- Modeling setup:
  - WRF version 3.8.1 used to simulate 1980–2018 with a three-domain structure: outer domain at 12 km, two inner domains at 4 km.
  - Domains cover Peru and the two study catchments: Rio Santa Basin and Vilcanota-Urubamba catchment.
  - Physics schemes include Morrison double moment microphysics, CAM radiation, Noah-MP land surface, and other standard WRF options.
  - Lateral boundary forcing from ERA5 every 6 hours; 1-year spin-up per year; one-way nesting; spectral nudging above model level 15.
- Data initialization and forcing:
  - ERA5 used for boundary conditions; topography from SRTM; glacier and land data aligned with Randolph Glacier Inventory.
- Bias correction and downscaling:
  - Precipitation bias-corrected first for the number of wet days, then magnitudes adjusted with a constant multiplicative factor.
  - Temperature corrected for elevation differences between model and station using a gradient derived from model output; daily min/max temperatures corrected with additive adjustments (constant for max, latitude/longitude/height dependent for min).
  - Station-derived corrections applied to adjust model outputs to observed conditions before interpolation to grid points.
- Data processing:
  - Model outputs averaged by catchment or over time; outputs include daily maximum/minimum temperatures and total precipitation, plus glacier-focused statistics.
  - Five on-glacier weather stations used for bias correction: Artesonraju (AG), Cuchillacocha (CG), Shallap (SG), Quelccaya Ice Cap (QIC), Quisoquipina (QQG). Station details (location, elevation) are provided.

## Data structure and contents
- Two study basins with equivalent data structures:
  - Rio Santa Basin (RS) and Vilcanota-Urubamba (VUV).
- File types and contents (examples):
  - average_annual_total_precip_RS.nc, average_annual_total_precip_VUV.nc – average total precipitation per year per grid point (mm).
  - average_temperature_RS.nc, average_temperature_VUV.nc – average temperature at 2 m per grid point (°C).
  - monthly_average_temperature_at_glacier_RS.csv, monthly_average_temperature_at_glacier_VUV.csv – annual cycles of temperature over glacierized regions (°C).
  - monthly_total_precipitation_at_glacier_RS.csv, monthly_total_precipitation_at_glacier_VUV.csv – annual cycles of precipitation over glacierized regions (mm).
  - seasonal_precipitation_RS.nc, seasonal_precipitation_VUV.nc – seasonal average total precipitation (mm) within basin boundaries.
  - WRF_elevation_RS.nc, WRF_elevation_VUV.nc – model elevation data for the two basins (m a.s.l.).
  - Glacier-specific daily temperature and precipitation files for Artesonraju, Cuchillacocha, Quelccaya, Quisoquipina, and Shallap glaciers (maximum/minimum daily temperatures, daily precipitation) (°C, mm).
- Units and structure:
  - NetCDF and CSV formats; clear units (mm, °C, m a.s.l.) and basin-specific datasets.
  - Datasets cover 1980–2018 with daily resolution for certain variables and monthly cycles for others.

## Data usage and applicability
- Provides long-term, bias-corrected climate forcing and glacier-relevant statistics to support energy and mass balance analyses in Peruvian glaciers.
- Data can underpin monitoring frameworks by offering:
  - Consistent, quality-checked baselines for climate impacts on glacier hydrology.
  - Transparently documented bias correction steps and data provenance.
  - Spatially-resolved (grid-point) and regionally aggregated metrics suitable for dashboards and reports.
- Emphasis on transparency and reproducibility through detailed methodology (model setup, bias correction, data processing) and access to the derived datasets.

## Governance, metadata, and data sharing considerations
- The dataset includes extensive metadata on model configuration, forcing data sources (ERA5), and correction procedures to enable verification and reuse.
- Public sharing of underlying data is discussed in the context of data governance challenges (e.g., openness, data management standards) and is addressed by providing clearly described outputs and data structures.
- Data provenance is maintained via explicit naming conventions, documented processing steps, and references to foundational datasets and model components (ERA5, CAM3.0, SRTM, Randolph Glacier Inventory, etc.).

## References and methodological context
- Core modeling and data sources:
  - ERA5 global reanalysis (Hersbach et al., 2020)
  - CAM 3.0 description (Collins et al., 2004)
  - SRTM topography (Jarvis et al., 2008)
  - Noah-MP land surface model (Niu et al., 2011)
  - WRF model description and configurations (Skamarock et al., 2008; Jiménez et al., 2012; Ma & Tan, 2009; Morrison et al., 2005; Nakanishi & Niino, 2004)
  - Randolph Glacier Inventory (Pfeffer et al., 2014)

## Practical takeaways for monitoring framework authors
- Implement end-to-end data pipelines that couple high-resolution climate modeling with bias correction anchored to local observations.
- Ensure comprehensive metadata and clear documentation of processing steps to support data governance and transparency.
- Provide both gridded and glacier-region aggregated outputs to support multiple decision-making scales.
- Anticipate data access and sharing barriers by delivering well-structured, openly described datasets that enable reproducibility and reuse in policy monitoring contexts.