# The EMEP-WRF global model, version 4.45

## Overview
- Global 1° x 1° gridded dataset of daily mean surface ozone concentrations (6am–6pm) for 2018, derived from the EMEP-WRF model (v4.45) and driven by WRF meteorology.
- Model chain: WRF v4.2.2 provides hourly meteorology; nudged every six hours with GFS-FNL data; emissions from IIASA ECLIPSE v6a GAINS for 2015; based on the EMEP MSC-W framework.
- Seasonal metric: seasonal mean ozone per grid cell for the grassland growing season (mid-April to mid-July) over the UK and USA, for 2018.

## Data provenance and collection/generation
- The EMEP-WRF model uses a latitude-longitude grid with 21 vertical layers (surface ~40 m to ~16 km).
- Emissions and meteorology inputs are integrated to produce ozone outputs.
- Outputs are provided as a shapefile representing the gridded data.

## Nature, units, and spatial reference
- Spatial reference: Geographic Coordinate System WGS 1984.
- Units: parts per billion (ppb).
- Grid: 1° by 1° cells; 5 attribute fields in the shapefile (see Data structure).

## Quality control and validation
- Undergoes QA/QC prior to use; model validation described in Mills et al. (2018).
- Comparison with Global Atmosphere Watch (GAW) observations shows the model captures spatial and temporal ozone variability, including peak episodes.

## Data structure and content
- Shapefile with gridded data (1° x 1°) and 5 attributes:
  1) FID: Unique grid cell identifier
  2) Lon: Longitude of grid cell center (decimal degrees)
  3) Lat: Latitude of grid cell center (decimal degrees)
  4) NAME: Country (USA or UK)
  5) O3_ppb: Daily surface ozone concentration in ppb, seasonal mean for mid-April to mid-July, 2018
- Values range: 19.3 ppb to 50.9 ppb

## Reuse, citations, and documentation
- Key references:
  - Mills et al. (2018). Ozone pollution will compromise efforts to increase global wheat production. Global Change Biology, 24, 3560-3574. DOI: 10.1111/gcb.14157
  - Simpson et al. (2012). The EMEP MSC-W chemical transport model technical description. Atmospheric Chemistry and Physics, 12, 7825-7865. DOI: http://doi.org/10.5194/acp-12-7825-2012
  - Vieno et al. (2016). The sensitivities of emissions reductions for the mitigation of UK PM2.5. Atmospheric Chemistry and Physics, 16, 265-276.
- Documentation indicates model lineage: EMEP MSC-W platform with ECMWF-IFS inputs; WRF-driven meteorology; GFS-FNL nudging.

## Governance, stewardship, and data management considerations
- Data lineage clearly defined: EMEP-WRF model outputs, meteorology from WRF, inputs from GAINS 2015 emissions, and validation against GAW data.
- Data format is shapefile with explicit metadata fields; coordinate system and units specified for interoperability.
- Temporal scope is 2018 with a seasonal subset (mid-April to mid-July) for UK and USA; emissions year is 2015 reference.
- Potential metadata needs for long-term stewardship: confirm licensing, access constraints, and any further updates or newer years/seasons.
- Practical considerations for data sharing and discovery: ensure the shapefile includes all five attributes and that users understand the seasonal aggregation and geographic scope (UK/USA only).