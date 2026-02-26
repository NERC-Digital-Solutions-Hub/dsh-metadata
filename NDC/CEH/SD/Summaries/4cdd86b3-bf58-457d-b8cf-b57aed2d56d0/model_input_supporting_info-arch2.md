# Supporting information for NE/W002930/1: Digital elevation models of bed rock and land surface topography, river discharge data, and settings files for the CAESAR-Lisflood model following the Chamoli ice-debris flow, India, February 2021

## Aim and scope
- Provides input files for CAESAR-Lisflood (CL), a coupled hydrodynamic-landscape evolution model, to evaluate the geomorphological response of river channels after the Chamoli 7 February 2021 ice-rock avalanche and debris flow.
- Intended to support reproducible modelling within the NE/W002930/1 project and facilitate interpretation of environmental response to a major debris-flow event.

## What the data contain
- 10 m digital elevation models (DEMs) of bedrock (pre-event) and land-surface topography (post-event) for CL.
- River discharge input time-series (hydro data) derived from GEOGloWS reanalysis data.
- CL model configuration/settings files (.xml) for each domain.
- Output-related data including domain-specific hydro outputs and DoD (difference of DEMs) related information used for validation (the DoD maps themselves are discussed and used in calibration/validation).

## Spatial and temporal coverage
- Spatial extent described by a bounding box in WGS 84 / UTM Zone 44:
  - Top left: 352,312 m E, 3,385,209 m N
  - Bottom right: 384,787 m E, 3,358,896 m N
- Temporal scope:
  - DEMs represent pre-event bedrock and post-event surface (Feb 2021) topography.
  - Data creation occurred between 1 June 2021 and 31 May 2022 (final calibrated model).
  - Hydrological inputs cover 10 February 2021 onward, with a 4-day pre-discharge wetting period (6–9 February 2021) to stabilize the model run.

## Data collection and processing methods
- CL configuration: XML files describing model setup and parameters; created within the CL executable and exported on project save.
- DEM processing: 2 m DEMs were down-sampled to 10 m in QGIS 3.18 to improve computational efficiency.
- Hydrology: Daily mean discharge inputs derived from GEOGloWS reanalysis data (freely accessible).
- Domain structure: Model run in “reach mode” split into four coupled sub-models (domains) with coupling at specified geomorphological segments (between Ronti Gad–Rishiganga, Rishiganga–Dhauliganga, and downstream of Tapovan Vishnugad).
- Grain size treatment: Nine size fractions (0.0001–1 m) with uniform distribution across the basin, with sub-model 2 calibrated to a finer distribution.
- Sediment flux: No external sediment flux inputs were used for the initial period to reflect post-event conditions dominated by new flood-deposited material; longer-term modelling would require external sediment inputs.
- Boundary conditions and parameters: A comprehensive set of CL inputs controls hydrological, sedimentological, and numerical behavior (see Table 1 in the document for final calibrated values).

## Model overview and setup
- CL combines CAESAR landscape evolution with LISFLOOD-FP flood hydraulics for long-term simulations, capable of handling erosion, deposition, sediment transport, and slope failures.
- The model uses a reduced spin-up approach to preserve the physicality of post-event conditions, with a brief 4-day wetting phase to stabilize computations.

## Calibration and validation
- Calibration approach: Compare modeled net volumetric change (domain scale) with DEM differencing for 10 February 2021 to 25 December 2021.
- Results:
  - Domain-scale volumetric change reproduced at 86.3% accuracy: modeled change -6.35 Mm3 vs observed -7.35 Mm3.
  - Independent validation with satellite DoD (10 Feb 2021 – 27 Jan 2022) reproduced 91.3% of observed change: modeled -6.38 Mm3 vs satellite -6.98 Mm3.
- Exclusions: Domains 1 and 2 were excluded from some comparisons due to substantial downstream mass deposition from avalanches in Aug–Oct 2021 which were not represented in the model.

## Output data and interpretations
- Primary outputs of interest:
  - Daily mean discharge (Qw) at the hydrological exit of each sub-model.
  - Daily sediment yields (Qs), including size-specific yields.
  - DoD maps generated every seven model days to show vertical topographic change since model start.
- Purpose: Enable monitoring-style assessment of hydrological and geomorphological responses to the Chamoli event over time.

## Dataset structure and access
- Folder organization by domain:
  - domain_1, domain_2, domain_3, domain_4
- Contents per domain:
  - chamoli_domain?.xml (model configuration)
  - domain?_bedr_DEM.txt (bedrock DEM)
  - domain?_surf_DEM.txt (surface/topography DEM)
  - <domain>_hydro_input.txt (flow discharge time-series)
  - <domain>_hydro_output.dat (upstream domain outputs fed into this domain)
- Output data: DoD maps and hydro outputs are designed to support reproducibility and cross-domain data flow (e.g., domain_1 outputs feed into domain_2 as inputs).
- Notes:
  - XML files are human-editable text files; DEM and hydro files are ASCII raster/tabular formats suitable for GIS and hydrological modelling.
  - The DoD data include uncertainty estimates derived from stable hillside areas to identify statistically significant changes.

## Quality control and limitations
- DoD data gaps reflect photogrammetry/remote-sensing limitations (cloud cover, occlusions, alignment issues).
- Uncertainty estimates (two-sigma) are provided for each DoD period to assess significance of detected changes.
- DoD stability polygons are provided to support uncertainty assessment.

## Completeness and reproducibility
- The dataset includes all input files required to run CAESAR-Lisflood and reproduce results.
- The CL executable is not included in this repository; it is available from the CAESAR-Lisflood project (SourceForge) with an accompanying wiki detailing parameters and usage.
- The data are designed to be reused with the model inputs to reproduce the final calibrated model and outputs.

## References
- Model and parameter references for CL, CAESAR, LISFLOOD-FP, and related methods cited in the document (e.g., Bates et al. 2010; Beven 1997; Coulthard et al.; Einstein 1950; Wilcock & Crowe 2003; Shugar et al. 2021; Shugar et al. 2021; Skinner & Coulthard 2017; etc.).