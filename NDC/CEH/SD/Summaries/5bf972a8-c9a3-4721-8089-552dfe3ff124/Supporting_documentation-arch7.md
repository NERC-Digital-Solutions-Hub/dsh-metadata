# Global inequities and political borders challenge nature conservation under climate change

- What the data are
  - Outputs from ensemble Species Distribution Models (SDMs) examining how socio-political factors influence bird and mammal biodiversity under climate change.
  - Three CSV datasets at global scope:
    - Climate_impacts_by_country.csv: national-level projections of changes in species richness (to 2070) and a governance metric for 189 countries.
    - Transboundary_richness.csv: current number of species whose ranges intersect each political border.
    - Transboundary_range_shifts.csv: projected number of species crossing each border under climate change.
  - Coverage: >12,700 terrestrial birds and mammals (≈80%), excluding species with highly restricted ranges.

- Data generation and methodology (GIS-friendly overview)
  - Modeling approach: ensemble SDMs using GAMs, GLMs, Random Forests, and Boosted Regression Trees.
  - Predictors: mean annual temperature, temperature seasonality, precipitation in wettest/driest months, and precipitation seasonality.
  - Projections: to 2070 under four climate scenarios (RCP 2.6, 4.5, 6.0, 8.5) using three GCMs (HadGEM2-ES, CCSM4, MIROC-ESM-CHEM).
  - Spatial strategy: data split into 10 blocks for cross-validation (10-fold); blocks chosen to balance area and bioclimate coverage.
  - Model evaluation: AUC (area under ROC) used to weight models in the ensemble; final species distributions are averaged across the ensemble.
  - Aggregation: grid-cell richness projected per species, then averaged to national level; national governance score is the mean of six World Bank Governance Indicators (data from 2018).

- Data files and structure (key details)
  - Climate_impacts_by_country.csv
    - 189 rows, 31 columns.
    - First column: ISO3 country code; last column: governance score (range -2.5 to 2.5).
    - Columns in the format: [scenario]_[taxon]_[measure], e.g., rcp85_bird_SR (species richness for birds under RCP 8.5).
    - Measures include SR (species richness, number of species) and pctChange (percent change relative to current richness).
  - Transboundary_richness.csv
    - 327 rows (one per border).
    - Columns: border (ISO3 pair), transboundary_richness (current intersecting species), transboundary_richness_threatened (threatened species intersecting border).
  - Transboundary_range_shifts.csv
    - 6 columns.
    - Columns: border, four shift-related columns (by taxon and climate scenario: mammals/birds × RCP 4.5 and RCP 8.5), barrier_species (non-flying mammals crossing fortified borders under high emissions; NA where no barrier or not fortified).
    - Barrier data applies only to borders with physical barriers; most borders flagged NA.

- How to use in GIS (practical guidance)
  - Country-level visualization:
    - Join Climate_impacts_by_country.csv to a country shapefile via ISO3 codes.
    - Create choropleth maps for current and future species richness, percent change, and governance scores.
    - Compare across climate scenarios (current, rcp26, rcp45, rcp60, rcp85).
  - Border-level visualization:
    - Use Transboundary_richness.csv to map current cross-border richness and threatened species at each border.
    - Use Transboundary_range_shifts.csv to map projected transboundary shifts by border, separated by taxon and scenario; display barrier_species where applicable.
  - Multi-layer analysis:
    - Assess relationships between governance scores and projected biodiversity changes at the national level.
    - Explore how transboundary dynamics align with geopolitical borders and governance indicators.
  - Data quality and reproducibility:
    - Data are ensemble-derived with cross-validation-based weighting; understand that projections depend on model choices, scenarios, and data inputs.
    - Governance metric reflects 2018 World Bank indicators; consider temporal alignment with biodiversity results.

- Limitations and considerations
  - Global scope with aggregations to national and border levels; finer local resolutions are not provided.
  - Excludes species with highly restricted ranges; results emphasize climate-driven broad patterns.
  - Projections rely on specific climate scenarios, SDM ensemble methods, and available covariates; inherent uncertainties in future forecasts.
  - Barrier_species data are NA for most borders; fortification details limited to those borders with known barriers.

- Context and reference
  - Methodological details and context available in the Materials and Methods of the cited open-access publication: Titley et al., 2021, Global inequities and political borders challenge nature conservation under climate change, Proceedings of the National Academy of Sciences, USA.