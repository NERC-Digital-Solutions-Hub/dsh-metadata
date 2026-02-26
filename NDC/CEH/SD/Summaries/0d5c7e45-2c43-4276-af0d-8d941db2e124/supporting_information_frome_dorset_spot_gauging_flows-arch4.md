# River Frome Dorset spot gauging flows dataset (2022)

## What is in this dataset
- A dataset of spot gauged river flows (m³/s) at multiple sites along the River Frome, Dorset, UK, collected in 2022.

## Where and when
- Location: lower River Frome between Environment Agency gauging stations at Dorchester and East Stoke; includes major tributaries South Winterbourne, Tadnoll Brook, and River Win. 19 river channels across 11 cross-sections; NGRs provided for all monitoring sites.
- Spatial layout: cross-sections spaced approximately 3 km apart; multiple channels measured per cross-section due to braided river reach.
- Time: measurements taken on flow accretion survey days between 12 April 2022 and 5 November 2022; surveys progressed upstream to downstream; not all sites measured on every date.

## How measurements were conducted
- Method: each river channel divided into at least 10 transects (5–10 transects for small streams); depth and flow velocity recorded at each transect; velocity measured at 40% above the riverbed.
- Calculations: cross-sectional area per transect = transect width × average depth of adjacent transects; discharge per transect = cross-sectional area × average velocity of adjacent transects; total discharge is the sum of all transect discharges.
- Instrumentation: Valeport current meter (models 001 & 002); impeller model used typically 002 (more suitable for shallow sections).
- Data capture: one measurement per site per day (no replicates).
- Data handling: measurements entered into a bespoke spreadsheet converting impeller revolutions to velocity (m/s) based on impeller model.

## Why this dataset was collected
- Part of a PhD project to hydrodynamically model nutrient fate and transport in the River Frome; spot gauging supports analysis of flow accretion along the reach and model development.

## Who collected and managed the data
- Collectors: Thomas Homan (PhD candidate, University of Bath) and supervisor Prof. Jan Hofman.
- Data management: Thomas collated and checked the data; monitoring equipment lent by Wessex Water.

## Data quality and completeness
- Completeness: on many survey days not all sites could be monitored due to time or weather; some dates are missing per site.
- Quality control: described as N/A in the dataset; no explicit quality control steps documented.
- Miscellaneous notes: very low flows during a hot, dry summer; groundwater levels at observation boreholes at record lows.
- Reference data: Environment Agency gauging station data are available for the same dates at Louds Mill, Stinsford, and East Stoke for cross-context comparison.

## Data structure and contents
- File: River_Frome_Dorset_spot_gauging_flows.csv
- Columns: Site, Description, NGR, Date, Start_time, Flow, Impeller
- Flow units: m³/s
- Impeller values: BMF001 or BMF002
- Descriptions: site locations (e.g., adjacent to road bridge); NGR provides the coordinate for mapping cross-sections.

## Additional notes for users
- Data can be cross-validated with EA gauging stations along the reach.
- The survey design aimed for cross-sections ~3 km apart; some sections required multiple channels to represent total cross-section flow.