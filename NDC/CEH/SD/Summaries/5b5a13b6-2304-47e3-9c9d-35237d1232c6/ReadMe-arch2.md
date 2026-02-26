# Traits data for the butterflies and macro-moths of Great Britain and Ireland, 2021

## Overview
- A dataset describing life-cycle ecology and phenology, host plant specificity, breeding habitat, morphological traits, conservation status, distribution trends, and abundance trends for butterflies and macro-moths of Great Britain and Ireland.
- Comprises six files: ecological_traits.csv, excluded_species.csv, excluded_subspecies.csv, hostplant_list_stacked.csv, hostplant_list_unstacked.csv, ReadMe.rtf (plus a ReadMe.pdf-style explanation in supplementary info) and a references list.
- Aims to support standardized, time-consistent environmental monitoring and policy performance assessment; designed for reuse alongside other environmental data.

## What the dataset covers
- Life-cycle ecology and phenology (egg, larval, pupal, adult stages; overwintering; diurnal/nocturnal activity; developmental timing).
- Host plant specificity and host plant categories, including native/non-native status and Ellenberg-based ecological values.
- Breeding habitats and habitat sections (detailed hierarchical categories for breeding sites and hostplant sections).
- Morphological characteristics (forewing dimensions, dry mass estimates with cautions about model-based estimates).
- Conservation status (Red List in GB and Ireland), occupancy and abundance trends, and long/short-term distribution trends with significance flags.
- Spatially explicit information through 10 km grid references and country-level occupancy data (GB, Ireland, and cross-boundary notes).
- Data are cross-referenced to multiple sources, with explicit metadata about boundary definitions.

## File descriptions (key points)
- ecological_traits.csv (970 rows, 324 KB): Traits across life cycle, host plant specificity, habitat, conservation status, distribution and abundance trends; includes multi-resolution habitat and hostplant categories; detailed header notes and boundary definitions.
- excluded_species.csv (2022 rows, 97 KB): Lepidoptera species excluded from the database (mainly adventive or micro-moths).
- excluded_subspecies.csv (276 rows, 19 KB): Lepidoptera subspecies/forms excluded.
- hostplant_list_stacked.csv (4,955 rows, 179 KB): Raw stacked hostplant data; multiple rows per species per hostplant.
- hostplant_list_unstacked.csv (798 rows, 612 KB): Unstacked per-species rows; a single row per species with hostplants as columns; binary indicators for usage.
- ReadMe.rtf (and supplementary metadata): Detailed derivation of columns, data sources, and criteria; includes Table 1 (files) and Table 2–6 header descriptions.
- References: Comprehensive citations for data sources and methods (e.g., Agassiz et al. 2013; Fox et al.; Henwood et al. 2020; Eeles 2019; Randle et al. 2019; NMRS, MothsIreland, etc.).

## Data fields and metadata (highlights)
- Core identifiers: abh_number, b&f_number, scientific_name, common_name, family.
- Distribution presence: recorded_present across England, Wales, Scotland, Northern Ireland, Republic of Ireland (with source notes).
- Status indicators: reintroduced, immigrant, resident; GB and Ireland-specific presence and overwintering notes.
- Trends: long_term_distribution_trend_gb, sig_long_term_distribution_trend_gb, range_long_term_distribution_trend_gb; short_term_distribution_trend_gb, sig_short_term_distribution_trend_gb, range_short_term_distribution_trend_gb; abundance_trend_gb, sig_abundance_trend_gb, range_abundance_trend_gb.
- Life-cycle timing: diurnal, nocturnal, larval_stage monthly indicators (12 months), pupal_stage monthly indicators, adult_stage monthly indicators; overwintering_stage.
- Overwintering and morphology: multiple overwintering strategies; partial overwintering indicators; forewing_minimum/maximum; estimated_dry_mass (model-based, with cautions).
- Phenology and generation: obligate_univoltine, obligate_multivoltine, partial_generation, phenology_shift.
- Host plant data: specificity (monophagous/oligophagous/polyphagous), number_hostplants, hostplant_or_hostplant_category and hostplant_category_min/max; hostplant_native_or_non_native; ported Ellenberg values (light_value, moisture_value, nitrogen, salt_tolerance); broad_host_plant_category and detailed host plant sections (roots, stems, leaves, seeds, etc.).
- Habitat and hostplant associations: habitat categories (breeding habitats, roots/stem/shoot, leaves, etc.), common_hostplants, and 20 listed hostplants/genera for each species.
- Data provenance: notes on data origins (BNM, NMRS, MothsIreland, Emmet & Heath, Henwood et al., Waring & Townsend, etc.), and years of data coverage (up to 2016 for some indicators).

## Geographic boundaries and metadata
- Boundary definitions used: Great Britain (England, Scotland, Wales); United Kingdom (GB + Northern Ireland); Ireland (Republic of Ireland + Northern Ireland); explicit notes on Channel Islands and Isle of Man where relevant.
- Distribution and trend data may be aligned to different political boundaries depending on the source; metadata documents the exact scope per column.

## Data sources and provenance
- Primary data streams: Butterflies for the New Millennium (BNM), National Moth Recording Scheme (NMRS), MothsIreland, UK Butterfly Monitoring Scheme (UKBMS), Rothamsted Insect Survey (RIS).
- Published checklists and red lists; field guides and peer-reviewed sources (e.g., Emmet & Heath; Waring & Townsend; Henwood et al.; Randle et al.).
- The ReadMe and supplementary materials describe column derivations, numbering criteria, and data processing steps.

## How this supports environmental monitoring
- Provides standardized traits and trends to assess environmental health and insect biodiversity over time.
- Enables integration with other environmental datasets (habitat, climate, land-use) to enhance monitoring value beyond single-use analyses.
- Structured outputs (reports, maps, charts) can support policy performance review and conservation planning.
- Includes mechanisms to access underlying data (hostplant lists, trait details) for transparency and re-use.

## Data quality, caveats, and considerations
- Some data are model-derived or expert-judgment-based (e.g., estimated dry mass; habitat classifications).
- Occupancy and trend data may be bounded by source boundaries and varying recording effort; occupancy models are noted for long-term trends.
- Missing values and uncertainty are indicated (e.g., '?' in monthly larval/pupal/adult columns; blanks where estimates could not be calculated).
- A clear caveat: use of mass data and other model-based fields should be cautious and appropriate to cross-species analyses.
- The ReadMe provides detailed documentation on column derivations, criteria, and data provenance to support proper interpretation.

## Access, storage, and usage recommendations
- Data should be cited using the provided citation: Cook et al. 2021 (Traits data for the butterflies and macro-moths of Great Britain and Ireland, 2021).
- Ensure alignment of boundary definitions with the selected analyses (GB vs Ireland vs UK-wide).
- Store and upload the resulting datasets to appropriate monitoring portals, as recommended in the metadata.
- For analysts: verify data quality, apply standardized methods, and generate outputs (maps, charts, reports) to compare environmental health and policy performance over time.
- Consider integrating these traits with broader environmental datasets to maximize their value and support data-sharing goals.