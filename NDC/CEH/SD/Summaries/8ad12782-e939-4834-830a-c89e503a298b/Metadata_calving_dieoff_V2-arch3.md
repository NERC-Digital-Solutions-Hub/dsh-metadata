# For shapefile: SAIGA_DIEOFF_CALVING_BETPAKDALA.shp

## Overview
- Represents locations (and available dates) of mass die-offs and normal calving events in the Betpak-dala saiga population, central Kazakhstan.
- Combines data from field visits, aerial surveys, telemetry, and literature, covering three major mortality events since 1981/1988/2015.
- Includes 214 sites total: 24 die-off sites (confirmed or likely due to haemorrhagic septicaemia) and the rest calving aggregations.
- Data used for modeling die-off probability at calving aggregations; 135 sites with environmental data used for this modeling (details in related papers under review).

## Data content and structure
- Spatial representation:
  - Die-off sites: polygons representing actual mortality event areas.
  - Calving sites: polygons (based on field/telemetry data) or buffers (6 km) around point locations from literature, reflecting average calving aggregation sizes.
- Key attributes:
  - ID, Year, Dieoff (0/1), Population (Betpakdala), Calving_ST/PK/ED (calving start/peak/end dates), Onset/Obs_deaths (first observed death dates), Last_death, Carcass_NO, Deaths_NO, Deaths_EV, Source_Loc/Source_Dat, Author, Accur (location accuracy: Exact, Good, Indicative, General), AREA_KM, PERIM_KM, LAT/LON, Province, District, Location, Numb_Calve (telemetry-based herd size classification).
- Data quality fields and notes:
  - Corrected error: 15/06/2018 year originally listed as 1988; updated to 1981 as appropriate.
  - Some fields combine multiple data origins (field, literature, telemetry, local informants); metadata explains reliability differences.

## Data sources and collection
- Fieldwork: direct observations and telemetry data (advantage: higher reliability; caveats with declining collar numbers over time).
- Aerial surveys: used to locate die-offs and calving aggregations.
- Literature: historic records (1981, 1988) and published compilations (e.g., Singh et al. 2010).
- Organizations: Association for the Conservation of Biodiversity of Kazakhstan (ACBK) under the Altyn Dala Conservation Initiative (ADCI); data rights held by ADCI.

## GIS data quality and metadata considerations
- Data quality heterogeneity:
  - Field observations are generally more reliable than telemetry-derived estimates, especially where telemetry data coverage declined after 2011.
  Calibration of Numb_Calve from telemetry may be less reliable with fewer collars.
- Metadata and provenance:
  - Origins of location and date data clearly documented; different source types (Field, Literature, Local informant, Reserve staff, etc.) noted per site.
- Data use limitations and governance:
  - ADCB/ACBK rights restricting data use; data primarily intended for investigation of mass die-off causes.
  - Data sharing and openness balanced against rights and integrity of source datasets.
- Analysis implications:
  - 135 sites with environmental data used to model die-off probability during calving; relationships and uncertainties described in associated papers (under review).

## Usage and status
- The underlying dataset supports modeling of die-off probability during calving periods and informs conservation monitoring decisions.
- Related analyses and updates are available via the EIDC page; historical records are cross-referenced with Kazakh institutions and published literature (e.g., Singh et al. 2010).

## Notes and references
- Key cited work: Singh, N. J., I.A. Grachev, A.B. Bekenov & E.J. Milner-Gulland 2010 (Biological Conservation) on calving site selection and disturbance.
- Historical data sources from Kazakh Institute of Zoology and Department of Reserves and Hunting; ADCI notes on data collection timelines and reliability.