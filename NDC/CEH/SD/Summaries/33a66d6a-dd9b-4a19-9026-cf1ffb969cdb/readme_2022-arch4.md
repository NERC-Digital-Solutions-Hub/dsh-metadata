# A traits database for the Butterflies and Macro-moths of Great Britain and Ireland

## Overview
- Comprehensive dataset describing life-cycle ecology, host-plant relationships, breeding habitats, distribution, abundance, and conservation status for butterflies and macro-moths of Great Britain and Ireland.
- Outputs across six files: ecological_traits.csv, excluded_species.csv, excluded_subspecies.csv, hostplant_list_stacked.csv, hostplant_list_unstacked.csv, ReadMe.docx.
- Published citation: Cook, P.M. et al. 2021. A traits database for the Butterflies and Macro-moths of Great Britain and Ireland.

## Data assets and structure
- ecological_traits.csv (970 rows; 293 KB): core traits table including life cycle ecology, phenology, host plant specificity, breeding habitat, morphological traits, distribution (presence by political area), abundance trends, and conservation status.
- excluded_species.csv (2022 rows; 97 KB): Lepidoptera species excluded from the database (primarily adventive or micro-moths).
- excluded_subspecies.csv (276 rows; 19 KB): excluded subspecies/forms.
- hostplant_list_stacked.csv (4955 rows; 179 KB): raw larval hostplant data; multiple rows per species where multiple hostplants are used.
- hostplant_list_unstacked.csv (798 rows; 612 KB): single-row-per-species format listing hostplants across columns; binary indicators for usage.
- ReadMe.docx (286 KB): detailed methodology, column derivations, data provenance, and references.

## Key data domains
- Life cycle and phenology
  - Monthly staging: egg_stage (12 months), larval_stage (monthly with uncertainty markers), pupal_stage (monthly with overwintering notes), adult_stage (monthly).
  - Overwintering strategies: overwintering_stage with main vs. lesser strategies; multiple overwintering possibilities noted.
  - Phenology shifts: phenology_shift and sig_phenology_shift_ indicators; date ranges for 1970s vs 2000–2016 comparisons.
- Distribution and trends
  - Presence: recorded_present across Great Britain (England, Scotland, Wales), Ireland, Northern Ireland, and related political boundaries; reintroduced/immigrant/resident/extinct statuses included.
  - Trends: long_term_distribution_trend_gb, short_term_distribution_trend_gb; abundance_trend_gb with significance flags and ranges.
  - Significance flags (sig_ fields): Y/N indicators for statistical significance where applicable.
  - Granularity: data aligned to political boundaries; GB vs Ireland-specific trends and extents; 2000–2016 occupancy data for GB and related areas.
- Conservation status and geography
  - Red List statuses for GB and Ireland; historical and recent extinction notes.
  - 10 km grid-square counts of records (gb_10_km_squares_(2000-2016), ireland_10_km_squares_(2000-2016)).
  - Habitat, and geographical distribution indicators.
- Life-history and morphology
  - Diurnal/nocturnal activity; easily disturbed indicators; communal/nest feeding; below-ground and other pupation habitats.
  - Morphometrics: forewing_minimum/maximum, estimated_dry_mass (model-derived; treat with caution).
- Host-plant associations
  - Hostplant breadth: monophagous/oligophagous/polyphagous definitions and counts (number_hostplants).
  - Hostplant lists: stacked vs unstacked formats; hostplant_category, host_plant_section, common_hostplants columns.
  - Habitat and hostplant context: native vs non-native status, Ellenberg values (light, moisture, reaction, nitrogen, salt tolerance) linked to hostplants.
- Habitat and breeding context
  - Breeding habitats captured with detailed subcategories (e.g., 1c_scrub_and_hedgerows, 1d_wet_woodland, 4c_acid_grassland, 5_wetland, montane_upland variants).
  - Habitat-attribution methodology and multiple habitat assignments per species.

## Data provenance and metadata
- Data compiled from multiple sources: British Isles Lepidoptera checklists, Butterfly Conservation and national recording schemes (BNM/NMRS/UKBMS), Henwood et al. 2020 hostplant data, Waring & Townsend, Emmet & Heath, Hill (Ellenberg values), Randle et al. (moth trends), and others.
- ReadMe.docx provides column-level explanations, data derivation criteria, and the numbering scheme used across files.
- Political boundary definitions explicitly stated: Great Britain, United Kingdom, Ireland, Isle of Man, Channel Islands, with metadata clarifying coverage for trend data.

## Data quality, limitations, and caveats
- Some data are model-derived or based on historical datasets; caution advised for certain numeric estimates (e.g., estimated_dry_mass).
- Monthly phenology and overwintering data may lack latitudinal granularity; analyses assume uniform monthly patterns within defined areas.
- Data ranges for trends and occupancy reflect the sources and years cited (e.g., 2000–2016 for GB occupancy; 2010–2014 red-list contexts).
- Uncertainty indicators exist (e.g., '?', '2' for partial overwintering, etc.) to flag data confidence.

## Usage, access, and citation
- Intended for use in cross-species trait analyses, distribution and phenology research, and conservation planning across Great Britain and Ireland.
- Proper citation required: Cook et al. 2021; include dataset citation in publications.
- Metadata-rich design supports data discovery, provenance tracking, and reuse across networks of data users and partners.

## Practical considerations for Data Leaders
- Use the ecological_traits.csv as a central trait matrix for integration with other data systems (e.g., policy analysis, habitat management, and biodiversity dashboards).
- Leverage hostplant_list_{stacked|unstacked} to study host-plant breadth and specialization in relation to conservation priorities.
- Reference ReadMe.docx and headers Table 2 for precise field definitions, boundary scopes, and data interpretation rules.
- Consider data governance implications: track lineage from multiple sources, note data update cycles, and document limitations when communicating with stakeholders.