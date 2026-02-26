# Modelled surface nitrogen dioxide (NO2) for the grassland growing season in the UK and USA in 2018

## Overview
- This study models surface NO2 for the grassland growing season (mid-April to mid-July) in 2018 for the UK and USA.
- Outputs include daily NO2 values on a 1° x 1° grid and a seasonal average for the specified period.

## Model framework and data sources
- Uses the EMEP-WRF global model, version 4.45, based on the EMEP MSC-W model.
- EMEP MSC-W uses ECMWF-IFS meteorology; EMEP-WRF uses the Weather Research and Forecasting (WRF) model.
- WRF v4.2.2 drives hourly 3D meteorological data for 2018; initialized and nudged every six hours with GFS-FNL data.
- Global domain with 1° x 1° horizontal resolution and 21 vertical layers (surface ~40 m to ~2 km top; total top ~16 km).
- Emissions data come from IIASA ECLIPSE v6a GAINS model for the year 2015.

## Output and spatial/temporal scope
- Daily surface NO2 values per 1° x 1° grid cell.
- Seasonal average computed for grassland growing season in 2018 for USA and UK.

## Units and data structure
- Coordinate system: Geographic Coordinate System WGS 1984.
- Units: micrograms per cubic metre (ug m-3).
- Shapefile structure: gridded data at 1° x 1° resolution with five attributes:
  - FID: Unique grid cell identifier
  - Lon: Longitude of grid cell centre
  - Lat: Latitude of grid cell centre
  - NAME: Country (USA or UK)
  - NO2_ug: Mean surface NO2 for the growing season (2018), in ug m-3

## Quality control and validation
- Data undergo QA/QC prior to analysis.
- Validation (Ge et al., 2021) indicates the global EMEP-WRF model (rv4.34 driven by WRF) captures overall spatial and seasonal variations for major inorganic pollutants, including NO2, across Europe, North America, and parts of Asia.
- Document references include evaluations and methodological details for the model suite.

## Data structure details
- The dataset consists of a 1° by 1° gridded shapefile with the five attribute columns described above, providing mean NO2 concentrations for each grid cell during the specified period and region.

## References
- CLRTAP (2017) Mapping critical levels for vegetation.
- Ge et al. (2021) Evaluation of global EMEP MSC-W (rv4.34) coupled with WRF.
- Mills et al. (2018) Ozone impacts on wheat production.
- Simpson et al. (2012) EMEP MSC-W chemical transport model description.
- Vieno et al. (2016) Emissions sensitivities for UK PM2.5.