# Column heading explanations and materials and methods for: Spatial radionuclide deposition data from the 60 km area around the Chernobyl nuclear power plant: results from a sampling survey in 1987

## Overview
- Purpose: establish a long-term monitoring and contamination-mapping framework for the 60-km zone around the Chernobyl Nuclear Power Plant (ChNPP).
- Study design: radial network of sampling points arranged every 10° from 5 to 60 km, totaling 540 potential sites.
- Execution: conducted in April–May 1987; 489 of 540 selected points were actually sampled (excluding swamps, rivers, and lakes).

## Data collected and variables
- Core dataset columns (with explanations and units):
  - Identifier: unique ID; typically not linked to units.
  - Angle_degree: direction from ChNPP (10–360 degrees; 90° = east, 180° = south, 270° = west, 0/360° = north); unit: degree.
  - Distance_from_ChNPP_km: radial distance from ChNPP reactor 4; unit: kilometres.
  - Date_gamma_measurement: date of gamma measurement; unit: dd-month-yyyy.
  - Exposure_dose_rate_mR/h: outdoor dose rate at 1 m height; unit: milliroentgen per hour.
  - Absorbed_dose_rate_microGray/h: absorbed dose rate; unit: microgray per hour.
  - Zr-95_Bqm2, Nb-95_Bqm2, Ru-106_Bqm2, Cs-134_Bqm2, Cs-137_Bqm2, Ce-144_Bqm2: soil contamination density (Bq/m^2) for each radionuclide; note conversions used (1 Ci/km^2 = 37 kBq/m^2).
  - Relative_error for each radionuclide: uncertainty at 68% confidence; unit: percent.
  - Exch_Cs-134+Cs-137_Bqm2: density of contamination in the exchangeable form of Cs-134 and Cs-137; unit: Bq/m^2; 68% confidence.
  - Instrument: detector used (two possible gamma spectrometers described); unit: instrument name/model.

## Methods and instrumentation
- Sampling approach:
  - Soil sampling with a 14 cm diameter corer to 5 cm depth.
  - Five-point envelope sampling design per site (~5–10 m between points); five cores per site, with one retained in the corer for integrity during transport.
  - Sampling area per core approximately 0.015 m^2.
- Measurement and analysis:
  - Gamma-emitting radionuclides measured in one soil sample per site using a high-purity germanium detector (GEM-30185 ORTEC) with an ADCAM-300 multichannel analyser; reporting at 68% confidence.
  - Exchangeable Cs-134+Cs-137 fraction determined from another 100 g aliquot leached with 1 M NH4OAc solution (pH 7).
  - Remaining four cores sent to other laboratories in the Soviet Union (data not available).
- Data processing:
  - Radionuclide activity concentrations converted to soil contamination density (Bq/m^2) considering the sampled area.
  - Reported values correspond to the measurement date, with analyses typically completed within ~1.5 months of collection.

## Sampling network and geography
- Radial network specifics:
  - Points positioned at distances: 5, 6, 7, 8.3, 10, 12, 14.7, 17, 20, 25, 30, 37.5, 45, 52.5, and 60 km from ChNPP.
  - Directions spaced every 10° around the circle (10° to 360° clockwise).
- Georeferencing:
  - Based on maps and topography.
  - Excluded sites located in swamps, rivers, or lakes resulting in 489 sampled locations.

## Data quality, metadata, and provenance
- Uncertainty and confidence:
  - All radionuclide concentrations reported with 68% confidence intervals.
  - Site-level uncertainty can be up to ~50% when a single soil core is used to estimate average contamination density for the site.
- Lab and measurement context:
  - Primary instrument: gamma spectrometry with GEM-30185 ORTEC detector (two configurations mentioned).
  - Some cores analyzed at multiple laboratories; full inter-lab data not available.

## Data interpretation and usage notes
- Data product:
  - Provides dose rate in air (mR/h) and soil contamination densities (Bq/m^2) for multiple radionuclides as of the measurement date.
  - Includes exchangeable fraction data for Cs-134+Cs-137.
- Conversion and units:
  - Contamination densities converted using the area of sampling (0.015 m^2) with the standard conversion where 1 Ci/km^2 equals 37 kBq/m^2.
- Temporal context:
  - Measurements reflect radionuclide activity shortly after collection (within ~1.5 months).

## References
- Kashparov, V., Levchuk, S., Zhurba, M., Protsak, V., Beresford, N.A., Chaplow, J.S. Spatial radionuclide deposition data from the 60 km area around the Chernobyl nuclear power plant: results from a sampling survey in 1987. Earth System Science Data, 2019 (in press).
- Khomutinin, Yu.; Fesenko, S.; Levchuk, S.; Zhebrovska, K.; Kashparov, V. Optimising sampling strategies for emergency response: 1. Soil. Journal of Environmental Radioactivity, 2019 (in press).