# Uncertain effectiveness of Miscanthus bioenergy expansion for climate change mitigation explored using land surface, agronomic and integrated assessment models

## Aim and scope
- Assess yield potential and soil carbon impacts of large-scale Miscanthus bioenergy production.
- Compare three modelling approaches (land surface, agronomic, and integrated assessment) to evaluate the potential effectiveness for climate change mitigation.
- Explore outcomes under a single climate-social pathway: SSP2 with RCP2.6 (SSP2-RCP2.6).

## Models and data inputs
- Models used:
  - MiscanFor: crop growth model dedicated to Miscanthus.
  - JULES: Dynamic Global Vegetation Model.
  - IMAGE: Integrated Assessment Model.
- Climate and land-use pathways:
  - All models driven by SSP2-RCP2.6; land-use expansion maps from IMAGE define bioenergy land use for all three models.
  - Meteorological inputs: HadGEM2-ES ISIMIP downscaled and bias-corrected to 1960–1999 climatology (2006–2099) for MiscanFor and JULES; IMAGE uses MAGICC-derived pathway downscaled similarly.
- Focus areas and purposes:
  - Tropics (2040–2049) and Europe (2090–2099) to illustrate early scale-up and later sustainable use for bioenergy feedstock with CCS.

## Outputs and indicators
- Primary outputs:
  - Bioenergy crop yield (MiscanFor directly; JULES/IMAGE biomass converted to dry matter).
  - Soil carbon change per hectare per year (per planted area for MiscanFor; per grid cell for JULES/IMAGE).
- Rationale: yield and soil carbon are key determinants of overall life-cycle carbon balance and common outputs across all models.

## Data structure and processing
- Data files and grid:
  - 6,858 grid cells selected from a global 0.5° grid (≈11% of global land area) that feature any bioenergy land use; remaining 89% not modeled for this scenario.
  - 12 output files (model_variable_period) in CSV (MiscanFor) or NetCDF (JULES, IMAGE) formats.
  - Data consolidated in MATLAB, regridded to 0.5°, and unit-converted to a common format.
- File content and units:
  - Each file contains columns: latitude, longitude, value.
  - Latitude/longitude align across all files; values correspond to either yield (t DM ha⁻¹ yr⁻¹) or soil carbon change (t C ha⁻¹ yr⁻¹).
  - Conversion: JULES/IMAGE biomass (t C) converted to dry matter using 48% carbon content assumption.
- Missing data:
  - NaN values indicate cells not modeled for certain periods/regions or where data are unavailable.

## Quality control and validation
- Models are state-of-the-art within their categories and subjected to rigorous testing and validation across multiple sites.
- Documentation of model versions and validation studies provided (e.g., Littleton et al. 2020, 2022; Daioglou et al. 2019; Doelman et al. 2019; Hempel et al. 2013; Shepherd et al. 2020).

## Data governance, access, and reproducibility
- The dataset underpins the referenced publication and provides raw model outputs for reproducibility.
- Model code accessibility:
  - JULES code publicly available via the Met Office repository (registration required).
  - Specific repository version used noted (r12164_biotiles_harvest).
- Data formats and metadata:
  - Clear documentation of grid, units, and data processing steps; cross-model harmonization (0.5° grid, unit conversions) aids comparability.
  - Some complexities arise from differing spatial definitions (per planted area vs. per grid cell) and missing data patterns, underscoring the need for careful metadata and data governance in monitoring frameworks.

## Relevance to monitoring frameworks
- Provides measurable indicators for environmental monitoring and policy assessment:
  - Yield potential of Miscanthus bioenergy.
  - Soil carbon changes associated with land-use change for bioenergy.
- Highlights cross-model comparability, uncertainty, and scenario dependence critical for monitoring frameworks.
- Demonstrates strengths and gaps in data availability, standardization, and transparency needed for robust governance and decision support.

## Implications for policy and monitoring
- Under SSP2-RCP2.6, the uncertain effectiveness of Miscanthus expansion for climate mitigation suggests cautious interpretation of large-scale bioenergy deployment.
- Emphasizes the need for:
  - Standardized data formats, complete metadata, and accessible model code to enable ongoing monitoring and intercomparison.
  - Transparent communication of uncertainties and scenario assumptions to inform policy decisions.
  - Consideration of regional focus (tropics vs. Europe) due to differing biophysical and socio-economic contexts. 

## References (selected)
- Littleton, E.W., Shepherd, A., Harper, A.B., et al. (2022). Uncertain effectiveness of Miscanthus bioenergy expansion for climate change mitigation explored using land surface, agronomic and integrated assessment models. GCB Bioenergy, 15, 303-318.
- Littleton, E., Harper, A., Vaughan, N., Oliver, R., Duran-Rojas, M., & Lenton, T. (2020). JULES-BE: Representation of bioenergy crops and harvesting in the joint UK land environment simulator vn5.1. Geoscientific Model Development, 13, 1123-1136.
- Daioglou, V., Doelman, J. C., Wicke, B., Faaij, A., & van Vuuren, D. P. (2019). Integrated assessment of biomass supply and demand in climate change mitigation scenarios. Global Environmental Change, 54, 88-101.
- Doelman, J. C., Stehfest, E., et al. (2018). Exploring SSP land-use dynamics using the IMAGE model. Global Environmental Change, 48, 119-135.
- Hempel, S., Frieler, K., Warszawski, L., Schewe, J., & Piontek, F. (2013). A trend-preserving bias correction - The ISI-MIP approach. Earth System Dynamics, 4, 219-236.
- Riahi, K., van Vuuren, D. P., Kriegler, E., et al. (2017). The shared socioeconomic pathways and their energy, land use, and greenhouse gas emissions implications. Global Environmental Change, 42, 153e168.
- Shepherd, A., Littleton, E., Clifton-Brown, J., Martin, M., & Hastings, A. (2020). Projections of global and UK bioenergy potential from miscanthus × giganteus — Feedstock yield, carbon cycling and electricity generation in the 21st century. GCB Bioenergy, 12, 287-305.