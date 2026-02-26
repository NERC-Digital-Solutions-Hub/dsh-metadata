# Stalybridge Water Table 2019-2022

## Overview
- Dataset of depth to water table measurements from ten experimental microcatchments on Stalybridge Moor, upland peatland, UK.
- Covers 2019–2022, spanning pre- and post-gully blocking, with a BACI design including unrestored controls and multiple interventions.
- Data collected by field technicians and researchers within the Protect-NFM project; depth measured from peat surface using dipwells.

## Data scope and content
- Microcatchments: A–J (named west to east). Each has two dipwell clusters (near-gull edge and far from edge), with 5 dipwells per cluster.
- Measurements: depth to water table from peat surface, in millimetres (mm). Negative values indicate water table above peat surface; 'nd' denotes no data.
- Locations: each dipwell cluster has UK grid references; data organized in a single CSV with dipwells as rows and observation dates as columns.
- Dipwell naming: [site]_[microcatchment]_[cluster type]_[dipwell number], e.g., ST_C_N_5.

## Experimental design and timeline
- BACI design:
  - Controls (unrestored): A, D, G, J.
  - Interventions (gully blocks or dam installations): B, C, E, F, H, I.
- Interventions:
  - B: 22 cobblestone dams.
  - C: 7 cobblestone + 13 peat dams.
  - E: 10 piped-peat dams.
  - F: 6 standard peat dams.
  - H: 6 standard peat dams.
  - I: 20 timber dams.
- Timeline:
  - Pre-intervention: May 2019–Mar 2020.
  - Gully blocking: 16–25 Mar 2020.
  - Post-intervention: Apr 2020 onward; dam designs updated in E (opening/closing pipes) and I (slot adjustments) at specified dates.
  - Field sampling primarily winter (Oct–Feb) with occasional summer/autumn measurements due to Covid restrictions.
  - Decommissioning and dipwell removal culminated by 2022-02-25.

## Data collection methods and instrumentation
- Dipwells: 1 m PVC tubes with 10 mm holes at ~100 mm intervals, base sealed; 100–150 mm protruding above peat.
- Clusters: 5 dipwells per cluster, placed randomly within a 2×2 m grid; near-edge cluster ~2 m from gully edge; far-edge cluster >10 m from edge.
- Datum: peat anchors and a metal rod to monitor changes in dipwell protrusion height.
- Measurement technique: insert a small tube into dipwell and blow air to hear bubbles; depth recorded, adjusted for protrusion height.
- Data gaps: dipwells occasionally unlocatable due to snow/vegetation; some dipwells removed during site decommission.

## Data structure and metadata
- Data format: CSV file containing the full depth-to-water-table record for all dipwells.
- Structure: rows represent individual dipwells; columns represent observation dates.
- Dipwell identifier: dipwell column (e.g., ST_C_N_5); subsequent date columns contain depth-to-water-table values (mm).
- Units: depth to water table from peat surface in millimetres (mm); negative values indicate higher water table than surface.
- Data qualifiers: 'nd' used for no data.

## Quality control and governance
- Vertical datum controls via peat anchors to ensure measurement consistency across time.
- Field and processing oversight by researchers within the Protect-NFM project.
- Documentation includes detailed description of sampling regime, intervention changes, and data handling (e.g., 'nd' entries).

## Limitations and caveats
- Covid-19 disruptions limited sampling cadence and forced inclusion of opportunistic measurements in non-winter months.
- Post-restoration period saw design changes to dam configurations, potentially affecting comparability across years.
- Some dipwells removed during decommissioning; final dates may have missing values.
- Data reflect site-specific conditions and gully-blocking interventions; generalization should consider local peatland dynamics.

## Reference and provenance
- Shuttleworth, E.L. et al. (2019). Restoration of blanket peat moorland delays stormflow from hillslopes and reduces peak discharge. Journal of Hydrology X, 2, 100006. DOI: https://doi.org/10.1016/j.hydroa.2018.100006.
- Project: Protect-NFM; NERC grant NE/R004560/1. Author: Adam Johnston.