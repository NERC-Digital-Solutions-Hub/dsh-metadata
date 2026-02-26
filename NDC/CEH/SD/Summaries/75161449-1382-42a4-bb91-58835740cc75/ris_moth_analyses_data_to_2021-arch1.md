# Annual abundance indices and trends for moths in Britain and Ireland from the Rothamsted Insect Survey light-trap network, 1968-2021, including country-level results for England, Scotland and Wales

## Overview
- Provides annual abundance indices and trends for 477 moth species (mostly macro-moths) from the Rothamsted Insect Survey (RIS) light-trap network, 1968–2021.
- Trends shown as year coefficients from the Generalized Abundance Index (GAI) model, expressed as Annual Growth Rates (AGR) and total percentage changes.
- Indices and trends include 95% confidence limits derived via bootstrapping.
- Includes network-wide results for Britain, Ireland and Channel Islands, plus country-level analyses for England, Scotland, and Wales.

## Data sources and network description
- RIS operates two insect trap networks in Britain & Ireland: suction-traps (aphids) and light-traps (moths). The light-trap network is standardised, with traps at about 1.2 m height, using a 200 W tungsten bulb and opaque lids to sample local fauna.
- Light-trap network has around 60 active traps currently; historically operated at ~560 locations, averaging ~90 traps per year.
- Traps are widespread across most of the British Isles but proximity to power and maintenance influences (anthropogenic context) means some local dispersion is not fully isolated.
- Over 14 million individual moths captured and identified across more than 1,500 species; dataset is one of the longest standardised terrestrial insect time series.
- Data are accessible via the Rothamsted Insect Survey online data warehouse.

## Data content and scope
- Time span: 1968–2021 (with some species-specific time periods shortened due to taxonomic or data issues).
- Data objects: abundance indices for each species at annual level for the entire network and for England, Scotland, and Wales; plus corresponding trends over time.
- Sample size: 4,934,822 abundance counts across 844 species (network-wide) from 551 traps (average ~92 traps operating annually).
- Species coverage: 477 species meeting data quality criteria for network analyses; country-level analyses include 441 (England), 242 (Scotland), 232 (Wales).
- Taxonomic notes: some species are analysed as aggregates due to identification changes; several species have adjusted time periods (e.g., Eupithecia spp. 1986–2021 or 1971–2021 for certain taxa).

## Analytical method and outputs
- Generalized Abundance Index (GAI) approach (Dennis et al. 2016):
  - Stage 1: Generalized Additive Model (GAM) to estimate annual abundance curves per species, standardised so area under the curve equals one; used to correct within-year recording gaps and produce site indices.
  - Stage 2: Poisson GAMs to estimate indices and trends with site and year as categorical effects; network indices are scaled to reflect the full network.
- Trends estimation:
  - A continuous year term is used to derive the Annual Growth Rate (AGR) and total percentage change over the time series.
  - AGR is computed by exponentiating the year coefficient and subtracting 1; zero AGR indicates no change.
  - Total percentage change calculated from AGR across the number of years in the series.
  - 95% confidence intervals derived via bootstrapping (1,000 replicates).
- Outputs:
  - Indices file: annual abundance indices per species per year with confidence intervals and bootstrap counts.
  - Trends file: AGR, agr_low, agr_upp, perc_cng, perc_cng_low, perc_cng_upp, n_years, first_year, last_year per species, plus bootstrap count.

## Dataset structure and accessibility
- Two result files per region (indices and trends) with region prefixes:
  - bi_ for Britain, Ireland & Channel Islands
  - eng_ for England
  - scot_ for Scotland
  - wales_ for Wales
- Index file columns: species, name, common_name, year, nsites, nsites_pos, index, index_low, index_upp, nboot.
- Trends file columns: species, name, common_name, nboot, agr, agr_low, agr_upp, perc_cng, perc_cng_low, perc_cng_upp, n_years, first_year, last_year.
- Supplementary names lookup file (supplementary_spp_names.csv) links Rothamsted species IDs to BRC, UKSI, Agassiz et al. checklists, and Bradley & Fletcher IDs, with columns including:
  - species_id, brc_concept, brc_species_name, abh_code, abh_species_name, abh_common_name, bf_code, bi, england, scotland, wales.
- Data availability note: dataset includes a robust cross-regional and taxonomic framework, with metadata to facilitate linking to external taxonomic sources.

## Data quality, limitations, and considerations
- Quality criteria applied to determine which species’ data meet basic reliability (e.g., data availability across years, confidence intervals). Network-level: 477 species; England: 441; Scotland: 242; Wales: 232.
- Some species have shorter time series due to taxonomic or data issues (specified per species), which may affect comparisons across the full 1968–2021 window.
- Data reflect local sampling near human activity centers due to logistical trap placements; interpretation should consider potential local biases and the sampling radius of light traps (~30–100 m depending on assumptions).
- The dataset emphasizes consistency and long-term trends, with bootstrapped CIs to quantify uncertainty in indices and trends.

## Supplementary and acknowledgements
- Supplementary taxonomic mappings enable cross-referencing with external checklists (BRC, UKSI, Agassiz et al., Bradley & Fletcher).
- Acknowledgements credit Defra funding (Outcome Indicator Framework Wildlife Indicator Development, C13638) and the RIS as a National Bioscience Research Infrastructure, with support from BBSRC and NERC through related programmes.

## Potential uses for analysts
- Identify correlations and patterns in long-term moth abundance across Britain, Ireland, and regions (England, Scotland, Wales).
- Assess regional and country-level differences in trends (AGR and total change) and relate to environmental drivers (e.g., climate, habitat change).
- Use the supplementary taxonomic linkage to integrate with external biodiversity datasets and conservation indicators.
- Employ the bootstrapped confidence intervals to gauge uncertainty when informing policy or research on insect biodiversity and ecosystem health.
- Reproduce or extend analyses with available data and metadata for transparency and accountability in ecological decision-making.