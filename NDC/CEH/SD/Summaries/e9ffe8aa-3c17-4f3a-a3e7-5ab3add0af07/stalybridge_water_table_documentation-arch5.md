# Stalybridge Water Table 2019-2022

## Overview
- Dataset of depth to water table from peat surface across ten experimental microcatchments (A–J) on Stalybridge Moor, a UK upland peatland.
- Timeframe: 2019–2022, covering pre- and post-gully blocking in six microcatchments; four microcatchments served as unrestored controls.
- In each microcatchment, two dipwell clusters (near gully edge and far from gully edge) with five dipwells per cluster.
- Measurements collected when field campaigns allowed, mainly monthly during winter (October–February); pandemic lockdowns caused deviations, leading to some summer/autumn measurements.
- Data collected and managed within the Protect-NFM project; linked to a BACI experimental design to assess gully restoration effects.

## Experimental design and sampling regime
- Experimental design: Before-After-Control-Intervention (BACI) approach.
- Controls: Microcatchments A, D, G, J remained unrestored throughout.
- Treatments: Microcatchments B–I with various dam installations (e.g., cobblestone, peat, piped-peat, timber dams) to modify gully flows.
- Intervention timing: Gully blocking conducted 16–25 March 2020; post-intervention data recorded from April 2020 onward.
- Dam design changes during the post-restoration period:
  - Microcatchment E: piped-peat dams initially with open orifices; from 22/02/2021 all piped-peat dams capped at 64 mm open diameter.
  - Microcatchment I: timber dam slots reduced in steps (25/03/2020; 27/01/2021; 29/03/2021).
- Pre-intervention period: May 2019–March 2020.
- Data gaps and constraints: site access restrictions and COVID-19 affected frequency; some measurements were opportunistic in summer/autumn; site decommission completed by 2022-02-25.

## Collection, generation, and transformation methods
- Dipwells: 1 m PVC tubes with 10 mm holes drilled at ~100 mm intervals; base sealed; dipwells inserted into peat with 100–150 mm protruding above the surface.
- Clusters: each with five dipwells placed on a 2×2 m grid; peat anchor used as vertical datum to monitor protrusion changes.
- Location within catchments: one cluster near the gully edge (2 m from edge) and one cluster far from the edge (>10 m).
- Depth to water table measurement: insert small tube into dipwell and blow until bubbles are heard; depth to water table is the tube depth minus the dipwell’s protrusion height.
- Data gaps: “nd” recorded where dipwells could not be located (snow/vegetation) or removed during decommissioning.
- Data structure: CSV file; rows for dipwells; columns for observation dates; dipwell naming convention: [site]_[microcatchment]_[cluster type: n/f]_[dipwell number] (e.g., ST_C_N_5).
- Measurement units: depth to water table from peat surface in millimetres (mm); negative values indicate water table height above peat surface.
- Calibration: dipwell protrusion height used to convert measurements to depth from peat surface.

## Data structure and accessibility
- Data provided as a single CSV containing all dipwells with dates as subsequent columns.
- First column: dipwell identifier; subsequent columns: dates of observation.
- Dipwell naming and cluster types clearly indicate proximity to gully edge (near = n, far = f).

## Location referencing and equipment
- UK grid references provided for each dipwell cluster, enabling precise geolocation.
- Field equipment: measuring tape and a 1 m blow-tube for depth measurements.

## Quality control, limitations, and caveats
- Quality control measures include a vertical datum (peat anchor) to monitor potential dipwell protrusion changes and to ensure consistent depth-to-water calculations.
- Potential data quality issues:
  - Incomplete data due to snow/vegetation or dipwell removal.
  - Pandemic-related disruptions leading to irregular sampling frequencies.
  - Post-restoration changes to dam designs may introduce non-uniform measurement contexts across microcatchments.
- Analytical methods: not applicable beyond measurement and conversion to depth from peat surface; no advanced processing described.

## References and provenance
- Primary reference: Shuttleworth, E.L. et al. (2019) Restortion of blanket peat moorland delays stormflow from hillslopes and reduces peak discharge.
- Project context: Protect-NFM, NERC grant NE/R004560/1 (Optimising NFM in headwater catchments to protect downstream communities).

## Data stewardship considerations
- Explicit BACI design with multiple controls and treatment microcatchments supports attribution of hydrological changes to restoration actions.
- Detailed metadata on dam types, installation dates, and post-restoration modifications supports reproducibility and secondary analyses.
- Clear data structure and naming conventions facilitate discoverability and reuse by researchers and data users.