Supporting information for NE/W002930/1: Digital elevation models of bed rock and land surface topography, river discharge data, and settings files for the CAESAR-Lisflood model following the Chamoli ice-debris flow, India, February 2021

## Overview
- Input dataset for CAESAR-Lisflood (CL) modelling of post-event geomorphic response in Chamoli, India (February 2021 ice-rock avalanche and debris flow).
- Contains 10 m DEMs of bedrock and surface topography, river discharge data, and configuration/settings files for CL runs.
- Final calibrated model outputs are provided; CL executable is not included.

## What is in the data
- CL input files required to run the model and reproduce results.
- DEM files (10 m) for bedrock (pre-event) and surface (post-event) topography.
- Hydro discharge time-series for rivers exiting model domains.
- XML configuration files for CL runs and domain-specific settings.
- DoD (difference of DEMs) outputs for topographic change.

## Why and how the data were collected
- Collected to support coupled hydrodynamic-landscape evolution modelling under project NE/W002930/1.
- Used CL to evaluate geomorphological response of Chamoli river channels to the February 2021 event.
- Data created between 1 June 2021 and 31 May 2022; final calibrated inputs produced for the calibrated model.

## Where and when
- Study area bounded within a defined WGS84/UTM 44 N box around Chamoli District, Uttarakhand, India.
- Timeframe spans June 2021–May 2022 for data creation; inputs reflect February 2021 event conditions and post-event calibration period.

## How the data were collected and processed
- CL configuration (.xml) files generated within the CL executable and exported on save.
- DEMs (.txt) derived in QGIS 3.18; originally at 2 m and down-sampled to 10 m for computational efficiency.
- River discharge inputs (.txt) from GEOGloWS reanalysis data (free access at geoglows.ecmwf.int), aligned to domain locations.
- Boundary conditions and parameters summarized in a domain-specific setup (four coupled sub-models/domains).

## Who produced and interpreted the data
- Project PI (principal investigator) authored the data with support from a Co-I.
- PI and Co-Is interpreted CL outputs; interpretation is not part of the data resource itself.
- No model output files are provided; users can reproduce outputs with the included inputs.

## Completeness and accessibility
- Dataset includes all input files required to run CL and reproduce results.
- Missing component: the CL executable itself (available separately on SourceForge with a wiki for operation).
- Documentation and parameter values are included to enable replication.

## Model and technical details
- CL combines CAESAR landscape evolution with LISFLOOD-FP hydrodynamics; supports floods, erosion/deposition across grain sizes, and slope failures.
- Model setup uses four coupled domains (domain_1 to domain_4) with specific coupling points along geomorphic segments.
- Boundary conditions include DEMs, discharge time-series, grain-size distributions, and numerical/physical model parameters.
- DEM choices: 2015 bedrock surface for bedrock; 2021 surface DEM for routing and incision; assumption of sediment-filled pre-event valley.
- Spin-up: traditional long spin-up avoided to preserve post-event physicality; valley wetting via a brief low-discharge period (6–9 February 2021) used to ensure numerical stability.
- Grain sizes: nine fractions (0.0001–1 m); proportions derived from field photos and refined during calibration.
- Sediment flux: no external sediment flux input included for the initial post-event year; external inputs become important for longer-term modelling.

## Calibration and validation
- Calibrated by matching modelled vs. DEM-differenced volumetric changes for 10 February 2021–25 December 2021.
- Domain-scale fit: 86.3% of volumetric change reproduced (-6.35 Mm3 modelled vs -7.35 Mm3 measured).
- Independent validation: DoD-based comparison for 10 Feb 2021–27 Jan 2022 reproduced 91.3% of satellite-derived change (-6.38 Mm3 modelled vs -6.98 Mm3).
- Excluded areas: domains 1 and 2 excluded due to substantial post-event avalanching (not reproducible with current CL setup) from 23 Aug 2021–20 Oct 2021.

## Output data and intended use
- Outputs of interest: daily mean discharge at hydrological exits of submodels, daily sediment yields by size fractions, and DoDs every seven model days.
- Data structure and formats designed to facilitate reproduction and analysis of model results.

## Nature and units of values
- XML: text-based configuration files (open/edit in text editors).
- DEMs: ASCII grid TXT; units in metres (topography).
- Hydro data: daily discharge in cubic metres per second (m3 s-1).
- DoD: raster grids indicating net vertical change (negative = erosion, positive = deposition).

## Quality control and uncertainty
- DoD gaps reflect data gaps in input DEMs from photogrammetry; gaps reproduced in DoD.
- Uncertainty thresholds established using stable hillside areas via Pléiades imagery; 2-sigma DoD uncertainty per period (ranging roughly 0.61–1.14 m, varying by period).
- Significant changes identified if they exceed period-specific thresholds.

## Dataset structure (folders and key files)
- domain_1: chamoli_domain1.xml, domain1_bedr_DEM.txt, domain1_surf_DEM.txt, rontigad_hydro_input.txt, domain1_hydro_output.dat, etc.
- domain_2: domain2_bedr_DEM.txt, domain2_surf_DEM.txt, rishiganga_hydro_input.txt, domain2_hydro_output.dat, etc.
- domain_3 and domain_4: similarly contain respective XML, DEMs, and hydro files.
- Notes on files: XMLs are CL configuration; DEMs describe bedrock/surface; hydro_input are internal inputs; hydro_output provide downstream sediment inputs for subsequent domains.

## References
- Key literature and data sources informing model choices, parameters, and validation (e.g., Bates et al. 2010; Beven 1997; Shugar et al. 2021; Shugar et al.; various CAESAR-Lisflood and sediment transport references).