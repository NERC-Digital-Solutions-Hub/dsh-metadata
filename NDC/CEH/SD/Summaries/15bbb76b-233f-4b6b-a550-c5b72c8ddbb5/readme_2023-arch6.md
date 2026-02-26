# A traits database for the Butterflies and Macro-moths of Great Britain and Ireland

## Overview
- A curated dataset describing life-cycle ecology, phenology, host plant preferences, breeding habitats, and morphology for butterflies and macro-moths of Great Britain and Ireland.
- Composed of multiple CSV files and accompanying documentation that together enable analysis and self-service exploration of species traits and host plant associations.
- Data sources span national recording schemes, published field guides, and specialist checklists, with explicit metadata and provenance.

## Dataset contents
- ecological_traits.csv
  - Core traits across life cycle ecology, phenology, host plant specificity and characteristics, breeding habitat, morphological traits, distribution and abundance trends, and related status indicators.
  - Includes hierarchical data resolution (broader categories with subcategories) and a wide set of indicator fields (e.g., presence/absence by country, red list status, extinction/immigration/resident statuses, long- and short-term distribution/abundance trends, diurnal/nocturnal activity, larval/pupal/adult stages, overwintering strategies, and phenology).
  - Contains per-species numeric coding for various states (e.g., 1/2/3) and months for life stages (egg, larval, pupal, adult) with some uncertainty markers (?).
  - Host plant and habitat sections are extensive, integrating host plant specificity, host plant categories, host plant sections, common and scientific host plants, habitat types, and breeding habitat details.
  - Includes Ellenberg-based environmental values for host plants (light, moisture, reaction, nitrogen, salt tolerance) and broad/narrow taxon-level information.
- excluded_species.csv
  - List of Lepidoptera species excluded from the database (primarily adventive or micro-moth species) with identifiers and family information.
- excluded_subspecies.csv
  - List of Lepidoptera subspecies and forms excluded from the database, with identifiers and family information.
- hostplant_list_stacked.csv
  - Raw data on larval host plant preferences from Henwood, Sterling & Lewington (2020); multiple rows per species where multiple hostplants are used; hostplants named according to Stace (2019).
- hostplant_list_unstacked.csv
  - Table-formatted data from Henwood, Sterling & Lewington (2020) where each species has a single row with hostplants as columns; cells marked with 1 indicate known use of that hostplant.
- ReadMe.doc
  - Detailed documentation on how each column in the CSV files was derived, data processing criteria, and interpretation rules (including how header data are structured, merges to save space, and notes on political boundary definitions).
- References and Citations
  - Comprehensive list of sources used for data assembly (illustrative sources include Agassiz et al. 2013; Fox et al. 2015/2019; Emmet & Heath 1991/1992; Henwood et al. 2020; Waring & Townsend 2017; Ellenberg values; and national recording schemes such as BNM, NMRS, UKBMS, MothsIreland, etc.).
  - The dataset must be cited as: Cook, P.M. et al., 2021. A traits database for the Butterflies and Macro-moths of Great Britain and Ireland. Butterfly Conservation & Centre for Hydrology and Ecology, United Kingdom.

## Data schema and headers (highlights)
- Key identifiers and taxonomy
  - abha_number, b&f_number, wiemers_checklist_number, k&r_number, scientific_name, common_name, family.
- Distribution and status
  - recorded_present by country/region (England, Wales, Scotland, Northern Ireland, Republic of Ireland) with sources; reintroduced/immigrant/resident/extinct statuses; country-level red list statuses; 10 km square occupancy counts; long/short term distribution and abundance trends; significance indicators for trends; range/date range fields.
- Life cycle and phenology
  - diurnal/nocturnal; easily_disturbed_by_day; communal or nest behavior; pupation positions (below ground, on ground, hostplant, internal, external, stones, dead wood, etc.); overwintering_stage; larval/pupal/adult monthly presence indicators (12-month grids) with potential uncertainty markers.
