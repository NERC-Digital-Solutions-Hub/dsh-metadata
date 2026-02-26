A traits database for the Butterflies and Macro-moths of Great Britain and Ireland

## Overview
- A multi-file dataset compiling ecological traits, hostplant relationships, and exclusion records for British and Irish Lepidoptera.
- Designed to support analyses of life cycle ecology, phenology, host plants, habitat, distribution, abundance trends, and conservation status.
- Cited as Cook et al., 2021. A traits database for the Butterflies and Macro-moths of Great Britain and Ireland.
- Six files total: ecological_traits.csv, excluded_species.csv, excluded_subspecies.csv, hostplant_list_stacked.csv, hostplant_list_unstacked.csv, ReadMe.docx.
- Data sources include national recording schemes and classic field guides; headers include mapping to political boundaries (Great Britain, United Kingdom, Ireland).

## Dataset contents
- ecological_traits.csv (970 rows; 293 KB): life cycle ecology, phenology, host plant specificity, breeding habitat, morphology; includes conservation status, distribution trend, and abundance trend data; multiple data resolutions; detailed header notes in Table 2.
- excluded_species.csv (2022 rows; 97 KB): Lepidoptera species excluded from the database (mainly adventive or micro-moths).
- excluded_subspecies.csv (276 rows; 19 KB): Excluded subspecies/forms.
- hostplant_list_stacked.csv (4955 rows; 179 KB): raw data on larval hostplant preferences; multiple rows per species for multiple hostplants.
- hostplant_list_unstacked.csv (798 rows; 612 KB): one row per species with hostplants as columns; binary indicators where 1 = known use.
- ReadMe.docx (286 KB): metadata derivation, column meanings, data provenance, and references; includes Table 1 describing files and detailed column-level explanations (Tables 2–6 referenced).

## Data structure and headers (ecological_traits.csv)
- Key identifiers: abh_number, b&f_number, wiemers_checklist_number, k&r_number, scientific_name, common_name, family.
- Presence/status fields by country: recorded_present (England, Wales, Scotland, Northern Ireland, Republic of Ireland); reintroduced, immigrant, resident, extinct_gb/ireland; red_list_gb/ireland.
- Distribution and abundance trends: long_term_distribution_trend_gb, sig_long_term_distribution_trend_gb, range_long_term_distribution_trend_gb, short_term_distribution_trend_gb, sig_short_term_distribution_trend_gb, range_short_term_distribution_trend_gb, abundance_trend_gb, sig_abundance_trend_gb, range_abundance_trend_gb.
- Life-history and activity: diurnal, nocturnal, easily_disturbed_by_day, communal_or_nest, below_ground, leaf_litter_moss_on_ground_soil_surface, hostplant_external, hostplant_internal_stem/root, other_vegetation_external, stone_inc_walls, dead_rotten_wood, wingless_reduced_wing_female, forewing_minimum, forewing_maximum, estimated_dry_mass, obligate_univoltine, obligate_multivoltine, partial_generation, phenology_shift, sig_phenology_shift_, egg_stage (monthly columns), larval_stage (monthly; with '?' for uncertain), pupal_stage (monthly; with '?'), adult_stage (monthly; Moths use >1% rule for months with records).
- Overwintering: overwintering_stage (multiple columns for different strategies).
- Additional trait classifications: specificity (monophagous/oligophagous/polyphagous), number_hostplants, hostplant_or_hostplant_category, hostplant_or_hostplant_category_scientific, hostplant_native_or_non_native, light_value, moisture_value, reaction, nitrogen, salt_tolerance, broad_host_plant_category, host_plant_section, common_hostplants, habitat (breeding habitats with both broad and subcategories; several columns detail specific habitat types and exclusions like 1c_scrub_and_hedgerows, 4c_acid_grassland, 5_wetland, 7_montane_upland, etc.).
- Notes: Some fields have latitudinal caveats (phenology not latitudinally adjusted); mass estimates derived from a model (Kinsella et al. 2020) and should be used with caution; table notes explain data provenance and transformations.

## Data provenance and boundaries
- Distribution and status data drawn from multiple schemes: BNM (Butterflies for the New Millennium), NMRS (National Moth Recording Scheme), MothsIreland, UKBMS, Rothamsted Insect Survey, and others; unit boundaries may vary by source.
- Political boundary definitions used in metadata:
  - Great Britain: England, Scotland, Wales
  - United Kingdom: England, Scotland, Wales, Northern Ireland
  - Ireland: Isle of Ireland (including Northern Ireland and Republic of Ireland)
  - Republic of Ireland, Isle of Man, Channel Islands noted where relevant
- Hostplant and habitat data sourced from Henwood, Sterling & Lewington (2020) and Stace (2019); hostplant classifications include Ellenberg values (Hill et al. 1999).

## Usage notes and cautions
- The ReadMe provides detailed criteria for data derivation, numbering schemes, and column definitions.
- Some data are not regionally harmonized (e.g., calendar-month phenology not adjusted for latitude).
- The dry mass estimates are model-derived and should be used for cross-family analyses rather than precise mass per species.
- Data may require careful provenance tracking due to multiple sources and potential updates.

## Access, citation, and references
- Citation required: Cook, P.M., Tordoff, G.M., Davis, A.M., Parsons, M.S., Dennis, E.B., Fox, R., Botham, M.S., Bourn, N.A.D., 2021. A traits database for the Butterflies and Macro-moths of Great Britain and Ireland.
- Acknowledges data providers and primary literature across butterfly and moth monitoring schemes, field guides, red lists, and habitat/plant references (e.g., Agassiz et al. 2013; Emmet & Heath; Henwood et al. 2020; Waring & Townsend 2017; Hill et al. 1999; Stace 2019; Rothamsted Insect Survey; UKBMS; MothsIreland; etc.).