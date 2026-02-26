# Ammonia concentration and deposition data from a peatland nitrogen pollution experiment, Whim Bog, Scotland, UK, 2002-2022

## Overview
- Dataset of ammonia (NH3) concentration and dry deposition flux from the Whim Bog NH3 enhancement experiment (2002–2022).
- Site: Whim Moss ombrotrophic bog near Edinburgh (approx. 55.76566°N, -3.27155°W; altitude 316 m).
- Purpose: investigate effects of elevated atmospheric NH3 on vegetation, bryophytes, lichens, and soil; flux estimates derived from measured concentrations.

## Data collection and calculations (Methods)
- NH3 enhancement system releases NH3 only when wind direction (180–215°) aligns with monitoring quadrats and wind speeds exceed 2.5 m/s.
- NH3 concentrations measured with UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers; analyses conducted monthly from May 2002 to December 2022.
- Monitoring locations (lateral and vertical) were adjusted over time to meet study requirements.
- Dry deposition to vegetation estimated using a unidirectional resistance model, Rt = Ra + Rb + Rc, with Ra (aerodynamic), Rb (boundary-layer), and Rc (canopy) resistances; deposition flux Fχ(z) = χa / Rt.
- 15-minute NH3 concentrations during release periods derived from monthly averages; Rc calculated for day and night using χ-adjusted formulations with constants from Jones et al. 2007; during non-release periods Rc fixed at 20 s m−1.
- Deposition flux calculated for each 15-minute period and summed monthly.
- Complete methodological details linked to primary publications (e.g., Leith et al. 2004; Jones et al. 2007; Cape et al. 2008).

## Quality control and data structure
- Data QC: visual checks; removal of errors from meteorological instrument failure, sampler damage/loss, and power cuts; monthly NH3 concentrations below ambient removed to avoid negative flux values.
- Missing values occur when ALPHA sampler locations changed during a year.
- Data structure: 6-parameter dataset with 6296 measurements; NA entries indicate missing NH3 concentration (NH3_conc) or missing deposition flux (Dep_kg_ha).
- Format: CSV with columns:
  - Month (year-month)
  - ID (sample label): E/W (east/west of main transect), Con/Amb (Control/Ambient)
  - Distance (m): distance from NH3 source; negative = upwind, positive = downwind
  - Height (m): measurement height above ground
  - NH3_conc: 1 = µg m−3 (instantaneous); 2 = monthly average NH3 concentration
  - Dep_kg_ha: 1 = kg ha−1 month−1 (deposition flux); 2 = monthly total deposition

## Data governance, provenance and usage
- Funding: Natural Environment Research Council (NE/R016429/1) under UK-SCAPE National Capability.
- Documentation scope suitable for data sharing and reuse: explicit measurement methods, modeling approach, and unit conventions; cross-referenced to foundational publications for full reproducibility.
- Related references detail model parameters, deposition processes, and prior calibration/validation (e.g., Leith et al. 2004; Cape et al. 2008; Jones et al. 2007; Smith et al. 2000; Tang et al. 2001).

## Practical considerations for data stewards
- Clear, testable metadata: measurement heights, sampling duration, sampler IDs, orientation, and upwind/downwind semantics are well defined.
- Versioning and updates: sampler relocations over time indicate the need for careful versioning and site metadata to enable comparability across years.
- Data quality and provenance: explicit QC steps and rationale for data removal ensure trustworthy datasets and facilitate audit trails.
- Interoperability: model-based deposition calculations rely on established constants and prior studies; ensure future derivatives document reference datasets and parameter choices.

## Limitations and caveats
- Sampler position changes during the study period introduce potential spatial-temporal discontinuities.
- Monthly data gaps correspond to changes in sampler locations or instrument-related issues.
- Non-release periods employ fixed Rc and monthly-averaged Ra/Rb; concentration dependence is not applied during these periods.
- Missing NH3 concentration data (NH3_conc) or missing deposition flux (Dep_kg_ha) are marked as NA.

## References and further information
- Leith et al. 2004; Jones et al. 2007; Cape et al. 2008 (methodological foundations for deposition modeling and ambient/concentration-dependent deposition).
- Additional foundational methods on dry deposition processes and related atmospheric chemistry cited within the dataset documentation.