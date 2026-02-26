# CEH Land Cover® Plus : Pesticides v2.0

## Purpose and scope
- Updates the CEH Land Cover® Plus : Pesticides product to cover Scotland and to map pesticide applications across England, Wales, and Scotland at 1 km resolution.
- Provides estimates of average annual pesticide applications (kg of active ingredient per year) for 162 active ingredients, using a 2012–2017 timeframe.
- Includes accompanying uncertainty maps to quantify confidence in estimated applications.
- Aims to support environmental health monitoring, risk assessment, and policy evaluation through standardized, traceable outputs.

## Key updates from v1.0
- Scotland coverage extended, enabled by Scottish Pesticide Survey data from SASA.
- Modelling refinements: removal of a global intercept term and updated GB extent to ensure consistent spatial coverage; some areas with high uncertainty where ingredients are regionally restricted.
- Temporal extension: inclusion of 2017 fodder and forage data for Scotland, extending temporal coverage to 2012–2017.
- Addition of 36 active ingredients not previously mapped.

## Data sources and inputs
- Pesticide Utilisation Survey (PUS) data for England and Wales (2012, 2014, 2016; with fodder/forage data for 2013) and Scotland (2012, 2014, 2016 arable; 2013, 2017 fodder/forage).
- Crop location data from CEH Land Cover® Plus : Crops to estimate crop areas within 1 km cells.
- County/local authority (LA) boundaries used to assign PUS records to spatial units; centroids used for location in modelling.
- Organic farming masking in England (via Organic Farming Scheme data); Wales/Scotland masking not implemented in this version.
- Spatial boundaries and crop area sources include OS Boundary Line (England/Wales) and SASA (Scotland).

## Methodology
- Data collation: summarize annual applications (kg/yr) by crop and county/LA; calculate annual application rates as kg per km² for each crop; exclude ingredients with too few observations (fewer than 10) prior to modelling.
- Modelling: annual application rates (kg/km²) modelled as a function of crop type and county location using a Lognormal distribution plus a Gaussian Markov Random Field (GMRF) spatial field estimated with INLA.
- Spatial assumption: a single spatial pattern applied across crops; years treated as independent replicates due to limited data for robust temporal trends.
- Prediction: for England, Scotland, and Wales, apply the spatially smoothed rates to 1 km cells using crop areas from LC Plus Crops (averaged over 2015–2017); sum across crops within each cell to obtain total annual application per active ingredient.
- Handling multiple estimates: for crops with multiple LC Plus Crops estimates (e.g., field beans vs. beans/peas), average estimates to avoid double counting.
- Uncertainty: propagate parameter uncertainty by drawing 100 samples per parameter (intercept, crop effects, spatial term) to build a distribution of total 1 km cell estimates; report 2.5th–97.5th percentile range as 95% interval; express uncertainty as a percentage of the mean estimate.

## Outputs and formats
- Output files at 1 km resolution in TIF or shapefile formats.
- Each file contains two layers in the British National Grid: 
  - Layer 1: estimated application (kg/year) per active ingredient.
  - Layer 2: corresponding uncertainty (percent).
- Data gaps occur in areas with no relevant crops (mountainous, urban) or where crops do not occur; some ingredients may have missing cells in limited crop ranges.

## Validation and quality
- No national independent validation dataset; regional totals compared against PUS statistics as a consistency check.
- Posterior predictive checks used to assess model performance (RMSE vs null models).
- For a subset of 11 ingredients, regional totals were compared; results varied by ingredient and region, with some discrepancies discussed (e.g., seed potatoes, Scotland data sparsity).
- Across the remaining ingredients, 162 models passed a primary RMSE test (out of 171; 9 failed and were removed), with 57% of remaining models passing a second spatial variation test.
- Overall, the product includes 162 active ingredients; 36 new ingredients added from v1.0.

## Differences vs v1.0
- Scotland coverage added; similarities in England/Wales patterns for many ingredients.
- Differences arise for potatoes/seed potatoes due to Scotland’s data and how seed potatoes are classified in LC Plus Crops.
- v2.0 includes 36 additional ingredients; some changes reflect data availability and spatial mapping adjustments.

## Data access, citation, and licensing
- Data can be accessed via the Environmental Information Data Centre (EIDC).
- Users should cite: Jarvis et al. (2020). CEH Land Cover plus: Pesticides 2012-2017 (England, Scotland and Wales). NERC Environmental Information Data Centre. DOI: 10.5285/99a2d3a8-1c7d-421e-ac9f-87a2c37bda62.
- Licence fees may apply for some users and some applications.

## Usage and applications
- High-resolution mapping of pesticide applications supports exposure risk assessment, agrochemical runoff modelling, targeting management interventions, and analysis of wildlife population trends in relation to pesticide use.
- Standardised datasets and accompanying uncertainty enable scrutiny of environmental health and policy performance over time.
- Outputs from this dataset can be uploaded to relevant portals and integrated with underlying data sources to enable broader data reuse.

## Temporal coverage and interpretation
- Snapshot represents average applications from 2012–2017, derived from averaging 2012, 2015, 2016, and 2017 crop coverage (via LC Plus Crops) to reflect crop composition in each 1 km cell.
- Temporal variation is not explicitly modelled; uncertainties capture year-to-year variation and data limitations.

## Caveats and notes
- Uncertainty maps reflect both variation in application rates and the proportion of land cropped; highest uncertainty occurs where application rates vary over time or where cropping is inconsistent.
- Mountainous and urban cells are omitted; some ingredients may be underestimated if they are primarily used on non-cropped or underrepresented crops.
- England masking for organic areas is implemented; Wales/Scotland masking not yet in this version.

## Acknowledgements
- Contributions from Fera, SASA, and CEH collaborators in data provision and project support.