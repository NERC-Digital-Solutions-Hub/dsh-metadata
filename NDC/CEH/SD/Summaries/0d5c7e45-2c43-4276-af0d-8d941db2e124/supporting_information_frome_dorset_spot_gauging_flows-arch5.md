# What? This is a dataset of spot gauged river flows (m 3 s -1 ) at multiple sites along the River Frome, Dorset, UK, conducted during the year 2022.

- What is included: A dataset of spot gauged river flows (discharge, m3 s-1) measured at 19 river channels across 11 cross-sections along the River Frome in 2022.
- Purpose: Data were collected to support hydrodynamic modelling of nutrient fate and transport in the River Frome as part of a PhD project.
- Geographic scope: River Frome, a chalk stream in West Dorset, between Environment Agency gauging stations at Dorchester and East Stoke; includes major tributaries (South Winterbourne, Tadnoll Brook, River Win). NGR coordinates provided for each monitoring site.
- Access and governance: Some sites on private land requiring permission; monitoring equipment lent by Wessex Water.
- Data structure: One CSV file (River_Frome_Dorset_spot_gauging_flows) with seven columns: Site, Description, NGR, Date, Start_time, Flow, Impeller. Flow in m3 s-1; Impeller recorded as BMF001 or BMF002.
- Temporal coverage: Measurements taken on multiple flow accretion survey days from 12 Apr 2022 to 5 Nov 2022; on each day, as many sites as feasible were measured upstream to downstream. Some dates missing for certain sites due to time or weather.
- Sampling design: Each survey divides channels into at least 10 transects (5–10 for small streams); depth and flow velocity recorded at each transect. Velocity measured at 40% depth above the riverbed; cross-sectional area per transect calculated from transect width and average depth of adjacent transects; discharge per transect calculated and summed to give total discharge.
- Equipment and method details: Valeport current meters (models 001 & 002) with impeller readings (BMF001/BMF002); for small streams, 5–10 transects; data processed via a bespoke spreadsheet converting revolutions to velocity and deriving discharge.
- Survey scope per day: Only one measurement per site per survey day (no replicates).
- Data completeness and quality notes:
  - Generally low flows due to one of the hottest and driest summers on record; groundwater levels at some boreholes were at historic lows.
  - Pallington Lakes flow on 09/05/22 suspected to be underestimated using BMF001 in shallower sections.
  - Environment Agency gauging station data (Loudsmill, Stinsford, East Stoke) available for cross-checking upstream/downstream flows on survey dates.
- Metadata and context: The dataset includes site descriptions, precise NGRs, dates, start times, and instrument used to support discoverability and reuse; cross-referencing with EA data recommended for broader hydrological context.