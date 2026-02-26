# Urban hydro-meteorological observation data 2016-2018  - Ouagadougou, Burkina Faso

## Overview
- Time period and location: 2016–2018 in Ouagadougou, Burkina Faso.
- Project context: DFID-funded AMMA-2050 (African Monsoon Multidisciplinary Analysis) project.
- Data types: time series of rainfall, water level, and river flow across multiple urban sites.
- Purpose: to understand hydrological function and support hydrological model development.
- Data collection methods: in-situ measurements using tipping bucket raingauges and pressure level sensors; spot gauging for river flows to develop rating curves for converting level to flow.
- Data processing: UK Centre for Ecology and Hydrology (UKCEH) designed the network; processing performed by UKCEH with partner 2iE; data gaps due to equipment malfunction and dry-season periods when pressure level sensors were withdrawn.

## Experimental design and sampling
- Measurement instruments: HOBO MX2001 pressure level sensors (PLS) and Casella tipping bucket rain gauges; spot gauging with MFPro for flow assessments.
- Sampling regime: 
  - Dam3 (flow): hourly
  - 2ie (rainfall): 15-minute intervals
  - Saaba (flow): 5-minute intervals
  - Rimkieta South (flow): 5-minute intervals
  - Rimkieta North (flow): 5-minute intervals
  - Kamboince (rainfall): 15-minute intervals
- Site summaries:
  - Dam3: PLS at dam outlet; measures water level relative to bed; central Ouagadougou; some data gaps due to malfunction.
  - 2ie: rainfall in city centre, secure location with minimal obstructions.
  - Saaba: PLS at culvert downstream, upstream area ~77 km², urban/bare earth mix.
  - Rimkieta South: culvert site, upstream ~73 km², some attenuation due to Boulimougou dam.
  - Rimkieta North: larger upstream area ~192 km²; urban/bare earth mix.
  - Kamboince: rainfall site at 2ie grounds in northern city location.
- Data management: data coordinates, elevations, and timestamps recorded to support site-specific analysis.

## Transformation, quality control and derivation
- Rating curves: derived for level-to-flow using intermittent spot gauging of storm flows (velocity and depth) to relate depth to flow per site.
- Flow calculation: flow from depth using cross-sectional area and velocity; rating curves applied to time-series depths.
- Data cleaning: erroneous measurements removed after visual inspection of rating curves; rainfall and dam level data visually inspected to remove errors.
- Data storage: processed time-series stored in an Oracle database; derived flow time series generated from rating curves.

## Data structure and recorded values
- Files: six CSV time-series files plus one metadata CSV summarizing sites.
- Flow files: columns – date_time, flow (m³/s), missing data index; minimum flow value 0 m³/s; M denotes missing values.
- Dam level file: columns – date_time, level (mAOD), missing data index.
- Rainfall files: columns – date_time, rainfall (mm), missing data index; minimum rainfall 0.2 mm in 15 minutes; zero values represent periods without rainfall.
- Time steps by site (as above): Dam3 hourly; 2ie 15-minute; Saaba 5-minute; Rimkieta South 5-minute; Rimkieta North 5-minute; Kamboince 15-minute.
- Metadata: a summary CSV providing site-level metadata (location, time coverage, instrumentation).

## Data availability, sharing and governance
- Dataset composition supports discovery and reuse for urban hydrology and model development.
- Metadata included for site identification, coordinates, elevation, data periods, sampling intervals, and units, aiding interoperability and reuse.
- Data quality notes highlight gaps and QC steps to inform users about data completeness and reliability.
- Sharing considerations: data are prepared for upload to relevant portals/catalogues; licensing/usage terms are not specified in the document; data gaps and QC procedures should be acknowledged in any reuse.

## Implications for Data Stewards
- Data governance: ensure complete, accurate metadata, including site attributes, sensor types, time coverage, and units.
- Data quality: maintain documentation of QC steps, rating-curve methodology, and gap handling to support reproducibility.
- Data interoperability: standardized CSV structure and explicit column definitions facilitate cross-site comparisons and integration with models.
- Data availability and updates: note data gaps due to equipment issues; provide guidance on how updates or corrections would be incorporated.
- User needs: documentation should clarify data scope (urban hydro-meteorological in Ouagadougou) and suitability for hydrological modeling and urban flood analysis.
- Challenges alignment: the dataset exemplifies typical Data Steward challenges—timely data provision, metadata completeness, system interoperability, and handling large, multi-resolution time-series.

## Practical reuse considerations
- Suitable applications: urban hydrology modeling, rating-curve validation, rainfall-runoff analysis, and hydro-meteorological research in West Africa.
- Reproducibility: transparent description of instrumentation, data processing, and QC enhances traceability of derived flow from depth data.
- Format and accessibility: CSV format with clear time stamps and units supports straightforward loading into common analysis tools; multi-site structure enables comparative studies.