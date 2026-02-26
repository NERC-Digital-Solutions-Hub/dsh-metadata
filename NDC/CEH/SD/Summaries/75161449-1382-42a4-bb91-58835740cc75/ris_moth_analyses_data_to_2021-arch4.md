# Annual abundance indices and trends for moths in Britain and Ireland from the Rothamsted Insect Survey light-trap network, 1968-2021, including country-level results for England, Scotland and Wales

## Overview
- Long-term dataset of annual abundance indices and trends for 477 moth species (primarily macro-moths) using Rothamsted Insect Survey (RIS) light-trap data from 1968–2021.
- Trends are derived with a Generalized Abundance Index (GAI) model, reported as year coefficients (Annual Growth Rate, AGR) and total percentage change over the time series, with 95% bootstrap confidence intervals.
- Includes network-wide results for Britain, Ireland, and the Channel Islands, plus country-level analyses for England, Scotland, and Wales.
- Data volume and scope: 4,934,822 abundance counts across 844 species (551 traps, average ~92 traps/year); more than 14 million individual moths captured historically; many studies have used RIS moth data for diverse ecological and climate-related questions.
- Outputs support cross-region comparisons and longitudinal biodiversity assessments.

## Data Source and Network
- Source: Rothamsted Insect Survey light-trap network (part of RIS two-trap networks sampling aphids and moths; sampling since 1964).
- Light-trap design: standardized 200 W tungsten bulb, trap height 1.2 m, opaque lid to sample local fauna; modest attraction radii (~60–100 m).
- Current deployment: around 60 active traps across Britain & Ireland; historically sampled at about 560 locations with ~90 traps operating annually.
- Coverage: traps distributed across England, Scotland, Wales, Channel Islands; Ireland has comparatively less coverage.
- Data accessibility: RIS moth-trap data are available via the Rothamsted Insect Survey online data warehouse (insectdatabase.rothamsted.ac.uk/login).

## Analytical Method (GAI)
- First stage: Generalized Additive Model to estimate annual abundance curves for each species, standardised so the area under the curve equals one, producing site indices to correct for within-year recording gaps.
- Second stage: Poisson Generalised Additive Models to derive abundance indices and trends; year treated as a categorical effect for indices, and as a continuous variable for trends.
- Regional scaling: region-specific coefficients are combined to produce network-wide indices; site-level results are aggregated to network scale.
- Trends and metrics:
  - Annual Growth Rate (AGR): exponential of the year coefficient minus one (per-year growth rate; AGR > 0 indicates increase).
  - Total percentage change (perc_cng): derived from AGR and number of years.
  - Uncertainty: 95% confidence intervals obtained via bootstrapping (1000 replicates).
- Quality criteria: only species meeting predefined data quality thresholds across the full period (and halves of the period) are reported; regional analyses have smaller species counts meeting criteria (England 441, Scotland 242, Wales 232).

## Data Files and Structure
- Output format: CSV files with two results files per region - one for annual abundance indices (_indices) and one for trends (_trends).
- Region coding:
  - bi_ for Britain, Ireland & Channel Islands (overall network)
  - eng_ for England
  - scot_ for Scotland
  - wales_ for Wales
- Abundance indices files contain (per row):
  - species, name, common_name, year
  - nsites (number of traps that recorded the species over the full time series)
  - nsites_pos (number of traps that recorded the species in that year)
  - index, index_low, index_upp (relative annual abundance index and 95% CI)
  - nboot (number of bootstraps producing an index)
- Trends files contain (per row):
  - species, name, common_name
  - nboot
  - agr, agr_low, agr_upp
  - perc_cng, perc_cng_low, perc_cng_upp
  - n_years, first_year, last_year
- Supplementary taxonomicNames file: supplementary_spp_names.csv provides cross-references to BRC, UKSI, Agassiz et al. (2013) checklists and Bradley & Fletcher IDs, with area indicators (eng, scotland, wales) to assist data integration and cross-source matching.

## Data Coverage and Taxa
- Overall: 477 species across Britain & Ireland meet quality criteria for the network analyses (variability in year coverage noted for some species).
- Regional species counts meeting criteria: England 441, Scotland 242, Wales 232.
- Taxonomic notes: majority are macro-moths; some easily identified micro-moths included when consistently identified (e.g., Nomophila noctuella, Plutella xylostella, Udea ferrugalis).

## Usage, Applications, and Context
- The dataset underpins long-term biodiversity assessments, climate-change-related phenology and population dynamics studies, and methodological work on monitoring biodiversity via standardized insect time series.
- Facilitates cross-regional comparisons and integration with external taxonomic codes via the supplementary names file.
- Widely used in past studies on diversity statistics, density dependence, climate impacts, and insect abundance trends (cited in references).

## Access, Governance, and Acknowledgements
- Funded by Defra (Wildlife Indicator Development); RIS is funded by BBSRC; supported by UK-SCAPE/NERC programs.
- Data and methodological framework draw on a broad history of RIS research and associated publications.