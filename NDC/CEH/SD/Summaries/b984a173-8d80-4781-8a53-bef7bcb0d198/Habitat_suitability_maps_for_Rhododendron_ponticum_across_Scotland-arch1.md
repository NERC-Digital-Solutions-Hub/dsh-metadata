# Habitat suitability maps for Rhododendron ponticum across Scotland as reservoir host for Phytophthora plant pathogens

## Aim and scope
- Describe methods, results, and quality control for modelling habitat suitability of Rhododendron ponticum (RP) across Scotland as a reservoir host for Phytophthora ramorum and Phytophthora kernoviae.
- Use to assess potential spillover risk to vulnerable habitats and infection sources.

## Data on Rhododendron ponticum occurrences
- 11 datasets (1950–2008) compiled; 70% of records volunteer-generated.
- Sources include Local Record Centres (LRCs) and the National Biodiversity Network (NBN) gateway.
- Edwards and Taylor (2008) contributed detailed RP stands in Argyll and Bute.
- All records summarized to 1 km x 1 km grid cells across Scotland: 82,690 cells with environmental data; 1,725 unique RP-present grid cells used for modelling.
- Presence data projected for habitat suitability modelling (Maxent).

## Habitat suitability modelling approach
- Modelling method: Maxent (maximum entropy), version 3.3.3e.
- Assumptions and biases addressed:
  - Invasive spread and sampling bias acknowledged; two adjustments tested:
    - Upweighting records with few geographic neighbours via a bias grid.
    - Testing background representations.
- Background options (areas from which pseudo-absences were drawn):
  - ALL: whole study area (Scotland) with available environmental data.
  - MCP: minimum convex polygons around each presence dataset, aggregated across regions.
  - REACH: reachable area defined by roads, railways, and urban land cover (gardens and roads promote spread).
- For each background, models run with and without upweighting, yielding six Maxent models.
- Model validation: 25 iterations with 30% held-out data each time; both linear and quadratic predictor terms included.
- Model projections produced for Scotland:
  - Mean predicted habitat suitability map
  - Standard deviation map
  - Clamping map (predictor values outside training range)
- Binary suitability maps created using threshold maximizing test set sensitivity + specificity.
- Model evaluation metrics:
  - AUC for training and test data
  - Predicted-to-Expected (P/E) ratio; monotonic increase indicates good calibration
  - Spearman correlations between predicted habitat suitability and RP cover (Argyll and Bute)
- Additional analyses:
  - Coincidence of RP-suitable habitat with potential sources of infection and with vulnerable habitats (native woodland, heathland, Larix kaempferi distributions)
  - Premises categorized as trade (nurseries, garden centres, wholesalers) vs non-trade (gardens, parks, hotels)

## Predictor variables
- Predictor variables and data sources:
  - Broad-leaf forest cover (BLWOOD) – dominant contributor
  - Coniferous forest cover (CWOOD)
  - Elevation (ELEV)
  - Annual mean Enhanced Vegetation Index (EVI)
  - Annual mean Normalised Difference Vegetation Index (NDVI)
  - Dominant soil carbon content (Carbon)
  - Dominant soil pH (PH)
- Key findings on predictors:
  - Broad-leaved woodland: ~55.8% average contribution; higher RP habitat suitability with more broad-leaved woodland.
  - EVI, soil carbon, elevation also important (around 9–12% each); elevation and soil carbon negatively related to suitability at extremes; EVI-related moisture effects nonlinear.

## Model results and validation
- Background choice effect:
  - ALL background with no weighting yielded the best overall performance; MCP background performed worst.
  - Upweighting records with few neighbours did not improve accuracy across background types.
- Model performance:
  - Best model (ALL background, unweighted) showed training AUC ≈ 0.838 and test AUC ≈ 0.831.
  - Predicted/Expected ratio increased with higher habitat suitability, indicating good model discrimination.
  - Omission tests indicated reasonable independence between training and test sets; weighted models showed poorer omission alignment, suggesting weighting amplified clustering.
- RP habitat and model fit:
  - 24% of Scotland’s 1 km grid cells predicted as RP-suitable habitat.
  - Substantial positive correlation between predicted RP suitability and RP cover in Argyll and Bute (Spearman ρ ≈ 0.58; p < 0.0001).
- Spatial patterns:
  - Contiguous high-suitability areas in Great Glen, central belt (Edinburgh–Glasgow), Fife, Perthshire, and parts of SE/Northeast coasts.
  - Predictions more uncertain at high elevations.
- Infection risk linkage:
  - Of premises inspected for P. kernoviae and P. ramorum, 71–73% occurred in cells predicted suitable for RP.
  - Non-trade (garden) premises: 23% in highly suitable RP habitat (vs 13% overall); 64% of Larix kaempferi populations occurred within RP-suitable habitat, 14% within highly suitable RP habitat.
- Vulnerable habitats overlap:
  - Core native woodland: 54% coincided with RP-suitable habitat; 10% within highly suitable RP habitat.
  - Heathlands: most of these outside RP-suitable habitat in SW Scotland, though some fringes near woodlands and Larix kaempferi align with RP suitability and potential infection sources.

## Implications and applications
- Highlights areas in Scotland where RP presence could support Phytophthora infection risk, guiding surveillance and management.
- Emphasizes importance of broad-leaved woodlands in determining RP habitat suitability; cautions on overreliance on data-poor areas and on background selection.
- Indicates concentration of risk around nurseries/garden trade premises and non-trade premises with RP-suitable habitat, informing biosecurity and monitoring priorities.
- Demonstrates the value of integrating diverse datasets (LRCs, NBN, forest/land cover, climatic proxies) and careful background representation to model invasive reservoir hosts.

## Supplementary context
- Tables and figures illustrate data sources (Table 1), predictor contributions (Table 2), and model evaluation metrics (Table 3), as well as maps and overlap analyses (Figures 1–5).
- Data and analyses implemented in GIS and statistical tools (e.g., ArcGIS 9.3, Maxent) with supplementary information S1–S6 referenced for methods like bias grids and background calculations.