# Climatic data (Meteorological Office recordings) from four sites along an altitudinal gradient in Cumbria. 1952 - 1990

## Overview
- A dataset of climatic observations from four sites along an altitude gradient in Cumbria.
- Collected according to standard Meteorological Office procedures as described in the Observer's Handbook (4th ed., 1982).
- Data stored in a database described by Cuthbertson (1993) and summarized in MM.pdf.
- Useful for GIS-based analyses of spatial and temporal climatic variation.

## Site locations and metadata
- Newton Rigg: Grid Reference 349300 531000; Altitude 171 m; data collected by staff at Newton Rigg Agricultural College.
- Widdybank Fell: Grid Reference 381700 529700; Altitude 527 m; data collected by Ian Findlay.
- Moor House: Grid Reference 375100 533400; Altitude 549 m; data collected by Andy Millar.
- Great Dun Fell: Grid Reference 371600 532100; Altitude 847 m; staff responsible unknown.
- Recording locations are indicated in the dataset by DATID.

## Recording locations and data structure
- Data descriptions are linked to DATID entries (e.g., Moor House, Newton Rigg, Widdybank Fell, Great Dun Fell) with corresponding earliest and last dates.
- Earliest and latest observation dates by site:
  - Moor House: 01-MAY-1952 to 31-DEC-1979
  - Newton Rigg: 01-JAN-1959 to 31-DEC-1990
  - Widdybank Fell: 01-JUN-1974 to 31-DEC-1989
  - Great Dun Fell: 01-JAN-1973 to 29-AUG-1975

## Variables included
- DATID: Data set identifier.
- REC_DTE: Record date.
- Temperature variables: MAXTMP (max daily temp, °C), MINTMP (min daily temp, °C), MEANTMP (mean daily temp, °C), MINGRTMP (min daily grass temp, °C).
- Soil temperatures: E10TMP (10 cm), E20TMP (20 cm), E30TMP (30 cm), E100TMP (100 cm), all in °C.
- Other temperature-related: DRYTMP (dry bulb), WETTMP (wet bulb), DEWTMP (dew point).
- Humidity and atmospheric conditions: HUMIDITY (percent), VAPPRESS (mbar, vapour pressure), SUNSHINE (hours of sunshine).
- Wind and sky: WINDDIR (wind direction), WINDVEL (wind velocity, knots), CLOUD (cloud cover, eighths), VISIBILITY (km).
- Weather descriptors and events: VISCODE (visibility code; see table below), WEATHDESC (weather description), THUNDER (Y if thunder occurred), GALE (Y if gale occurred), FOG (Y if fog occurred).
- Snow-related: HALFSNOW (0 or 1 for ground snow cover), SNOWDEPTH (cm), NEWSNOW (cm of new snow).
- Additional: REC_DTE, DATID linkage for data provenance.

## Visibility codes
- 1: Thick fog
- 2: Thick fog (alternate)
- 3: Fog
- 4: Moderate fog
- 5: Very poor
- 6: Poor
- 7: Moderate
- 8: Very good
- 9: Excellent

## Data provenance and related resources
- The UK Environmental Change Network (ECN) has continued Moor House monitoring from 1991-2015 (Rennie et al., 2017), with data available via the NERC Environmental Information Data Centre (doi: 10.5285/fc9bcd1c-e3fc-4c5a-b5692fe62d40f2f5).

## Potential GIS uses and considerations
- Enables multi-site, altitude-stratified climate comparisons and time-series analyses.
- Suitable for creating map-based visualisations of temperature, humidity, wind, cloud, and visibility patterns across the four locations.
- Helpful for integrating with other environmental layers (e.g., elevation, land cover) to study climate-vegetation or climate-habitat relationships.
- Considerations: differing time spans by site; data quality and consistency depend on adherence to MO procedures; data join relies on DATID and site metadata; potential gaps due to site-specific observation periods.