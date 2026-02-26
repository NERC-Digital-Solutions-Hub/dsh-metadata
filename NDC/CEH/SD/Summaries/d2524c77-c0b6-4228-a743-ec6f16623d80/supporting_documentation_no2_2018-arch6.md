# Modelled surface nitrogen dioxide (NO2) for the grassland growing season in the UK and USA in 2018.

- The dataset provides modelled daily surface NO2 concentrations and a seasonal average (mid-April to mid-July) for the grassland growing season in 2018, covering the UK and USA.
- Data are generated with the EMEP-WRF global model, version 4.45, based on the EMEP MSC-W chemical transport framework.
- The modeling relies on hourly 3D meteorology from WRF v4.2.2, driven by six-hourly GFS-FNL reanalysis data, over a global 1° × 1° grid with 21 vertical layers.
- Emissions are from the IIASA ECLIPSE v6a GAINS model for the year 2015.
- The output is provided as a shapefile with gridded 1° × 1° cells and 5 attributes.

## Data content and units

- Variable: surface NO2 concentration
- Spatial resolution: 1° by 1° grid
- Temporal scope: daily values for 2018; seasonal average for mid-April to mid-July, 2018
- Location: United Kingdom and United States
- Unit: micrograms per cubic metre (ug m-3)
- Shapefile attributes (5 columns):
  - FID: Unique grid cell identifier
  - Lon: Longitude of cell centre (decimal degrees)
  - Lat: Latitude of cell centre (decimal degrees)
  - NAME: Country (USA or UK)
  - NO2_ug: Mean surface NO2 for the grassland growing season (2018), in ug m-3

## Data generation method

- Model framework: EMEP-WRF global model, version 4.45, built on the EMEP MSC-W framework
- Meteorology: hourly 3D data from WRF (v4.2.2)
- Driving data: GFS-FNL reanalysis (initialised and nudged every six hours)
- Domain and resolution: global coverage with 1° × 1° grid; 21 vertical layers (surface ~40 m to ~16 km)
- Emissions: IIASA ECLIPSE v6a GAINS model (year 2015)
- Output processing: daily surface NO2 values per grid cell; seasonal average computed for grassland growing season (mid-April to mid-July, 2018)

## Data quality and validation

- Quality assurance/quality control applied to EMEP model outputs prior to analysis
- Validation study (Ge et al., 2021) shows the global EMEP-WRF (rv4.34) with WRF meteorology reasonably captures spatial and seasonal variations of NO2 and other major inorganic pollutants across key regions (East Asia, Southeast Asia, Europe, North America)

## Data structure and provenance

- Structure: shapefile with gridded data (1° × 1°)
- Key references:
  - CLRTAP (2017) Mapping critical levels for vegetation
  - Ge, Y. et al. (2021) Evaluation of global EMEP MSC-W (rv4.34) with measurements
  - Mills et al. (2018) Ozone pollution and crop impacts
  - Simpson et al. (2012) EMEP MSC-W model technical description
  - Vieno et al. (2016) Sensitivities of emissions reductions for UK PM2.5

## Usage considerations

- Provides a ready-to-use, self-contained gridded dataset for assessing NO2 exposure over the grassland growing season in the UK and USA for 2018
- Useful for informing policy, impact assessments, or further data products that require NO2 exposure context at continental-spatial scales
- Note: model-based estimates depend on input emissions year (2015 GAINS for 2015 emissions) and meteorological drivers from 2018; seasonality and regional performance should be considered alongside validation studies