# Modelled surface nitrogen dioxide (NO2) for the grassland growing season in the UK and USA in 2018.

## Overview
- Dataset representing modeled surface NO2 for the grassland growing season (mid-April to mid-July) in 2018 for the UK and USA.
- Generated using the EMEP-WRF global model framework.

## Data Generation & Lineage
- Modeling framework: EMEP-WRF global model, version 4.45 (based on EMEP MSC-W).
- MSC-W model uses ECMWF-IFS data; EMEP-WRF uses WRF (v4.2.2) to produce hourly 3D meteorology.
- Data assimilation: WRF initialization/nudging every six hours with GFS-FNL data.
- Domain and resolution: global domain at 1° x 1° grid, with 21 vertical layers (surface ~40 m, top ~16 km).
- Emissions base: IIASA ECLIPSE v6a GAINS model (year 2015).
- Outputs: daily surface NO2 values per 1° x 1° grid cell; seasonal average calculated for grassland growing season (mid-April to mid-July) for 2018.

## Spatial/Temporal Coverage
- Regions: United Kingdom and United States.
- Timeframe: 2018, seasonal average for grassland growing period (mid-April to mid-July).
- Spatial grid: 1° x 1° gridded dataset.

## Data Format, Structure, and Metadata
- Coordinate reference system: WGS 1984.
- Units: micrograms per cubic meter (ug m-3).
- Data format: shapefile with 5 attribute columns:
  - FID: unique grid cell identifier
  - Lon: longitude of grid cell center (decimal degrees)
  - Lat: latitude of grid cell center (decimal degrees)
  - NAME: country (USA or UK)
  - NO2_ug: mean surface NO2 for the grassland season (2018) in ug m-3

## Quality Assurance & Validation
- Outputs pass through QA/QC processes before use in analyses.
- Validation reference: Ge et al. (2021) evaluation of global EMEP MSC-W (rv4.34) driven by WRF, showing the model captures overall spatial and seasonal variations for NO2 and related pollutants across major regions.

## Provenance & References
- Core references and model descriptions include:
  - CLRTAP (2017) Mapping critical levels for vegetation
  - Ge et al. (2021) Geoscientific Model Development: evaluation of EMEP-MSC-W/WRF
  - Mills et al. (2018) Ozone pollution and wheat production
  - Simpson et al. (2012) EMEP MSC-W technical description
  - Vieno et al. (2016) Emissions sensitivity for UK PM2.5
- Data-specific methodological notes drawn from these sources and the dataset description.

## Data Use, Access & Governance Considerations for Data Stewards
- Format and schema: shapefile with defined 1° grid and 5 attributes; ensure consistent metadata for discoverability and reuse.
- Metadata should include: dataset title, creators, model version (EMEP-WRF v4.45), WRF version, data sources (GFS-FNL, IIASA GAINS v6a 2015), temporal coverage (2018 grassland season), spatial resolution (1° x 1°), coordinate system (WGS84), and units (ug m-3).
- Provenance tracking: record model lineage and processing steps to support reproducibility (EMEP-WRF processing chain, seasonal averaging).
- Licensing and access: license or usage rights not specified in the document; ensure appropriate rights are captured in metadata before sharing.
- Data scale and updating: current dataset reflects 2018; consider versioning if re-runs or updates are released; document any embargoes or publication status if applicable.