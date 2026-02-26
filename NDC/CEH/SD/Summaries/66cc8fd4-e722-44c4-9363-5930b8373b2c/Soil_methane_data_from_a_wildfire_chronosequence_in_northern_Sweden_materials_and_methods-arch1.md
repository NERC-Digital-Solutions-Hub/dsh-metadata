# Soil methane sink capacity response to a long-term wildfire chronosequence in northern Sweden

## Overview
- Investigates soil CH4 fluxes and the capacity for methane oxidation across a long-term wildfire chronosequence on 30 boreal forest freshwater islands in northern Sweden.
- Combines in situ and ex situ flux measurements with stable isotope analyses to quantify CH4 oxidation and related ecosystem properties.
- Uses statistical modelling to relate CH4 dynamics to successional stage, humus development, and depth.

## Study system and design
- Location: Archipelago of over 400 islands in lakes Uddjaure and Hornaven (N65°15′–N66°99′, E17°55′), boreal forest region.
- Islands: 30 islands varied in size (0.02–15 ha) but sharing climate and geology; wildfire frequency is the main extrinsic factor that differs among islands.
- Chronosequence concept: Major wildfire ages determined by 14C dating of buried charcoal and fire scars from the last ~250 years, creating a retrogressive chronosequence with island size linked to retrogression.
- Climate context: Mean annual precipitation ~750 mm; mean July temperature ~13 °C and January ~-14 °C.

## In situ CH4 flux measurements
- Timing and method: CH4 fluxes measured over one week in August 2006 using static chambers (n=5 per island; chamber volume 0.0054 m3; diameter 0.2 m).
- Procedure: Base rings installed into humus to 5 cm; headspace gas samples taken at 0, 5, 10, 15, 20, 25, 30 minutes after sealing; samples stored in exetainers for up to a month before GC analysis.
- Analysis: CH4 quantified by gas chromatography with flame ionization detector; calibration with certified standards; detection limit corresponding to ~3 g CH4 m−2 h−1; fluxes calculated by standard linear regression.
- Notes: Fluxes below detection limit retained in analyses per prior work.

## Ex situ CH4 flux measurements
- 2006: Four intact soil cores (11 cm diameter, 25 cm depth) per island (40 per island size classification) were collected and maintained at field moisture; fluxes measured using static chambers (volume 0.0008 m3) with sampling at 0, 30, 60, 90, 120, 150 minutes.
- 2007: One full profile core per island (0.15 m diameter, from humus to bedrock; 20–85 cm depth) collected; flux measurements with static chambers (volume 0.0021 m3, diameter 0.15 m) under the same conditions as 2006.
- Handling: Cores stored at 12 °C in the dark; moisture content determined after drying; sample storage and GC analysis as described for in situ samples.

## In situ depth profiles of CH4 and δ13CH4
- Depth profiling: Gas samples collected within humus profiles at depths corresponding to 15, 35, 55, and 75 cm over four days in July 2007.
- Sampling: Four stainless steel probes inserted into soil; 100 mL samples taken per depth with 90 mL sent to a bottle and 9 mL to an exetainer.
- Isotopic analysis: δ13C of CH4 measured at NERC Life Sciences Mass Spectrometry Facility after pre-concentration and CO2/water removal; isotope precision ≤ 0.2‰ with reference standards calibrated to NIST and CH4 standards.
- Purpose: Enables isotopic investigations of CH4 sources and transport within soil profiles.

## Isotopic method to determine CH4 oxidation
- Concept: Use non-equilibrium or kinetic isotope effects (KIEs) via the oxidation fractionation factor a_ox, which relates rates of 12CH4 and 13CH4 during methanotrophy.
- Top-to-Bottom δ13CH4 approach: Determines the fraction of atmospheric CH4 that passes through soil layers by comparing δ13CCH4 values at atmospheric and soil depths; accounts for diffusion-related fractionation.
- Mass balance model: Estimates the fraction of CH4 oxidised (F_o) using isotopic measurements, isotopic composition of soil and atmosphere (δ_soil and δ_atmos), and an isotopic fractionation associated with gas transport (a_trans). F_o is multiplied by 100 to yield percentage oxidised.
- Transport fractionation: a_trans is not directly measurable; the study adopts a diffusion-based value of 1.0195 (diffusion fractionation for temperate forest soils) to avoid underestimating oxidation.
- Note: The model integrates both biological oxidation and CH4 transport effects.

## Ecosystem properties and auxiliary measurements
- Soil properties: pH (via soil:water 1:3), soil carbon and nitrogen percentages (oxidative combustion with thermal detection).
- Humus depth: Measured along transects with depth to bedrock, to characterize humus development.
- Vegetation and soil context: Additional data on vegetation mass, shrub productivity, tree productivity, and humus mass referenced to prior work on the island chronosequence.

## Statistical analyses
- Software: R (as of 2011).
- Primary approaches:
  - Simple regressions to relate response variables to successional age (from 14C dating) and humus development.
  - Differences among successional stages (Early, Mid, Late) tested with generalized linear models (glm); data non-negativity ensured by adding lowest datapoint + 1.
  - Non-normal CH4 metrics (e.g., CH4 concentration, δ13C, % CH4 oxidised) analyzed with linear mixed-effect models (lme), island as random effect to account for repeated measures on the same cores.
  - Diagnostic checks: Residual plots used to assess bias and heteroscedasticity.

## Ethics, permissions, and conflicts of interest
- Field sites: 30 freshwater islands in boreal Sweden; land is public and not national reserves; no special permissions required.
- Ethics: No human or animal subjects; no commercial interests or conflicts of interest reported.
- Compliance: All national and international rules followed during fieldwork.

## Key takeaways for data-focused interpretation
- The study integrates direct CH4 flux measurements with stable isotope techniques to quantify CH4 oxidation across a wildfire-driven successional gradient.
- Data span in situ and ex situ fluxes, depth-resolved isotopic profiles, and basic soil/vegetation properties to elucidate drivers of methane uptake capacity.
- Analyses are designed to reveal correlations between CH4 dynamics and island successional stage, soil development, and depth, while accounting for island-level dependencies.