# SAIGA_DIEOFF_CALVING_BETPAKDALA.shp

## Overview
- Shapefile documenting locations of mass die-off events and normal calving aggregations for the Betpak-dala population of saiga antelope in central Kazakhstan.
- Contains 214 sites (die-off and calving) collected from field visits, aerial surveys, telemetry, and literature.
- 24 die-off sites are confirmed or highly likely to be caused by haemorrhagic septicaemia.
- 135 sites with environmental data were used to model the probability of a die-off during calving.
- Distinguishes die-off events (mass mortality) from regular calving aggregations.

## Data content and structure
- Site types:
  - Die-off sites (mass mortality; some sites from 1981, 1988, and 2015 data)
  - Calving aggregations (normal calving sites)
- Spatial representation:
  - Field/telemetry-derived sites: polygons representing actual die-off/calving areas.
  - Literature-derived sites: points with 6 km buffers around them to reflect average calving aggregation size.
- Key attributes (examples):
  - ID, Year, Dieoff flag (0/1), Population (Betpakdala)
  - Calving start, peak, end dates; Onset date when deaths were first observed
  - Observed deaths, Last death, Carcass numbers, Deaths numbers, Deaths in event
  - Location sources: Field, Literature, Local informant, Reserve staff, etc.
  - Source locations and dates; Accuracy (Exact, Good, Indicative, General)
  - Area (km2), Perimeter (km), Latitude/Longitude of site centroid
  - Administrative fields: Province, District, Location name
  - Numb_Calve (calving data from telemetry; reliability varies)
  - Author/Data source attribution
- Data completeness: 214 total sites; 135 with environmental data used for modeling

## Temporal and spatial scope
- Time periods: die-off and calving events documented for 1981, 1988, and 2015; additional data up to 2016 from ADCI-related work
- Geographic scope: Betpak-dala population in central Kazakhstan

## Data sources and provenance
- Primary data sources:
  - Fieldwork, aerial surveys, telemetry data
  - Soviet-era literature (1981, 1988)
  - Later data collected 2008–2016 by the Association for the Conservation of Biodiversity of Kazakhstan (ACBK)
  - Earlier calving data compiled by Singh et al. (2010)
- Data incorporation:
  - 214 sites derived from multiple sources; 24 die-off sites selected where mortality attributed to haemorrhagic septicaemia
  - 135 sites used for modeling probability of die-off during calving
- Notes on data handling:
  - Literature-derived locations used as points with buffers; field/telemetry-derived data used as polygons
  - Data cross-referenced and quality-checked; some inconsistencies noted (e.g., 2018/1988 year correction)

## Data quality, caveats, and usage notes
- GIS data from ACBK calving areas (2008–2014) have varying reliability:
  - Field observations generally more reliable than telemetry-based estimates
  - 2008–2009 data may be incomplete due to limited expeditions
  - Telemetry data contributed since 2009; completeness peaked around 2011 and declined thereafter
  - Numb_Calve (telemetry-based calving counts) becomes less reliable with fewer collars
- Data rights and scope:
  - Data collected for calving area investigations; rights belong to ADCI
  - Primarily intended for investigating causes of mass die-offs
- Ongoing work:
  - Collection and use of data and details of mass mortality events described in related papers (under review)

## References
- Data sources and related work:
  - Singh, N. J., I.A. Grachev, A.B. Bekenov & E.J. Milner-Gulland (2010). Saiga antelope calving site selection is increasingly driven by human disturbance. Biological Conservation, 143, 1770-1779.
  - Kazakh Institute of Zoology and Department of Reserves and Hunting reports (1981, 1988)
  - Data with the ADCI framework and updates via the EIDC page