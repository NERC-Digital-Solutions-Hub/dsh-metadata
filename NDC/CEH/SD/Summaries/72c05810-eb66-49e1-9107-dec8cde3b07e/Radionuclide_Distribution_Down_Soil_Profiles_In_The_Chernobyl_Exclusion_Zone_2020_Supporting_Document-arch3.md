# Radionuclide distribution down soil profiles in the Chernobyl Exclusion Zone 2020

## Aim and Context
- Following severe wildfires in April 2020, this study (Sept–Oct 2020) measures the vertical migration of Cs-137 and Sr-90 in soils.
- Three study sites within the Chornobyl Exclusion Zone (forest plantations on the left bank of the Pripyat River) with differing fire impacts (control, slight, heavy).

## Study Sites and Design
- Site 1: control (no fire damage); Site 2: slight fire impact (soot up to 2 m); Site 3: heavy fire impact (soot up to 7 m); all sites dominated by pine.
- Plots: Site 1 and Site 3—250 m² (radius 8.9 m); Site 2—100 m² (radius 5.64 m).
- At each site:
  - Central tripod established; plot coordinates recorded; tree data collected (diameter, height, alive/dead).
  - Three soil sampling points per circular plot: center and two edges (opposite directions).
  - At each sampling point, collect forest litter/ash (0.078 m²) and soil in depth layers up to 1 m (0–10 cm, 10–20 cm, 20–30 cm, 40–50 cm, 50–60 cm, 60–70 cm, 70–80 cm, 80–90 cm, 90–100 cm).

## Field Methods
- Layer-by-layer soil sampling to capture rapid radionuclide migration in soddy-podzolic Ukrainian Polissia soils.
- Dry mass determination:
  - Sub-sample taken at one sampling point per site to determine dry mass per soil layer.
  - Fresh mass weighed in the field; dried at 105°C; dry mass per m² calculated.
- Litter/ash dry mass also recorded.

## Laboratory Analysis
- Sample preparation: air-dry, homogenise; sub-sample for Cs-137 and Sr-90 analyses; soil dried to 105°C and sieved to 1 mm (litter/ash not sieved).
- Cs-137 analysis: low-background gamma spectrometry with a GEM detector; data processed with GammaVision 32.
- Sr-90 analysis: non-destructive beta spectrometry; calibration with certified standards; spectral deconvolution with AkWin.
- Quantification:
  - Sr-90 quantified via calibrated beta spectrometry; energy range 100–3500 keV; MDA for Sr-90+Y in typical samples ~1 Bq (10 h counting).
  - Calibration ensures identical geometry and matrix to samples.
- Data quality indicators: detector characteristics (energy resolution, linearity, stability) and background counts stated.

## Datasets Provided
- Radionuclide_Distribution_Down_Soil_Profiles.csv
  - Site and sampling point identifier; fire impact assessment; site location (latitude/longitude, WGS84); sampling date.
  - Cs-137 and Sr-90 activity concentrations (Bq kg⁻¹) with 2-sigma uncertainties, in 10 cm depth intervals to 1 m.
  - Dry mass per 1 m² for each layer (ND if not determined); values below detection limits noted as <.
- Description_Of_Trees.csv
  - Site and tree identifiers; tree genus; tree condition after wildfire (as of Oct 8, 2020); tree diameter (at 1.3 m) and height.

## Data Quality, Limitations and Uncertainties
- Depth-resolved radionuclide measurements enable assessment of vertical migration post-fire.
- Detection limits and measurement uncertainties explicitly recorded; some values are below detection thresholds (<) or not determined (ND).
- Metadata includes precise location, sampling dates, and fire impact levels to support reproducibility and cross-site comparisons.

## Relevance for Monitoring Frameworks
- Demonstrates a structured, multi-layer soil sampling approach to monitor radionuclide mobility under disturbance (wildfire) scenarios.
- Integrates robust laboratory QA/QC (calibration with matrix-matched standards, explicit MDA) to ensure traceability and data reliability.
- Produces rich metadata (site, depth, fire impact, dates, geographic coordinates) suitable for integration into monitoring dashboards, trend analyses, and policy-informed risk assessments.
- Highlights governance-relevant aspects for monitoring work: clear metadata, uncertainty quantification, and accessible, well-documented datasets.

## References
- Ivanov, Y.A. et al. 1997. Migration of Cs-137 and Sr-90 from Chornobyl fallout in Ukrainian, Belarussian and Russian soils.
- Courti, A. et al. 2002. Beta spectrometry for environmental radioactivity measurements.