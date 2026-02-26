# Habitat suitability maps for Rhododendron ponticum across Scotland as reservoir host for Phytophthora plant pathogens

## Data sources and dataset assembly
- Eleven presence datasets for Rhododendron ponticum in Scotland (1950–2008): mainly Local Record Centres (volunteer-recorded, ~70% of records), plus a National Biodiversity Network dataset and an Argyll and Bute dataset (Edwards & Taylor, 2008).
- Records at 1 km or finer; 1725 unique 1 km grid squares with R. ponticum; 82690 squares with environmental data.
- Presence data also categorized by cover type (dense, scattered, or controlled) to test relationships with predicted habitat suitability.

## Modelling approach
- Habitat suitability modelling with Maxent (version 3.3.3e).
- Model setup: 25 iterations with 30% of data withheld for cross-validation; linear and quadratic terms for predictors.
- Six alternative Maxent models based on:
  - Three background options: ALL (whole study area), MCP-based maximum survey extent, REACH (roads, rails, urban areas).
  - With or without upweighting of records to reflect sampling bias.
- Background options reflect differing assumptions about survey effort and accessible area.
- Outputs per model: mean predicted habitat suitability, standard deviation across iterations, and clamp maps.

## Data processing and predictor variables
- Environmental predictors (apriori selection): 
  - Broad-leaved forest (%; BLWOOD)
  - Coniferous forest (%; CWOOD)
  - Elevation (ELEV)
  - Enhancement vegetation index (EVI)
  - Normalised difference vegetation index (NDVI)
  - Dominant soil carbon content (Carbon)
  - Dominant soil pH (PH)
- Predictors derived and averaged at 1 km resolution; calculations performed in ArcGIS 9.3.

## Model evaluation and validation
- Model performance assessed with training and test AUC; additional metrics include predicted-to-expected (P/E) ratios and correlation with observed R. ponticum cover in Argyll and Bute (Spearman’s ρ).
- Upweighting (bias-adjustment) did not improve predictive accuracy; ALL background with no weighting performed best.
- Cross-validated stability assessed via withholding 30% of data across 25 iterations; clamping maps indicate extrapolation risk.

## Key predictors and their importance
- Broad-leaved woodland (BLWOOD) was the most influential predictor, contributing about 55.8% on average.
- Other important predictors (approximate contributions): soil carbon content (~11.6%), elevation (~10.7%), elevation-related effects; environmental moisture proxies (EVI ~9.1%), NDVI (~6.3%).
- Predictions indicated higher habitat suitability with more broad-leaved woodland, moderate moisture signals, and certain soil/altitude conditions.

## Results and interpretation
- Best model: ALL background with no weighting; mean training and test AUC ~0.83.
- Across Scotland, 24% of 1 km grid cells predicted as suitable habitat for R. ponticum.
- Premises inspections for Phytophthora species were disproportionately located within R. ponticum suitable habitat:
  - 71% of all inspected premises and 73% of non-trade garden premises fell in suitable cells.
  - 23% of non-trade garden premises occurred in highly suitable habitat (>0.65 probability) versus 13% of all inspected premises.
- Distribution patterns for other features:
  - 64% of Larix kaempferi populations occurred within suitable habitat; 14% within highly suitable areas.
  - 54% of core native woodland overlapped with suitable habitat; 10% within highly suitable zones.
  - Heathland largely outside suitable habitat, though some fringes exist where vulnerability and reservoir-host presence co-occur.
- Implications for surveillance and risk: areas where R. ponticum suitability overlaps with vulnerable habitats and plant-pathogen sources (nurseries, gardens, larix plantations) may pose higher risks for pathogen spread.

## Implications for monitoring and data sharing
- Demonstrates value of integrating multiple datasets to produce standardized habitat-suitability outputs for environmental monitoring.
- Highlights importance of addressing sampling biases and carefully choosing background areas to improve extrapolation and interpretation.
- Results support targeted surveillance and risk assessment by overlaying predicted suitability with habitat networks, premises data, and potential reservoir-hosts.

## Limitations and caveats
- Invasive species may not be in equilibrium with environment; presence records can be clustered, affecting model bias.
- Background selection and weighting choices influence results; although weighting did not improve accuracy here, they remain a critical consideration.
- Predictions depend on predictor choice and data resolution; clamping maps indicate where projections extend beyond training data ranges.

## Conclusion
- The study provides a robust Maxent-based map of Rhododendron ponticum habitat suitability across Scotland, identifying broad spatial patterns and areas where reservoir-host presence coincides with premises and vulnerable habitats, informing monitoring, surveillance prioritization, and policy planning for emergent Phytophthora pathogens.