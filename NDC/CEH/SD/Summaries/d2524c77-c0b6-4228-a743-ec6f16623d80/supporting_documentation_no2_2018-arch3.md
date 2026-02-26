# Modelled surface nitrogen dioxide (NO2) for the grassland growing season in the UK and USA in 2018.

## Overview
- A modeled dataset of surface NO2 concentrations for the grassland growing season (mid-April to mid-July) in 2018 for the UK and USA.
- Outputs are daily values on a 1° × 1° grid, with a seasonal average produced for the specified period.
- Data are produced to support monitoring and evaluation of environmental health implications for vegetation and policy decisions.

## Modelling framework and data sources
- Model: EMEP-WRF global model, version 4.45, based on the EMEP MSC-W model.
- Meteorology: Weather Research and Forecasting (WRF) model, version 4.2.2, providing hourly 3D meteorological data for 2018.
- Initialization/nudging: Every six hours using GFS-FNL data.
- Domain and resolution: Global domain with 1° × 1° horizontal resolution and 21 vertical layers (surface ~40 m to ~2 km).
- Emissions: IIASA GAINS (GAINS) model, using 2015 emissions (GAINS v6a).
- Output: Daily surface NO2 per 1° × 1° grid cell; seasonal average for April 15–July 15, 2018, for the USA and UK.

## Data outputs, units and structure
- Spatial grid: 1° × 1° cells in a global Geographic Coordinate System (WGS 1984).
- Units: NO2 in micrograms per cubic meter (ug m^-3).
- Data format: Shapefile with five attributes per grid cell:
  - FID: Unique identifier
  - Lon: Longitude of grid cell center (decimal degrees)
  - Lat: Latitude of grid cell center (decimal degrees)
  - NAME: Country (USA or UK)
  - NO2_ug: Mean surface NO2 for the grassland growing season (2018), in ug m^-3

## Quality assurance and validation
- QA/QC applied to EMEP model outputs prior to analysis.
- Validation study (Ge et al., 2021) evaluating global EMEP MSC-W (rv4.34) driven by WRF against measurements for 2010 and 2015 showed the model generally captured spatial and seasonal variation for major inorganic pollutants, including NO2, across Europe, North America, and other regions.

## Data governance, metadata and accessibility
- Metadata quality and completeness are important for reuse; there may be barriers to publicly sharing underlying datasets.
- Emphasis on data management, openness, and appropriate data sharing to support monitoring and governance processes.

## Practical implications for monitoring frameworks
- Provides a quantified environmental health indicator (NO2 exposure over grassland vegetation) for policy scrutiny and decision support.
- Useful for assessing potential vegetation responses and informing emission control strategies.
- Must be interpreted with awareness of model-based uncertainties, grid resolution (1°), and the use of 2015 emissions for a 2018 product.

## Limitations and considerations
- Spatial resolution limited to 1° × 1°.
- Emissions input reflects 2015 GAINS data, which may affect representativeness for 2018.
- Seasonal and year-specific outputs; applicability to other years requires new modelling.

## References
- CLRTAP (2017) Mapping critical levels for vegetation. LRTAP Convention Modelling and Mapping Manual.
- Ge, Y., et al. (2021) Evaluation of global EMEP MSC-W (rv4.34) with WRF; Geoscientific Model Development.
- Mills, G., et al. (2018) Ozone pollution will compromise efforts to increase global wheat production. Global Change Biology.
- Simpson, D., et al. (2012) The EMEP MSC-W chemical transport model technical description. Atmospheric Chemistry and Physics.
- Vieno, M., et al. (2016) The sensitivities of emissions reductions for the mitigation of UK PM2.5. Atmospheric Chemistry and Physics.