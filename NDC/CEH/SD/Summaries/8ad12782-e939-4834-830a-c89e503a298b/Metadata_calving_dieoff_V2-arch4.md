# SAIGA_DIEOFF_CALVING_BETPAKDALA.shp

## Overview
- Shapefile of 214 saiga die-off and calving sites in Betpak-dala, central Kazakhstan.
- Covers mass mortality events (primarily due to haemorrhagic septicaemia from Pasteurella multocida) occurring mainly in May during calving.
- Includes 24 die-off sites and 190 calving aggregations (with 14 of 15 calving die-offs from 2015 retained; one inconsistent site excluded).
- Data sources: field visits, aerial surveys, telemetry, and literature (1981, 1988, 2015 and later field data up to 2016).

## Data Content and Structure
- Locations: both precise polygons (field-derived die-offs/calving sites) and literature-derived points buffered to 6 km to represent calving aggregations.
- Key fields include: ID, Site_ID, Year, Dieoff (0/1), Population, Calving_ST, Calving_PK, Calving_ED, Onset, Obs_deaths, Last_death, Carcass_NO, Deaths_NO, Deaths_EV, Source_Loc, Source_Dat, Author, AREA_KM, PERIM_KM, LAT, LON, and Numb_Calve.
- Data provenance notes indicate different reliability levels (Exact, Good, Indicative, General) for location data.
- 135 sites with environmental data were used to model the probability of die-offs during calving.
- Data compilation spans Soviet-era literature and modern field/telemetry records (2008–2016) gathered by the Association for the Conservation of Biodiversity of Kazakhstan (ACBK).

## Spatial and Temporal Aspects
- Betpak-dala population is one of three in Kazakhstan; the study area is in central Kazakhstan.
- Temporal coverage includes historical records (1981, 1988) and contemporary observations (primarily 2015; ongoing data through 2016).
- Geometry:
  - Field-derived: polygons representing actual die-off/calving site extents.
  - Literature-derived: point locations with 6 km buffers representing average calving aggregation size.

## Data Quality, Limitations, and Provenance
- Notable data quality notes:
  - One 2015 site (original ID 4) has inconsistencies and is excluded.
  - A correction: the 1988 date was previously misrecorded as 1988; corrected to 1981.
  - Telemetry data completeness has declined since 2011, reducing reliability of calving-area estimates (Numb_Calve).
  - Some 2008–2009 calving data may be incomplete due to field-based collection; field observations considered more reliable than telemetry-based estimates.
- Data rights and governance:
  - ADCI holds rights to the GIS data; primarily intended for investigations into mass die-off causes.
  - Data usage is linked to references and notes within the dataset; licensing and access are governed by ADCI and contributing institutions.

## Uses and Analytical Value
- Used to model die-off probability during calving; 135 sites with environmental data underpin the modeling efforts.
- Supports research into calving site selection, spatial clustering, and factors driving mass mortality events.
- Documentation references and notes (e.g., Singh et al. 2010) provide context on human disturbance and calving site selection.

## Implications for Data Leadership and Management
- Data fragmentation across multiple sources (field data, aerial surveys, telemetry, and literature) highlights the need for:
  - Standardized metadata and data quality flags to improve discoverability and interoperability.
  - Clear provenance and versioning to track updates, corrections, and inconsistencies.
  - strengthened governance around access, rights, and licensing, especially for restricted-use datasets.
- Gaps and opportunities:
  - Improve granularity and consistency of location data across sources.
  - Maintain and report accuracy metadata (Exact/Good/Indicative/General) for end users.
  - Foster cross-institution collaboration to standardize data collection methods and share updates more efficiently.

## Notes and References
- Data sources include field observations, aerial surveys, literature (Soviet-era and more recent), and ADCI-derived data.
- References: Singh, N. J., I.A. Grachev, A.B. Bekenov & E.J. Milner-Gulland (2010) Biological Conservation; ADCI notes; Kazakh Institute of Zoology records.