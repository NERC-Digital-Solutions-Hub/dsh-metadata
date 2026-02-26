# Supporting information for NE/W002930/1: Digital elevation models of bed rock and land surface topography, river discharge data, and settings files for the CAESAR-Lisflood model following the Chamoli ice-debris flow, India, February 2021

- A dataset of input files for CAESAR-Lisflood (CL), a numerical hydrodynamic-landscape evolution model.
- Includes 10 m digital elevation models (DEMs) of bedrock and land-surface topography, river discharge data, and configuration settings files for CL modelling.
- Final, calibrated model inputs intended to reproduce the geomorphic response to the February 7, 2021 Chamoli ice-rock avalanche and debris flow.

## Purpose and context

- Created to support coupled hydrodynamic-landscape evolution modelling within project NE/W002930/1.
- Used CL outputs to evaluate how river channels responded geomorphologically to the Chamoli disaster.
- Data are designed to enable reconstruction and reproduction of the modelling workflow and results.

## Location and timing

- Spatial extent described by a bounding box in WGS 84 / UTM Zone 44 coordinates (approximate extents):
  - Top left: 352,312 m E, 3,385,209 m N
  - Bottom right: 384,787 m E, 3,358,896 m N
- Timeframe:
  - Data creation roughly June 1, 2021 to May 31, 2022 (final, calibrated inputs).
- Model structure:
  - Four coupled domains/sub-models (domain_1 to domain_4) forming a reach-based setup.
  - Key junctions between geomorphological segments defined for coupling.

## Data collection and processing

- XML configuration files (chamoli_domain*.xml) define CL model settings; these are created within the CL executable and exported when the project is saved.
- DEMs (domain*_bedr_DEM.txt for bedrock; domain*_surf_DEM.txt for surface) are gridded elevations in metres, down-sampled from 2 m to 10 m in QGIS to improve computational efficiency.
- Hydrology inputs (rontigad_hydro_input.txt, alaknanda_hydro_input.txt, rishiganga_hydro_input.txt, dhauliganga_hydro_input.txt) consist of daily discharge time-series derived from GEOGloWS reanalysis data (https://geoglows.ecmwf.int/).
- The February 2021 event initial conditions assume valley-floor sediment infill from the pre-event bedrock, with surface DEM representing post-event topography.
- A very short pre-conditioning “wetting” of the valley floor (4 days, 6–9 February 2021) with very low discharge was used to stabilize the numerical model; real hydrologic inputs start on February 10, 2021.
- A uniform nine-fraction grain-size distribution (0.0001 to 1 m) was applied broadly; sub-model 2 used a finer distribution after calibration.
- External pre-disturbance sediment flux was not input due to lack of local information and the dominance of new debris-flow–derived material in the first year post-event.
- Local calibration involved adjusting grain-size distributions in sub-model 2 and other parameters to improve fit.

## Model overview and setup

- CL combines CAESAR landscape evolution with LISFLOOD-FP hydrodynamics to simulate events over long timescales.
- Reach-mode operation with four coupled domains; coupling points between specified geomorphological segments (e.g., Ronti Gad–Rishiganga confluence, Rishiganga–Dhauliganga confluence, downstream of Tapovan HEP).
- Required inputs per domain:
  - DEMs for bedrock and surface
  - Input river-discharge time-series
  - Grain-size information (and distribution across active layers)
  - Numerical, hydrological, and sedimentological parameters
- Key parameter choices (Table 1 in the document) include:
  - DEM heights (bedrock active-channel DEM ~1,345–3,937 m above ellipsoid for active channel)
  - Flow initiation locations and associated GEOGloWS stream IDs
  - Nine grain-size fractions (0.0001–1.00 m)
  - Sediment transport laws (Wilcock and Crowe vs Einstein; Wilcock-Crowe applied in sub-model 3)
  - Erosion limits, active-layer thickness, lateral erosion, slope-failure thresholds, edge-cell slope, Courant number, Manning’s roughness
- Model calibration adjustments:
  - Sub-model 2 used a refined, finer grain-size distribution
  - Slope-failure thresholds increased to mitigate artefacts from DEM edges
- Data inputs emphasize a localization of boundary conditions to each domain, where domain1 outputs feed domain2 inputs, and so on.

## Calibration and validation

- Calibration approach: compare modelled net volumetric change with DEM-difference (DoD) estimates for Feb 10, 2021 to Dec 25, 2021.
- Domain-scale reproduction: 86.3% of volumetric change matched (modelled -6.35 Mm3 vs measured -7.35 Mm3).
- Independent validation: DoD-derived validation for Feb 10, 2021 to Jan 27, 2022 reproduced 91.3% of changes (modelled -6.38 Mm3 vs DoD -6.98 Mm3) over roughly one year post-event.
- Exclusions: Domains 1 and 2 excluded from comparison due to substantial late-2021 mass deposition from avalanches not represented in the CL model.
- DoD validation timeframe aligns with 351 days after the event.

## Output data

- Daily mean discharge (Qw) at each sub-model’s exit.
- Daily bulk- and size-specific sediment yields (Qs) across nine grain-size fractions.
- Difference-of-digital-elevation (DoD) maps generated every seven model days to show vertical topographic change since model start.
- The dataset is structured to facilitate accessing these outputs and reproducing results.

## Data quality and uncertainty

- DoD uncertainty assessed using stable hillside areas identified in Pleaides orthoimagery; standard deviations used to compute two-sigma thresholds.
- Reported DoD uncertainties:
  - DoD 2015-02-10: ±1.11 m
  - DoD 2021-06-06: ±0.91 m
  - DoD 2021-12-25: ±0.61 m
  - DoD 2021-02-10 to 2021-12-25: ±1.14 m
  - DoD 2021-02-10 to 2022-01-27: ±1.06 m
- DoD values exceeding the threshold are considered statistically significant.
- Stable area polygons used for uncertainty estimation are included with the data resource.

## Dataset structure and access

- Folder structure includes domain_1, domain_2, domain_3, domain_4 with corresponding files:
  - chamoli_domain*.xml (CL configuration)
  - domain*_bedr_DEM.txt (bedrock DEM)
  - domain*_surf_DEM.txt (surface DEM)
  - *_hydro_input.txt (domain input hydro data for the domain)
  - domain*_hydro_output.dat (hydro outputs used as inputs to downstream domains)
- The hydro_input files contain daily discharge time-series; hydro_output files carry sediment flux inputs for downstream coupling (nine grain-size fractions, columns 5–14).
- Users can run the model in order (domain_1 to domain_4) and reproduce DoD and outputs, or regenerate outputs by re-running upstream domains.
- The CL executable itself is not included in this dataset; it is available from SourceForge (CAESAR-Lisflood) along with a comprehensive wiki describing operation and parameter guidance.
- Overall, the dataset includes all inputs needed to run CL and reproduce results, aside from the executable.

## References

- Foundational model and methods papers and data sets, including:
  - Bates, Horritt, Fewtrell (2010)
  - Beven (1997)
  - Bhushan and Shean (2021)
  - Coulthard et al. (2002, 2006, 2007)
  - Einstein (1950)
  - Hancock et al. (2011)
  - Shugar et al. (2021)
  - Shean et al. (2021)
  - Skinner and Coulthard (2017)
  - Wiel et al. (2007)
  - Wilcock and Crowe (2003)