# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from South Basin of Windermere 2021 - 2022

## Overview
- Ongoing fortnightly monitoring of multiple limnological parameters for the South Basin of Windermere, Cumbria, England.
- Time period: January 2021 to end of 2022.
- Data describe surface temperature, surface oxygen saturation, water clarity, alkalinity, pH, inorganic nitrogen, phosphorus, silica, and phytoplankton chlorophyll a.
- Data are provided as raw measurements collected from a boat at a marked buoy position in the deepest part of the lake, integrated from 0 to 7 m depth.

## Sampling regime and collection methods
- Fortnightly sampling schedule.
- Measurements collected from a boat at a fixed buoy location representing the deepest part of the lake.
- Integrated water column sample from 0–7 m depth.

## Variables and units (in downloadable CSV)
- TEMP: surface temperature, deg C.
- OXYG: surface oxygen saturation, % air-saturation.
- SECC: Secchi depth, metres (water transparency).
- ALKA: alkalinity, µg CaCO3 per litre.
- pH: acidity/alkalinity measure.
- NH4N: ammonium, µg N per litre.
- NO3N: nitrate, µg N per litre.
- PO4P: soluble reactive phosphate, µg P per litre.
- TOTP: total phosphorus, µg P per litre.
- SIO2: dissolved reactive silicon, µg per litre.
- TOCA: phytoplankton chlorophyll a, µg per litre.
- Note: Some values may be below detection limits, indicated by a < sign in the Sign(if<LOD) column.

## Data structure and download format
- Data delivered as a comma-separated values (CSV) file.
- Columns include Date, Variable/Description, Value/Description, and Sign(if<LOD), with a description of each variable and its units.

## Quality control, validation, and caveats
- These are raw data and have not yet undergone full quality control or calibration.
- Data have been double-entered and visually checked.
- Gaps in data primarily due to weather, Covid-19 restrictions, or staff shortages.

## Data provenance and acknowledgments
- Data collection supported by Natural Environment Research Council (NERC), award NE/R016429/1, as part of the UK-SCaPE programme delivering National Capability.
- Data validation supported by NERC, award NE/Y006208/1, as part of the ACCESS-UK programme delivering National Capability.

## GIS considerations and recommended usage
- Spatial scope is the South Basin of Windermere, using a single, fixed buoy location (deepest part of the lake); suitable for time-series mapping and basemap integration of water quality and physical parameters.
- Data can be ingested into GIS as a point dataset with timestamped attributes for each measurement event; 0–7 m integration influences interpretation of surface-layer conditions.
- Important caveat: data are raw and not fully quality-controlled; treat as preliminary and cross-validate with other QC’d datasets if possible.
- When creating map-based products, ensure consistent units and clearly annotate below-detection values (Sign(if<LOD)).
- Potential applications: visualization of seasonal trends, basin-wide comparisons (if combined with additional basins/datasets), and integration with other environmental layers (e.g., depth, basin hydraulics) for policy and public-facing maps.