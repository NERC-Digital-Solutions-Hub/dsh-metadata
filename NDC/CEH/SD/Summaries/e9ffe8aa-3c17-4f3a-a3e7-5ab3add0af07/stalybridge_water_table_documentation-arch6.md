# Stalybridge Water Table 2019-2022

## Overview
- Depth to water table measurements from ten experimental microcatchments (0.43–9 hectares) on Stalybridge Moor, an upland peatland in the UK.
- Timeframe: 2019–2022, covering pre- and post-gully blocking periods.
- Experimental setup: four unrestored control microcatchments (A, D, G, J) and six intervened microcatchments (B, C, E, F, H, I) with gully-blocking implemented in March 2020.
- Within each microcatchment, two dipwell clusters (near-gully edge and far from gully edge), each cluster containing five dipwells.

## Experimental design
- BACI design (Before-After-Control-Intervention) to assess effects of gully blocking on water table depth.
- Microcatchments A, D, G, J serve as controls; B, C, E, F, H, I receive interventions (various dam/delivery structures).
- Pre-intervention period: May 2019–March 2020.
- Gully blocking occurred 16–25 March 2020; post-intervention measurements follow.
- Dam design changes during post-restoration period:
  - E: piped-peat dams initially open pipes (150 mm diameter) with a unique lower dam; on 22 Feb 2021 all piped-peat dams capped to 64 mm.
  - I: timber dams with slots 150 × 40 mm; 27 Jan 2021 lower dam slot constricted to 50 × 40 mm; 29 Mar 2021 remaining slots reduced to 50 × 40 mm.

## Data collection and processing
- Dipwells: 1 m PVC pipes with 10 mm holes drilled at ~100 mm intervals; base sealed; dipwells protrude 100–150 mm above peat surface.
- Clusters: random positions within 2 × 2 m; peat anchor used as vertical datum to monitor dipwell protrusion changes.
- Measurement method: depth to water table from peat surface measured by inserting a tube into the dipwell, blowing bubbles, and reading the depth; dipwell protrusion height used to convert to depth from peat surface.
- Data integrity: some dipwells unlocatable due to snow/vegetation or removed during decommission; ‘nd’ denotes no data.

## Data structure and content
- Data stored as a single CSV with the entire depth-to-water-table record for all dipwells.
- Rows: individual dipwells; Columns: dates of observation (after the first column listing the dipwell).
- Dipwell naming convention: [site]_[microcatchment]_[cluster type]_[dipwell number], where cluster type is 'n' for near-gully edge and 'f' for far from gully edge.
  - Example: ST_C_N_5 is the 5th dipwell in the near-gully edge cluster in microcatchment C at Stalybridge.
- Units: depth to water table from peat surface in millimetres (mm); negative values indicate water table above peat surface.
- Contacts/locations: UK grid references provided for each dipwell cluster.
- Data notes: 'nd' used where data are missing due to unlocatability or removal.

## Fieldwork schedule and access
- Winter campaigns targeted monthly measurements October–February.
- COVID-19 and access restrictions led to opportunistic measurements during summer/autumn.
- Site decommissioning occurred by 2022-02-25, so some dipwells were removed earlier than others.

## Data quality and limitations
- Vertical datum (peat anchor) helps monitor dipwell protrusion changes to ensure data consistency.
- Potential data gaps due to weather, vegetation, snow, and site decommissioning.
- Post-intervention design changes (dams) may introduce additional variability in water-table depth readings.

## Units and interpretation
- Depth-to-water-table values are in mm from the peat surface; negative values indicate a water table above the peat surface.
- 'nd' entries indicate missing data.

## References
- Shuttleworth, E.L. et al. (2019) Restorations of blanket peat moorland and hydrological responses. Journal of Hydrology X, 2, 100006. DOI: https://doi.org/10.1016/j.hydroa.2018.100006

## Related data use and potential products
- Suitable for BACI analysis of gully-blocking effects on water-table dynamics.
- Can be combined with other Protect-NFM datasets to explore hydrological responses and to develop data products (dashboards, summaries) for end users.