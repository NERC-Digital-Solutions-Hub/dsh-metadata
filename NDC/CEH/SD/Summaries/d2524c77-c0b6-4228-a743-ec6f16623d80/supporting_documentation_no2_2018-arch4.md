# Modelled surface nitrogen dioxide (NO2) for the grassland growing season in the UK and USA in 2018.

## Overview
- A modeled dataset of surface NO2 for the grassland growing season (mid-April to mid-July) in 2018 for the UK and USA.
- Generated using the EMEP-WRF global model, version 4.45, with lineage traceable to the EMEP MSC-W model.
- Outputs are daily NO2 values on a 1° × 1° grid, with a seasonal average computed for the specified period and regions.

## Data provenance and collection
- Model family: EMEP-WRF (global) v4.45, based on EMEP MSC-W.
- Meteorology: 3D hourly data from WRF v4.2.2 driven by ECMWF IFS for initialization; nudged every six hours with GFS-FNL data.
- Emissions: IIASA ECLIPSE v6a GAINS for 2015.
- Outputs: daily surface NO2 per 1° × 1° grid, with a seasonal average for mid-April to mid-July, 2018, for the UK and USA.

## Spatial and temporal coverage
- Spatial grid: global 1° × 1° resolution; dataset subset includes UK and USA.
- Temporal scope: all of 2018 for daily values; Grassland growing season averages (mid-April to mid-July) for 2018.

## Data format and structure
- Coordinate system: Geographic Coordinate System WGS 1984.
- Units: micrograms per cubic meter (ug m^-3).
- Data format: shapefile with gridded data at 1° × 1° resolution.
- Attributes (5 fields):
  - FID: Unique grid cell identifier
  - Lon: Center longitude (decimal degrees)
  - Lat: Center latitude (decimal degrees)
  - NAME: Country (USA or UK)
  - NO2_ug: Mean surface NO2 for the grassland season (2018), in ug m^-3

## Data quality and validation
- Quality assurance/quality control is applied to EMEP model outputs before use.
- External validation: Ge et al. (2021) evaluated global EMEP MSC-W driven by WRF (rv4.34) against measurements, showing good capture of spatial and seasonal variations for NO2 across major regions (East/Southeast Asia, Europe, North America).

## Data governance, usability, and considerations for Data Leaders
- Model-derived data intended to inform understanding of NO2 exposure over the grassland growing season; suitable for policy and analytical contexts where observational data are sparse.
- Data discoverability and metadata are embedded in the shapefile structure and accompanying references; users should note the dataset is model-generated (not direct observations) and reflect the 1° grid resolution.
- Potential use cases include evaluating seasonal exposure patterns, informing agricultural or environmental policy, and supporting cross-regional comparisons (UK vs USA) during 2018.
- Considerations and caveats:
  - Spatial resolution is 1° × 1°, which may limit fine-scale analyses.
  - Model-based outputs depend on emissions, meteorology, and model assumptions; validate where possible with ground or atmospheric measurements.
  - Emissions data correspond to 2015 GAINS inputs; assess sensitivity to emission year assumptions if applying to other periods.

## References
- CLRTAP (2017) Mapping critical levels for vegetation. LRTAP Modelling and Mapping Manual.
- Ge, Y., et al. (2021) Evaluation of global EMEP MSC-W (rv4.34) with WRF; Geoscientific Model Development.
- Mills, G., et al. (2018) Ozone pollution and wheat production; Global Change Biology.
- Simpson, D., et al. (2012) The EMEP MSC-W chemical transport model technical description.
- Vieno, M., et al. (2016) Sensitivities of emissions reductions for UK PM2.5; Atmospheric Chemistry and Physics.