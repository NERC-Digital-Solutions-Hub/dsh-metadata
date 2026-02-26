# A traits database for the Butterflies and Macro-moths of Great Britain and Ireland

## Overview
- Dataset comprises six files: ecological_traits.csv, excluded_species.csv, excluded_subspecies.csv, hostplant_list_stacked.csv, hostplant_list_unstacked.csv, ReadMe.doc.
- Purpose: a comprehensive traits database for butterflies and macro-moths of Great Britain and Ireland; suitable for GIS-based analysis and map visualisations.
- Must be cited as: Cook et al. 2021, A traits database for the Butterflies and Macro-moths of Great Britain and Ireland.

## Data files and what they contain
- ecological_traits.csv
  - Life cycle ecology, phenology, host plant specificity, breeding habitat, morphology, conservation status, distribution (occupancy) trend, and abundance trend.
  - Data include multiple resolutions (broader categories split into sub-categories) and various status/trend indicators.
  - Headers and data definitions are described in ReadMe.pdf and Table 2 notes.
  - Distribution/abundance data are aligned to political boundaries (see Boundaries section).
- excluded_species.csv
  - List of Lepidoptera species excluded from the database (mainly adventive or micro-moths).
- excluded_subspecies.csv
  - List of Lepidoptera subspecies/forms excluded from the database.
- hostplant_list_stacked.csv
  - Raw data on larval host plant preferences; multiple rows per species corresponding to hostplants used.
- hostplant_list_unstacked.csv
  - Table-formatted host plant data; one row per species with hostplants as columns; a 1 indicates a known hostplant use.
- ReadMe.doc
  - Detailed methodology for deriving columns, numbering criteria, and data provenance; includes references used.

## Key fields and mapping-relevant content (highlights for GIS)
- Geographic scope and boundaries
  - Distribution data referenced to political boundaries: Great Britain (England, Scotland, Wales), United Kingdom (GB + Northern Ireland), and Ireland (Republic of Ireland + Northern Ireland).
  - Some trend data explicitly notes boundaries including the Republic of Ireland, Isle of Man, and Channel Islands where relevant.
- Presence, status, and trends
  - recorded_present (country-level presence columns), reintroduced, immigrant, resident, extinct_gb, red_list_gb, red_list_ireland.
  - 10 km grid square counts (gb/ireland) for occupancy records (where available).
  - Long-term and short-term distribution trends (gb; with range and significance indicators), abundance trend (gb), and significance flags.
  - Diurnal/nocturnal, easily disturbed by day, communal nesting, and various overwintering strategies.
- Life cycle and phenology
  - Egg_stage (12 months), larval_stage (12 months with uncertainty markers), pupal_stage (12 months, with partial overwintering indicators), adult_stage (12 months).
  - Overwintering_stage (main vs lesser strategies) and related notes.
  - Phenology shift (year-to-year flight period changes), including significance flags.
- Habitat and host plants
  - Habitat/breeding habitats (broad categories and subcategories), with detailed notes on scope (e.g., scrub/hedgerows, wet woodland, montane upland).
  - Hostplant specificity (monophagous, oligophagous by genus/family, polyphagous), number of hostplants, common hostplants, and hostplant sections.
  - Hostplant native vs non-native, Ellenberg indicator values for hostplants (light, moisture, reaction, nitrogen, salt tolerance), and broad host plant categories.
  - Hostplant lists (stacked and unstacked) link hosts to species via ABH numbers.
- Morphology and mass
  - Estimated dry mass (cautioned model-based values; best for cross-family analyses).
  - Forewing size ranges (minimum/maximum) and wing-wing-related traits.
- Data provenance and quality notes
  - Multiple sources; data can vary in resolution and completeness.
  - Some phenology fields do not account for latitudinal variation.
  - Mass and some trait estimates should be used with caution; thoroughly reference metadata for each field.
- Metadata and headers
  - Table 2 (headers for ecological_traits.csv) provides definitions and data source mappings for each column; distribution boundaries and column-level notes are included.

## Spatial scope and considerations
- Boundaries used for data interpretation may differ by source; users should consult Table 2 and ReadMe for exact boundary definitions per column.
- Grassroots spatial cues include country-level presence, occupancy trends, and 10 km grid-based measures (where provided).
- When visualising trends, note that significant/non-significant status is indicated (e.g., sig_long_term_distribution_trend_gb, sig_short_term_distribution_trend_gb).

## Data quality, provenance, and usage notes
- Data integrate multiple authoritative datasets (e.g., Butterflies for the New Millennium, UKBMS, MothsIreland, Rothamsted Insect Survey, etc.).
- The ReadMe explains column derivations, numbering criteria, and references; Table 1–6 list file details and sizes.
- Practical cautions for GIS work:
  - Expect blanks in many fields; join with other datasets to fill gaps where needed.
  - Latitudinal phenology variation is not captured in some monthly columns.
  - Mass/density estimates are model-derived and should be used for comparative analyses rather than exact biomass per species.
- Proper citation is required when using any data from this database.

## How this supports GIS workflows
- Rich, multi-resolution attribute data enable:
  - Distribution maps by country and by 10 km grid squares.
  - Temporal trend maps (long-term, short-term, and abundance) with significance overlays.
  - Phenology and life-stage maps (egg/larva/pupa/adult) by month.
  - Habitat- and hostplant-based thematic maps, including hostplant category, section, native status, and Ellenberg-based environmental preferences.
  - Species-hostplant interaction layers (via ABH numbers) for co-distribution analyses.
- Suitable for layering with external GIS datasets (e.g., land cover, climate, or vegetation data) to explore drivers of distribution and phenology.

## Citation and references
- Cook, P.M., Tordoff, G.M., Davis, A.M., Parsons, M.S., Dennis, E.B., Fox, R., Botham, M.S., Bourn, N.A.D., 2021. A traits database for the Butterflies and Macro-moths of Great Britain and Ireland. Butterfly Conservation & Centre for Hydrology and Ecology, United Kingdom.
- Acknowledges data sources and related literature cited in ReadMe.doc (e.g., Henwood et al., Waring & Townsend, Ellenberg values, UKBMS, MothsIreland, Rothamsted Insect Survey, etc.).