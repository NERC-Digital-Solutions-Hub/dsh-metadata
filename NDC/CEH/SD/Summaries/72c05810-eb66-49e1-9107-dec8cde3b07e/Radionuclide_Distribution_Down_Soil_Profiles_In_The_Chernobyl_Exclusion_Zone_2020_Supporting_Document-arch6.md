# Radionuclide distribution down soil profiles in the Chernobyl Exclusion Zone 2020

## Purpose and study context
- Presents results of a study conducted after the April 2020 wildfires to measure the migration of 137Cs and 90Sr in soils.
- Fieldwork conducted September/October 2020 across three forest sites within the Chornobyl Exclusion Zone (left bank of the Pripyat River).

## Study sites
- Site 1: control, not damaged by fire.
- Site 2: slightly affected by fire (soot up to 2 m on trees), near Site 1.
- Site 3: heavily affected by fire (soot up to 7 m), no surviving trees.
- All sites are pine-dominated forest plantations.

## Field sampling design
- Sampling date: September 21, 2020; tripod installed at plot center; coordinates recorded October 8, 2020.
- Plot sizes: Site 1 and Site 3 ≈ 250 m2 (radius 8.9 m); Site 2 ≈ 100 m2 (radius 5.64 m).
- Sampling points per plot: three (center and two opposite edges).
- Litter/ash sample area: 0.078 m2.
- Soil sampling depths per point: 0–10 cm, 10–20 cm, 20–30 cm, 40–50 cm, 50–60 cm, 60–70 cm, 70–80 cm, 80–90 cm, 90–100 cm (up to 1 m total).
- Dry mass sampling: at one point per site; fresh mass weighed in the field, dried at 105°C; dry mass per m2 calculated.
- Tree data collection within plots: diameter at breast height (1.3 m) and tree height; condition recorded (dead/alive) on Oct 8, 2020.

## Laboratory analyses
- Sample preparation: air-dried; homogenised; sub-sample for Cs-137 and Sr-90; soils dried to 105°C and sieved to 1 mm.
- Cs-137: measured with low-background gamma spectrometry (Ge detector) and analyzed with GammaVision software.
- Sr-90: measured with beta spectrometry; calibration with certified mono-radionuclide standards; spectral deconvolution with AkWin software.
- Uncertainty and detection: activity concentrations reported with 2-sigma uncertainty; background counts and method specifics noted.
- Minimum detectable activity (MDA) for 90Sr+90Y in typical sample geometry provided.

## Datasets provided
- Radionuclide_Distribution_Down_Soil_Profiles.csv
  - Site and sampling point identifiers.
  - Fire impact assessment per site.
  - Site coordinates (latitude/longitude, WGS84).
  - Sampling date.
  - Cs-137 and Sr-90 activity concentrations (Bq/kg) with 2-sigma uncertainty; values below detection limits indicated by <.
  - Dry mass of soil (kg/m2) at 10 cm intervals up to 1 m (ND if not determined).
- Description_Of_Trees.csv
  - Site and tree identifier.
  - Tree genus.
  - Tree condition after wildfire (observed Oct 8, 2020).
  - Tree diameter (at 1.3 m) and height (m).

## Data interpretation and potential analyses
- Enables vertical profiling of Cs-137 and Sr-90 down to 1 m and assessment of post-fire redistribution.
- Facilitates analysis of relationships between radionuclide distribution, fire severity, and tree/stand characteristics.
- Can be combined with other soil and forest datasets for broader studies of radionuclide migration in soddy-podzolic soils and post-wildfire dynamics.

## Data quality, limitations, and notes
- Some dry mass data are ND (not determined).
- Detection limits applied; some values shown as <.
- Depth coverage limited to specified sampling depths up to 1 m.
- Methodology aligned with referenced standard studies for soil radionuclide analysis.

## Practical considerations for data support
- Data are in accessible CSV format with geospatial coordinates suitable for mapping and dashboards.
- Keys for merging: Site ID, Sampling Point ID, and depth interval.
- Includes measurement uncertainties, enabling robust uncertainty-aware analyses and visualizations.

## References (methodology)
- Ivanov, Y.A., et al. 1997. Migration of Cs-137 and Sr-90 from Chornobyl fallout in Ukrainian, Belarussian and Russian soils.
- Courti, A., Bouisset, P., Chevallier, P. 2002. Beta spectrometry for environmental radioactivity measurements.