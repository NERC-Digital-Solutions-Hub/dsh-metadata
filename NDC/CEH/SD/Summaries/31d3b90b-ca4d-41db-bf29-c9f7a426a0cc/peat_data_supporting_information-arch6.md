# West Halladale wildfire peat cores - data collection, measurement and analysis methods

- 34 peat cores were collected across the West Halladale wildfire footprint (Flow Country peatlands) to assess burn severity, drainage status, and peat properties.
- Sampling targeted a severity x drainage matrix (low, medium, high; drained vs undrained/near-natural), with plots selected from a severity map and distributed across the footprint.
- Field work occurred in late February to mid-March 2020, with five field visits to collect cores; COVID-19 caused some delays with laboratory analysis for ten cores.

## Study area and sampling design

- Location: Flow Country peatlands, Caithness and Sutherland, Scotland; wildfire footprint includes West Halladale SSSI and Forsinard Flows NNR.
- Burn severity mapping used a NatureScot severity map to define plots: low, medium, high severity across drained and near-natural bogland.
- Plot selection: 10–15 plots per severity x drainage combination, coded by severity (H, M, L) and drainage (N for near-natural/undrained); total of 34 cores collected after field feasibility constraints (e.g., slope, peat depth, land management access).
- Core depth targeted: 40–50 cm; cores were intended to be contiguous 5 cm sub-sections for lab analyses.

## Field data collection and metadata

- Core identification: CODENAME based on severity, drainage, and a numeric index (e.g., H1, M4, L7, etc.).
- In-field data collected per core: core depth, coordinates, elevation, slope exposure, surrounding vegetation; field notes and photographs captured.
- Field coordinates recorded with GPS; core locations and depths logged in Peat_core_coordinate.csv.
- Core collection method: Russian corer, PVC half-pipe liners, saran wrap for transport; labeling ensured traceability between field and laboratory samples.

## Sample storage, handling, and timing

- Cores transported to cold storage to prevent deterioration; most analyses conducted within a few days, with ten cores stored for later analysis during late July 2020 due to Covid restrictions.
- Post-collection handling included documentation of date, observer, severity, codename, core depth, coordinates, and elevation; samples prepared for laboratory subsampling.

## Datasets and data structure

- Dataset: Peat_core_coordinate.csv
  - COREID: unique identifier (severity letter + number; e.g., H1, M12, N-M, etc.)
  - Depth_cm: core depth (40–50 cm)
  - Lat_OSGB, Long_OSGB: geographic coordinates in OSGB
  - Grid_Reference: British Grid Reference
  - Alt_masl: altitude above sea level
  - Exposure: slope aspect/angle
  - Vegetation: vegetation description around the sampling location

- Dataset: Peat_core_data.csv (per 5 cm sub-section)
  - COREID: core identifier
  - DEPTH_cm: sub-section depth (0–50 cm, 5 cm increments)
  - SEVERITY: LOW, MEDIUM, HIGH (from map and field)
  - TYPE: DRAINED or UNDRAINED
  - VOL: sample volume (cm3)
  - WET_PEAT, DRY_PEAT: wet and dry weights (g)
  - BD: Bulk Density (g cm-3)
  - MOIST%: moisture percentage
  - vonPOST: peat decomposition (1–10)
  - WET_PEAT10, DRY_PEAT10: weights for LOI at 10 g peat
  - ASHg: ash weight (g)
  - OM%: organic matter percentage
  - ASH%: ash percentage
  - OC%: organic carbon percentage
  - OM% and OC% derived/linked to LOI results; OC% ≈ OM%/2 (Beilman et al., 2009)

## Analytical methods and data generation

- Bulk density and moisture
  - Wet weight measured; volume determined by water displacement; cores dried at 105°C; BD calculated as dry weight per volume; moisture content calculated from wet/dry weights.
- Organic matter and carbon
  - Organic matter (OM) determined by loss-on-ignition (LOI) at 550°C for 4 h; OM% = LOI dry weight / (105°C dry weight) × 100.
  - Ash content (ASH%) from ashed residue relative to dry weight; OC% derived as OM%/2 (assuming 50% organic carbon in organic matter).
- von Post decomposition index
  - Humification tier (H1–H9, and additional H1o) assessed via a tactile peat-squeezing test to categorize decomposition stage.
- Analytical workflow for laboratory analyses
  - 5 cm sub-sections cut and photographed; samples weighed, dried, and ashed according to standard protocols (Beilman et al.; Heiri et al.; Chambers et al.; Ratcliffe et al.).
  - Wet weight (mw) and dry weight (md) used to compute BD and moisture; LOI (550°C) used to determine OM% and ash; OC% derived via OM%/2.
- Equipment and calibration
  - Field: GPS for coordinates; Russian corer; PVC tubes; measuring tape; camera; field notebooks.
  - Laboratory: balances (five- and three-decimal); 100 mL cylinder for volume via water displacement; oven (105°C) and muffle furnace (550°C) for LOI; desiccator; crucibles; Milli-Q water purification system.
  - Balances calibrated per manufacturer guidelines with standard weights.

## Data quality control and cleaning

- All data collected and entered into centralized folders; quality checks performed on field notes, coordinates, depths, and lab measurements.
- Data integrity: sub-samples with weighing inconsistencies (e.g., dry weight exceeding wet weight) were removed to prevent erroneous calculations.
- Documentation includes step-by-step calculation formulas for BD, moisture, OM, ash, OC, and von Post classifications; references provided for methods.

## Data use and potential products

- Data can be combined with other peat carbon datasets to assess spatial variability in carbon stock, decomposition, and soil properties across burn severity and drainage regimes.
- Potential data products:
  - Dashboards enabling experts and non-experts to filter by severity, drainage, and depth to visualize BD, MC, OM, OC, and decomposition trends.
  - Visualization of core property changes with depth by plot and by severity/drainage category.
  - Data dictionaries and provenance trails to support reproducibility and reuse.
- Use cases include peat carbon balance studies, post-fire recovery analyses, and policy-relevant reporting for land management and restoration.

## Limitations and challenges

- Field sampling constraints led to fewer plots per severity/drainage combination than initially planned; some plots were not suitable due to terrain or land management.
- COVID-19 introduced delays in analysis for several cores, affecting the timeline of data availability.
- Patchy data across combinations and missing sub-samples due to indentified weighing errors were excluded from final calculations.

## References

- Beilman, D.W., MacDonald, G.M., Smith, L.C. & Reimer, P.J. (2009) Carbon accumulation in peatlands of West Siberia over the last 2000 years.
- Chambers, F.M., Beilman, D.W. & Yu, Z. (2011). Methods for determining peat humification and quantifying peat bulk density, organic matter and carbon content.
- Ekono, I. (1981). Energy use of peat.
- Heiri, O., Lotter, A.F. & Lemcke, G. (2001). LOI as method for estimating organic and carbonate content.
- Melling, L. et al. (2006). Soils of Loagan Bunut National Park, etc.
- Ratcliffe, J.L. et al. (2018a, 2018b). Holocene carbon accumulation and contemporary carbon fluxes studies.