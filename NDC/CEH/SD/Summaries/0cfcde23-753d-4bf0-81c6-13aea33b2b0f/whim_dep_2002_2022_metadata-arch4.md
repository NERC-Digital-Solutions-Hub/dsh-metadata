# Ammonia concentration and deposition data from a peatland nitrogen pollution experiment, Whim Bog, Scotland, UK, 2002-2022

## Overview
- Long-term study (2002–2022) at Whim Moss ombrotrophic bog near Edinburgh to examine effects of elevated atmospheric NH3 on vegetation, bryophytes, lichens, and soil.
- NH3 enhancement system is wind-driven, releasing NH3 only when wind is toward monitoring quadrats and above a threshold speed.
- NH3 concentrations measured monthly with ALPHA passive samplers; deposition to vegetation estimated using a unidirectional resistance model.
- Sampling locations (lateral and vertical) were adjusted over time to meet study needs.
- Complete experimental design, methodology, analysis, and findings are detailed in referenced works (Leith et al. 2004; Jones et al. 2007; Cape et al. 2008).

## Data collection and flux calculations (methods)
- Measurement period: 15-minute NH3 concentrations during NH3 release periods; monthly averages used for extended calculations.
- Sampling: UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers; 6296 measurements across 6 parameters.
- Deposition flux calculation: Fχ(z) = χa / Rt, where Rt = Ra + Rb + Rc (total resistance).
  - Ra (aerodynamic resistance) derived from wind speed, measurement height, and velocity parameters.
  - Rb (boundary-layer resistance) computed using Reynolds number and Schmidt number for NH3.
  - Rc (canopy resistance) daytime and night-time parameterizations based on observed NH3 concentration χ and constants A, B, Rbox.
  - During NH3 release: Rc is calculated with daytime/night-time equations; constants derived from prior work (Jones et al. 2007).
  - During periods with no NH3 release: Rc fixed (20 s m−1) and Rt computed from average Ra and Rb; deposition flux uses ambient NH3 concentration for the month.
- Flux calculation cadence: 15-minute intervals; fluxes summed monthly.
- Notes: Detailed model formulas and constants originate from multiple prior studies (citations provided in the document).

## Data structure and metadata
- Data file: CSV with 6 parameters per measurement.
- Columns include:
  - Month: year and month
  - ID: sampler identifier
  - E/W: orientation (East/West) relative to the transect
  - Con/Amb: Control or Ambient
  - Distance: distance from NH3 source (positive downwind, negative upwind)
  - Height: measurement height above ground
  - NH3_conc: NH3 concentration (µg m−3); monthly average NH3 concentration available
  - Dep_kg_ha: monthly deposition flux (kg ha−1 month−1)
- Data notes:
  - NA in NH3_conc indicates missing NH3 concentration data (e.g., sampler damage/loss)
  - NA in Dep_kg_ha indicates missing deposition flux (due to missing NH3 or meteorological data)
- Total measurements: 6296 across 6 parameters

## Quality control and data quality
- Visual quality checks performed; erroneous data from instrument faults, damage, or power interruptions removed.
- Monthly NH3 concentrations lower than ambient values removed to avoid negative flux values.
- Missing values occur where sampler locations changed during a year (expected due to study design changes).

## Data accessibility and provenance
- Data type: long-term time series available as CSV with clearly defined fields and units.
- Data lineage: calculations based on established deposition-velocity models and parameters from prior peer-reviewed studies (citations included in the document).
- Related publications for fuller methodology and validation:
  - Leith et al. 2004
  - Jones et al. 2007
  - Cape et al. 2008
- Funding: Natural Environment Research Council Award NE/R016429/1 (UK-SCAPE programme delivering National Capability).

## Implications for data governance and reuse (for Data Leaders)
- Longitudinal, multi-site data with changes in sampling design over time; requires clear metadata to enable reanalysis and cross-site comparability.
- Explicit documentation of data processing steps (QA/QC, handling of missing data, and flux calculation methodology) supports reproducibility and integration with other data networks.
- Rich metadata around sampler IDs, orientation, distance from source, and measurement heights enhances discoverability and reusability for policy-relevant assessments of ammonia deposition impacts.
- Data gaps and sampling relocations are transparently noted, enabling appropriate gap analysis and uncertainty assessment in downstream analyses.