# Radionuclide distribution down soil profiles in the Chernobyl Exclusion Zone 2020

## Overview
- A dataset describing the migration of Cs-137 and Sr-90 in soils after the April 2020 wildfires in the Chernobyl Exclusion Zone.
- Based on fieldwork in September–October 2020 across three forested study sites with varying fire impact (control, slight burn, heavy burn).
- Combines soil radionuclide concentration data with site/tree information to support analyses of post-fire radionuclide redistribution in Ukrainian Polissia soils.

## Study sites and context
- Three sites located on the left bank of the Pripyat River within the Chornobyl Exclusion Zone, dominated by pine.
  - Site 1: control, not affected by fire.
  - Site 2: slight fire impact (soot up to 2 m on trees), near Site 1.
  - Site 3: heavy fire impact (soot up to 7 m), no trees survived.
- Each site documented fire impact and environmental context through plot-level data and tree measurements.

## Field methods
- September 21, 2020: circular plots established; plot sizes: Site 1 and 3 = 250 m² (radius 8.9 m), Site 2 = 100 m² (radius 5.64 m).
- October 8, 2020: central tripod installed; coordinates and tree data (diameter, height, alive/dead) recorded.
- Soil sampling design:
  - Three sampling points per plot: center and two opposite edges.
  - Soil layers sampled from 0–100 cm in 10 cm increments, with a specified layer sequence (0–10, 10–20, 20–30, 40–50, 50–60, 60–70, 70–80, 80–90, 90–100 cm) and forest litter/ash collected from 0.078 m² area at each sampling point.
  - At one sampling point per site, a sub-sample (~180 g fresh mass) was taken to determine dry mass per soil layer; other samples weighed fresh and dried at 105°C.

## Laboratory methods
- Soil samples air-dried, homogenized, and sub-sampled for Cs-137 and Sr-90 analysis.
- Cs-137: measured with a low-background gamma spectrometer (germanium detector); spectra analyzed with GammaVision software.
- Sr-90: measured by beta-spectrometry using a scintillation detector; β-spectrum deconvolution performed with AkWin software.
- Calibration: using certified mono-radionuclide standards (137 Cs, 90 Sr, 40 K) in exact sample geometry and matrix.
- Analytical performance:
  - Energy range for deconvolution: 100–3500 keV.
  - β-spectrometer energy resolution 10–15% for conversion electrons; background <0.4 counts per second in 200–1200 keV.
  - Minimum detectable activity (MDA) for 90Sr+90Y: 1 Bq per sample (330 mg/cm²) with 10 h counting time.

## Datasets and file descriptions
- Radionuclide_Distribution_Down_Soil_Profiles.csv
  - Site and sampling point identifiers; fire impact assessment per site.
  - Site coordinates (latitude/longitude, WGS84).
  - Sampling date.
  - Cs-137 and Sr-90 activity concentrations (Bq/kg) with 2-sigma uncertainties; detection limits indicated as <.
  - Dry mass per 1 m² for each soil layer (10 cm intervals up to 1 m); ND if not determined.
- Description_Of_Trees.csv
  - Site and tree identifiers.
  - Tree genus; tree condition after wildfire (as observed Oct 8, 2020).
  - Tree diameter at 1.3 m height and tree height (m).

## Data quality, limitations, and governance
- Includes measurement uncertainties (2-sigma) and explicit MDA for Sr-90 measurements.
- Soil depth coverage up to 100 cm with specific 10 cm interval scheme, noting a gap in the 30–40 cm layer sequence.
- Limited number of study sites (three) and sampling points per plot, which may influence spatial generalizability.
- Data discoverability enhanced by explicit geolocation (WGS84) and structured metadata describing sampling context and laboratory methods.

## Potential uses and relevance for data strategy
- Supports modeling of post-fire radionuclide redistribution in soils and depth profiles.
- Demonstrates end-to-end data stewardship: field design, laboratory analysis, and detailed metadata suitable for reuse in environmental radiological studies.
- Highlights importance of linking environmental disturbance (wildfire impact) with contaminant distribution and biological context (tree condition).
- Provides a clear example of dataset documentation, including units, detection limits, uncertainties, and data provenance, aligning with data governance and stewardship goals for data leaders. 

## References
- Ivanov, Y.A. et al. 1997. Migration of Cs-137 and Sr-90 from Chornobyl fallout in Ukrainian, Belarussian and Russian soils. Journal of Environmental Radioactivity.
- Courti, A. et al. 2002. Beta spectrometry for environmental radioactivity measurements. Radioprotection.