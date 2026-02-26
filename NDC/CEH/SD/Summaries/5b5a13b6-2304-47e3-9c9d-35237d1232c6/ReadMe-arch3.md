# Traits data for the butterflies and macro-moths of Great Britain and Ireland, 2021

## Overview
- A multi-file dataset documenting life-cycle ecology, phenology, host-plant associations, breeding habitat, morphology, conservation status, distribution, and abundance trends for butterflies and macro-moths of Great Britain and Ireland.
- Intended to support monitoring frameworks by providing standardized trait and distribution data to scrutinise policy, inform decisions, and enable future analyses.
- Six core files (plus ReadMe and references) with detailed metadata and provenance to aid data governance and reuse.

## File structure and contents
- ecological_traits.csv
  - Traits related to life-cycle ecology and phenology, host-plant specificity, breeding habitat, and morphology.
  - Includes broader categories with sub-categories for data resolution; contains conservation status, occupancy/trend data.
  - Metadata describes derivation and country-specific data coverage; notes on political boundaries.
- excluded_species.csv
  - Lepidoptera species excluded from the database (mainly adventive or micro-moths).
- excluded_subspecies.csv
  - Lepidoptera subspecies/forms excluded from the database.
- hostplant_list_stacked.csv
  - Raw data on larval host-plant preferences; multiple rows per species for multiple hostplants.
- hostplant_list_unstacked.csv
  - One row per species with hostplants as columns; cells marked with 1 indicate usage.
- ReadMe.rtf
  - Detailed information on column derivations, numbering criteria, and data sources.
- Readme and files size summaries (Table 1 in the document) and a References section listing data sources and acknowledgments.

## Metadata, structure, and headers (ecological_traits.csv)
- Table 2 describes headers and data sources; includes notes on data merging (e.g., egg stage represented across 12 months in the dataset).
- Geographic boundaries and context:
  - Great Britain: England, Scotland, Wales
  - United Kingdom: GB + Northern Ireland
  - Ireland: island of Ireland (includes Northern Ireland and ROI)
  - Specific mention of the Republic of Ireland, Isle of Man, and Channel Islands where relevant to trend data
- Key header examples and data columns:
  - Identification: abh_number, b&f_number, scientific_name, common_name, family
  - Presence/status: recorded_present (present in England, Wales, Scotland, Northern Ireland, ROI), reintroduced, resident
  - Distribution and trends: extinct_gb, extinct_i, red_list_gb, red_list_ireland, gb_10_km_squares_2000-2016, ireland_10_km_squares_2000-2016
  - Rarity and trends: rarity_gb, long_term_distribution_trend_gb, sig_long_term_distribution_trend_gb, range_long_term_distribution_trend_gb, short_term_distribution_trend_gb, sig_short_term_distribution_trend_gb, range_short_term_distribution_trend_gb, abundance_trend_gb, sig_abundance_trend_gb, range_abundance_trend_gb
  - Life-cycle and ecology: diurnal, nocturnal, easily_disturbed_by_day, communal_or_nest, below_ground, leaf_litter_moss_on_ground_soil_surface, hostplant_external, hostplant_internal_stem, hostplant_internal_root, hostplant_external, hostplant_internal_others, etc.
  - Morphology and development: wing characteristics (forewing_minimum/maximum), estimated_dry_mass, obligate_univoltine, obligate_multivoltine, partial_generation, phenology_shift, and monthly-stage indicators (egg_stage, larval_stage, pupal_stage, adult_stage) across the year
  - Overwintering and life history: overwintering_stage, multiple overwintering strategies
  - Host-plant relationships: specificity (monophagous/oligophagous/polyphagous), number_hostplants, hostplant_category, hostplant_or_hostplant_category, hostplant_native_or_non_native, and broad_host_plant_category
  - Habitat and breeding: habitat sections and breeding habitats with both broad categories and subcategories; lists of common hostplants and habitat associations
- The dataset notes that some fields use 1/2/3 encodings, plus '?' where uncertain, with meanings described in the header metadata.
- Data sources and citations are provided for traceability and reproducibility.

## Data provenance, references, and acknowledgments
- Data compiled from multiple authoritative sources, including:
  - Butterflies for the New Millennium (BNM)
  - National Moth Recording Scheme (NMRS)
  - MothsIreland
  - Rothamsted Insect Survey (UKBMS data)
  - Butterfly Conservation and related taxonomic and distribution work
- The dataset explicitly acknowledges permission to incorporate raw host-plant data from Henwood, Sterling & Lewington (2020) and other foundational references.
- Primary citation for the dataset:
  Cook, P.M.; Tordoff, G.M.; Davis, A.M.; Parsons, M.S.; Dennis, E.B.; Fox, R.; Botham, M.S.; Bourn, N.A.D. (2021). Traits data for the butterflies and macro-moths of Great Britain and Ireland, 2021. NERC EDS Environmental Information Data Centre. https://doi.org/10.5285/5b5a13b6-2304-47e3-9c9d-35237d1232c6

## Relevance to monitoring frameworks
- Provides a standardized, multi-source trait and distribution dataset suitable for informing monitoring design and policy evaluation.
- Enables cross-species comparisons of life histories, host-plant dependencies, habitat requirements, and phenology shifts, which are crucial for assessing environmental health and policy outcomes.
- The inclusion of occupancy, extirpation, red-list status, and trend metrics supports monitoring indicators at national and regional levels.

## Use considerations, data quality, and governance
- Data integration involves harmonizing data from different political boundaries and recording schemes; users should consult Table 2 and the ReadMe for boundary definitions and scope.
- Metadata quality and completeness are emphasized; certain data points come with uncertainties (e.g., '?' markers) or are only available for certain taxa or timeframes.
- Data governance considerations include the need to cite the dataset properly in publications and the potential barriers to sharing underlying data, as noted in the ReadMe.
- Users should review the provenance, methods, and caveats in ReadMe.rtf to understand column derivations and allocation criteria before applying the data to monitoring analyses.