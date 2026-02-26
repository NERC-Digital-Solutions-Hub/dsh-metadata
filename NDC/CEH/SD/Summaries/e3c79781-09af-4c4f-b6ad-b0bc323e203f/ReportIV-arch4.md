# SUMMARY

## Context and Aims
- Four years into the NERC Soil Biodiversity Thematic Programme at the Sourhope site, focusing on linking soil biodiversity with above-ground plant communities and ecosystem processes.
- Study centres on management impacts (mowing, fertilisation, insecticide) on productivity (above-ground biomass), species composition, and diversity, with a broader aim to understand data-on-ground relationships across a multi-project programme.

## Data Architecture and Assets
- Site design: Rigg Foot Experimental Site with 5 replicate blocks along a downslope gradient; each block contains 6 main plots subdivided into 10 sub-plots, with 0.5 m x 0.5 m cells used for data collection.
- Treatments (plot-level and site-level): Control 1, Control 2 (no treatment); Nitrogen; Lime; Nitrogen & Lime; Insecticide (formerly Biocide) — applied and monitored across years.
- Data types collected (1998–2002):
  - Above-ground biomass: regular harvests from 0.5 m2 cells, dried and weighed.
  - Weather and climate: on-site Automatic Weather Station (rainfall, radiation, temperature, moisture, etc.).
  - Soil properties: soil pH (water), moisture (theta probe), sampled by plot and cell.
  - Botanical data: baseline and repeated point-analysis surveys (0.5 m2 cells with 25-point and 100-point grids), species identification (vascular plants and bryophytes, bryophytes refined to species in 2002).
  - Biomass and vegetation surveys: additional small-scale and targeted surveys; detailed appendices catalog species lists and survey methods.
- Data analyses applied:
  - Descriptive summaries and trend analyses over time.
  - Split-plot ANOVA to test effects of Treatment, Year, and their interaction on biomass.
  - Correlation and regression analyses linking soil pH, moisture, and biomass.
  - Principal Components Analysis (PCA) of point-analysis data to distinguish treatment groups.
  - Shannon Diversity Index calculations for plant communities.
  - CSR (Grime) functional-type classification to interpret community responses.

## Data Collection, Management, and Governance
- Regular, standardized data collection across multi-year cycles (1999–2002) with explicit mowing schedule and treatment dates.
- Strengths:
  - Multi-scale data capturing productivity, species composition, and environmental context.
  - Consistent reporting of treatment effects and their functional implications (C-S-R shifts, stress tolerance).
  - Comprehensive metadata in appendices (site activity, treatment summaries, species lists, weather data, and biomass records) enabling data reuse.
- Data challenges and gaps:
  - 2002 weather data gaps due to a malfunction (about 6 weeks); some data substituted from the Konza weather station.
  - New data streams introduced in 2002 (more detailed bryophyte identification; expanded point analysis) to improve taxonomic resolution.
  - Some plots (e.g., C2) experienced trampling during intense field activities, complicating interpretation of productivity data for that year.
- Documentation and accessibility:
  - Appendices provide full context: site activities, detailed treatment regimes (N, Lime, Insecticide), species lists, weather data, biomass time series, and PCA loadings.
  - Data are distributed across multiple projects within Phase I and Phase II, with cross-referencing via project PIs and published appendices.

## Analyses and Key Findings
- Biomass and productivity (1999–2002):
  - Fertilised plots (N and/or Lime, especially when combined) show higher productivity; Control 2 plots generally lower; overall biomass increased over time relative to 1999 baseline, though 2002 biomass declined relative to 2001 in several treatments.
  - A notable block/position effect: lower slopes (Block 1) showed larger biomass gains in some years; steeper blocks (Block 5) showed declines.
- Soil chemistry and moisture:
  - Lime dramatically increases soil pH toward ~7 in upper soil layers; nitrogen also raises pH modestly.
  - Positive relationship between soil pH and biomass when all treatments included; the relationship weakens or reverses within certain treatments (notably when both N and Lime are present).
  - Negative correlation between soil moisture and pH; drier, limed plots tended to perform differently from wetter, unimproved ones.
