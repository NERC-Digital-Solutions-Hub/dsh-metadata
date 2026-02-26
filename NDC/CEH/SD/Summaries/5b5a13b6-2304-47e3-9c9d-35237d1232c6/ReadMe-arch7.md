# Traits data for the butterflies and macro-moths of Great Britain and Ireland, 2021

- Six files constitute the dataset: ecological_traits.csv, excluded_species.csv, excluded_subspecies.csv, hostplant_list_stacked.csv, hostplant_list_unstacked.csv, and ReadMe.rtf, plus a cited publication for use in publications.
- Purpose: a trait database for butterflies and macro-moths of Great Britain and Ireland, designed to support map-based analysis and GIS visualisations of life cycles, phenology, host plants, habitat, distribution, and trends.

## Data files and structure

- ecological_traits.csv
  - Traits on life cycle ecology and phenology, host plant specificity and characteristics, breeding habitat, morphological traits, conservation status, and distribution/abundance trends.
  - Nested data resolutions: broader categories (e.g., habitat) split into sub-categories for multiple data resolutions.
  - Includes columns for occupancy by country and trend data across Great Britain and Ireland.
  - Key derived fields describe status (recorded_present, reintroduced, immigrant, resident) and various trend metrics.
  - Monthly phenology data for egg, larva, pupa, and adult stages; overwintering strategies; and various morphological and ecological attributes.

- excluded_species.csv
  - List of Lepidoptera species from Agassiz, Beavan & Heckford (2013) excluded from the database (primarily adventive or micro-moths).

- excluded_subspecies.csv
  - List of Lepidoptera subspecies/forms excluded from the database.

- hostplant_list_stacked.csv
  - Raw, stacked host-plant data from Henwood, Sterling & Lewington (2020); multiple rows per species to reflect multiple hostplants.
  - Includes both vernacular and scientific hostplant names.

- hostplant_list_unstacked.csv
  - Unstacked host-plant data; one row per species with hostplants indicated in columns; 1 denotes known usage as a main/occasional hostplant.

- ReadMe.rtf
  - Documentation on how each column was derived, criteria for numbering, and references used to compile the dataset.
  - Includes header definitions and guidance on data provenance.

- Table references and metadata
  - Table 2 (headers for ecological_traits.csv) documents header notes, data sources, and the mapping of monthly and multi-year fields.
  - ReadMe and Table 1–6 provide detailed explanations of all files and their headers.

## Boundary definitions and spatial scope

- Distribution and occupancy data are provided at varying political boundaries depending on the data source.
- Boundaries used:
  - Great Britain (GB): England, Scotland, Wales
  - United Kingdom (UK): GB plus Northern Ireland
  - Ireland: Republic of Ireland and Northern Ireland
  - Channel Islands, Isle of Man mentioned where relevant
- 10 km x 10 km grid square counts are used for certain trend metrics (gb_10_km_squares and ireland_10_km_squares).

## Key fields and GIS interpretation

- Identifiers and taxonomy
  - abh_number, b&f_number, scientific_name, common_name, family
- Occurrence and status
  - recorded_present across England, Wales, Scotland, Northern Ireland, Republic of Ireland
  - status flags: reintroduced, immigrant, resident, extinct_gb, extinct_i, red_list_gb, red_list_ireland, etc.
- Distribution and abundance trends
  - long_term_distribution_trend_gb, sig_long_term_distribution_trend_gb, range_long_term_distribution_trend_gb
  - short_term_distribution_trend_gb, sig_short_term_distribution_trend_gb, range_short_term_distribution_trend_gb
  - abundance_trend_gb, sig_abundance_trend_gb, range_abundance_trend_gb
- Phenology and life stages
  - diurnal, nocturnal, easily_disturbed_by_day, communal_or_nest, below_ground, leaf_litter_moss_on_ground_soil_surface, hostplant_external, hostplant_internal_stem, hostplant_internal_root, hostplant_external_other_vegetation, etc.
  - egg_stage (monthly columns AX-BI), larval_stage (monthly columns BJ-BV), pupal_stage (monthly columns BW-CI), adult_stage (monthly columns CJ-CU)
  - overwintering_stage (CV-CY), with interpretations for multiple strategies
  - larval_overwintering_multi, pupa_overwintering_multi, etc.
- Ecology and habitat
  - specificity (monophagous/oligophagous/polyphagous), number_hostplants
  - hostplant_or_hostplant_category, hostplant_or_hostplant_category_scientific
  - hostplant_native_or_non_native, light_value, moisture_value, reaction, nitrogen, salt_tolerance
  - broad_host_plant_category (e.g., sedges, grasses, trees, shrubs, mosses, detritus, etc.)
  - habitat and breeding habitat categories (with 1 indicating usage)
  - common_hostplants, host_plant_section (specific larval feeding zones on hostplants)
- Morphometrics and life history
  - estimated_dry_mass (model-derived; caution advised)
  - obligate_univoltine, obligate_multivoltine, partial_generation, phenology_shift
  - forewing_minimum, forewing_maximum (mature measurements)
  - wingless_reduced_wing_female
- Data provenance and caveats
  - Data are derived from multiple sources with notes in headers; some fields may be blank where trends are not estimable.
  - Some mass estimates are model-based and should be used for cross-species analyses rather than precise mass per species.
  - Data standards may vary across sources; headers may be merged to save space.

## Data quality, limitations, and considerations for GIS

- Boundary and scale
  - Occupancy and trend data may be defined across different political boundaries; ensure alignment with target GIS boundaries before analysis.
- Completeness
  - Not all species have complete trend or phenology data; blanks are possible in several fields.
- Data provenance
  - Extensive references and metadata accompany the dataset; ensure proper citation (Cook et al., 2021) when using in publications or products.
- Exclusions
  - Some species/subspecies are intentionally excluded; consider this when aggregating biodiversity measures.

## How to use this data in GIS

- Create spatial layers for occupancy and trends
  - Build layers by country or by 10 km grid cells to visualize long-term and short-term distribution trends and abundance trends.
- Phenology and life-cycle mapping
  - Use monthly egg/larva/pupa/adult presence to animate or filter seasonal maps; distinguish diurnal vs nocturnal species.
- Habitat and host-plant integration
  - Link host-plant data (stacked and unstacked) to vegetation layers and land cover to model habitat associations and potential distributions.
  - Use broad and specific habitat categories to create habitat suitability or breeding-habitat maps.
- Native vs non-native host-plant context
  - Incorporate host-plant nativity data to assess conservation implications and potential invasive plant interactions.
- Data fusion and attribution
  - Leverage header documentation (Table 2 and ReadMe) to map dataset attributes to GIS fields; maintain traceability to primary sources.

## Citation

- Cook, P.M.; Tordoff, G.M.; Davis, A.M.; Parsons, M.S.; Dennis, E.B.; Fox, R.; Botham, M.S.; Bourn, N.A.D. (2021). Traits data for the butterflies and macro-moths of Great Britain and Ireland, 2021. NERC EDS Environmental Information Data Centre. https://doi.org/10.5285/5b5a13b6-2304-47e3-9c9d-35237d1232c6

- Acknowledgments and References
  - Acknowledges data contributors and foundational references (e.g., Henwood et al., Eeles, Randle et al., Fox et al., UKBMS, NMRS, MothsIreland, Hill et al., Stace, etc.).
  - Comprehensive references list provided in ReadMe and associated documentation.