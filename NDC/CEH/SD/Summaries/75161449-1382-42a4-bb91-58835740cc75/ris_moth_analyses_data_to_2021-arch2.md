# Annual abundance indices and trends for moths in Britain and Ireland from the Rothamsted Insect Survey light-trap network, 1968-2021, including country-level results for England, Scotland and Wales

## Summary for Analysts Monitoring the Environment
- Purpose: Provide long-term, standardized measures of moth abundance and trends to assess environmental health and policy performance over time.
- Scope: 477 moth species (primarily macro-moths) with annual abundance indices and trends across Britain & Ireland (1968–2021); country-level analyses for England, Scotland, and Wales.
- Data breadth: 4,934,822 abundance counts across 844 species from all traps (551 traps total, average ≈92 traps/year); over 14 million individual moths recorded historically.
- Monitoring network: Rothamsted Insect Survey light-trap network—around 60 active traps currently; long-running, standardized design sampling local fauna rather than high-flying moths.
- Analytical framework: Generalized Abundance Index (GAI) with two-stage modelling
  - Stage 1: Generalized Additive Models (GAMs) estimate annual abundance curves per species, standardised to unit area under the curve to correct within-year gaps.
  - Stage 2: Poisson GAMs produce abundance indices and trends; site and year as explanatory effects; indices scaled to the network.
  - Trends expressed as Annual Growth Rate (AGR) and total percentage change over the time series; 95% CIs obtained via bootstrapping (1000 replicates).
- Outputs: Two main CSV result sets per region
  - _indices files: annual abundance indices with confidence intervals
  - _trends files: AGR, total percentage change, bootstraps, years data used, and time period details
- Regional scope and data quality: Britain, Ireland, Channel Islands network results plus England, Scotland, and Wales at country level; quality criteria applied to ensure robust species-level results (477 species network-wide; 441 England; 242 Scotland; 232 Wales).
- Data structure and accessibility: Supplementary names file to aid cross-referencing external taxonomies; data available via the Rothamsted Insect Survey online data warehouse; primary data and analyses are well-documented with explicit column definitions.
- Use and value: Data widely used in biodiversity and climate-related research (phenologies, biodiversity trends, population dynamics); suitable for integration with other environmental data to enhance utility beyond single-use analyses.

## Data and Analytical Method Details
- Data sources
  - RIS light-trap network (1968–2021) sampling moths with a standardized 200W tungsten bulb, trap height 1.2 m, near-power sources for maintenance.
  - Traps predominantly sample local fauna (attraction radii ≈ 30–60–100 m depending on bulb), not long-range dispersal.
- Data volume and coverage
  - 551 traps historically; average ~92 traps active yearly; broad geographic coverage across England, Scotland, Wales, Channel Islands; Ireland coverage more limited.
  - >14 million moths identified from the network; >1,500 species recorded historically; majority of data focused on macro-moths; some easily identified micro-moths included.
- Time period and species handling
  - Standard analyses cover 1968–2021 for most species; some taxa analyzed over shorter periods due to taxonomic or data issues (see Tables 1–2 in the dataset note).
  - Taxonomic decisions and aggregations documented where necessary (e.g., species aggregates with specified component taxa).
- Analytical method (GAI)
  - Step 1: GAM-based annual abundance curves per species, standardized so area under the curve sums to one; used to fill within-year recording gaps and generate site indices.
  - Step 2: Poisson GAMs estimate abundance indices and trends; site and year treated as categorical factors; typical-site scaling to project to the network.
  - Trends: Year coefficient converted to AGR (AGR = exp(year_coef) − 1); total percentage change derived from AGR across the number of years used; bootstrapped CIs (1000 replicates).

## Dataset Structure and Contents
- Primary outputs
  - Indices: species, scientific name, common name, year, nsites, nsites_pos, index, index_low, index_upp, nboot
  - Trends: species, scientific name, common name, nboot, agr, agr_low, agr_upp, perc_cng, perc_cng_low, perc_cng_upp, n_years, first_year, last_year
- Regional organization
  - Files prefixed by region codes:
    - bi_ for Britain, Ireland & Channel Islands
    - eng_ for England
    - scot_ for Scotland
    - wales_ for Wales
  - Each region provides two files: *_indices and *_trends
- Supplementary data
  - supplementary_spp_names.csv: links Rothamsted species IDs to external taxonomic identifiers (BRC, UKSI, Agassiz et al. checklist) and includes Bradley & Fletcher IDs
  - Columns include species_id, brc_concept, brc_species_name, abh_code, abh_species_name, abh_common_name, bf_code, bi, england, scotland, wales

## Regional Coverage, Time Periods, and Data Quality
- Coverage and criteria
  - 477 species meet basic quality criteria across Britain & Ireland
  - England: 441 species; Scotland: 242; Wales: 232
- Time period nuances
  - Generally 1968–2021; some species have shortened periods (e.g., Eupithecia pug species often 1986–2021; several other taxa 1971–2021 or 1975–2021 due to data/taxonomic issues)
- Quality assessment
  - Criteria include data completeness, confidence interval width, and temporal coverage; designed to ensure robust trend estimation across the time series and among the first/last halves of the period

## Access, Usage, and Supplementary Information
- Data access
  - Primary moth-trap counts and dataset availability via the Rothamsted Insect Survey online data warehouse: https://insectdatabase.rothamsted.ac.uk/login
- Documentation
  - Detailed method descriptions, data file structures, and taxonomic note tables accompany the dataset
- Acknowledgements
  - Funded by Defra under the Outcome Indicator Framework Wildlife Indicator Development (C13638); RIS as a National Bioscience Research Infrastructure; further supported by BBSRC and NERC/UK-SCAPE programme

## Key Implications for Environmental Analysts
- Standardized, long-term indicators enable temporal and regional comparisons of moth abundance and trends, supporting assessments of environmental health and policy effectiveness.
- The dataset’s explicit uncertainty (bootstrapped 95% CIs) and explicit handling of site-level variation make outputs robust for monitoring, reporting, and integration with other environmental indicators.
- The approach facilitates dataset re-use and combination with other data sources to increase value beyond single outputs, aligning with the challenge of maximizing dataset utility for monitoring programs.