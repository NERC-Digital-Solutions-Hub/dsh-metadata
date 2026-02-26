# SAIGA_DIEOFF_CALVING_BETPAKDALA.shp

## Overview
- Shapefile representing locations and dates of (i) mass die-offs and (ii) normal calving events in the Betpak-dala saiga population (central Kazakhstan).
- Contains 214 sites (die-off and calving) collected from field visits, aerial surveys, telemetry, and literature.
- Documented die-offs are linked to haemorrhagic septicaemia (Pasteurella multocida); die-offs cluster in May during calving when saiga form dense aggregations.
- 24 die-off sites include mortality likely caused by the disease; 15 of these are used as die-off sites in the dataset.
- 7 sites recorded in 1988; in 1981, deaths concentrated in three main areas (represented as three sites in the database).
- 135 sites with environmental data were used to model die-off probability during calving (details in papers currently under review).

## Data structure and content
- Site representations:
  - Field/telemetry sources: polygons representing actual size/shape of die-off or calving sites.
  - Literature sources: point data buffered to 6 km to represent average calving aggregations.
- Key attributes (examples):
  - ID, Site_ID, Year, Dieoff (0/1)
  - Population (Betpakdala)
  - Calving_ST, Calving_PK, Calving_ED (start, peak, end dates of calving)
  - Onset, Obs_deaths, Last_death, Carcass_NO, Deaths_NO, Deaths_EV, Deaths_EV
  - Source_Loc, Source_Dat (data provenance)
  - Field, Literature, Local informant, Reserve staff (data provenance)
  - AREA_KM, PERIM_KM (size/shape metrics)
  - LAT, LON (centroid coordinates)
  - Author (data collection attribution)
  - Numb_Calve (calving data from ACBK; categorical: Low/Medium/High)
  - Province, District, Location (administrative/place names)
- Data provenance notes:
  - 1981 year corrected from 1988 in one record.
  - 2015 calving deaths include 15 sites (one excluded due to inconsistencies).
  - 214 locations are historical references for ongoing use.

## Data sources and quality
- Primary data sources:
  - Field observations, aerial surveys, telemetry
  - Soviet-era literature (1981, 1988)
  - Recent data from the Association for the Conservation of Biodiversity of Kazakhstan (ACBK) 2008–2016 (ADCI)
  - Literature: Singh et al. 2010 (calving site selection; human disturbance)
- GIS data notes (ACBK 2008–2014):
  - Field data more reliable than telemetry-derived estimates
  - 2008–2009 data may be incomplete
  - Telemetry data: as number of tracking collars declines, reliability of herd size estimates (Numb_Calve) decreases
  - Data intended for investigation of causes of mass die-off; rights belong to ADCI
- Data usage caveats:
  - 135 sites with available environmental data used to model die-off probability
  - Some data are historical and may require careful contextual interpretation

## Usage, modeling, and outputs
- Potential uses:
  - Spatial analysis of die-off risk during calving
  - Mapping calving site distributions and die-off hotspots
  - Integrating with environmental covariates to model die-off probability
  - Creating self-serve GIS dashboards or reports for management and outreach
- Modeling context:
  - Environmental data availability limited to a subset (135 sites)
  - Ongoing papers under review with more methodological detail and results
- Access and rights:
  - Data rights held by ADCI; usage should acknowledge ADCI and data sources as described

## Considerations for data reuse and collaboration
- Expect variability in data quality across years (1981, 1988, 2008–2016) and data sources
- When combining site data with other datasets, distinguish field/telemetry-derived polygons from literature-based buffered points
- Be mindful of location accuracy classes (Exact, Good, Indicative, General) where applicable
- If modeling across years, account for potential inconsistencies and the changing reliability of calving counts (Numb_Calve)

## References and additional context
- Data sources and historical references include field surveys, Soviet literature, ADCI data, and Singh et al. (2010) Biological Conservation article on calving site selection and disturbance.