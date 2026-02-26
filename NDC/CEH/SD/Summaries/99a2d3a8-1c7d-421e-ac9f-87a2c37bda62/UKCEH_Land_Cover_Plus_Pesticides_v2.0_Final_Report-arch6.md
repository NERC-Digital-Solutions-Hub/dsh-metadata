# CEH Land Cover® Plus : Pesticides v2.0

- Purpose: A GB-wide dataset delivering 1 km resolution estimates of pesticide application rates (kg active ingredient per year) for 162 active ingredients, plus accompanying uncertainty, for England, Scotland, and Wales, covering an average period 2012–2017. Outputs include application maps and uncertainty maps in TIFF or shapefile formats to enable exploration and analysis of pesticide use patterns.

- Key updates from v1.0:
  - Scotland included using SASA data; Scotland coverage extended.
  - Modelling refined by removing a global intercept and expanding spatial extent to GB; each application map covers the same spatial extent, with higher uncertainty in areas with little data.
  - Temporal coverage extended to 2012–2017 (including 2017 fodder and forage data for Scotland).
  - 36 additional active ingredients added to the mapping.

- Data sources and coverage:
  - Pesticide Utilisation Surveys (PUS) for England, Wales, and Scotland (2012–2017 with varying crop year coverage) including foliar and seed treatments.
  - Crop presence/area data from CEH Land Cover Plus: Crops to assign per-1 km2 crop areas.
  - County/Local Authority (LA) boundaries and centroids for location assignment; Scottish boundaries provided by SASA.
  - Organic Farming Scheme (England) used to mask organic areas; (Wales/Scotland masking not implemented in this version).
  - British National Grid projection; 1 km resolution; outputs include both application and uncertainty layers.

- Product specification and outputs:
  - Resolution: 1 km; units: kg active ingredient per year; output layers:
    - Layer 1: estimated application (kg/yr) per active ingredient.
    - Layer 2: uncertainty (percentage) associated with the estimated application.
  - 162 active ingredients (herbicides, insecticides, molluscicides, fungicides) included; 36 new ingredients compared with v1.0.
  - Temporal context: snapshot of average applications 2012–2017, using 2015–2017 crop coverage to reflect cropping patterns.
  - Missing data areas: mountains, urban areas, and cells without relevant crops; organic areas masked in England.

- Methodology: data collation, modelling, predictions, and uncertainty
  - Data collation:
    - PUS data from 2012, 2013 (fodder/forage only), 2014, 2016; Scotland includes 2017 fodder/forage data.
    - Data cleaned to remove unspecified actives, non-pesticide uses, and non-pesticide controls.
    - Annual applications per crop and per county/LA calculated; annual application rate = total kg of active ingredient applied / area grown (km2).
    - Active ingredients with fewer than 10 observations were excluded early; 171/189 ingredients progressed to modelling.
  - Spatial assignment:
    - County/LA boundaries linked to PUS data; centroids used for location.
  - Modelling approach:
    - Annual application rates (kg/km2) modelled as a lognormal function of crop type and county location.
    - Spatial variation captured with a Gaussian Markov Random Field (GMRF) via INLA; assumes a common spatial pattern across crops.
    - Years treated as independent replicates due to limited data to estimate temporal trends.
  - Predictions:
    - 1 km cell predictions use crop areas from LC Plus Crops averaged 2015–2017.
    - Organic areas masked in England; not masked in Wales/Scotland in this version.
    - For crops with multiple LC Plus Crops estimates (e.g., field beans vs. beans/peas), an average is used to avoid double counting.
    - Total per cell = sum over crops of (crop-area in cell × crop-specific application rate).
  - Uncertainty and validation:
    - 100 draws from parameter distributions produce a distribution of estimates per 1 km cell; 2.5th to 97.5th percentile interval used to derive 95% CI.
    - Relative uncertainty = (97.5th quantile − 2.5th quantile) / mean × 100.
    - Validation: regional totals compared to PUS statistics; posterior predictive checks computed RMSE against null models (constant across space) and a crop-varying model; 9/162 models failed the first RMSE test and were excluded; 93 of the remaining 162 models passed the second RMSE test.
    - No independent national-scale validation data; regional totals used for sanity checks; results vary by ingredient and region.

- Differences between v1.0 and v2.0:
  - Scotland added; vegetable/seed potato patterns and mapping shifts observed due to Scotland-specific data and LC Plus Crops category mappings (“other” crops may include seed potatoes).
  - Overall patterns similar; some ingredients show regional shifts driven by crop-specific mapping and data availability.

- Outputs and example interpretation:
  - Example outputs (e.g., diflufenican) show spatial gradients with higher average applications in central/eastern England and Scotland; lower in western regions and Wales; white areas indicate no data (e.g., mountains/urban areas).
  - Uncertainty maps illustrate higher relative uncertainty where data are sparse or where application rates vary markedly over time.
  - Appendix materials provide detailed validation results by region and ingredient, and lists of ingredients that passed/failed statistical tests.

- Access, citation, and acknowledgements:
  - Data accessible via Environmental Information Data Centre (eidc.ceh.ac.uk); licence fees may apply.
  - Citation: Jarvis, S.G.; Redhead, J.W.; Henrys, P.A.; Risser, H.A.; Da Silva Osório, B.M.; Pywell, R.F. (2020). CEH Land Cover plus: Pesticides 2012-2017 (England, Scotland and Wales). NERC Environmental Information Data Centre. DOI provided.
  - Acknowledgements to data providers (Fera, SASA) and CEH colleagues.