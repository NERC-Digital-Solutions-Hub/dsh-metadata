# River Frome Dorset spot gauging flows 2022

## Overview
- Dataset of spot gauged river flows (m^3 s^-1) at multiple sites along the River Frome, Dorset, UK, conducted in 2022.
- 19 river channels measured across 11 cross-sections; some cross-sections required multiple channels due to river braiding.
- Purpose: support hydrodynamic modeling of nutrient fate and transport in the River Frome; informs flow accretion along the reach.

## Location (Where)
- River Frome in West Dorset, between Environment Agency gauging stations near Dorchester and East Stoke (lower Frome reach).
- Includes major tributaries: South Winterbourne, Tadnoll Brook, River Win.
- 11 river cross-sections with 19 monitored channels; NGRs provided for each channel.
- Sections designed to be ~3 km apart; site locations chosen for accessibility and suitable measuring conditions (some on private land).

## Temporal Coverage (When)
- Measurements taken on multiple flow accretion survey days between 12/04/2022 and 05/11/2022.
- On each survey day, as many sites as feasible were measured upstream to downstream.
- Each site recorded once per day (no replicates).

## Methodology (How)
- River channel divided into at least 10 transects (5–10 for small streams); depth and flow velocity recorded at each transect.
- Flow velocity measured at 40% depth above the riverbed; cross-sectional area per transect = width × average depth of adjacent transects; discharge per transect = cross-sectional area × average velocity of adjacent transects; total discharge = sum of transects.
- Instrumentation: Valeport current meters (models 001 & 002; impeller model 002 preferred for shallow streams).
- Data recorded as revolutions on a monitor, converted to velocity via a bespoke spreadsheet.
- Notes indicate some data may underestimate flows when shallower sections are not adequately captured.

## Data Structure (Data Format)
- Single CSV file: River_Frome_Dorset_spot_gauging_flows.csv
- Columns: Site, Description, NGR, Date, Start_time, Flow, Impeller
  - Site: monitoring site name
  - Description: brief site location
  - NGR: British National Grid Reference
  - Date: measurement date
  - Start_time: measurement start time
  - Flow: total discharge for the stream channel (m^3 s^-1)
  - Impeller: flow meter model used (BMF001 or BMF002)

## Quality and Limitations (Quality)
- Quality control: not formally documented (N/A).
- Notable caveats:
  - Pallington Lakes discharge on 09/05/22 suspected to be underestimated due to BMF001 impeller limitations in shallow sections.
  - Generally low flows during the measurement period due to a very hot, dry summer.

## Completeness (Completeness)
- Not all sites surveyed on every day due to time and weather constraints; some dates are missing for certain sites.

## Related Data and Context (Notes)
- Environment Agency gauging stations available for reference: Louds Mill (Dorchester area), Stinsford, East Stoke.
- Data can be used in conjunction with EA gauge data to compare upstream/downstream conditions along the study reach.