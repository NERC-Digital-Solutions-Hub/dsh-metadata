# Traits data for the butterflies and macro-moths of Great Britain and Ireland, 2021

- A multi-file dataset providing trait information for butterflies and macro-moths across Great Britain and Ireland, assembled in 2021 and citable via Cook, P.M. et al. (2021).
- Six primary components: ecological_traits.csv, excluded_species.csv, excluded_subspecies.csv, hostplant_list_stacked.csv, hostplant_list_unstacked.csv, ReadMe.rtf, plus a references list.
- Intended to support analysis of life cycle ecology, phenology, host plant relationships, breeding habitats, morphological traits, and population trends (distribution and abundance).

## What the dataset covers

- Life cycle ecology and phenology (egg, larval, pupal, and adult stages; monthly resolution for some traits).
- Host plant specificity and characteristics (monophagous, oligophagous, polyphagous; hostplant categories and species-level details).
- Breeding habitats and habitat usage (breeding site preferences and related subcategories).
- Morphological characteristics (e.g., forewing length, dry mass estimates, wingedness, overwintering strategies).
- Conservation and distribution indicators (extinction status, red list status for GB and Ireland, occupancy and abundance trends; long- and short-term distribution trends; diurnal/nocturnal activity).
- Overwintering strategies and generation patterns (univoltine/multivoltine, partial generations, and related terminology).
- Data provenance and boundaries across political regions (Great Britain, United Kingdom, Ireland, and related areas).

## File-level details

- ecological_traits.csv
  - Contains 970 rows and 324 KB of data with life history, phenology, host plant relationships, habitat, conservation status, and trend metrics.
  - Includes monthly columns for various life stages (egg, larval, pupal, adult) and overwintering stages; many fields coded numerically (1, 2, 3, etc.) with some '?' for uncertainty.
  - Provides definitions and notes in Table 2, and context on how data map to political boundaries (Great Britain, UK, Ireland, etc).
- excluded_species.csv
  - List of Lepidoptera species (from Agassiz, Beavan & Heckford 2013) excluded from the database (primarily adventive or micro-moths).
- excluded_subspecies.csv
  - List of Lepidoptera subspecies/forms excluded from the database (source references similar to above).
- hostplant_list_stacked.csv
  - Raw data on larvae host plant preferences from Henwood, Sterling & Lewington (2020); multiple rows per species for multiple hostplants.
- hostplant_list_unstacked.csv
  - Table-formatted data from Henwood, Sterling & Lewington (2020) where each species has a single row with hostplants as columns; binary indicators denote known use.
- ReadMe.rtf
  - Detailed information on how each column was derived across ecological_traits.csv and the hostplant files; criteria for numbering; notes about data provenance and usage.
- References
  - Extensive list of data sources and literature underpinning the dataset (e.g., Agassiz et al. 2013; Eeles 2019; Henwood et al. 2020; Fox et al.; Rothamsted Insect Survey; UKBMS; MothsIreland; and others).

## Data schema and key definitions

- Header and boundary notes (Table 2 in ecological_traits.csv)
  - Core identifiers: abh_number, b&f_number, scientific_name, common_name, family.
  - Distribution and status fields: recorded_present across England, Wales, Scotland, Northern Ireland, Republic of Ireland; presence statuses (reintroduced, immigrant, resident).
  - Population and trend fields: extinction status (extinct_gb, extinct_i), red list status (red_list_gb, red_list_ireland), occupancy/tenure metrics (10 km squares, long/short-term trends, abundance trends).
  - Life cycle and phenology fields: diurnal/nocturnal activity, easily_disturbed_by_day, communal_nest, pupation location (above/below ground, hostplant-associated), wing-related traits (forewing_minimum/maximum, estimated_dry_mass), overwintering_stage, and generation-related indicators (obligate_univoltine, obligate_multivoltine, partial_generation).
  - Phenology timing: egg_stage, larval_stage, pupal_stage, adult_stage (monthly columns; some months may be uncertain or conditional on overwintering behavior).
  - Host plant and habitat fields: specificity, hostplant_category (monophagous/oligophagous/polyphagous), number_hostplants, hostplant_native_or_non_native, Ellenberg-based plant trait values (light, moisture, nitrogen, salt_tolerance), broad_host_plant_category, host_plant_section, common_hostplants, habitat categories (breeding habitats and subcategories).
- Data interpretation notes
  - Distribution and abundance data may be defined by different political boundaries depending on data sources.
  - A mix of binary indicators (1/2/3) and qualitative notes, with '?' indicating uncertainty in some months or stages.
  - Hostplant data tie to specific source nomenclature (Stace 2019; Henwood et al. 2020) and include both general and genus-level classifications.

## Provenance, sources, and acknowledgments

- Primary sources include Agassiz et al. (2013), Emmet & Heath (1991, 1992), Henwood et al. (2020), Hill et al. (1999), Waring & Townsend (2017), Eeles (2019), Randle et al. (2019), NMRS (2021), BNM (2021), MothsIreland (2021), Rothamsted Insect Survey (2021), UKBMS (2021), and others.
- Data contributors acknowledged for data permission and interpretation guidance (e.g., Henwood, Sterling, Lewington; Callum McGregor for dry mass interpretation).
- The dataset is intended for publication and dissemination under the citation Cook, P.M. et al. (2021) with DOI provided in the citation.

## Usage, governance, and caveats for Data Leaders

- Purpose and applicability
  - Facilitates data-driven decisions around Lepidoptera trait analysis, cross-border biodiversity assessments, and data-informed policy support or networked conservation planning.
  - Supports co-ownership and collaborative use of data products through transparent metadata and standardized trait definitions.
- Governance and quality considerations
  - Data are compiled from multiple authoritative sources with explicit provenance; users should respect source-specific limitations and boundary definitions.
  - The monthly and stage-specific fields require careful interpretation, especially where uncertainty indicators ('?') or cross-boundary data mappings exist.
  - Excluded lists indicate the dataset’s scope limitations; users should exclude or treat excluded taxa accordingly.
- Citation and reuse
  - Must cite Cook, P.M.; Tordoff, G.M.; Davis, A.M.; Parsons, M.S.; Dennis, E.B.; Fox, R.; Botham, M.S.; Bourn, N.A.D. (2021) when used in publications.
  - Data products, including any derived analyses, should acknowledge the original data sources and ReadMe guidance.
- Practical notes for integration
  - When integrating with other data systems, align boundary definitions and timeframes (GB, UK, Ireland, etc) as defined in Table 2 and accompanying metadata.
  - Use both stacked and unstacked hostplant data to support different analytical needs (detailed species-level vs. presence/absence per hostplant across species).
  - Leverage ReadMe.rtf for column derivations, data derivation criteria, and methodological context to ensure consistent interpretation.

- Overall, the dataset provides a comprehensive, multilayered trait resource for butterflies and macro-moths across Great Britain and Ireland, with robust metadata, clear provenance, and a structured framework suitable for advanced data leadership in data strategy, governance, and cross-organisational collaboration.