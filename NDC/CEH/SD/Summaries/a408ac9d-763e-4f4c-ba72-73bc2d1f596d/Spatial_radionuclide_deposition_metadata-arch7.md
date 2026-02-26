# Column heading explanations and materials and methods for: Spatial radionuclide deposition data from the 60 km area around the Chernobyl nuclear power plant: results from a sampling survey in 1987

## Overview
- Describes a GIS-friendly dataset of radionuclide deposition in the 60 km zone around the Chernobyl NPP, collected in 1987.
- Data are prepared for mapping contamination patterns and supporting long-term monitoring.

## Sampling design and fieldwork
- Radial network: sampling points arranged every 10° (10° to 360° clockwise) at multiple distances from the ChNPP reactor 4 (5, 6, 7, 8.3, 10, 12, 14.7, 17, 20, 25, 30, 37.5, 45, 52.5, 60 km) for a total planned 540 points.
- Realized fieldwork: 489 of 540 selected points were sampled; sampling excluded swamps, rivers, and lakes.
- At each site: soil cores collected with a 14 cm diameter, 5 cm depth; five sampling points per site arranged in an envelope design with 5–10 m spacing.
- Georeferencing: points were spatially located using maps and topography.
- Sampling goal: enable long-term contamination mapping and monitoring.

## Laboratory analysis and data products
- One soil core per site analyzed via gamma spectrometry (GEM-30185 ORTEC detector, ADCAM-300) to determine gamma-emitting radionuclide concentrations.
- Radionuclides measured: 95Zr+95Nd, 106Ru, 134Cs, 137Cs, 144Ce; a second set of cores was sent to other Soviet laboratories (data not available).
- Exchangeable fraction: leaching of a 100 g soil aliquot with 1 M NH4Ac (pH 7) to determine the exchangeable Cs-134+Cs-137 fraction.
- Dose and contamination metrics:
  - Dose rate in air at 1 m height (mR/h).
  - Contamination density for each radionuclide (Bq/m^2). Conversion: 1 Ci/km^2 = 37 kBq/m^2.
  - Reported with 68% confidence interval (one standard deviation).
  - Inclusion of 134+137 Cs in exchangeable form (Bq/m^2).
- Data reporting notes:
  - Empty cells indicate data not available (e.g., sampling not performed at certain sites or for certain measurements).
  - Measured activity concentrations reflect the date of measurement; analysis occurred within ~1.5 months of collection.
  - Uncertainty for site-average estimates from a single 0.015 m^2 sampling area may be up to ~50%.

## Data fields and interpretation for GIS use
- Spatial reference: each site is defined by distance from ChNPP (km) and direction (Angle_degree, 10–360°; 90° = east, 180° = south, 270° = west, 0/360° = north).
- Key fields:
  - Identifier: unique ID for each data record.
  - Distance_from_ChNPP_km: radial distance from ChNPP reactor 4.
  - Angle_degree: direction from the ChNPP.
  - Date_gamma_measurement: date of gamma activity measurement.
  - Exposure_dose_rate_mR/h: dose rate in air at 1 m height.
  - Absorbed_dose_rate_microGray/h: absorbed dose rate.
  - Zr-95_Bqm2, Nb-95_Bqm2, Ru-106_Bqm2, Cs-134_Bqm2, Cs-137_Bqm2, Ce-144_Bqm2: soil contamination densities (Bq/m^2) for each radionuclide.
  - Zr-95_relative_error, Nb-95_relative_error, Ru-106_relative_error, Cs-134_relative_error, Cs-137_relative_error, Ce-144_relative_error: relative uncertainties (68% CL) for each measurement.
  - Exch_Cs-134+Cs-137_Bqm2: density of exchangeable Cs-134+Cs-137 in soil.
  - Instrument: gamma spectrometry instrument details (detector/model) used for measurements.
- GIS considerations:
  - Data enable creation of radial deposition maps, cross-sections, and isopleth visualizations.
  - Uncertainties should be propagated in GIS analyses where possible, especially for site-averages.
  - The dataset is anchored to a 1987 field campaign, useful for historical exposure mapping and temporal trend analyses when combined with newer datasets.

## Data quality, limitations, and references
- Data quality: measurements have 68% confidence intervals; potential up to ~50% uncertainty for site-average estimates from single-site cores.
- Coverage limitations: 540 planned points; 489 sampled; some areas not sampled due to presence of water bodies.
- Temporal context: measurements and analyses conducted in 1987, with results reported in 2019 as part of Earth System Science Data.
- References for deeper methodological context:
  - Kashparov et al., 2019, Earth System Science Data.
  - Khomutinin et al., 2019, Journal of Environmental Radioactivity (sampling strategy optimisation).