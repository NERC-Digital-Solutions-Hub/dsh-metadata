# SAIGA_DIEOFF_CALVING_BETPAKDALA.shp

## Overview
- GIS dataset of saiga antelope mass die-off events and normal calving aggregations in the Betpak-dala population, central Kazakhstan.
- Temporal span and event counts: das die-offs and calving events documented for 1981, 1988, and 2015; 214 total locations (die-off and calving sites).
- Purpose: support understanding and modelling of die-off probability during calving periods; 135 sites with environmental data used for modelling.

## Data Content and Structure
- Site types:
  - Die-off sites: 24 locations, with mortality confirmed or likely due to haemorrhagic septicaemia.
  - Calving sites: normal calving aggregations; some sites used to infer die-offs when needed.
  - 2015 dataset includes 15 calving aggregations with deaths; 14 retained (one excluded due to inconsistencies).
  - Historical data (1981, 1988) drawn from fieldwork, aerial surveys, telemetry, and literature.
- Spatial representations:
  - Field-derived die-off/calving sites: polygons representing actual size/shape.
  - Literature-sourced sites: points with 6 km buffers created to represent average calving aggregation size.
- Data coverage: 214 locations; 135 sites with available environmental data used for modelling die-off probability during calving.

## Spatial Representation and Dataset Schema
- Geometry:
  - Polygons for sites derived from field, aerial, or telemetry data.
  - Points with 6 km buffers for literature-derived calving aggregations.
- Key fields (examples):
  - ID, Site_ID, Year, Dieoff (0/1), Population (Betpak-dala only)
  - Calving_ST (start), Calving_PK (peak), Calving_ED (end), Onset
  - Obs_deaths, Last_death, Carcass_NO, Deaths_NO, Deaths_EV
  - Source_Loc, Source_Dat
  - Field, Literature, Local informant, Reserve staff (data origins/ reliability)
  - Accur (location accuracy): Exact, Good, Indicative, General
  - Numb_Calve (calving herd size, telemetry-based, with caveats)
  - Province, District, Location
  - AREA_KM, PERIM_KM
  - LAT, LON (centroid coordinates)
  - Author (data collectors, ADCB/ACBK attribution)
- Data corrections: a documented correction notes 15/06/2018 where a year was incorrectly labeled as 1988 and corrected to 1981.

## Data Sources and Provenance
- Primary sources:
  - Field observations, aerial surveys, telemetry data (since 2009; reliability varies by data type and collar coverage).
  - Soviet literature data for historical sites (1981, 1988).
  - Association for the Conservation of Biodiversity of Kazakhstan (ACBK/ADCI data collection 2008–2016).
- Related literature:
  - Singh et al. 2010 (calving site selection influenced by human disturbance) referenced for context.
  - Kazakh Institute of Zoology and Reserve/ Hunting reports for older data.
- Rights and usage:
  - Data collected under ADCI; rights retained by ADCB/ACBK; dataset intended for investigations into causes of mass die-offs.

## Data Quality, Limitations, and Notes
- Data quality considerations:
  - Calving-area data from field/telemetry are generally more reliable than those solely from literature.
  - Telemetry data quality declined after 2011 due to reduced collar submissions; calving herd size estimates (Numb_Calve) become less reliable with fewer collars.
  - Some 2008–2009 data may be incomplete due to expedition-based collection.
- Spatial accuracy:
  - Location accuracy classifications (Exact, Good, Indicative, General) guide GIS handling and uncertainty.
- Scope and use restrictions:
  - Data intended for studying calving-related mass die-offs; rights and use are with ADCB/ACBK.
  - The 135-site environmental data subset is specifically used for modelling die-off probability during calving events.

## Usage Context for GIS Specialists
- Data integration:
  - Combine diverse data resolutions (polygons for field-derived sites; buffers for literature-derived sites) into a consistent GIS workflow.
  - Use 135-site subset with environmental data to drive probabilistic modelling of die-off risk during calving.
- Visualisation:
  - Map die-off vs. calving sites; differentiate data sources (field/telemetry vs. literature) and accuracy levels.
  - Represent calving clusters with buffers; display die-off sites as polygons where available.
- Data preparation:
  - Validate year labels (note: corrected 1981 vs 1988 where applicable).
  - Ensure coordinate systems align; leverage LAT/LON for point data and centroid placement for polygons.
- Modelling and analysis:
  - Use site-level attributes (Onset, Obs_deaths, Deaths_NO, etc.) alongside environmental variables to model die-off probability.
  - Respect data provenance and reliability when weighting observations in analyses.

## References
- Data sources and notes on ADCI data collection (2008–2014) and related methodological caveats.
- Singh, N. J., I.A. Grachev, A.B. Bekenov & E.J. Milner-Gulland (2010) on calving site selection and human disturbance.