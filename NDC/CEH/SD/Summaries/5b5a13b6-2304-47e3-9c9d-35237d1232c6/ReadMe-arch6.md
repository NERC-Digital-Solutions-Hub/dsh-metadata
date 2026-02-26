# Traits data for the butterflies and macro-moths of Great Britain and Ireland, 2021

## Overview
- A six-file dataset (plus ReadMe) creating a comprehensive traits database for butterflies and macro-moths of Great Britain and Ireland, 2021.
- Aimed at enabling analysis of life cycle ecology, phenology, host plant associations, breeding habitats, morphology, distribution, and abundance trends.
- Data synthesized from multiple sources with extensive metadata to support data quality, provenance, and reproducibility.
- Includes a formal citation to be used in publications and acknowledgments to original data providers.

## Files and what they contain
- ecological_traits.csv
  - Traits on life cycle ecology and phenology, host plant specificity and characteristics, breeding habitat, and morphological traits.
  - Includes conservation status, distribution/occupancy trend, and abundance trend.
  - Offers data at varying resolutions (broader categories split into sub-categories for detail).
  - Metadata in ReadMe.pdf (supplementary information) explains data derivation.
- excluded_species.csv
  - List of Lepidoptera species excluded from the database (mainly adventive or micro-moths).
- excluded_subspecies.csv
  - List of Lepidoptera subspecies/forms excluded from the database.
- hostplant_list_stacked.csv
  - Raw data on larvae host plant preferences (multiple rows per species for multiple hostplants).
  - Hostplants named according to Stace (2019).
- hostplant_list_unstacked.csv
  - One-row-per-species format; hostplants listed as columns; binary indicator (1 means known to use that hostplant).
- ReadMe.rtf
  - Detailed methods on how each column across the datasets was derived, including criteria and numbering explanations.
- ReadMe (text) and References
  - Acknowledgments and references for data sources and related works.

## Data content and structure
- Species identifiers and taxonomy
  - abh_number, b&f_number, scientific_name, common_name, family.
- Distribution and presence
  - recorded_present across England, Wales, Scotland, Northern Ireland, and the Republic of Ireland.
  - Status indicators for reintroduction, residency, and immigrant patterns.
- Red lists and conservation
  - red_list_gb and red_list_ireland (GB and Ireland statuses).
- Range, occupancy, and abundance trends
  - gb_10_km_squares, ireland_10_km_squares (historical occupancy/coverage).
  - long_term_distribution_trend_gb, sig_long_term_distribution_trend_gb, range_long_term_distribution_trend_gb.
  - short_term_distribution_trend_gb, sig_short_term_distribution_trend_gb, range_short_term_distribution_trend_gb.
  - abundance_trend_gb, sig_abundance_trend_gb, range_abundance_trend_gb.
- Life history and phenology
  - diurnal and nocturnal activity indicators.
  - overwintering_stage, pupal_stage, larval_stage, egg_stage, adult_stage (monthly or monthly-aggregated columns; some >12 months with special codes).
  - larval_overwintering and pupal_overwintering details (including multiple overwintering options and uncertainty markers).
- Habitat and host plants
  - specificity (monophagous, oligophagous-genus, oligophagous-family, polyphagous).
  - number_hostplants and hostplant-related fields (specificity, native/non-native status, Ellenberg values for light, moisture, nitrogen, salt tolerance).
  - broad_host_plant_category and host_plant_section (habitat-specific feeding locations like roots, stems, leaves, bark, etc.).
  - common_hostplants (top hostplants by species) and detailed hostplant lists (stacked and unstacked formats).
- Breeding habitat and habitat categorization
  - habitat categories and subcategories used for breeding (e.g., 1_woodland, 1a_broadleaved_woodland, wet woodland, acid grassland, wetlands, montane upland, etc.).
- Morphology and mass (where available)
  - estimated_dry_mass (with caveats: model-based estimates, most reliable for forewing length >12.5 mm).
- Other traits
  - wing measurements (forewing_minimum, forewing_maximum), wingedness (wingless_reduced_wing_female), egg/larval/pupal timing, and other trait indicators.

## Geography and boundaries
- Political/administrative boundaries used in the dataset
  - Great Britain: England, Scotland, Wales.
  - United Kingdom: England, Scotland, Wales, Northern Ireland.
  - Ireland: Isle of Ireland (includes Northern Ireland and Republic of Ireland).
  - Notes indicate some distribution/abundance data exist at different political boundaries depending on source; metadata clarifies which area each column covers.

## Data provenance and sources
- Primary data sources cited within the metadata (examples)
  - Butterflies for the New Millennium (BNM 2021), NMRS (National Moth Recording Scheme 2021), MothsIreland (2021).
  - Historic and contemporary references for life cycles, red lists, and distribution (e.g., Emmet & Heath, Fox et al., Waring & Townsend, Henwood et al., Randle et al., etc.).
  - Host plant information from Henwood, Sterling & Lewington (2020) and Stace (2019).
- Acknowledgments recognize data providers and the contributors who allowed use of raw hostplant data.

## Usage, citation, and provenance
- The dataset must be cited in publications with the provided citation: Cook, P.M. et al. (2021). Traits data for the butterflies and macro-moths of Great Britain and Ireland, 2021. NERC EDS Environmental Information Data Centre.
- A list of references accompanies the dataset, detailing primary data sources and related literature.
- Acknowledgments highlight data providers and contributors to the compilation.

## Formats, size, and accessibility
- File sizes and row counts:
  - ecological_traits.csv: 324 KB, 970 rows.
  - excluded_species.csv: 97 KB, 2022 rows.
  - excluded_subspecies.csv: 19 KB, 276 rows.
  - hostplant_list_stacked.csv: 179 KB, 4955 rows.
  - hostplant_list_unstacked.csv: 612 KB, 798 rows.
  - ReadMe.rtf: 271 KB.
- Rich metadata and header guidance are provided to interpret complex, multi-dimensional trait data and to map the columns to biological concepts.

## Key considerations for data use (Data Support perspective)
- Data richness with extensive trait coverage enables cross-species comparisons of life history, habitat, and hostplant interactions.
- The dataset integrates multiple, sometimes heterogeneous data sources with explicit boundary definitions; users should consult metadata to understand scope and boundary applicability for analyses.
- Some fields (e.g., months for life stages, overwintering tactics) include uncertainties or special coding (e.g., '?', 1/2/3), requiring careful data cleaning and interpretation.
- Temporal coverage includes occupancy and trend data up to circa 2016 for certain presence indicators and up to 2021 for other sources; users should verify the exact periods when conducting time-series analyses.
- The inclusion of stacked and unstacked hostplant data supports both broad overview analyses and detailed, row-level examinations of hostplant use.

## Practical takeaway
- This dataset provides a comprehensive, well-documented foundation for analyzing the ecology, phenology, hostplant relationships, and distribution trends of Britain and Ireland’s butterflies and macro-moths, suitable for creating self-service data products, dashboards, or targeted policy/research insights, with robust provenance and usage guidance.