- Plant functional composition (CSR framework):
  - Fertilised plots (especially N+L) show a shift toward competitive-stress-ruderal (CSR) and CS-R-dominated communities; unimproved plots retain more stress-tolerant species.
  - SR/CSR and CSR groups become more dominant in fertilised plots over time; stress-tolerant species increase in unimproved plots.
- Species composition and diversity:
  - Point-analysis shows shifts in the relative frequency of grasses associated with improved pastures (e.g., Festuca rubra, Poa pratensis) in fertilised plots; unimproved plots retain Festuca ovina and Anthoxanthum odoratum dominance.
  - Bryophytes (mosses and liverworts) become more abundant across the site, particularly in unimproved plots, contributing to higher bryophyte hits and relative biomass in those plots.
  - Insecticide (Dursban) treatment shows potential positive effects on overall plant diversity, aligning with literature on herbivore control benefiting certain palatable species, though direct causation remains cautious.
  - 2002 data reveal significant differences in litter presence and bryophyte representation by treatment; mosses increase with mowing and reduced disturbance.
- Diversity metrics:
  - Shannon Diversity Index declines in nitrogen-and-lime plots by 2002 relative to baseline, while increases are observed in other treatments, with the insecticide-treated plots showing notable diversity gains.
- Data interpretation and caveats:
  - Insecticide effects on diversity are discussed with potential mechanisms (herbivory reduction allowing palatable species to persist) but require cautious interpretation due to limited direct herbivory data.
  - The trampling event in the C2 plots and 2002 data gaps must be considered when interpreting productivity and composition trends for that year.

## Data Quality, Gaps, and Challenges
- Data continuity:
  - A 2002 weather-station outage caused missing measurements; some values were substituted from an external station.
  - The C2 trampling incident introduced potential confounding effects on productivity data for 2002.
- Taxonomic resolution:
  - Bryophytes were identified to species level in 2002, enhancing data quality for bryophyte dynamics.
- Treatment documentation:
  - Detailed, year-by-year treatment schedules (dates and rates) are captured in appendices, enabling reproducibility and re-analysis.
- Cross-project data integration:
  - Data are distributed across Phase I and Phase II projects, requiring careful data integration and provenance tracking to ensure consistent interpretation.

## Documentation and Access
- Appendices of the report provide:
  - Site activity summaries and a map of treatment allocations.
  - Full species lists for 2002, including bryophytes.
  - Weather data and biomass measurements by plot and year.
  - Detailed biomass time-series and PCA loadings.
  - Descriptions of treatment regimes (N, Lime, N&L, Insecticide) and mowing schedule.
- The dataset supports cross-year trend analyses and functional interpretation across multiple data streams (productivity, composition, diversity, environment).

## Implications for Data Leaders
- Data architecture and governance:
  - The Sourhope dataset demonstrates the value of integrated multi-scale data (biomass, species, soil chemistry, moisture, weather) linked to a well-documented experimental design.
  - Maintaining rigorous metadata on treatments (timing, rates), mowing, and disturbance is essential for interpreting plant functional shifts and productivity outcomes.
- Data quality and resilience:
  - Anticipate and document data gaps (e.g., equipment outages) and establish strategies for data imputation or cross-station substitution while preserving data lineage.
  - Track exceptional events (trampling, weather-related interruptions) and their potential impact on results.
- Usability and reproducibility:
  - Comprehensive appendices (treatment regimes, species lists, schedules) are critical for data reuse by cross-project teams.
  - Employ standardized analyses (ANOVA, PCA, CSR classification, Shannon index) to enable consistent cross-year and cross-treatment comparisons.
- Lessons for data systems:
  - Integrate above- and below-ground data streams to enable holistic ecosystem interpretation.
  - Provide clear, accessible documentation of protocols and data provenance to support future analyses and replication.
  - Ensure data discoverability through structured metadata and cross-referencing of appendices, plots, and treatments to facilitate reuse for policy and research networks.