# The EMEP-WRF global model, version 4.45: Seasonal average surface ozone concentrations for the UK and USA in 2018

- Purpose and product
  - Provides a GIS-ready seasonal average of surface ozone (O3) concentrations for the grassland growing season (mid-April to mid-July) in the UK and USA for 2018.
  - Output is organized on a global 1° x 1° grid, suitable for map-based visualization and spatial analysis.

- Model framework and data sources
  - Based on the EMEP MSC-W chemical transport model, with collection/generation using the EMEP-WRF global model, version 4.45.
  - The EMEP-WRF model uses hourly 3D meteorology from WRF (v4.2.2) driven by six-hourly nudged GFS-FNL reanalysis data.
  - Global domain with 1° x 1° horizontal resolution and 21 vertical layers (surface ~40 m to ~2 km near the top of the 16 km boundary).
  - Emissions are taken from IIASA ECLIPSE v6a GAINS model for the year 2015.

- Spatial, temporal coverage
  - Global model domain; outputs daily mean surface ozone concentrations for 2018.
  - Seasonal averaging applied to UK and USA grid cells during the grassland growing season (mid-April to mid-July, 2018).

- Output specifics and units
  - Variable: daily surface ozone concentration, expressed in parts per billion (ppb).
  - Coordinate reference system: WGS 1984; data values in decimal degrees for grid cell centers.
  - The dataset for the summarized product is presented as a shapefile with 1° x 1° grid cells.

- Data structure and attributes
  - Shapefile contains gridded data with five attributes:
    - FID: Unique grid cell identifier
    - Lon: Longitude of grid cell center (decimal degrees)
    - Lat: Latitude of grid cell center (decimal degrees)
    - NAME: Country (USA or UK)
    - O3_ppb: Seasonal mean surface ozone concentration in ppb for mid-April to mid-July, 2018
  - O3_ppb range across the dataset: 19.3 ppb to 50.9 ppb

- Quality control and validation
  - Model outputs undergo QA/QC before use in analyses.
  - Validation references include Mills et al. (2018), with comparisons to Global Atmosphere Watch (GAW) network observations to assess daily maximum ozone variation.
  - The model generally captures spatial and temporal variations, including higher ozone episodes and seasonal patterns.

- How this data supports GIS-based analysis
  - Enables map-based visualization of ozone exposure patterns at 1° resolution.
  - Facilitates cross-regional comparisons (UK vs USA) and integration with other spatial datasets.
  - Suitable for coupling with other GIS layers to assess exposure, risk, or policy-relevant spatial analyses.

- References
  - Mills et al. (2018). Ozone pollution will compromise efforts to increase global wheat production. Global Change Biology.
  - Simpson et al. (2012). The EMEP MSC-W chemical transport model technical description.
  - Vieno et al. (2016). Sensitivities of emissions reductions for UK PM2.5 mitigation. Atmospheric Chemistry and Physics.
  - Additional details on dataset construction and validation are provided in the cited supplementary materials.