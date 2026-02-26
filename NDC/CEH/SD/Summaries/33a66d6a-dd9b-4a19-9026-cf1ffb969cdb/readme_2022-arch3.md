# A traits database for the Butterflies and Macro-moths of Great Britain and Ireland

## Overview
- A compiled dataset describing traits, ecology, phenology, hostplant associations, breeding habitats, and morphological characteristics for butterflies and macro-moths of Great Britain and Ireland.
- Published citation: Cook, P.M. et al., 2021. A traits database for the Butterflies and Macro-moths of Great Britain and Ireland.

## Files included
- ecological_traits.csv: traits on life cycle ecology, host plant specificity, breeding habitat, morphology; includes conservation status, distribution (occupancy) and abundance trend.
- excluded_species.csv: Lepidoptera species excluded from the database (mostly adventive or micro-moths).
- excluded_subspecies.csv: Lepidoptera subspecies/forms excluded from the database.
- hostplant_list_stacked.csv: raw data on larvae hostplant preferences (multiple rows per species for multiple hostplants).
- hostplant_list_unstacked.csv: table-formatted data with a single row per species and hostplants mapped to columns.
- ReadMe.docx: metadata explanations, data derivation criteria, and references; explains column origins and numbering rules.

## Dataset content and structure
- ecological_traits.csv:
  - Contains life cycle ecology, phenology, host plant specificity/characteristics, breeding habitat, and morphology.
  - Includes conservation status, occupancy distribution, and abundance trends.
  - Table 2 (header notes) explains headers and data sources; notes that distribution/abundance data are defined across political boundaries (e.g., Great Britain, United Kingdom, Ireland).
  - Political boundaries definitions used: Great Britain (England, Scotland, Wales), United Kingdom (GB plus Northern Ireland), Ireland (Republic of Ireland and Northern Ireland), with explicit mentions of Isle of Man and Channel Islands where relevant.
- Excluded files (excluded_species.csv and excluded_subspecies.csv) list taxa excluded from the dataset with basic taxonomic identifiers.
- Hostplant lists (hostplant_list_stacked.csv and hostplant_list_unstacked.csv) capture larval hostplant data from Henwood, Sterling & Lewington (2020), including both raw and consolidated formats; hostplants are aligned with Stace (2019) plant nomenclature.
- ReadMe.docx provides detailed derivations, criteria for data numbering, and a bibliography of data sources.

## Data fields and key measures (from ecological_traits.csv)
- Identity and taxonomy:
  - ABH number, B&F number, Wiemers checklist number, K&R number, scientific_name, common_name, family.
- Occurrence and status:
  - recorded_present by country, reintroduced, immigrant, resident, extinct_gb, extinct_i, red_list_gb, red_list_ireland.
- Range and trend metrics:
  - gb_10_km_squares, ireland_10_km_squares, rarity_gb, long_term_distribution_trend_gb, sig_long_term_distribution_trend_gb, range_long_term_distribution_trend_gb, short_term_distribution_trend_gb, sig_short_term_distribution_trend_gb, range_short_term_distribution_trend_gb, abundance_trend_gb, sig_abundance_trend_gb, range_abundance_trend_gb.
- Activity and behavior:
  - diurnal, nocturnal, easily_disturbed_by_day, communal_or_nest, below_ground, leaf_litter_moss_on_ground_soil_surface, hostplant_external, hostplant_internal_stem/root, other_vegetation_external, etc.
  - overwintering_stage: columns CY-DB (with multiple overwinter strategies where applicable).
  - overwintering nuances: pupa, larva, and adult overwintering details, including multiple overwintering references (e.g., pup_multiple, lar_multiple).
- Life cycle and phenology:
  - obligate_univoltine, obligate_multivoltine, partial_generation, phenology_shift, sig_phenology_shift_.
  - egg_stage (months Jan-Dec), larval_stage (months), pupal_stage (months), adult_stage (months).
  - larval overwintering notes (larval overwintering status per year).
  - larval stage uncertainties (e.g., '?').
