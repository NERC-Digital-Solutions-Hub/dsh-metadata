# Soil methane sink capacity response to a long-term wildfire chronosequence in northern Sweden

- Aim and scope
  - Assess soil methane (CH4) sink capacity in boreal forest soils across a long-term wildfire chronosequence.
  - Use a standardized data approach to evaluate environmental health and policy-relevant methane cycling over time.

- Study system and context
  - 30 freshwater islands in the Boreal forest region of northern Sweden, part of an archipelago on lakes Uddjaure and Hornaven.
  - Islands form a retrogressive chronosequence: varying wildfire frequency tied to island size.
  - Similar geology, climate (mean annual precipitation ~750 mm; July mean temp ~13°C; January ~-14°C), and distance to shore across islands.
  - Major extrinsic variable is wildfire history; ages dated by radiocarbon and fire scar analysis over the last ~250 years.

- In situ determination of CH4 fluxes
  - Timeframe: one-week measurements in August 2006; n=5 per island.
  - Method: static chamber with a 0.0054 m3 chamber volume and 0.2 m diameter base rings installed into the humus (5 cm depth).
  - Sampling: headspace samples (9 mL) at 0, 5, 10, 15, 20, 25, 30 minutes after sealing; CH4 analyzed by GC with FID.
  - Detection and data handling: detectable change as low as 0.05 ppm CH4, equivalent to ~3 μg CH4 m−2 h−1; measurements used even if below detection limit.
  - Calculations: standard linear regression to derive exchange rates.

- Ex situ CH4 fluxes from intact cores
  - 2006: top 25 cm cores collected (four per island per size class; 40 cores per island size classification) and kept at ~12°C with controlled moisture.
  - 2006 measurements: static chamber (volume 0.0008 m3) with sampling at 0, 30, 60, 90, 120, 150 minutes; moisture content recorded post-drying.
  - 2007: full soil profile cores (0.15 m diameter) sampled from each island to bedrock (20–85 cm depth); similar chamber approach with 0.0021 m3 volume.
  - Successional context: cores grouped into late, mid, early successional stages; n=10 per stage.
  - Data handling: soil moisture and CH4 fluxes measured; samples stored for GC analysis as described above.

- In situ depth profiles and isotopic measurements
  - Gas sampling at depths within humus profiles: 15, 35, 55, 75 cm over 4 days in July 2007.
  - Probes and sampling: four stainless steel probes; 100 mL samples collected, with most transferred to exetainer vials for CH4 and 9 mL for δ13CH4 analyses.
  - Isotopic analyses: δ13C-CH4 determined via isotope ratio mass spectrometry after preconcentration; calibration against NIST references and CH4 standards.
  - Isotopic precision: ≤0.2 ‰; δ13C expressed relative to PDB.

- Isotopic method to determine CH4 oxidation
  - Use the Top-to-Bottom δ13C-CH4 approach to estimate CH4 oxidation fraction (F0) in soils.
  - Mass-balance model accounts for oxidation and transport fractionation; fractionation factor for transport (atrans) set to 1.0195 (diffusion-based) due to difficulty in direct measurement.
  - Calculation yields the fraction of atmospheric CH4 oxidised within soil layers; results expressed as a percentage (F0 × 100).

- Ecosystem properties and ancillary measurements
  - Soil properties: pH, % carbon (C), % nitrogen (N) measured from 2006 cores.
  - Humus depth: assessed in July 2007 via transect measurements to bedrock.
  - Additional vegetation and humus data referenced from prior studies on island ecosystem properties.

- Statistical analyses and data handling
  - Software: R (statistical computing environment).
  - Analyses:
    - Simple regression to relate CH4 response variables to successional age (from 14C dating) and humus development.
    - Differences in CH4 fluxes across successional stages (Early, Mid, Late) assessed using generalized linear models (glm). Non-negative data adjustments applied (lowest datapoint + 1).
    - For CH4 oxidation measures (δ13C and % CH4 oxidised), linear mixed-effects models with island as a random effect to account for nested measurements within cores.
  - Model diagnostics ensured no biases or heteroscedasticity in residuals.

- Ethics and permissions
  - Fieldwork conducted on public islands; no protected areas or special permissions required.
  - No measurements on humans or animals; negligible ecosystem disturbance; no conflicts of interest or commercial interests reported.

- Relevance for environmental monitoring
  - Provides standardized, multi-bind data on CH4 fluxes and oxidation across a wildfire-driven gradient in boreal soils.
  - Combines in situ and ex situ measurements with isotopic approaches to disentangle production, consumption, and transport processes.
  - Supports understanding of how long-term wildfire history modulates soil CH4 sinks, informing climate-relevant environmental health assessments and policy monitoring.
  - Data collection and analysis follow established, repeatable protocols suitable for integration into monitoring datasets and portals.