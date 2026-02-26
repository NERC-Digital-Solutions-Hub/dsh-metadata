# SAIGA_DIEOFF_CALVING_BETPAKDALA.shp

## Overview
- Represents locations (and available dates) of mass die-offs and normal calving events for the Betpak-dala saiga population in central Kazakhstan.
- Contains 214 sites (die-off and calving) from field visits, aerial surveys, telemetry, and literature.
- Historical context: die-offs recorded in 1981, 1988, and 2015; 2015 data include 15 calving aggregations with mass mortality at 14 sites (one excluded due to inconsistencies); 1988 accounts record seven sites; 1981 accounts indicate deaths concentrated around three main areas.
- Betpak-dala is one of three saiga populations in Kazakhstan.

## Data content and structure
- Location types and geometry
  - Die-off and calving sites derived from field data, aerial surveys, or telemetry are represented as polygons (actual size/shape of sites).
  - Literature-sourced locations are points buffered by 6 km to represent average calving aggregation size.
- Dataset size and composition
  - 214 total locations.
  - Of these, 135 sites with available environmental data were used to model the probability of a die-off during calving.
- Key fields and their meanings
  - ID: Unique sequential identifier.
  - Site_ID: Arbitrary ID for each die-off or calving site.
  - Year: Year of die-off or calving record (note: a correction indicates 1981 was mis-stated as 1988 in one entry).
  - Dieoff: 0/1 indicator whether a die-off occurred.
  - Population: Always "Betpakdala" for this dataset.
  - Calving_ST / Calving_PK / Calving_ED: Start, peak, and end dates of calving.
  - Onset / Obs_deaths / Last_death / Carcass_NO / Deaths_NO / Deaths_EV: Dates and counts related to observed mortality (site-level and event-level where available).
  - Deaths_EV: Total deaths for the entire event (when site-level data are unavailable).
  - Source_Loc / Source_Dat: Sources for location and onset/date information.
  - Data provenance indicators: Field, Literature, Local informant, Reserve staff, etc.
  - Accur: Location accuracy (Exact, Good, Indicative, General).
  - Administrative fields: Province, District, Location (name).
  - Area-related fields: AREA_KM (site size in km²), PERIM_KM (perimeter in km), LAT / LON (centroid coordinates for literature-derived points).
  - Author: Data contributor(s).
  - Numb_Calve: Telemetry-based calving herd size (where available; reliability varies with collar availability).
- Data provenance notes
  - 1981 and 1988 data drawn from Soviet literature and ground/aerial counts; 2015 data from fieldwork and aerial surveys; 2008–2016 data from the Association for the Conservation of Biodiversity of Kazakhstan (ACBK) as part of the ADCI.

## Data provenance and sources
- Primary sources
  - Soviet literature for early die-off/calving sites (1981, 1988).
  - Association for the Conservation of Biodiversity of Kazakhstan (ACBK) data (2008–2016) from field data, aerial surveys, and telemetry; notes on reliability and data quality.
  - Additional sources: Singh et al. (2010) for calving site selection context.
- Documentation notes
  - ADCI notes emphasize reliability hierarchy: direct field observations more reliable than telemetry; completeness of calving-area data has varied with collar usage.
  - Data rights belong to ADCI; calving-area datasets are intended for investigations of mass die-offs.

## Modeling and usage
- About 135 sites with environmental data were used to model the probability of a die-off occurring during calving.
- Ongoing write-ups and papers under review (EIDC page) provide further detail on mass mortality events and modeling approaches.

## GIS data notes and data quality considerations
- Calving-area data quality varies by source:
  - Direct field observations generally more reliable than telemetry-based estimates.
  - 2008–2009 data may be incomplete; telemetry data collection increased since 2009 but collar declines reduce completeness over time.
  - Numb_Calve estimates from telemetry become less reliable as collar data become sparser.
- Data scope and scale considerations:
  - Location representations differ by source (polygons vs. 6 km buffered points); researchers should account for this when integrating datasets.
  - Data are intended for calving-area investigations and mass-mortality analysis, with rights retained by ADCI.

## Notable limitations and challenges
- Data gaps at relevant scales, especially historical data.
- Access and harmonization challenges across field, telemetry, and literature sources.
- Variability in data accuracy and completeness over time, affecting model inputs and interpretation.

## References and related notes
- Sing, N. J., I. A. Grachev, A. B. Bekenov & E. J. Milner-Gulland (2010) on calving-site selection and human disturbance.
- Kazakh Institute of Zoology and Department of Reserves and Hunting reports for historical data.
- ADCI data notes and caveats on data reliability and data rights.