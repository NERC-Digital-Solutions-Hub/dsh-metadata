# Productivity in a dominant herbaceous species is largely unrelated to soil macronutrient stocks

## Aim
- Assess above-ground net primary production (NPP) of bracken (Pteridium aquilinum) from a single peak biomass sample to enable rapid, broad-site sampling.
- Explore links between bracken biomass and soil macronutrient stocks, environmental conditions, and floristic traits.
- Provide outputs in clear, standardized formats and contribute to consistent environmental monitoring over time.

## Study design and site selection
- Survey conducted 21 July 2014 – 6 August 2014.
- 49 plots identified across two regions: northern Snowdonia (North Wales) and the Lake District.
- Plots chosen to cover a range of geological substrates; approximately equal regional representation.
- Bracken stands required ≥80% cover and had not been trampled by grazing animals; bracken restricted to free-draining soils.

## Data sources and site context
- Mean annual precipitation: CEH-GEAR interpolated grid dataset.
- Location altitude: field GPS measurements.
- Nitrogen deposition: APIS 2015 estimates.
- Plot-level environmental traits inferred from species composition using indicator values.

## Measurements and sample processing
- Plot size: 1 × 1 m; all plant species recorded within plot boundaries.
- Bracken biomass: fronds cut at ground level, bulked, weighed; subsample (~500 g) dried at 60°C and reweighed to determine moisture content; total dry bracken biomass calculated.
- Other vegetation: cut at ground level and boundaries, dried at 60°C to constant weight.
- Biochemical analyses on bracken: 25 g subsample ground for chemical analysis; carbon and nitrogen measured by oxidative combustion with a thermal conductivity detector.
- Soil sampling: three subsamples per plot, 5 cm diameter auger to 15 cm depth (alternative holes recorded if stones blocked auger).
  - Fresh soil weighed; moisture content determined after drying.
  - Organic carbon determined by ignition at 350°C.
  - Bulk density calculated from soil mass and volume sampled.
  - pH measured in 10 g soil with 25 mL water.
  - Soils dried, sieved (2 mm), and ground for chemical analysis.
  - Total C, N, P, K, Ca, Mg measured by the same methods as plant tissue; organic P inferred from difference between total and inorganic P.
  - Inorganic P extracted with 0.5 M sulfuric acid, analyzed by molybdate colorimetry.

## Nutrient stocks and environmental indicators
- Soil nutrient stocks (g m⁻²) calculated for top 15 cm using bulk density; organic P and total K, Ca, Mg stocks used as indicators of availability.
- Soil total N/C ratio used as an indicator of N availability.
- Plant species data used to derive environmental trait scores (Ellenberg N, R, F, L); plot means computed from present species (UK-adjusted scores); no cover-weighting applied to minimize bracken dominance effects and to reduce short-term variation influence.

## Data analysis and statistical approach
- Software: R (version 3.2.2).
- Normality checks with Shapiro test; data transformed as needed for normality.
- Multivariate relationships explored with principal components analysis (PCA) after transformation and standardization.
- Biomass prediction assessed via analysis of variance (ANOVA) to test against the null model.
- Model selection: multiple linear models evaluated using Akaike’s information criterion (AIC) across three predictor categories:
  - Soil chemistry
  - Plant chemistry
  - Floristic/biophysical trait means and environmental variables
- Final evaluation included combinations of the best four predictors (from all categories) based on AIC for single-factor models.

## Datasets, data management, and outputs
- Outputs presented in standardised formats (e.g., biomass, nutrient stocks, environmental indicators, and model results).
- Datasets stored in appropriate repositories/portals with uploading and data stewardship practices.

## Challenges and data-use considerations
- Increasing the value of monitoring datasets by integrating them with related data sources (avoiding single-use datasets).
- Facilitating access to underlying data used to generate final outputs for transparency and reuse.

## Acknowledgements
- Funded by the UK Natural Environment Research Council (Macronutrient Cycling Research Programme; LTLS project) and the University of Liverpool.
- Acknowledgement of statistical advice and site access permissions.