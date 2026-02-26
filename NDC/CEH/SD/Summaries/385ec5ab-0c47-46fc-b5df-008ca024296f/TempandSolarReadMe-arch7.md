# TempandSolar.csv

## Overview
- Datasets temperature and solar radiation data collected during four urine collection trials with Welsh Mountain ewes in 2016.
- Aims aligned with GIS-oriented data products: enabling map-based visualization and spatial-temporal exploration of environmental conditions.

## Data Description
- Project: Uplands-N2O
- Grant number: NE/M015351/1
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Mick J Whelan, Andrew J King, Rory P Wilson, Alice F Charteris, Laura M Cardenas, Davey L Jones, Dave R Chadwick
- Data reuse: fully cite the dataset if reused.
- Content: temperature (AirTemp, in °C) and solar radiation (SolarRadiation, in W m^-2) data.
- Trials: four urine collection trials with Welsh Mountain ewes conducted in 2016.
- Sites/seasons:
  - 1) Spring semi-improved site
  - 2) Summer semi-improved site
  - 3) Autumn semi-improved site
  - 4) Autumn improved site
- Data source: meteorological station installed at each site (Skye Instrument, Llandrindod Wells, UK).
- Sampling frequency:
  - Half-hourly intervals for most data
  - Hourly intervals for the autumn improved site
- TimeDate: timestamps provided as dd/mm/yyyy hh:mm

## Spatial Coverage
- Sites are described by type (Semi-improved vs Improved) and season; exact geographic coordinates are not specified in the description.
- Weather data are station-based (at/near each site), suitable for mapping environmental conditions across trial locations when site coordinates are known.

## Temporal Coverage
- Year: 2016
- Timestamps in dd/mm/yyyy hh:mm format
- Variable sampling frequency (half-hourly generally; hourly for one site)

## Provenance and Quality Notes
- Data originate from on-site meteorological equipment (Skye Instrument).
- Metadata emphasizes citation if reused, implying traceability to source.
- Data may require cleaning and transformation to integrate across trials due to differing resolutions (half-hourly vs hourly) and potential site-specific gaps.

## GIS Use and Applications
- Suitable for map-based visualizations of temperature and solar radiation across sites and seasons.
- Can support:
  - Temporal heatmaps or time-series mapping by site
  - Spatial joins with land-use, vegetation, or climate layers
  - Aggregation to common time intervals for comparative analyses
- Important considerations:
  - Aligning data from different sampling intervals
  - Incorporating site locations or polygons to enable accurate spatial representation
  - Handling potential data gaps and ensuring consistent units and time references

## Limitations and Considerations
- No explicit latitude/longitude or site polygons provided in the description; spatial analysis requires obtaining site coordinates or boundaries.
- Time zone information is not stated; ensure consistency when integrating with other datasets.
- Data standardization may be needed before cross-site aggregation (different seasons and site types).