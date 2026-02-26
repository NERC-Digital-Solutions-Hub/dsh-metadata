# Radionuclide distribution down soil profiles in the Chernobyl Exclusion Zone 2020

## Objective and context
- Assess migration of radionuclides 137Cs and 90Sr in soils after the April 2020 wildfires in the Chernobyl Exclusion Zone.
- Study conducted in September–October 2020 across three forested study sites on the left bank of the Pripyat River (Chornobyl Exclusion Zone).
- Compare sites with varying fire impact: Site 1 (control, no fire), Site 2 (slightly affected), Site 3 (heavily affected).

## Study sites and sampling design
- Three circular plots per site with sizes 250 m2 (Sites 1 and 3) and 100 m2 (Site 2).
- Central tripod established; plot coordinates recorded; tree density and condition documented.
- At each site, three soil sampling points per plot: one near center, two near opposite edges.
- Litter/ash collected from 0.078 m2 area; soil samples collected in depth layers up to 1 m (0–10, 10–20, 20–30, 40–50, 50–60, 60–70, 70–80, 80–90, 90–100 cm).
- Dry mass determined for one sub-sample per site (max 180 g) to calculate dry mass per 1 m2; dry mass for litter/ash also calculated.

## Field procedures
- Sampling performed on September 21, 2020.
- Depth-resolved sampling to capture rapid vertical migration in soddy-podzolic Ukrainian Polissia soils.

## Laboratory analyses
- Samples air-dried, homogenised; sub-samples prepared for Cs-137 and Sr-90 analyses.
- Cs-137: low-background gamma spectrometry with GEM detector; spectra analysed with GammaVision 32.
- Sr-90: beta spectrometry (non-destructive); 60 g dry soil aliquots scanned; deconvolution performed with AkWin to resolve 90Sr, 137Cs, and 40K signals.
- Calibration with certified mono-radionuclide standards in matching geometry and matrix.
- Key performance: beta spectrometer energy range 100–3500 keV; energy resolution 10–15% for 137mBa; background <0.4 counts per second; minimum detectable activity for 90Sr+90Y ~1 Bq for 10 h counting.

## Datasets and metadata
- Radionuclide_Distribution_Down_Soil_Profiles.csv
  - Site and sampling point identifiers; fire impact assessment; site coordinates (latitude/longitude, WGS84); sampling date.
  - Cs-137 and Sr-90 activity concentrations (Bq kg-1) with 2-sigma uncertainties, in 10 cm depth intervals to 1 m; values below detection limits marked as <.
  - Dry mass of soil per 10 cm interval up to 1 m; ND for not determined.
- Description_Of_Trees.csv
  - Site and tree identifiers; genus; tree condition post-fire (as of Oct 8, 2020); diameter at breast height; tree height.

## Relevance to environmental monitoring objectives
- Provides depth-resolved data on post-fire radionuclide redistribution in forest soils, enabling assessment of environmental health and long-term radionuclide mobility.
- Uses standardized field and lab methods, enabling comparability across sites and potential temporal comparisons.
- Geolocated data and explicit metadata support integration with other environmental datasets (e.g., wildfire severity, soil properties, forest structure).

## Data quality, accessibility, and interoperability
- Clear documentation of sampling design, depths, and analytical methods; uncertainties reported with activity concentrations.
- Data are organized in machine-readable CSV formats with explicit field descriptions; designed for storage in monitoring portals or data repositories and subsequent sharing.

## References
- Ivanov, Y.A. et al., 1997. Migration of Cs-137 and Sr-90 from Chornobyl fallout in Ukrainian, Belarussian and Russian soils.
- Courti, A. et al., 2002. Beta spectrometry for environmental radioactivity measurements.