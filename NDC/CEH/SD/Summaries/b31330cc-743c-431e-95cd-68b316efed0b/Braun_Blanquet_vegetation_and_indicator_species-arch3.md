# DATA HEADER INFORMATION for Braun_Blanquet_vegetation_and_indicator species.csv

## Overview
- Documents that the dataset records the percent cover of indicator species using the Braun-Blanquet scale.
- Associated with ESPA Programme and the P4GES project (WP4).
- DOI provided; acknowledgement required for products derived from these data.

## Data structure and fields
- site_id: P4GES WP4 site code (text string).
- Scientific_name: scientific name of the inventoried species (text string).
- Local_name: vernacular/local name of the inventoried species (text string).
- Family: scientific family of the inventoried species (text string).
- Life_form: life form category (categorical): Fern/Shrub/Herb/Grass/Vine/Tree.
- Percent_cover: percent cover of the inventoried species (numeric, percent).
- Indicator_species: whether the species is a specific indicator of a land use (binomial Yes/No).
- B_B_scale: Braun-Blanquet scale value (categorical) with ordered categories:
  - 0 Not present
  - 1 1-5% cover
  - 2 5-25% cover
  - 3 25-50% cover
  - 4 50-75% cover
  - 5 75-95% cover
  - 6 >95% cover
- Data provenance: field materials/resource s = botanist; indicates source of expertise for data entry.
- Unit/Type notes: Percent_cover is numeric; B_B_scale is categorical; site_id and names are text.

## Scales and interpretation
- Percent_cover provides a numeric measure of dominance; B_B_scale provides a categorical Braun-Blanquet interpretation of cover.
- Life_form classifies species into broad ecological groups for analysis.
- Indicator_species flag identifies species used as land-use indicators.

## Provenance and usage notes
- Data originate from ESPA (European Space Agency / Ecosystem Services for Poverty Alleviation) and the P4GES project, with a specific WP4 site code.
- DOI authentication and data provenance included for traceability.
- Acknowledgement required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).

## Data quality, gaps, and governance considerations for monitoring frameworks
- Metadata depth: While field and taxonomic details are provided, method-related metadata (sampling design, dates, locations, and QA procedures) are not fully detailed; would benefit from expanded metadata for robust governance.
- Data sharing and openness: The document implies data sharing is expected but does not specify licensing or access constraints; ensure clear data governance and public sharing policies.
- Data integration: The coexistence of Percent_cover (numeric) and B_B_scale (categorical) requires consistent interpretation when integrating with other datasets; ensure standardization across datasets.
- Silo risk and provenance: Clear attribution to botanists as field sources helps, but broader documentation of data collection workflows can reduce silos and improve reproducibility.
- Use in dashboards and reports: The combination of species-level indicators, life forms, and site codes supports monitoring vegetation health and land-use indicators, but users will need complete methodological metadata to interpret results accurately.