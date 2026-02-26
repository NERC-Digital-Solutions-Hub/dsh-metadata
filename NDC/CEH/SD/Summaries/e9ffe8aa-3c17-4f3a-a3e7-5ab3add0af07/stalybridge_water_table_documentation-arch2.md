# Stalybridge Water Table 2019-2022

- Purpose: Dataset of depth to water table (DTWT) measurements from ten experimental microcatchments on Stalybridge Moor (upland peatland) to support evaluation of natural flood management/restoration efforts under Protect-NFM.
- Scope: 2019–2022, capturing pre- and post-gully blocking conditions with a BACI (Before-After-Control-Intervention) framework.

## Experimental design and timeline

- Microcatchments labeled A–J from west to east; four are unrestored controls (A, D, G, J).
- Interventions: gully blocking undertaken 16–25 March 2020 in targeted microcatchments.
- Post-intervention changes: dam design adjustments occurred in several microcatchments (e.g., microcatchment E and microcatchment I) with changes in open-portion sizes and eventual capping or slot reductions.
- Pre-intervention period: May 2019–March 2020. Post-intervention period: March 2020 onward.

## Data collection and processing

- Measurement method: DTWT from peat surface using blow-tube method in 1 m PVC dipwells (10 mm holes at ~100 mm intervals; 5 dipwells per cluster).
- Clusters per catchment: near-gully edge (2 m from edge) and far from edge (>10 m).
- Field cadence: aimed for monthly measurements in winter months (Oct–Feb); COVID-19 and access constraints led to irregular winter coverage and opportunistic summer/autumn measurements.
- Datum: peat surface DTWT corrected by subtracting dipwell protrusion height (using peat anchors and a vertical datum).
- Data status: missing data marked as nd (due to dipwell concealment, removal, or decommission).

## Data structure and units

- Format: CSV with one row per dipwell; columns after the first are observation dates.
- Dipwell naming: [site]_[microcatchment]_[cluster type]_[dipwell number]
  - Example: ST_C_N_5 (Stalybridge, microcatchment C, near-gully edge cluster, dipwell 5)
  - Cluster type: n = near, f = far
- Variable: depth to water table from peat surface, in millimetres (mm).
- Negative values indicate a water table higher than the peat surface.
- Data entries: numeric values or nd for no data.

## Location, sampling, and equipment

- Dipwells constructed from 1 m PVC with 10 mm holes; base sealed; protruding 100–150 mm above surface.
- Each dipwell cluster includes a peat anchor (vertical datum) and 5 dipwells arranged in a 2×2 m grid.
- Locations provided as UK grid references for each dipwell cluster (near and far positions per microcatchment).

## Quality control and data provenance

- Use of peat anchors and vertical datums to monitor changes in dipwell protrusion height (data integrity across time).
- Documentation covers equipment, calibration steps (protrusion correction), and data transformation steps (from blow-tube depth to DTWT from peat surface).

## Post-restoration interventions by microcatchment

- E (pip ed-peat dams): from 25/03/2020–22/02/2021, open pipes with 150 mm diameter; then capped to 64 mm open orifice from 22/02/2021 onward.
- I (timber dams): from 25/03/2020–27/01/2021, initial slot 150×40 mm; lower dam reduced to 50×40 mm on 27/01/2021; all remaining slots reduced to 50×40 mm by 29/03/2021.
- Other microcatchments involved different dam configurations (B, C, F, H) as part of the RESTORATION design.

## Temporal and data access considerations

- Winter-only regular measurements intended; pandemic and access limits caused gaps and opportunistic measurements in other seasons.
- Several dipwells removed during decommission, leading to final data gaps by 2022-02-25.

## Relevance for environmental monitoring

- Provides standardized, BACI-structured DTWT data across multiple microcatchments to assess peatland hydrology responses to restoration measures.
- Supports cross-dataset integration by using standardized dipwell naming, measurement methods, and a clear data structure suitable for trend, comparative, and policy-performance analyses.

## Reference

- Shuttleworth, E.L. et al. (2019) Restoration of blanket peat moorland delays stormflow from hillslopes and reduces peak discharge. Journal of Hydrology X, 2, p. 100006.