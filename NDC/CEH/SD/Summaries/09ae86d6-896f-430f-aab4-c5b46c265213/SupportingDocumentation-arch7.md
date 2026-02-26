# Stable isotope values for 108 water samples collected in the Gandak River Basin, in Bihar, India are presented, with accompanying values for SEC (specific electrical conductivity) for most of these samples.

## Overview
- Compiles stable isotope measurements (d18O and dD) for 108 water samples from the Gandak River Basin, Bihar, India.
- Samples include surface water, groundwater, and rainfall collected between February 2017 and February 2019.
- Specific electrical conductivity (SEC) values accompany most samples.
- Sampling and analysis were conducted as part of the CHANSE (Coupled Human And Natural Systems Environment) project.
- Isotope analysis performed at British Geological Survey laboratories (UK); SEC measured at source in the field.

## Data content and variables
- Isotopic data:
  - d18O_VSMOW (‰)
  - dD_VSMOW (‰)
- Conductivity:
  - SEC (µS/cm)
- Temporal data:
  - sample_date
- Identifier:
  - BGS Sample identifier or Lab Code
- Missing values:
  - Represented by blanks

## Dataset structure and fields
- Core fields:
  - sample_id / BGS Sample identifier or Lab Code
  - sample_date
  - d18O_VSMOW2 (‰)
  - dD_VSMOW2 (‰)
  - SEC_uS_cm
- Data handling:
  - All fields use blank to denote missing values

## Site locations and attributes
- Sample IDs include a wide range of sources and locations (e.g., 13965-0001, 13965-0002, …, 14466-0029, and various labeled A, S, CHPat, NIGL, etc.).
- Location details available for many samples:
  - Latitude and longitude (lat, long) enabling GIS mapping
  - Source type (e.g., River Gandak, groundwater via tube well/hand pump, canal, rainfall)
  - Source water type (surface water, groundwater, rainfall)
  - Source use (domestic, irrigation, temple, etc.)
  - Source depth (where provided)
  - Surface elevation (mOD)
  - Notes with sampling context (e.g., proximity to canals, pump timing, sampling conditions)
- Spatial distribution covers multiple areas within the Gandak River Basin, including riverine sites, wells, canals, rainfall collectors, and related features.

## Temporal coverage
- Sampling period spans February 2017 to February 2019.
- Dates are recorded per sample (e.g., 28/02/2017, 06/03/2017, 07/03/2017, etc.), enabling time-series analysis and trend assessment alongside spatial mapping.

## Data provenance and context
- Data gathered as part of the CHANSE project.
- Isotopic analysis conducted at the British Geological Survey laboratories (UK).
- Field SEC measurements taken at the sampling source.

## GIS applications and workflows
- Map construction:
  - Use lat/long to create point layers for isotopic data; color-code by source_type or source_water_type.
  - Create separate layers for surface water, groundwater, and rainfall to compare isotopic signatures spatially.
- Data integration:
  - Join isotopic data to site attributes (Source_use, notes, depth, elevation) for enriched feature pop-ups.
  - Integrate with digital elevation models (DEM) and hydrographic networks to analyze groundwater–surface water interactions.
- Visual analytics:
  - Plot d18O and dD values to identify mixing lines or evaporation trends.
  - Overlay SEC values to assess water quality context alongside isotopic signals.
- Temporal analysis:
  - Build time-series dashboards or maps to observe seasonal or interannual isotopic changes.

## Data quality, limitations, and considerations
- Some fields are incomplete or contain inconsistent notes; ensure careful data cleaning where necessary.
- Coordinate data are provided for many samples but not guaranteed for all entries; verify geolocation completeness during GIS integration.
- Units and formats:
  - Isotope values are expressed in per mil deviations; SEC in microSiemens per centimeter; standardize as needed for analyses.
- Data synthesis:
  - Because samples come from varied sources (river, groundwater, rainfall) and different uses, consider stratifying analyses by source_type and Source_use to avoid conflating distinct hydrological components.

## Best practices for GIS-ready use
- Standardize coordinate reference system to a common CRS (e.g., WGS84) and ensure consistent decimal degrees.
- Normalize date formats to ISO 8601 for temporal analyses.
- Validate sample_id keys for reliable joins across isotope, SEC, and site-attribute datasets.
- Create metadata documenting data provenance (CHANSE), measurement methods, and any known data gaps or caveats.

## Provenance and usage notes
- CHANSE project data collection; isotopic analyses performed at BGS, UK.
- Useful for isotope-based hydrological investigations, groundwater–surface water interaction studies, and rainfall input characterization within the Gandak River Basin, with GIS-enabled visualization and analysis.