# Soil methane sink capacity response to a long-term wildfire chronosequence in northern Sweden

## Overview
- Investigates how soil methane (CH4) sink capacity responds to long-term wildfire-driven chronosequence in boreal Sweden.
- Combines in situ and ex situ CH4 flux measurements with isotopic analyses to quantify CH4 oxidation and its controls.
- Integrates ecosystem properties (soil chemistry, humus depth, biomass data) and uses statistical models to relate CH4 fluxes and oxidation to successional stage and island characteristics.

## Study System and Design
- 30 freshwater islands in the boreal forest region of northern Sweden; part of a larger archipelago in lakes Uddjaure and Hornaven.
- Islands share similar climate and geology; the sole varying extrinsic factor is wildfire frequency, determined historically by fire scars and radiocarbon dating, forming a retrogressive chronosequence as island size decreases.
- Islands span a size range from 0.02 to 15 ha and exhibit differing wildfire histories, enabling analysis across successional stages (early, mid, late).

## Data Collected

### In situ CH4 Fluxes
- Measured over one week per island using static chambers (volume 0.0054 m3; diameter 0.2 m); 5 measurements per island.
- Gas samples collected at 0, 5, 10, 15, 20, 25, 30 min after sealing; CH4 analyzed by GC-FID.
- Detection limit: about 0.05 ppm CH4, corresponding to ~3 g CH4 m−2 h−1; fluxes below detection still included in analyses.

### Ex situ CH4 Fluxes from Intact Cores
- Top 25 cm soils collected in 2006; entire humus profile to bedrock in 2007 (0.15 m diameter cores, 0.15 m depth).
- 2006: four cores per island (40 cores per island size class); moistures maintained with artificial rain solution; fluxes measured with smaller chambers (0.0008 m3) at 0–150 min intervals.
- 2007: full profile cores measured with larger chambers (0.0021 m3).
- Cores grouped by successional stage (early, mid, late); n = 10 per group.

### In situ Depth Profiles of CH4, δ13CH4, and CO2
- In July 2007, sampling within humus profiles at depths of 15, 35, 55, and 75 cm using stainless steel probes.
- Gas samples collected and isotopic analysis of δ13CH4 performed via isotope ratio mass spectrometry after gas pre-concentration and CO2/CH4 scrubbing.
- Isotopic precision: ≤0.2 ‰; δ13CCH4 values expressed relative to PDB.

### Isotopic Method for CH4 Oxidation (aox and Fo)
- Uses Top-to-Bottom δ13C-CH4 approach to determine the fractionation factor for CH4 oxidation (aox) for each island.
- A mass-balance model (Equation 1) calculates Fo, the fraction of CH4 oxidised, incorporating isotopic compositions of soil- and atmosphere-derived CH4 and an isotopic fractionation for gas transport (atrans).
- Since atrans cannot be directly measured, atrans is set to 1.0195 based on diffusion in temperate forest soils, per prior studies.

### Ecosystem Properties
- Soil pH, %C, and %N measured from 2006 soil cores.
- Humus depth assessed in July 2007 along transects across each island.
- Additional data on vegetation mass, shrub and tree productivity, and humus mass referenced from prior work.

## Data Processing and Analysis

### Calculations and Isotopic Modelling
- Fo (fraction CH4 oxidised) derived from the mass-balance model using δ13CCH4 data from soil and atmosphere and fixed atrans.
- Isotopic and concentration data used to infer CH4 oxidation dynamics across depths and successional stages.

### Statistical Analyses
- Conducted in R.
- Simple regression to relate response variables to predictors such as successional age (from 14C dating) and humus development.
- Differences in CH4 fluxes (in situ and ex situ) and CH4 oxidation across successional stages (Early, Mid, Late) analyzed with generalized linear models (glm). A constant value (lowest datapoint + 1) added to ensure non-negative data.
- For other CH4 measures (CH4 concentration, δ13C of CH4, % CH4 oxidised) analyzed with linear mixed-effects models (lme; nlme package), Island included as a random effect to account for repeated measures within cores.
- Model diagnostics included residual plots to check for bias and heteroscedasticity.

## Quality, Assumptions, and Uncertainties
- CH4 flux calculations include data below detection limits to avoid discarding information, following established practices.
- Transport fractionation (atrans) values are assumed (1.0195) due to lack of direct measurement, which can influence Fo estimates.
- Isotopic precision is high (≤0.2 ‰), and calibration relies on standard references for CH4 and CO2.

## Ethics and Compliance
- Fieldwork conducted on public, non-protected islands; no permission required.
- No human or animal measurements; no commercial interests or conflicts of interest reported.

## Implications for Data Use
- The study generates a multi-dimensional dataset linking CH4 fluxes (in situ and ex situ), CH4 oxidation (via δ13C and isotopic modelling), and soil/ecosystem properties across a wildfire-driven successional gradient.
- Data suitable for creating data products that explore spatial (island-level) and temporal (successional stage) patterns in soil CH4 dynamics, supporting modelling of boreal forest CH4 sinks under changing fire regimes.
- Potential outputs include comparable CH4 flux datasets, oxidation fractions by depth and stage, and relationships between soil properties and CH4 dynamics for informing policy and land management decisions.