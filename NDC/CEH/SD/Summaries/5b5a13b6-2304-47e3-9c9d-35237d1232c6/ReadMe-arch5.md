# Traits data for the butterflies and macro-moths of Great Britain and Ireland, 2021

## Overview
- A six-file dataset describing life cycle ecology, phenology, host plant use, breeding habitats, morphology, and conservation status for butterflies and macro-moths of Great Britain and Ireland.
- Includes lists of excluded species/subspecies and hostplant data in stacked and unstacked formats.
- ReadMe provides detailed metadata, provenance, and data derivation notes.
- Publication citation required when using the data: Cook et al. (2021), NERC EDS Environmental Information Data Centre.

## Dataset contents and file details
- ecological_traits.csv
  - Traits across life cycle ecology, phenology, host plant specificity, breeding habitat, morphology, conservation status, distribution, and abundance trends.
  - Multiple data resolutions (broader categories split into sub-categories).
  - 970 rows, 324 KB.
- excluded_species.csv
  - Lepidoptera species excluded from the database (mainly adventive or micro-moths).
  - 2022 rows, 97 KB.
- excluded_subspecies.csv
  - Lepidoptera subspecies/forms excluded from the database.
  - 276 rows, 19 KB.
- hostplant_list_stacked.csv
  - Raw hostplant data from Henwood, Sterling & Lewington (2020); multiple hostplants per species.
  - 4955 rows, 179 KB.
- hostplant_list_unstacked.csv
  - Table-formatted hostplant data; one row per species with hostplants as columns; 1 indicates known use.
  - 798 rows, 612 KB.
- ReadMe.rtf
  - Detailed derivation notes for all CSV files and accompanying tables; includes references and data provenance.
  - 271 KB.

## Data structure and headers (key points for governance)
- Header descriptions and data mapping (ecological_traits.csv) are provided, including:
  - Core identifiers: abh_number, b&f_number, scientific_name, common_name, family.
  - Distribution indicators: recorded_present across England, Wales, Scotland, Northern Ireland, Republic of Ireland; derived status columns (resident, immigrant, reintroduced, etc.).
  - Conservation and status indicators: red_list_gb, red_list_ireland, 10 km square occupancy counts (gb_10_km_squares_2000-2016; ireland_10_km_squares_2000-2016), rarity and distribution trend fields (long_term_distribution_trend_gb, sig_long_term_distribution_trend_gb, short_term_distribution_trend_gb, abundance_trend_gb, and their significance flags).
  - Life cycle and phenology: diurnal/nocturnal, easily_disturbed_by_day, communal_or_nest, below_ground, pupal/larval/adult_stage monthly indicators, overwintering_stage.
  - Generational strategy: obligate_univoltine, obligate_multivoltine, partial_generation, and related phenology shifts.
  - Hostplant associations: specificity (monophagous/oligophagous/polyphagous), number_hostplants, hostplant_category and hostplant_native_or_non_native, environmental tolerances ( Ellenberg values for light, moisture, nitrogen, salt_tolerance ), broad_host_plant_category, host_plant_section, common_hostplants.
  - Habitat and breeding: habitat categories and subcategories, sections of hostplants used for larval feeding, and breeding habitat classifications.
  - Hostplant lists: 20 most commonly used hostplants and associated genera for each species.
- Spatial boundaries and metadata:
  - Distribution and trend data are provided against defined political boundaries:
    - Great Britain (England, Scotland, Wales)
    - United Kingdom (GB plus Northern Ireland)
    - Ireland (Republic of Ireland and Northern Ireland)
    - Channel Islands and Isle of Man (where relevant)
  - Metadata clarifies which political area each data column covers.
- Data provenance:
  - Aggregated from multiple sources (e.g., BNM, NMRS, MothsIreland, UKBMS, Rothamsted Insect Survey, Emmet & Heath; Henwood et al. 2020; Stace 2019; others listed in References).
  - Acknowledges data providers (e.g., Henwood, Sterling, Lewington) and permissions to incorporate raw hostplant data.
- Data lineage and references:
  - Extensive references list (e.g., Agassiz et al. 2013; Eeles 2019; Fox et al. 2015/2019; Randle et al. 2019; Waring & Townsend 2017; Hill et al. 1999; etc.).
  - ReadMe details how columns were derived and numbering schemes.

## Access, use, and governance considerations
- Citation and credit:
  - Must cite Cook et al. (2021) when publishing results derived from this dataset; dataset hosted in the NERC Environmental Information Data Centre.
- Licensing and reuse:
  - Specific license not stated in the summary; follow ReadMe and data centre terms; acknowledge data providers per ReadMe.
- Data interoperability and standardization:
  - Large, multi-faceted trait dataset with numerous monthly columns (egg/larval/pupal/adult stages) and multiple boundary definitions; plan for mapping to standard vocabularies and aligning with other trait databases.
- Metadata quality and documentation:
  - Rich metadata in Table 2 style headers and ReadMe; critical for correct interpretation of merged vs. split categories, monthly indicators, and boundary-specific data.
- Update and version control:
  - Data derived from historical schemes (e.g., 2000-2016 occupancy, 1970-1979 vs 2000-2016 flight periods); consider versioning to capture updates from ongoing monitoring schemes (BNM, NMRS, MothsIreland, UKBMS).

## Practical implications for Data Stewards
- Data governance and storage:
  - Store as a structured data package with clear versioning, including both stacked and unstacked hostplant lists for compatibility.
  - Maintain ReadMe.rtf with full provenance, metadata definitions, and derivation notes.
- Data quality and interoperability:
  - Ensure column definitions are preserved and clearly mapped when integrating with other datasets.
  - Provide data dictionaries and crosswalks for key fields (e.g., life cycle phases, overwintering strategies, hostplant taxonomy).
- Data sharing and access:
  - Facilitate discovery via catalogue entries that describe political boundaries, temporal range, and data legends.
  - Ensure citation mechanism is clear and enforced in downstream uses.
- Compliance and ethics:
  - Acknowledge all data providers; follow licensing terms; respect any embargoes or restricted-use notes as indicated in ReadMe and metadata.

## Endnotes
- Acknowledgments and full references are included in the dataset materials, with specific thanks to data providers and contributing publications.