- Phenology specifics
  - phenology_shift and sig_phenology_shift_ flags; egg_stage (12 monthly columns), larval_stage (12 monthly columns, with possible uncertain markers), pupal_stage (12 monthly columns, with multiple-overwintering indicators), adult_stage (12 monthly columns; for moths, proportion-based presence thresholds).
- Host plants and plant environment
  - hostplant lists (stacked and unstacked formats), total hostplants, hostplant category, hostplant section, common_hostplants, and a broad_host_plant_category with numerous subcategories (e.g., grasses, trees, shrubs, mosses, fungi, detritus).
  - hostplant_native_or_non_native classification; Ellenberg indicator values for light, moisture, reaction, nitrogen, salt_tolerance; plant-numeric fields used to describe habitat associations.
- Habitat and breeding
  - habitat columns with both broad and subcategories; breeding habitats, including detailed examples like 1a_broadleaved_woodland; 1c_scrub_and_hedgerows; 4c_acid_grassland; 5_wetland; montane upland classifications; habitat assignment rules and exceptions.
- Data quality andNotes
  - guidance on how columns were merged to save space, and how to interpret merged examples (e.g., egg stage represented across 12 monthly columns but described in a single Table 2 header row).
  - caveats about data boundaries (Great Britain vs United Kingdom vs Ireland), and about how distribution data are tied to specific political areas per source.

## Data provenance and sources
- Data compiled from multiple authoritative sources, with explicit provenance in ReadMe and Table 2 header explanations.
- Primary sources include national recording schemes (BNM, NMRS, UKBMS, MothsIreland), field guides (Waring & Townsend; Henwood et al. 2020), checklists (Agassiz et al. 2013), red lists (Regan et al. 2010; Allen et al. 2016), and contemporary research (Randle et al. 2019; Kinsella et al. 2020) among others.
- ReadMe and Table 2 provide detailed mapping of how columns derive from each source and how data integration was performed.

## Usage guidance
- Intended for data exploration, cross-species comparisons, and creation of data products (dashboards, pivot tables) to support self-serve analysis of Lepidoptera traits and host plant interactions.
- Two formats for host plants:
  - Stacked (stacked.csv): wide coverage with multiple rows per species for each hostplant.
  - Unstacked (unstacked.csv): single row per species with hostplants as binary-flag columns.
- Data interpretation notes
  - 1, 2, 3 coding schemes indicate presence, predominance, or multiple/conditional states in various fields.
  - '?' marks indicate uncertainty or conditional presence (especially in larval/pupal months).
  - Biomass/dry mass values are model-derived and should be used cautiously (best for cross-family analyses rather than precise mass estimates).
  - Phenology fields are not latitudinally adjusted in the egg/larval/pupal/adult monthly grids; interpretations should account for possible geographic/latitudinal variation.
- Boundaries and terminology
  - Distribution and trend data are tied to political boundaries as defined in metadata (Great Britain, United Kingdom, Ireland, Isle of Man, Channel Islands) with explicit source notes for each boundary.
- Citation and reuse
  - Any use in publications requires the provided Cook et al. 2021 citation; data provenance and sources are detailed in the ReadMe and references.

## Practical considerations for data support
- When integrating data across files, align on scientific_name and abh numbers; use hostplant_list_unstacked for a compact species-by-hostplant view or stacked for a full hostplant-to-species mapping.
- Use the habitat and breeding habitat fields to classify species by ecological niche and to support habitat-risk or conservation planning analyses.
- Leverage the longitudinal trend fields (long_term_distribution_trend_gb, sig_long_term_distribution_trend_gb, short_term_distribution_trend_gb, etc.) to assess changes over time in distribution and abundance, with attention to whether significance indicators are present.
- Cross-reference red list statuses and extinction/resident/immigrant indicators to inform conservation prioritization and policy discussions.