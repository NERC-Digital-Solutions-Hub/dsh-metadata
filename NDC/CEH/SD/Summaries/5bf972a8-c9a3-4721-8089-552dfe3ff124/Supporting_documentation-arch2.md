# Global inequities and political borders challenge nature conservation under climate change

## Overview
- Analyse how climate change and socio-political factors affect biodiversity (birds and mammals) using ensemble species distribution models (SDMs).
- Provide standardized national-level metrics and cross-border biodiversity indicators to support environmental monitoring and policy assessment over time.
- Emphasize data accessibility and comparability across countries and borders to enable scrutiny and integration with other datasets.

## Data and scope
- Global scope covering 12,700+ terrestrial birds and mammals (about 80% of species), excluding restricted-range species.
- Data outputs come from three CSV files:
  - Climate_impacts_by_country.csv: national-level projections of changes in species richness under multiple climate scenarios.
  - Transboundary_richness.csv: current number of species whose ranges intersect each political border.
  - Transboundary_range_shifts.csv: projected number of species crossing borders due to climate-driven range shifts.
- Datasets support analysis of biodiversity loss under climate change and its relation to national governance.

## Data and methods used to generate outputs
- Data sources for species distributions: IUCN Red List and BirdLife International/HBW.
- SDM ensemble comprised of four model types: Generalised Additive Models (GAMs), Generalised Linear Models (GLMs), Random Forests (RFs), and Boosted Regression Trees (BRTs).
- Climatic predictors: mean annual temperature, temperature seasonality, precipitation in wettest/driest months, and precipitation seasonality.
- Projections to 2070 under four climate scenarios from IPCC AR5: RCP 2.6, 4.5, 6.0, 8.5.
- Climate projections from three Global Circulation Models: HadGEM2-ES, CCSM4, MIROC-ESM-CHEM.
- Spatial design for model validation: data split into 10 spatial blocks to perform 10-fold cross-validation; block design ensures representative bioclimates and area.
- Model evaluation: discrimination via AUC (area under the ROC curve); ensemble projections weighted by each model’s AUC.
- Aggregation: grid-cell species richness projections averaged to national level; outputs include percentage changes and current vs. future richness.

## Data structure and units
- Climate_impacts_by_country.csv
  - 189 rows (one per country); 31 columns.
  - First column: ISO3 country code; last column: governance score (mean of six World Bank Governance Indicators; scale -2.5 to 2.5; data from 2018).
  - Columns named as climate_scenario_taxon_measure (e.g., rcp85_bird_SR or current_mammal_pctChange).
- Transboundary_richness.csv
  - 327 rows (one per border); 3 columns.
  - Border identifier; transboundary_richness: number of species currently intersecting the border; transboundary_richness_threatened: number of threatened species intersecting the border.
- Transboundary_range_shifts.csv
  - 6 columns.
  - Border identifier; shifts by taxon (mammals/birds) and climate scenario (RCP 4.5 and RCP 8.5); final column barrier_species indicating non-flying mammals likely to cross fortified borders under high emissions (RCP 8.5); NA where no barrier.
  
## How this supports environmental monitoring
- Provides standardized, comparable indicators of climate change impact on biodiversity at national and border levels.
- Enables assessment of conservation challenges linked to political borders and governance context.
- Produces outputs suitable for reports, maps, and charts to communicate environmental health and policy performance.
- Datasets are organized for storage and portal upload, supporting ongoing monitoring and data sharing.

## Practice and data use implications
- Contextualizes biodiversity risk within governance quality (World Bank indicators) to inform policy prioritization.
- Highlights transboundary conservation needs and potential for coordination across blocs and borders.
- Facilitates integration with other environmental datasets to increase analytical value and cross-domain insights.

## Limitations and notes
- Species coverage excludes certain restricted-range species; results reflect model-based projections with inherent uncertainties.
- Border analyses depend on current political borders and fortifications; barrier_species only applicable to fortified borders.
- Governance metric uses 2018 data; updates may alter contextual interpretation over time.

## Source context
- Methodological details and interpretation are aligned with the open-access publication: Titley M.A., Butchart S. H. M., Jones, V.R., Whittingham M.J, Willis, S.G. Global inequities and political borders challenge nature conservation under climate change, Proceedings of the National Academy of Sciences (2021, in press).