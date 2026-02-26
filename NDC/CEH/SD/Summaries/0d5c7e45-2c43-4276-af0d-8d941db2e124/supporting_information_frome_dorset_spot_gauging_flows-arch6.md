# River Frome Dorset spot gauging flows 2022

## Overview
- A dataset of spot gauged river flows (m3 s-1) at multiple sites along the River Frome, Dorset, UK, collected in 2022.
- Aimed to support hydrodynamic modeling of nutrient fate and transport by providing flow accretion data along the river reach.

## Data coverage

- Location and reach
  - River Frome between Dorchester and East Stoke Environment Agency gauging stations (lower part of the river).
  - 11 river cross-sections sampled, incorporating 19 river channels across these cross-sections.
  - Major tributaries included: South Winterbourne, Tadnoll Brook, and River Win.
  - Sites distributed along the reach with cross-section locations dictated by accessibility; NGRs provided for each channel.
- Temporal coverage
  - Measurements taken on multiple flow accretion survey days from 12 April 2022 to 5 November 2022.
  - On each survey day, as many sites as possible were gauged, moving upstream to downstream.
  - Not all sites are monitored on every survey day due to time or weather constraints.
- Site details
  - Some cross-sections required multiple channels to obtain total discharge due to braiding (e.g., Pallington Lakes, LM bypass links).

## Measurement methodology

- Channel and transect approach
  - Each river channel was divided into at least 10 equally spaced transects (5–10 transects for small streams <3 m wide).
  - Depth and flow velocity recorded at each transect; velocity measured at a depth of 40% above the riverbed.
  - Cross-sectional area per transect = width × average depth of adjacent transects; discharge per transect = cross-sectional area × average velocity of adjacent transects.
  - Total discharge for each site = sum of all transect discharges.
- Instruments and data processing
  - Valeport current meters used (Model 001 & 002); Model 002 impeller used for shallow flows.
  - Flow velocity derived from impeller revolutions (recorded over a specified period) and converted to m/s using impeller model.
  - Data entered into a bespoke spreadsheet to convert revolutions to velocity; discharge per transect aggregated to site total.
- Sampling design details
  - One flow recording per site per survey day (no replicates).
  - Measurements conducted upstream to downstream when possible.
  - Some sites are private land requiring permission for access.

## Data structure and access

- Data file
  - Single CSV: River_Frome_Dorset_spot_gauging_flows
  - Seven columns: Site, Description, NGR, Date, Start_time, Flow, Impeller
- Content
  - Site: monitoring site name
  - Description: location description (e.g., adjacent to road bridge)
  - NGR: British National Grid Reference for the site
  - Date and Start_time: date and start time of measurement
  - Flow: total discharge for the corresponding stream channel (m3 s-1)
  - Impeller: current meter impeller used (BMF001 or BMF002)

## Quality, completeness, and caveats

- Completeness
  - Not all sites measured on every survey day due to time/weather constraints; some dates missing for certain sites.
- Data quality notes
  - Generally very low river flows during the monitoring period due to an unusually hot, dry summer; groundwater levels reached record lows in boreholes.
  - Potential underestimation on 09/05/22 at Pallington Lakes when using BMF001 (less effective in shallow sections) compared with BMF002.
- Cross-referencing
  - Environment Agency gauging stations available for the study reach: Louds Mill (Dorchester), Stinsford, and East Stoke, which can be used to compare upstream/downstream conditions.

## Provenance

- Collectors
  - Thomas Homan (PhD candidate, University of Bath) and supervisor Prof. Jan Hofman.
- Data handling
  - Data collated and checked by Thomas Homan.
- Equipment support
  - Monitoring equipment lent by Wessex Water Ltd.

## Related data and context

- Availability of EA gauging station data for the study dates, enabling context on upstream and downstream flow comparisons across the study reach:
  - Louds Mill (Dorchester), Stinsford, East Stoke gauging stations.

## Potential data products and usage

- Hydrodynamic model calibration/validation for nutrient fate and transport studies.
- Reach-scale analysis of flow accretion and cross-sectional flow distribution along braided river reaches.
- Dashboards or reports enabling end-users to explore self-serve flow data by site, date, and cross-section.
- Cross-reference with EA gauge data to assess flow variability and data reliability across the study period.