# Methods lifted from Productivity in a dominant herbaceous species is largely unrelated to soil macronutrient stocks

## Overview
- Study aims to rapidly assess above-ground net primary production (NPP) of bracken across multiple sites and relate biomass to soil chemistry, plant chemistry, and environmental variables.
- Survey conducted July 21 to August 6, 2014, across 49 plots in two UK regions (North Wales/Snowdonia and the Lake District) chosen to cover varied substrates and ensure at least 80% bracken cover.
- Sites selected from ground observations and Google Earth imagery; stands on free-draining soils and not trampled by grazing animals.
- Data collected include bracken biomass, soil properties, plant and soil chemistry, and environmental context (precipitation, altitude, nitrogen deposition).
- Analyses performed in R to identify predictors of total above-ground bracken biomass.

## Data Collected
- Bracken biomass
  - Plots: 1 × 1 m, minimum 80% bracken cover.
  - Fronds cut at ground level, bulked and weighed (fresh weight).
  - Subsample (~500 g) weighed, dried at 60°C to constant weight, re-weighed to determine moisture content.
  - 25 g subsample of dry bracken fronds ground for chemical analysis.
- Vegetation
  - All plant species within plot recorded (presence-absence used for environmental indicators).
- Soil sampling and analysis
  - Three sampling spots per plot with a 5 cm diameter split-tube auger to 15 cm depth (or excavations where stones prevented auger use).
  - Fresh sample weighed; moisture content measured after drying; organic C concentration by ignition at 350°C for 3 days.
  - Bulk density calculated from sample mass and volume.
  - pH measured in a soil-water slurry (10 g soil in 25 mL water).
  - Remaining soil dried; stones/roots removed; ground; subsamples taken for chemical analysis.
  - Total concentrations measured for C, N, P, K, Ca, Mg using methods identical to plant tissue analyses.
  - Organic P derived as total P minus inorganic P.
  - Inorganic P extracted from milled sub-sample (0.5 g) with 25 mL 0.5 M H2SO4, shaken 16 h, centrifuged, and analyzed by molybdate colorimetry (AQ2 analyzer).
  - Stocks calculated (g m^-2) for top 15 cm using bulk density; organic P stock and total K, Ca, Mg stocks used as indicators of availability.
- Environmental and regional context
  - Mean annual precipitation from CEH-GEAR dataset.
  - Site altitude measured in the field with GPS.
  - Site-specific nitrogen deposition estimates from APIS (2015).
- Floristic indicators
  - Environmental trait scores calculated from presence-absence data using Diekmann (2003) indicator values.
  - Ellenberg indicator values (N, alkalinity R, moisture F, light L) computed for UK species via Hill et al. (2000) and averaged across present species (no cover weighting).

## Data Sources and Tools
- Precipitation: CEH-GEAR dataset.
- Nitrogen deposition: APIS (2015).
- Indicator values: Ellenberg values adapted for UK species (Hill et al., 2000); Diekmann (2003) trait scores.
- Statistical analyses: R, version 3.2.2.

## Data Processing and Quality Assurance
- Normality assessed with Shapiro tests; transformations applied as needed to achieve normal/near-normal distributions.
- Data normalization prior to analyses (mean-centering and scaling).
- Handling of sampling constraints (e.g., plots with stones prevented full 15 cm depth sampling).
- Stocks used for interpretation to reflect nutrient availability in dense soils; presence-absence data used to reduce susceptibility to short-term environmental variation.

## Analyses and Modelling
- Exploratory data analysis
  - Principal components analysis (PCA) to explore relationships among biomass and explanatory variables, with appropriate transformations and normalization.
- Hypothesis testing
  - Analysis of variance (ANOVA) to test significant effects on biomass relative to predictors.
- Model selection and prediction
  - Akaike’s information criterion (AIC) used to select the best combinations of predictors from three categories: soil chemistry, plant chemistry, and floristic trait means plus biophysical variables.
  - Evaluated combinations of the best four predictors from all categories; also tested cross-category combinations of the best four predictors.

## Outputs and Data Products
- Quantified relationships between bracken biomass and soil/plant chemistry, floristic indicators, and environmental context.
- Derived predictor-based models to estimate above-ground bracken biomass at the plot level.
- Detailed dataset including biomass measurements, soil chemical stocks, nutrient concentrations, and environmental covariates enabling cross-site comparisons and potential meta-analyses.

## Acknowledgements and References
- Funded by the UK Natural Environment Research Council (Macronutrient Cycling LTLS) and the University of Liverpool.
- Acknowledgement of statistical and field contributions; references listed for methods and indicator values used.