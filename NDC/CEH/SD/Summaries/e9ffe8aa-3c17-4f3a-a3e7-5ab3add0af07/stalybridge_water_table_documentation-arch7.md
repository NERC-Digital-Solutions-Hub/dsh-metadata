# Stalybridge Water Table 2019-2022

- Dataset of depth to water table measurements from ten experimental microcatchments (A–J) on Stalybridge Moor, upland UK peatland.
- Each microcatchment contains two dipwell clusters (near gully edge and far from gully edge), with five dipwells per cluster (total 100 dipwells).
- Timeframe: 2019–2022, spanning pre- and post-gully blocking; measurements concentrated Oct–Feb due to winter campaigns, with summer/autumn measurements included because of COVID-related disruptions.
- Fieldwork was conducted under the Protect-NFM project; data collection and processing involved field technicians and researchers.

## Experimental design

- BACI (Before-After-Control-Intervention) design.
- Controls: microcatchments A, D, G, J (no gully blocking).
- Treatments: microcatchments B–I with various dam deployments (e.g., cobblestone, peat, piped-peat, timber dams).
- Intervention timing: gully blocking conducted 16–25 March 2020.
- Post-intervention design changes: adjustments to dam configurations during 2020–2021 (e.g., piped-peat dam orifice reductions/capping; timber dam slot modifications).

## Collection, generation, or transformation methods

- Dipwells: 1 m PVC pipes with 10 mm holes at ~100 mm intervals; 100–150 mm protruding above peat.
- Clusters: random 2×2 m grid; each cluster has a peat anchor as a vertical datum.
- Locations: one near-gully edge (2 m from edge) and one far from edge (>10 m) per catchment.
- Measurement: depth to water table by blowing air through a small tube in the dipwell; subtract protrusion height to obtain depth from peat surface.
- Data gaps: marked as 'nd' when dipwells cannot be located (snow, vegetation) or removed during decommissioning.
- Coordinates: dipwell locations provided as UK grid references for each dipwell cluster.

## Nature and units of recorded values

- Recorded values: depth to water table from the peat surface, in millimetres (mm).
- Negative values indicate water table above the peat surface.
- Data entries 'nd' denote no data.

## Data structure and naming

- Format: CSV; rows are individual dipwells; columns after the first are observation dates.
- Dipwell naming convention: [site]_[microcatchment]_[cluster type]_[dipwell number] (e.g., ST_C_N_5 for microcatchment C near-gully edge, dipwell 5).
- Columns after the dipwell identifier: dates of observations with depth-to-water-table (mm).

## Quality control

- Presence of a peat anchor and vertical datum to monitor dipwell protrusion height changes.
- Documentation of data gaps due to field conditions and site decommissioning.

## Geographic and temporal scope

- Locations: dipwell coordinates provided for each cluster (UK grid references).
- Temporal coverage: May 2019–February 2022 (pre- vs post-intervention periods; post-March 2020 following gully blocking).

## Data notes and caveats

- Some measurements were opportunistic or limited by access constraints during winter or lockdowns.
- Post-restoration changes to dam designs may affect comparability across periods and microcatchments.
- Data are suitable for GIS-based spatial-temporal analyses of water-table depth in relation to gully-blocking interventions and dam configurations.

## References

- Shuttleworth, E.L. et al. (2019) Restor. of blanket peat moorland delays stormflow... Journal of Hydrology X, 2, 100006. DOI: https://doi.org/10.1016/j.hydroa.2018.100006