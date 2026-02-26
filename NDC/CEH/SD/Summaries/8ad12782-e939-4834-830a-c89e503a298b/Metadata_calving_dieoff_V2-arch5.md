# For shapefile: SAIGA_DIEOFF_CALVING_BETPAKDALA.shp

- The dataset documents the locations and timing of mass die-off events and normal calving aggregations for the Betpak-dala population of saiga antelope in central Kazakhstan.
- Mass mortality events are primarily associated with haemorrhagic septicaemia (Pasteurella multocida) and typically occur in May during calving when saiga form dense aggregations.

## Data Content and Geographic Scope

- Contains 214 saiga die-off and calving sites collected from field visits, aerial surveys, telemetry, and literature.
- Betpak-dala population is one of three in Kazakhstan (central provinces).
- Die-off context:
  - 24 die-off sites where mortality was certain or likely caused by the disease (recorded from fieldwork/aerial surveys in 2015 and from 1981/1988 Soviet literature).
  - 15 sites with deaths in 2015; 14 retained (one site excluded due to inconsistencies).
  - 7 sites recorded in 1988.
  - 1981 data: historically concentrated in three main areas (represented as three sites) though deaths occurred as saiga moved northward during calving.
- Calving context:
  - The remaining sites represent normal calving aggregations with no mass mortality events.
- Spatial representation:
  - Field-derived die-off/calving sites are polygons representing true size/shape.
  - Literature-sourced calving areas are points with 6 km buffers around them to reflect average calving aggregation sizes.
- Temporal frame spans 1981, 1988, 2015, and later field/telemetry data through 2008–2016 (with updates described in accompanying papers).

## Data Model and Attributes

- Core identifiers:
  - ID: Unique sequential identifier.
  - Site_ID: Arbitrary ID per site (inherited from other files; no duplications).
  - Year: Year of die-off or calving record (note: 1988/1981 year corrected to 1981 for a specific record).
- Event indicators and timing:
  - Dieoff: 0 or 1 indicating a die-off event at the site.
  - Calving_ST / Calving_PK / Calving_ED: Start, peak, and end dates of calving.
  - Onset / Obs_deaths / Last_death / Carcass_NO / Deaths_NO / Deaths_EV: Various date or count fields related to first observed deaths, onset, and mortality totals (with some fields repurposed as onset in certain cases).
  - Source_Loc / Source_Dat: Source of location and onset/date information (field, literature, telemetry, etc.).
- Data quality and reliability:
  - Accur: Level of locational accuracy (Exact, Good, Indicative, General).
  - Numb_Calve: Calving herd size data from ACBK (telemetry-based, with reliability caveats).
  - Location metadata:
    - Province / District / Location: Administrative and site labels.
    - AREA_KM / PERIM_KM: Area and perimeter of polygons (or buffers for point-derived sites).
    - LAT / LON: Centroid coordinates (decimal degrees).
- Data provenance and custodianship:
  - Author: Person or organization responsible for the data entry for a given site / record.
  - Field / Literature / Local informant / Reserve staff: Data provenance indicators.
- Source notes:
  - Some data marked as collected by the Association for the Conservation of Biodiversity of Kazakhstan (ACBK) under the Altyn Dala Conservation Initiative (ADCI).
  - Other data from literature (e.g., Singh et al. 2010) or Soviet-era sources.

## Data Provenance, Sources, and Documentation

- Primary data sources:
  - Field observations and aerial surveys (2015; Soviet literature 1981/1988).
  - Telemetry data (2008–2016; reliability varies with collar deployment).
  - Soviet literature and Kazakh institutions (Institute of Zoology, Reserves and Hunting reports).
  - Data curated by the Association for the Conservation of Biodiversity of Kazakhstan (ACBK) as part of ADCI (2008–2014).
- Documentation notes:
  - 135 of the 214 locations with environmental data were used to model the probability of a die-off during calving.
  - The accompanying papers detailing collection and modeling are under review; updates available on the EIDC page.
- References:
  - Data historically drawn from Kazakh sources and used/mentioned in Singh et al. (2010): Saiga calving site selection and human disturbance impacts.

## Data Quality, Limitations, and Governance

- Reliability considerations:
  - Field-derived calving data generally more reliable than telemetry-derived estimates.
  - 2008–2009 calving data may be incomplete due to data collection limitations.
  - Telemetry reliance increased since 2009, but decreasing collar numbers after 2011 reduced the completeness of calving-area representations.
  - Numb_Calve estimates based on telemetry become less reliable as collar coverage drops.
- Data rights and usage:
  - All rights held by ADCI; data intended for investigations into mass die-off causes.
  - Accessibility and usage governed by ADCI oversight; specific restrictions may apply to data use in publications and sharing.

## Usage and Applications

- Intended use to identify and model die-off risk during calving periods, informing conservation and management decisions.
- 135 sites with sufficient environmental data used for probabilistic modeling of die-offs during calving.
- Data support for understanding spatial patterns of die-off risk and calving aggregation locations, as well as potential drivers (e.g., human disturbance, telemetry coverage gaps).

## Practical Considerations for Data Stewards

- Maintain clear provenance for each site (source type, accuracy, and date).
- Preserve the distinction between polygon-based die-off/calving sites (field data) and point-based calving sites with buffers (literature data).
- Track changes to Year and other corrected fields (e.g., 1981 vs 1988 year correction) and maintain audit trails.
- Ensure metadata captures reliability notes (Accur, data source type) and caveats about telemetry versus field data.
- Manage rights and access through ADCI governance; document any embargoes or user restrictions.
- Plan for updates as new field or telemetry data become available; align with EIDC page updates and related publications.

## Notes

- Corrections: Year 1988 incorrectly listed for one entry; corrected to 1981.
- The dataset integrates historical literature with contemporary field/telemetry data to provide a comprehensive view of die-off and calving sites in Betpak-dala.