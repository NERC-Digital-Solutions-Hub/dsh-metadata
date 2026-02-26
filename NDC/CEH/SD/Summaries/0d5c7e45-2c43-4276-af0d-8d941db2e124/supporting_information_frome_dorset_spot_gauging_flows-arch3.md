# River Frome Dorset spot gauging flows

- What this dataset is: A dataset of spot gauged river flows (m3 s-1) at multiple sites along the River Frome, Dorset, UK, collected in 2022 to support hydrodynamic modelling of nutrient fate and transport.

## Where and when data were collected

- Location: River Frome in West Dorset, a chalk stream; monitoring spanned the lower reach between Environment Agency gauging stations at Dorchester and East Stoke. Included major tributaries: South Winterbourne, Tadnoll Brook, and River Win.
- Coverage: 19 river channels across 11 river cross-sections; some cross-sections required multiple channels due to braided sections.
- Spatial layout: Cross-sections spaced approximately 3 km apart; site locations chosen by accessibility and suitability for flow measurement. All sites have British national grid references (NGRs) provided.
- Timeframe: Measurements taken on multiple flow accretion survey days between 12/04/2022 and 05/11/2022, with as many sites measured as possible each day, from upstream to downstream.
- Completeness: Not all sites monitored on every survey day due to time or weather constraints; some dates missing for certain sites.

## How measurements were collected

- Method: River channel divided into at least 10 transects (5–10 for small streams <3 m wide). Depth and flow velocity recorded at each vertical transect; velocity measured at 40% river depth.
- Calculations: Cross-sectional area per transect = transect width × average depth of the two adjacent transects; discharge per transect = cross-sectional area × average velocity of the two adjacent transects. Total discharge is the sum across all transects.
- Instruments: Valeport current meters (models 001 & 002) and a wading set; model 002 impeller used primarily for shallow sections.
- Data capture: On each survey day, all feasible sites recorded in upstream-to-downstream order; typically a single recording per site per survey (no replication).
- Data handling: Measurements entered into a bespoke spreadsheet to convert impeller revolutions to flow velocity (m/s) according to the impeller model; dataset details and site descriptions provided in associated materials (e.g., Table 1).

## Why the data were collected

- Purpose: To obtain spot gauged river flows to analyse flow accretion along the River Frome reach and to support the development of a hydrodynamic model for nutrient fate and transport.

## Who collected and checked the data

- Primary collector: Thomas Homan (PhD candidate, University of Bath).
- Supervisor: Prof. Jan Hofman (University of Bath).
- Data collator/checker: Thomas Homan.
- Equipment lender: Wessex Water Ltd.

## Data structure and file details

- File format: A single CSV file named River_Frome_Dorset_spot_gauging_flows.
- Columns: Site, Description, NGR, Date, Start_time, Flow, Impeller.
  - Site: Monitoring site name.
  - Description: Brief site location description (e.g., adjacent to road bridge).
  - NGR: River cross-section site coordinates.
  - Date: Measurement date.
  - Start_time: Start time of measurement.
  - Flow: Derived total discharge for the site (m3 s-1).
  - Impeller: Flow meter model used (BMF001 or BMF002).

## Quality, caveats, and cross-references

- Quality control: Not explicitly detailed (N/A).
- Data notes:
  - Flows were generally very low during the monitoring period due to an unusually hot, dry summer; groundwater levels also at record lows.
  - The Pallington Lakes measurement on 09/05/22 may be underestimated when using impeller BMF001, suggesting potential under-reading in shallow sections with this model.
  - Environment Agency gauging station data are available for cross-reference on the study dates at Loudsmill (Dorchester area), Stinsford, and East Stoke stations.
- Miscellaneous: Some monitoring sites are on private land requiring permission; exact site details and cross-section mappings are provided in accompanying tables (e.g., Table 1).