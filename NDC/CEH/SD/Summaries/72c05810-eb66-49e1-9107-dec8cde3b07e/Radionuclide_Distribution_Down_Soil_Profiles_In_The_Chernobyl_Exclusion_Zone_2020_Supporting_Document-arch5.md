# Radionuclide distribution down soil profiles in the Chernobyl Exclusion Zone 2020

## Overview
- Study conducted after the April 2020 wildfires in the Chernobyl Exclusion Zone to measure the migration of Cs-137 and Sr-90 in soils.
- Field work occurred in September–October 2020 across three forested study sites with varying fire impact.
- Aims to characterize vertical distribution of radionuclides to a depth of 1 m and provide data for understanding post-fire radionuclide redistribution.

## Study sites and sampling design
- Three study sites within forest plantations on the left bank of the Pripyat River (Chornobyl Exclusion Zone):
  - Site 1: Control, not damaged by fire.
  - Site 2: Slightly affected by fire (soot height up to 2 m).
  - Site 3: Heavily affected by fire (soot height up to 7 m; no trees survived).
- Plot sizes and layout:
  - Site 1: 250 m^2 plot (radius 8.9 m).
  - Site 2: 100 m^2 plot (radius 5.64 m).
  - Site 3: 250 m^2 plot (radius 8.9 m).
- Tree data collection occurred on Oct 8, 2020, including coordinates, diameter, height, and condition (dead/alive).

## Field methods
- At each site, three circular plots were established; within each plot, three soil sampling points were used (center plus two opposite edges).
- Litter/ash samples collected from a 0.078 m^2 area at each sampling point.
- Soil sampling depths (layer-by-layer) extended to 1 m but with specific depth intervals:
  - 0-10 cm, 10-20 cm, 20-30 cm, 40-50 cm, 50-60 cm, 60-70 cm, 70-80 cm, 80-90 cm, and 90-100 cm.
- Dry mass measurement:
  - One sampling point per site had a sub-sample for dry mass determination (up to 180 g fresh mass).
  - Dry mass per 1 m^2 calculated; dry mass of litter/ash also calculated.

## Laboratory methods and QA
- Sample preparation:
  - All samples air-dried, homogenised; sub-samples taken for Cs-137 and Sr-90 analysis.
  - Soil samples dried at 105°C and sieved through a 1-mm mesh.
- Cs-137 analysis:
  - Low-background gamma spectrometry with a germanium detector; spectra analysed with GammaVision software.
- Sr-90 analysis:
  - Non-destructive beta-spectrometry using a scintillation beta-spectrometer; deconvolution of a mixed beta spectrum with AkWin software.
  - Calibration with certified mono-radionuclide standards (137 Cs, 90 Sr, 40 K) in identical geometry and matrix.
  - Instrument specifics: energy resolution 10–15% for conversion electrons; background counts <0.4 cps in 200–1200 keV; MDA for 90 Sr+90Y in samples ~1 Bq (330 mg cm^-2 thickness, 10 h counting).
- Data outputs include activity concentrations (Bq kg^-1) with 2-sigma uncertainties and notes for values below detection limits.

## Datasets and data fields
- Dataset 1: Radionuclide_Distribution_Down_Soil_Profiles.csv
  - Site and sampling point identifier.
  - Assessment of the fire impact at the site.
  - Site location (latitude/longitude; WGS84).
  - Sampling date.
  - Cs-137 and Sr-90 activity concentrations (Bq kg^-1) with 2-sigma uncertainty; values below detection limits marked with "<".
  - Dry mass of soil (kg m^-2) per layer (0-10 cm to 90-100 cm).
  - Dry mass of litter/ash per sample where applicable.
- Dataset 2: Description_Of_Trees.csv
  - Site and tree identifier.
  - Tree genus.
  - Tree condition after wildfire (observed Oct 8, 2020).
  - Tree diameter (at 1.3 m height) and tree height (m).

## Usage context and provenance
- References for methods:
  - Ivanov et al. 1997. Migration of Cs-137 and Sr-90 from Chornobyl fallout in Ukrainian, Belarussian and Russian soils.
  - Courti et al. 2002. Beta spectrometry for environmental radioactivity measurements.
- Archive purpose: map vertical distribution of radionuclides and assess post-fire redistribution dynamics; enable cross-site comparisons and potential modeling of migration with depth and fire severity.

## Data governance and stewardship considerations
- Metadata and standardization
  - Ensure coordinates use consistent WGS84 format; clearly document coordinate precision.
  - Maintain consistent depth interval definitions and units (Bq kg^-1, kg m^-2).
  - Record measurement uncertainties (2-sigma) and detection limits; properly handle censored data (< detection limit).
  - Document laboratory methods, calibration standards, instrument models, and QA procedures to support reproducibility.
- Data quality and integrity
  - Validate that soil dry mass and litter/ash masses are correctly computed per 1 m^2 per depth layer.
  - Flag and review any 'ND' or missing values; determine if imputation or exclusion is appropriate.
- Usability and interoperability
  - Provide clear data dictionaries for both CSV files to enable reuse by other researchers and data portals.
  - Link dataset to related measurements (tree data) to support integrated analyses of fire impact, vegetation, and radionuclide distribution.
- Access, licensing, and updates
  - Establish a data access license and citation instructions; include references to the two methodological papers.
  - Plan for updates or corrections if future re-analyses or additional sampling occur; document versioning and change logs.

## References
- Ivanov, Y.A., Lewyckyj, N., Levchuk, S.E., Prister, B.S., Firsakova, S.K., Arkhipov, N.P, Arkhipov, A.N., Kruglov, S.V., Alexakhin, R.M., Sandalls, J., Askbrant, S. 1997. Migration of Cs-137 and Sr-90 from Chornobyl fallout in Ukrainian, Belarussian and Russian soils. Journal of Environmental Radioactivity, 35, 1-21. https://doi.org/10.1016/S0265-931X(96)00036-7
- Courti, A., Bouisset, P., Chevallier, P., 2002. Beta spectrometry for environmental radioactivity measurements. Radioprotection, 37, 911-916. https://doi.org/10.1051/radiopro/2002223