# Soil methane sink capacity response to a long-term wildfire chronosequence in northern Sweden

## Overview
- Investigates soil CH4 fluxes across 30 freshwater boreal island sites to understand long-term wildfire effects on methane cycling.
- Combines in situ flux measurements, ex situ core incubations, and in situ isotopic (δ13CH4) profiling to quantify CH4 oxidation in soils.
- Uses a mass-balance isotopic approach to estimate the fraction of CH4 oxidised and to infer oxidation processes within soil profiles.
- Analyzes data with regression and mixed-effects models, treating island as a random effect to account for site-level dependencies.

## Study system and design
- Location: Boreal forest islands in lakes Uddjaure and Hornaven, northern Sweden; archipelago of >400 islands, this study on 30 islands.
- Island characteristics: similar geology and climate; mean annual precipitation ~750 mm; July mean temperature ~13°C; January ~-14°C.
- Experimental design: retrogressive wildfire chronosequence across island size; age of major wildfires determined by 14C dating and fire scar analysis over the last ~250 years.
- Primary variable: wildfire frequency (varying among islands) with retroduction of ecosystem properties along an island size gradient.

## Data collected and methods

### In situ CH4 flux measurements
- Method: static chamber (volume 0.0054 m3; diameter 0.2 m) deployed on 5 replicates per island for one week in August 2006.
- Procedure: headspace samples collected at 0, 5, 10, 15, 20, 25, 30 minutes; concentrations measured by GC-FID after storage in exetainer vials.
- Detection limit: 0.05 ppm CH4, corresponding to ~3 g CH4 m^-2 h^-1; fluxes below detection still included in analyses.
- Data processing: standard linear regression to derive flux rates.

### Ex situ CH4 flux measurements from intact cores
- 2006: four intact soil cores (11 cm diameter, 25 cm depth) per island (n=40 per island size class); moisture adjusted with artificial rain solution (pH 5.6, conductivity 22.4 µS).
- 2006 measurements: static chamber (volume 0.0008 m3) with sampling at 0, 30, 60, 90, 120, 150 minutes.
- 2007: full-profile cores (0.15 m diameter) collected from each island humus profile to bedrock (20–85 cm depth); chamber volume 0.0021 m3; measurement under same conditions.
- Additional data: soil moisture calculated after oven-drying samples; measurements linked to island successional stage (early, mid, late).

### In situ depth profiles of δ13CH4 and CH4/CO2
- July 2007: isotopic sampling within humus profiles at depths up to 75 cm using four probes.
- Sample processing: 100 ml gas samples collected, with 90 ml sent to a 50 ml bottle and 9 ml to a 3.6 ml exetainer; wax-sealed probes stored for isotope analysis.
- Isotope analysis: δ13CH4 measured at NERC facility using mass spectrometry after pre-concentration and gas cleanup; precision better than or equal to 0.2 ‰.
- Standards: δ13C CH4 calibrated to PDB; CO2 standards anchored to NIST references.

### Isotopic method to determine CH4 oxidation
- Approach: Top-to-Bottom δ13C-CH4 method to determine the fractionation associated with methanotrophy (aox).
- Concept: oxidation enriches remaining CH4 in 13C; atmospheric vs soil CH4 δ13C difference used to estimate oxidation fraction.
- Mass-balance model: Fo (fraction oxidised) is estimated via a model that accounts for oxidation and transport fractionation.
- Transport fractionation (atrans): not directly measurable; two common assumptions exist. This study uses a trans value of 1.0195 (diffusion-dependent) to avoid underestimating oxidation.

### Ecosystem properties and ancillary measurements
- Soil properties: pH (soil:water 1:3), %C, %N using oxidative combustion and thermal conductivity detection.
- Humus depth: measured July 2007 along transects across each island.
- Additional data: vegetation mass, shrub productivity, tree productivity, and humus mass from prior studies.

## Data analysis and statistics
- Software: R (statistical programming environment).
- Analyses:
  - Simple regression to relate response variables to predictors (successional age from 14C dating; humus development).
  - Differences across successional stages (Early, Mid, Late) evaluated with generalized linear models (glm); data adjusted by adding a constant (lowest datapoint + 1) to ensure non-negativity and to accommodate non-normal distributions.
  - CH4 oxidation metrics and other CH4 measures analyzed with linear mixed-effects models (lme); island included as a random effect to account for non-independence within cores.
  - Model diagnostics included residual plots to check for bias and heteroscedasticity.

## Ethics and governance
- Ethics: study conducted on public island land; no permits required; no human or animal subjects; no conflicts of interest or commercial interests reported.
- Compliance: adherence to national and international rules during fieldwork.

## Data management considerations for Data Stewards
- Data types and provenance:
  - In situ CH4 fluxes (temporal series per island), ex situ CH4 fluxes (topsoil and full profile), isotopic δ13CH4 measurements, and derived oxidation fractions (Fo) with associated aox and atans.
  - Supporting ecosystem data: soil pH, %C, %N, humus depth, and productivity metrics.
- Metadata needs:
  - Site identifiers (island ID), geographic coordinates, island size, successional stage, sampling dates, and sampling depths.
  - Technical details: chamber volumes, core dimensions, moisture maintenance methods, GC and isotope instrument models, calibration standards, detection limits, and QA/QC procedures.
  - Data processing steps: flux calculation methods, isotopic fractionation corrections, mass-balance equation parameters, and statistical model specifications (including random effects and transformations).
- Data usability and reproducibility:
  - Clear documentation of units (e.g., CH4 flux in g CH4 m^-2 h^-1; δ13CH4 in ‰; depths in cm; pH; %C, %N).
  - Availability of raw and processed datasets, along with code or explicit modeling steps where feasible to enable reanalysis.
- Limitations and caveats to capture:
  - Detection limit implications for flux estimates; assumption of trans = 1.0195 for diffusion-related fractionation; one-week duration for in situ flux measurements; potential moisture and temperature controls on fluxes not exhaustively enumerated.
- Governance implications:
  - The dataset is multi-layered (gas fluxes, isotopic data, soil properties, vegetation), requiring harmonized metadata schema and consistent data curation to enable cross-island comparisons and long-term meta-analyses.