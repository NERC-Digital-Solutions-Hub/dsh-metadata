# Supporting documentation for EMEP4UK modelled daily atmospheric composition

- Purpose: Documentation of the EMEP4UK atmosphere model (ACTM) combined with WRF, presenting daily averaged outputs and the data structure used to simulate atmospheric composition and deposition of key pollutants.

## Model components and outputs

- Core model: EMEP4UK atmosphere chemistry transport model (ACTM) coupled with the Weather Research and Forecasting model (WRF); daily averaged data are included.
- Temporal resolution: Hourly to annual simulations; daily averages available in the dataset.
- Emissions included:
  - Anthropogenic and natural emissions for NOx, NH3, SO2, primary PM2.5, primary PM coarse, CO, and NMVOC.
  - UK emissions from the National Atmospheric Emission Inventory (NAEI) at 1 km × 1 km, aggregated to 5 km × 5 km.
  - rest of Europe emissions from EMEP CEIP at 50 km × 50 km.
  - International shipping emissions (ENTEC 2010i) aggregated to 5 km × 5 km in the British Isles domain.
  - Forest fires and biogenic emissions (isoprene and, when needed, monoterpenes) calculated by the model for each grid cell and time-step using near-surface temperature.
- Output focus: Surface concentrations of various pollutants (detailed below) and related atmospheric species.

## Species, units, and NetCDF variables

- Surface concentrations (NetCDF variables) include:
  - Nitric oxide (NO): µg/m3; SURF_ug_NO
  - Nitrogen dioxide (NO2): µg/m3; SURF_ug_NO2
  - Particulate matter PM10: µg/m3; SURF_ug_PM10
  - Particulate matter PM2.5: µg/m3; SURF_ug_PM2.5
  - Ammonia (NH3): µg/m3; SURF_ug_NH3
  - Nitric acid (HNO3): µg/m3; SURF_ug_HNO3
  - Sulphur dioxide (SO2): µg/m3; SURF_ug_SO2
  - Ammonium (NH4) for PM2.5: µg/m3; SURF_ug_NH4_F
  - Nitrate (TNO3) for PM10: µg/m3; SURF_ug_TNO3
  - Sulphate (SO4) for PM2.5: µg/m3; SURF_ug_SO4
  - Particulate organic matter (POM) for PM2.5: µg/m3; SURF_ug_PART_OM_F
  - Ozone (O3): ppbv; SURF_ppb_O3
- NetCDF metadata includes standard naming conventions, grid mapping, and coordinate references.

## Data structure and format

- File type: NetCDF daily outputs (example filename: EMEP4UK_UK_webrun_emep_4.3_2001_day.nc).
- Dimensions:
  - time: daily records
  - i: grid x-coordinate (EMEP grid)
  - j: grid y-coordinate (EMEP grid)
- Grid and coordinate system:
  - Polar stereographic grid mapping with i (GeoX) and j (GeoY) coordinates in kilometers.
  - Example internal dimensions: i = 220, j = 270 (as in the example).
- Time reference:
  - time variable uses units "days since 1900-01-01 00:00:0".
  - time represents the middle of the daily period.
- Dataset examples and notes:
  - Includes attributes such as current_date_first and current_date_last for the data period.
  - Descriptions emphasize the dataset structure and coordinate mappings.

## Validation and quality control

- Validation sources:
  - AURN monitoring network used to verify hourly model output.
  - UK Met Office AWS used to verify WRF outputs.
- QA/QC approach:
  - Simple linear regression comparison between observations and model values.
  - No additional QA/QC procedures are reported.
- Disclaimer:
  - Use of dataset content is at your own risk; no warranty or guarantee that content is error-free or fit for any purpose.

## Key temporal and model-version notes

- Forest fire data:
  - Forest fire data included only for the years 2002–2012.
- Emissions consistency:
  - The emissions for 2013 and 2014 are the same as those for 2012.
- WRF model versions:
  - 2001–2012 utilize WRF version 3.1.1.
  - 2013–2014 use WRF version 3.6.1, with changes such as no longer nudging specific humidity with reanalysis in the WRF setup.
- Additional documentation:
  - Supporting reference to final reports and model documentation available through DEFRA/UK-AIR sources.

## Notes on data accessibility and use in monitoring

- Outputs are designed to support monitoring of environmental health and policy performance over time by providing standardized daily surface concentrations and related species data.
- The dataset enables the creation of reports, maps, and charts for environmental health assessment and policy evaluation.
- While the underlying emissions and grid configurations are described, users should be aware of the domain-specific resolutions (UK 5 km, broader Europe 50 km) and the time-period-specific model versions when performing trend analyses or comparisons.