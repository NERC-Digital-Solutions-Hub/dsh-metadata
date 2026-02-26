# Global inequities and political borders challenge nature conservation under climate change

## Data overview
- Outputs from ensemble Species Distribution Models (SDMs) assessing how socio-political factors affect bird and mammal biodiversity under climate change.
- National-level data for 189 countries projecting changes in species richness to 2070, linked to governance and socio-economic indicators.
- Border-focused analyses estimating:
  - The number of species whose ranges currently intersect each political border (transboundary richness).
  - The number of species whose ranges are projected to cross each border under climate change (transboundary range shifts).
- Global scope, covering >12,700 terrestrial mammals and birds (≈80%), excluding species with highly restricted ranges.

## Datasets included
- Climate_impacts_by_country.csv
  - National-level projections of climate change impacts on species richness, across multiple scenarios and taxonomic groups.
- Transboundary_richness.csv
  - Current intersections of species ranges with political borders, by border.
- Transboundary_range_shifts.csv
  - Projected species range crossings across borders under climate change, by border, taxon, and scenario; includes barrier_species for borders with physical barriers.

## Data collection and generation methods
- Data sources for species: IUCN Red List and BirdLife International/Handbook of the Birds of the World.
- Modeling approach: ensemble SDMs combining GAMs, GLMs, Random Forests, and Boosted Regression Trees.
- Climatic predictors: mean annual temperature, temperature seasonality, precipitation (wettest/driest months), and precipitation seasonality.
- Climate projections: four scenarios (RCP 2.6, 4.5, 6.0, 8.5) to 2070.
- Climate projections: three GCMs (HadGEM2-ES, CCSM4, MIROC-ESM-CHEM).
- Spatial structure handling: data split into ten blocks for spatially explicit 10-fold cross-validation; blocks preserve area and bioclimate diversity.
- Model evaluation: area under the ROC curve (AUC) used to weight models in ensemble projections.
- Outputs: for each species, an ensemble of 120 projections per climate scenario (4 model types x 10 blocks x 3 GCMs) and then mean presence/absence weighted by AUC.
- Aggregation: grid-cell projections stacked to produce total species richness; grid-cell results aggregated to national level (mean across grid cells).
- Governance measure: mean of six World Bank Governance Indicators (based on 2018 data).

## Details of data structure and units
- Climate_impacts_by_country.csv
  - 189 rows (one per country).
  - Columns:
    - First column: ISO3 country code.
    - Last column: governance score (range -2.5 to 2.5, mean of six World Bank indicators).
    - Other columns: climate-science-derived measures with names like:
      - current_rcp26_bird_SR
      - rcp85_mammal_pctChange
      - etc.
    - Naming convention: [scenario]_[taxon]_[measure], where scenario ∈ {current, rcp26, rcp45, rcp60, rcp85}, taxon ∈ {bird, mammal, both}, measure ∈ {SR, pctChange}.
- Transboundary_richness.csv
  - 327 rows (one per border).
  - Columns: border, transboundary_richness (number of species intersecting border), transboundary_richness_threatened (number of threatened species intersecting border).
- Transboundary_range_shifts.csv
  - 6 columns total.
  - Columns: border, followed by four columns for projected transboundary range shifts (by taxon: mammals or birds; by climate scenario: RCP 4.5 and RCP 8.5), and barrier_species (non-flying mammals crossing fortified borders under high-emissions scenario).
  - NA indicates borders without physical barriers.

## Other information
- Context and methodological details available in the Materials and Methods of the cited open-access publication:
  Titley M.A., Butchart S. H. M., Jones, V.R., Whittingham M.J, Willis, S.G. Global inequities and political borders challenge nature conservation under climate change, Proceedings of the National Academy of Sciences, USA (2021, in press).

## Relevance for monitoring frameworks
- Provides concrete, globally standardized indicators for environmental health monitoring:
  - National-level impacts of climate change on biodiversity (richness changes by country and scenario).
  - Governance context (World Bank governance score) as a potential moderator or predictor.
  - Cross-border conservation implications via transboundary richness and range shifts.
  - Specific risk indicators for borders with barriers (barrier_species) to inform transboundary policy and infrastructure decisions.
- Data accessibility and governance considerations:
  - Data are organized for reuse (CSV files) and linked to open methodology.
  - Public sharing of underlying data supports transparency but may present barriers for some datasets or metadata gaps; governance processes are highlighted as essential for data quality and up-to-date datasets.