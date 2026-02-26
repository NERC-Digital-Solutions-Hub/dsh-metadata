# Radionuclide distribution down soil profiles in the Chernobyl Exclusion Zone 2020

## Purpose and study context
- Assess migration of Cs-137 and Sr-90 in soils following the April 2020 wildfires in the Chernobyl Exclusion Zone.
- Three forested study sites located on the left bank of the Pripyat River within the Chornobyl Exclusion Zone; pine-dominated stands.
- Site 1: control (not fire-damaged); Site 2: slight fire impact (soot up to 2 m); Site 3: heavy fire impact (soot up to 7 m; all trees killed).

## Study design and sampling sites
- Plots and sizes:
  - Site 1: 250 m^2 (radius 8.9 m)
  - Site 2: 100 m^2 (radius 5.64 m)
  - Site 3: 250 m^2 (radius 8.9 m)
- Sampling framework:
  - At each site, circular plots with three sampling points (central area and opposite edge points).
  - Litter/ash sampled over 0.078 m^2.
  - Depths sampled from 0 to 1 m in 10 cm intervals across multiple layers (0-10, 10-20, 20-30, 40-50, 50-60, 60-70, 70-80, 80-90, 90-100 cm).
  - One sampling point per site had a sub-sample for dry mass determination.
- Location data: site coordinates (latitude/longitude, WGS84) and sampling dates.

## Field procedures
- Soil sampling: rotary sampler (diameter 6.8 cm) to collect layer-by-layer samples at each plot point.
- Depth intervals chosen to capture rapid radionuclide migration in soddy-podzolic Ukrainian Polissia soils.

## Laboratory analyses
- Sample preparation: air-dry, homogenise, and sub-sample for Cs-137 and Sr-90 analysis; soils dried at 105°C and sieved to <1 mm.
- Cs-137 measurement: low-background gamma spectrometry with GEM-30185 detector; data processed using GammaVision.
- Sr-90 measurement: non-destructive beta-spectrometry (SEB-01-150) with calibration against certified standards; spectra deconvoluted using AkWin.
- Calibration and quality: standards contain Cs-137, Sr-90, and 40K; geometry/matrix matched to samples.
- Instrument performance: beta spectrum resolution 10-15% for conversion electrons; <1% linearity; <2% temporary instability; background <0.4 cps; minimum detectable activity for 90Sr+90Y ~1 Bq per 10 h for a 330 mg cm^-2 sample.

## Data products and dataset descriptions
- Radionuclide_Distribution_Down_Soil_Profiles.csv
  - Columns include: site and sampling point identifiers, fire impact assessment, site coordinates, sampling date, Cs-137 and Sr-90 activity concentrations (Bq/kg) with 2-sigma uncertainties, and dry mass (kg/m^2) per 10 cm interval up to 1 m.
  - Depth-wise data: values reported in 10 cm increments down to 1 m; below-detection values marked as "<".
- Description_Of_Trees.csv
  - Columns include: site and tree identifiers, tree genus, tree condition after wildfire (as of Oct 8, 2020), diameter at breast height (cm), and tree height (m).

## Considerations for analysis and modelling
- Enables analysis of vertical distribution and migration patterns of Cs-137 and Sr-90 post-fire.
- Facilitates correlations with fire severity, litter/ash input, and site location.
- Supports development of predictive models for radionuclide behavior in soddy-podzolic soils under wildfire disturbance.
- Data granularity includes uncertainties and per-layer dry mass, aiding unit-consistent concentration calculations; awareness of a missing 30-40 cm depth interval in the reported layers.