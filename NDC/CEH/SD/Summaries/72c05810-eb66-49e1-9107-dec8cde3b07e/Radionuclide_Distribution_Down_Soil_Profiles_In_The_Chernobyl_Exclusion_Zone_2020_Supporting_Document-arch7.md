# Radionuclide distribution down soil profiles in the Chernobyl Exclusion Zone 2020

## Overview
- Dataset documenting the migration of 137Cs and 90Sr in soils after the April 2020 wildfires in the Chernobyl Exclusion Zone, collected September–October 2020.
- Three forest study sites with varying fire impact (control, slight, heavy) located on the left bank of the Pripyat River within Chornobyl Exclusion Zone.
- Depth-resolved soil measurements up to 1 meter, plus forest litter/ash data and tree measurements.

## Study Sites and Field Layout
- Site 1: control (not damaged by fire).
- Site 2: slight fire impact (soot up to 2 m on trees).
- Site 3: heavy fire impact (soot up to 7 m; no trees survived).
- All sites: pine-dominated forest plantations.
- Field plots per site:
  - Site 1: 250 m² (radius 8.9 m)
  - Site 2: 100 m² (radius 5.64 m)
  - Site 3: 250 m² (radius 8.9 m)
- Sampling within each plot:
  - Three sampling points: center and two opposite-edge points.
  - At each point: forest litter/ash sample and soil samples from multiple layers.

## Sampling Methodology
- Soil samples collected layer-by-layer from depths: 0–10 cm, 10–20 cm, 20–30 cm, 40–50 cm, 50–60 cm, 60–70 cm, 70–80 cm, 80–90 cm, and 90–100 cm (up to 1 m depth; note the 30–40 cm interval is not sampled per the report).
- At one sampling point per site (point 1): sub-sample (max 180 g fresh) for dry mass determination; dry mass calculated per 1 m² for each layer.

## Laboratory Analysis
- Samples air-dried, homogenized; sub-samples prepared for Cs-137 and Sr-90 analysis.
- Cs-137: measured by low-background gamma spectrometry (germanium detector, GammaVision software).
- Sr-90: measured non-destructively by beta-spectrometry with calibration against certified standards.
- Uncertainties and sensitivity:
  - Cs-137 and Sr-90 activity concentrations provided with 2-sigma uncertainties.
  - Values below detection limits marked as <.
  - Beta-spectrometry method details include energy range and background conditions; minimum detectable activity for Sr-90+Sr-90Y is ~1 Bq under specified counting conditions.

## Datasets and File Structures
- Dataset 1: Radionuclide_Distribution_Down_Soil_Profiles.csv
  - Site and sampling point identifiers
  - Fire impact assessment per site
  - Site location (latitude/longitude; WGS84)
  - Sampling date
  - Cs-137 and Sr-90 activity concentrations (Bq/kg) with 2-sigma uncertainties
  - Dry mass per 1 m² for each soil layer (kg/m²)
  - Depth intervals: 0–10, 10–20, 20–30, 40–50, 50–60, 60–70, 70–80, 80–90, 90–100 cm
  - Values below detection: marked with “<”
- Dataset 2: Description_Of_Trees.csv
  - Site and tree identifiers
  - Tree genus
  - Tree condition after wildfire (as of Oct 8, 2020)
  - Tree diameter at breast height (DBH) and tree height (m)

## Data Attributes and Spatial Coverage
- Spatial data: site coordinates in WGS84; sampling points correspond to plot centers and edges within circular plots.
- Depth-resolved radionuclide data: 9 depth intervals up to 1 m, enabling depth profiles and vertical interpolation.
- Associated tree data per site: enables GIS analyses linking soil radionuclide distribution with vegetation status post-fire.
- Data quality indicators: 2-sigma uncertainties for concentrations; below-detection values noted; detailed lab methodology provides context for interpretation.

## GIS-ready Considerations and Potential Uses
- Map products:
  - Depth-profile maps of Cs-137 and Sr-90 concentrations per site/plot.
  - 3D visualization or cross-sections showing vertical distribution with depth.
  - Interpolation (kriging/IDW) across plots to create continuous surfaces of radionuclide activity by depth.
  - Overlay with fire impact indicators (soot height) to assess fire severity effects on radionuclide migration.
  - Joinable datasets: Radionuclide_Distribution_Down_Soil_Profiles.csv with Description_Of_Trees.csv via site and sampling point identifiers for integrated soil–vegetation analyses.
- Data integration considerations:
  - Ensure consistent handling of values marked as “<” (detection limits) in analyses and visualizations.
  - Respect depth interval gaps (notably 30–40 cm is not sampled) when creating uniform depth layers.
  - Use the provided coordinates (WGS84) for accurate georeferencing; incorporate plot geometry (circles with specified radii) if needed for spatial analyses.
- Temporal context: sampling conducted in Sept–Oct 2020; suitable for temporal comparisons with other post-fire datasets if available.

## References
- Ivanov, Y.A. et al. 1997. Migration of Cs-137 and Sr-90 from Chornobyl fallout in Ukrainian, Belarussian and Russian soils. Journal of Environmental Radioactivity.
- Courti, A. et al. 2002. Beta spectrometry for environmental radioactivity measurements. Radioprotection.