- Morphometrics and other traits:
  - forewing_minimum, forewing_maximum (measurements in mm), estimated_dry_mass (mg; model-based estimate with caution).
- Host plant and habitat context:
  - specificity (monophagous/oligophagous/polyphagous classifications).
  - number_hostplants, hostplant_or_hostplant_category, hostplant_or_hostplant_category_scientific, hostplant_native_or_non_native, and Ellenberg-based environmental preferences (light_value, moisture_value, reaction, nitrogen, salt_tolerance).
  - broad_host_plant_category (multiple categories, with coding 1-4 to reflect frequency and geographic reporting).
  - host_plant_section (feeding sections on hostplants: roots, stem/shoot, bark, leaves, etc.).
  - common_hostplants (top 20 hostplants by species, with main vs. occasional vs. “also reported”).
- Habitat and breeding context:
  - habitat (columns FH-GB), with both broad and specific subcategories for breeding habitats (e.g., 1c_scrub_and_hedgerows, 1d_wet_woodland, 4c_acid_grassland, 5_wetland, 7_montane_upland with boundary definitions for upland).

## Provenance, references, and governance
- Data sources include national recording schemes and published atlases (e.g., BNM, NMRS, MothsIreland, Rothamsted Insect Survey, UKBMS, Henwood et al., Waring & Townsend, Hill et al., etc.).
- ReadMe.docx documents column derivations, criteria used for sequencing/numbers, and a comprehensive reference list.
- Primary citation for the dataset: Cook, P.M. et al., 2021.
- Acknowledgments highlight data contributions from key authors and institutions (e.g., Henwood, Sterling, Lewington, MothsIreland).

## Data governance, access, and use in monitoring
- The dataset emphasizes transparency and traceability through ReadMe documentation and explicit data provenance.
- Data are designed to support monitoring and evaluation by providing standardized trait and distribution information that can inform policy assessment, target setting, and cross-border analyses.
- Data sharing requires proper citation; metadata and sources are explicitly documented, promoting reproducibility and governance.
- Some caveats noted in the dataset structure:
  - Phenology fields do not account for latitudinal differences.
  - Some data are model-derived (e.g., estimated_dry_mass) and should be treated with caution.
  - Uncertainty indicators exist in monthly stage data (e.g., '?') for larval stages.

## Relevance for monitoring frameworks
- Provides structured, multi-dimensional trait and status data that can feed environmental health monitoring and policy evaluation:
  - occupancy and distribution trends across GB and Ireland enable cross-border trend analysis.
  - red list status and extinction records inform conservation risk assessments and prioritization.
  - phenology and life-cycle timing can be used to monitor climate- and habitat-related shifts.
  - hostplant associations and habitat preferences support habitat management and restoration planning.
  - morphometric and ecological trait data enable trait-based indicators of ecosystem health and biodiversity responses.

## Caveats and considerations for users
- Data boundaries and boundaries used for analyses vary by source; users should consult Table 2 and ReadMe for boundary definitions and data coverage.
- Some data are incomplete or uncertain (e.g., monthly presence with '?', mortality or overwintering details, and model-derived mass estimates).
- Latitude-specific phenology not captured; may limit seasonal timing comparisons across latitudes.

## Citation and references
- Core dataset citation: Cook, P.M., Tordoff, G.M., Davis, A.M., Parsons, M.S., Dennis, E.B., Fox, R., Botham, M.S., Bourn, N.A.D., 2021. A traits database for the Butterflies and Macro-moths of Great Britain and Ireland. Butterfly Conservation & Centre for Hydrology and Ecology, United Kingdom.
- References listed within ReadMe.docx, including key works on British and Irish Lepidoptera, hostplants, and monitoring schemes (e.g., Agassiz et al. 2013; Henwood et al. 2020; Randle et al. 2019; Fox et al. 2015/2019; Hill et al. 1999; Stace 2019).