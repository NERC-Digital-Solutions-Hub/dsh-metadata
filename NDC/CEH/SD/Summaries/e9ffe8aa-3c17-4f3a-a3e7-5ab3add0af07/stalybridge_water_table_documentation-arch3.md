# Stalybridge Water Table 2019-2022

- Dataset of depth to water table from ten experimental microcatchments (0.4–3.9 ha) on Stalybridge Moor, upland peatland in the UK, collected 2019–2022 under the Protect-NFM project (NERC NE/R004560/1).
- BACI experimental design to assess the impact of gully blocking on soil water regime.
- Microcatchments A, D, G, and J served as unrestored controls; microcatchments B, C, E, F, H, and I received gully restoration interventions using various dam types.
- Each microcatchment contains two dipwell clusters (near gully edge and far from gully edge), with five dipwells per cluster (total of 100 dipwells).
- Measurements were intended to be monthly during the winter period (October–February); Covid-19 restrictions led to limited winter sampling and more opportunistic summer/autumn measurements. Site decommissioning in 2022 led to some dipwells being removed.

## Experimental design and sampling regime

- Design: Before-After-Control-Intervention (BACI) to evaluate effects of gully blocking on depth to water table.
- Timeline:
  - Pre-intervention: May 2019–March 2020.
  - Intervention: gully blocking conducted 16–25 March 2020.
  - Post-intervention: subsequent period with some modifications to dam designs.
- Dam and intervention details:
  - Microcatchments B, C, E, F, H, I received various dam configurations (cobblestone, peat dams, piped-peat dams, timber dams).
  - Post-restoration changes included adjustments to dam open-circuit diameters and slot widths, and, for some microcatchments, changes occurred in 2021.
- Data collection period affected by access constraints and pandemic; some measurements occurred in summer/autumn when winter sampling was limited.

## Collection, generation, and transformation methods

- Dipwells:
  - 1 m long PVC tubes with 10 mm holes drilled at ~100 mm intervals; base sealed; protruded 100–150 mm above peat surface.
  - Each cluster: five dipwells arranged in a 2×2 m grid; a peat anchor and vertical datum rod placed to monitor protrusion changes.
  - Clusters positioned near gully edge (2 m from edge) and far from edge (>10 m).
- Measurement protocol:
  - Depth to water table measured by blowing air through a small tube in the dipwell until bubbles are heard; depth to water table from the top of the dipwell is recorded, then corrected for dipwell protrusion to yield depth to water table from the peat surface.
  - Post-processing includes converting raw measurement to depth from peat surface.
- Data completeness:
  - Occasional missing data entries ('nd') when dipwells could not be located due to snow/vegetation or due to dipwell removal during decommissioning.
- Location data:
  - Each dipwell cluster is identified by UK grid references (provided for each cluster).

## Nature, units, and structure of recorded data

- Recorded variable: depth to water table from the peat surface (millimetres, mm).
- Negative values indicate a water table above the peat surface.
- Data are stored in a single CSV file; rows correspond to individual dipwells and columns to dates; first column is dipwell identifier.
- Dipwell naming convention example: ST_C_N_5 denotes microcatchment C, near-gully edge cluster, dipwell number 5.
- Date columns are labeled with observation dates; data values are integers (mm) or 'nd' for no data.

## Data quality, limitations, and governance

- Quality controls:
  - Each cluster includes a peat anchor and vertical datum to monitor protrusion changes.
  - Consistent measurement procedure using a blow-tube method.
- Limitations:
  - Covid-19 disruptions reduced winter sampling frequency.
  - Some dipwells were removed during decommissioning; data gaps ('nd') occur on final collection dates for removed dipwells.
  - Field conditions (snow/vegetation) occasionally impeded dipwell localization.
- Data processing notes:
  - Depth to water table is derived by adjusting measured dipwell depth with protrusion height of the dipwell.

## Data interpretation and references

- Dataset intended for assesssing hydrological responses to gully restoration in blanket peat moorland and to support broader analyses of restoration outcomes.
- Relevant methodological reference for BACI design: Shuttleworth, E.L. et al. (2019) Restor­ation of blanket peat moorland delays stormflow from hillslopes and reduces peak discharge.

## References

- Shuttleworth, E.L. et al. (2019). Restoration of blanket peat moorland delays stormflow from hillslopes and reduces peak discharge. Journal of Hydrology X, 2, 100006. https://doi.org/10.1016/j.hydroa.2018.100006