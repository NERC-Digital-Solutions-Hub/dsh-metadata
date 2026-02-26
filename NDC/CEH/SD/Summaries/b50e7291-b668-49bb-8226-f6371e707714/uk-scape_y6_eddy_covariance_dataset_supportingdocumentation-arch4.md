# Meteorology, soil physics, and eddy covariance measurements of carbon dioxide, energy, and water exchange from a distributed network of sites across England and Wales, 2023 to 2024

- A dataset describing land surface–atmosphere exchanges of sensible heat (H) and latent heat (LE), plus supporting meteorological and soil-physics data
- Collected at six eddy covariance (EC) flux tower sites across England and Wales
- Time period: 2023–2024
- Primary dataset name: UK-SCAPE_Y6_Flux_Dataset
- Accompanying site metadata and data-dictionary files provided to describe site characteristics and variable definitions

## Study sites and site metadata

- Six flux monitoring sites include:
  - Three croplands (two on peat, one on mineral soils)
  - One peatland grassland
  - One lowland fen under conservation management
  - One relatively intact upland raised bog
- Elevation range: from 2 m below sea level to 565 m above sea level
- Mean annual temperature: 5–10 °C; mean annual precipitation: 534–1815 mm
- Site metadata described in UK-SCAPE_Y6_Site_Metadata.csv (variables include site name, file name, start/end dates, land use, soil type, sensor models, measurement heights, geographic coordinates, and other site characteristics)
- Table 1 summarizes site-level metadata fields (IDs, land use, soil type, measurement heights, sensor models, canopy and soil measurements, and other operational details)

## Data collection: fluxes and ancillary measurements

- Flux data: turbulent sensible heat (H) and latent heat (LE) fluxes measured above the canopy using open-path EC systems
- Instruments: sonic anemometer, LI-7500 IRGA for CO2 and H2O, 20 Hz sampling; data logged on CR3000 Micrologger and telemetered
- Measurements at multiple heights; sea-level and various elevations considered (Zm varies by site; maize crops raised Zm to ~5 m)
- Ancillary meteorological and soil data collected concurrently, including:
  - Air temperature (TA) and relative humidity (RH) at 2.0 m
  - Barometric pressure (PA)
  - Net radiation (NETRAD) and component shortwave/longwave radiation (SW_IN, SW_OUT, LW_IN, LW_OUT)
  - Soil heat flux (G) at 0.03 m depth; soil water content (SWC) and soil temperature (TS)
  - Precipitation (P)
  - Water table depth (WATER_TABLE_DEPTH) in peatlands where possible
- Vegetation data: canopy height, leaf area index (LAI), and biomass via destructive sampling (leaves, stems, roots, grains as applicable)

## Data processing and quality control

- Flux calculations: processed with EddyPro software (v7.0.6), using 30-minute block-average fluxes
- Corrections included: angle-of-attack, planar rotation, high/low-frequency cospectral corrections, density corrections for H and LE
- Data quality control (QC):
  - Outlier removal via median absolute deviation
  - Stationarity and turbulence tests; periods failing tests removed
  - Footprint analysis to ensure representativeness (>80% flux originating from target ecosystem)
  - Visual inspection of all flux and ancillary data; clearly erroneous values removed
- Calibration: gas analyzers calibrated according to manufacturer specifications (in-house or by manufacturer)

## Gap filling and flux partitioning

- Gap filling: Marginal Distribution Sampling approach
- Flux partitioning: decomposition of Net Ecosystem Exchange (NEE) into Gross Primary Production (GPP) and Reco using Reichstein et al. and Lasslop et al. methods
- Tools: REddyProc in R (REddyProc package)
- Ancillary data gap filling: where feasible, using collocated COSMOS-UK sites

## Data structure and accessibility

- Time-series data provided as six separate CSV files (one per site)
- Each file follows the structure described in UK-SCAPE_Data_Dictionary.csv
- Time series begin at START_DATE and end at END_DATE from UK-SCAPE_Y6_Site_Metadata.csv
- Missing values denoted by -9999
- TIMESTAMP_START and TIMESTAMP_END may appear in scientific notation in some software (e.g., Excel)
- Vegetation data provided as non-continuous time series in CSV format, with variables described in UK-SCAPE_Data_Dictionary.csv
- Data dictionary (UK-SCAPE_Data_Dictionary.csv) details variable definitions and units

## Metadata, documentation, and acknowledgments

- Comprehensive metadata and variable definitions are available via accompanying files:
  - UK-SCAPE_Y6_Site_Metadata.csv (site-level metadata)
  - UK-SCAPE_Data_Dictionary.csv (variable descriptions and units)
- Data collection funded by the NERC UK-SCAPE programme (NE/R016429/1); additional support from landowners and contributing organizations (e.g., Grange Farm flux tower)
- Acknowledges landowners and partner organizations (e.g., Natural Resources Wales, RSPB, Natural England)
- References provided for data processing methods, QC procedures, footprint analysis, and gap-filling/partitioning techniques