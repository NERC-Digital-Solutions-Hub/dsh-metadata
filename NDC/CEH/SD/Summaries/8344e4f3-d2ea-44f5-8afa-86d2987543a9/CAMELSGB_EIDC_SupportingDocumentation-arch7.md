# Catchment attributes and hydro-meteorological timeseries for 671 catchments across Great Britain (CAMELS-GB)

## Overview
- Freely available, large-sample dataset of catchment hydro-meteorological timeseries and landscape attributes for 671 Great Britain catchments.
- Combines NRFA river flow data with new meteorological timeseries and a comprehensive set of catchment attributes.
- Aimed at enabling environmental data analysis and modelling through map-based data products and analyses.

## Spatial data and catchments
- Catchments: 671, drawn from the UK NRFA SLA network; Northern Ireland excluded due to meteorological data gaps; two gauges excluded where boundaries could not be meaningfully defined.
- Catchment boundaries: derived from CEH IHDTM flow-direction grids; boundaries may introduce errors if the topographic mask poorly defines the area.
- Boundary data: provided as a shapefile CAMELS_GB_catchment_boundaries on the British National Grid projection.
- Attribute and boundary data are designed for spatial analyses and map-based presentation.

## Hydro-meteorological timeseries (temporal data)
- Period: 1 October 1970 to 30 September 2015.
- Variables per catchment: daily discharges/flows, rainfall, potential evapotranspiration (PET), temperature, short-wave and long-wave radiation, specific humidity, and wind speed.
- Data sources:
  - Rainfall: CEH-GEAR (1 km gridded)
  - Meteorology: CHESS-met (1 km gridded)
  - PET: CHESS-PE (Penman-Monteith)
- PET estimates: two variants provided—PET (transpiration only, no interception) and PETI (includes interception on rainy days).
- Data completeness: meteorological series have no missing data; flow series may contain NaN values.
- File structure: 671 CSV time-series files named CAMELS_GB_hydromet_timeseries_<catchmentID>_19701001-20150930 with 16436 rows and 11 columns; Column 1 is date, remaining columns describe various time-series values as per a provided table.

## Catchment attributes (static data)
- Eight attribute files corresponding to classes:
  - Topographic
  - Climatic
  - Hydrologic
  - Land Cover
  - Soil
  - Hydrogeology
  - Hydrometry
  - Human Influences
- Each file contains catchment-level attributes for all 671 CAMELS-GB catchments; first column is gauge_id (NRFA ID), followed by attribute-specific columns.
- Key attribute themes:
  - Location and topography: gauge_id/name, latitude/longitude, easting/northing, area, mean/min/max elevations, elevation percentiles, mean drainage path slope.
  - Climate: mean daily precipitation and PET, aridity, seasonality, snow fraction, and various precipitation/dry/wet day metrics.
  - Hydrology: mean discharge, runoff ratio, streamflow elasticity, slope of flow duration curve, baseflow indices, and related hydrologic signatures.
  - Land cover: percent cover of deciduous/evergreen woodland, grass, shrubs, crops, urban, inland water, bare soil/rocks, and dominant land cover.
  - Soils: comprehensive soil properties (sand/silt/clay fractions, bulk density, total available water content, porosity, depth to bedrock, etc.) with quality flags and percentile values; notes on uncertainties and pedotransfer function limitations.
  - Hydrogeology: productivity fractions for hydrogeological units; groundwater intergranular/fracture flow classifications.
  - Hydrometry: gauging station type, data period availability, discharge uncertainty, bankfull and structure-full flow, and uncertainty metadata.
  - Human influences: reservoir data (count, capacity, storage use, usage by sector), abstractions and discharges (England-only caveats), and other human infrastructure indicators.
- Data caveats:
  - Land cover is based on a 2015 snapshot (LCM2015) and may differ from NRFA-derived classifications (LCM2000); uncertainties in satellite data and classification.
  - Soil data have high spatial heterogeneity; pedotransfer function choices can affect applicability.
  - Abstraction/discharge data are England-only, time-varying, and do not capture all possible withdrawals/returns; appropriate use is as a guide rather than exact totals.
  - Some attributes are suitable for regional/national comparisons rather than sub-catchment scale applications.

## Derivation and data integration
- Timeseries/attributes are derived by mapping 50 m grid cells within each catchment mask to the corresponding dataset cell and computing a weighted average (area-weighted) to account for varying grid sizes, ensuring representative catchment-level values.

## Data access, guidance, and provenance
- Data and metadata are designed for broad accessibility and reuse, with recommended reading of the CAMELS-GB paper for detailed methodology and limitations.
- Data sources include:
  - UK National River Flow Archive (NRFA)
  - CEH Gridded Estimates of Areal Rainfall (CEHGEAR)
  - CHESS-met (meteorology)
  - CHESS-PE (potential evapotranspiration)
  - CEH’s IHDTM for boundaries
  - UK land cover maps (LCM2015)
  - European Soil Database and other soil/hydrogeology datasets
- A dedicated CAMELS-GB paper detailing dataset construction will be published in Earth System Science Data.
- Contact: gemma.coxon@bristol.ac.uk for data usage questions.

## Appendix and acknowledgements
- Appendix: list of gauge IDs used for CAMELS-GB.
- Acknowledgements: funded by NERC MaRIUS project (grant NE/L010399/1); thanks to contributors and data providers.
- References include foundational CAMELS datasets (USA, Chile) and supporting methodological papers for geospatial and hydrological analyses.