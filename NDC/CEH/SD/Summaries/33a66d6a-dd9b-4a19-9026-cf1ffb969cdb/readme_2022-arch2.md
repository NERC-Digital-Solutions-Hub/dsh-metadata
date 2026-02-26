# A traits database for the Butterflies and Macro-moths of Great Britain and Ireland

## Purpose and relevance for environmental monitoring analysts
- Provides a standardized, citable dataset to assess environmental health and policy performance over time for Lepidoptera in Britain and Ireland.
- Combines life-cycle ecology, phenology, host-plant relationships, habitat use, morphology, and conservation status into a single resource.
- Supports cross-cutting analyses by linking species traits with distribution and abundance trends from established monitoring schemes.

## What is included
- ecological_traits.csv: trait information on life cycle ecology, phenology, host plant specificity, breeding habitat, morphology; includes conservation status, distribution/occupancy trends, and abundance trends.
- excluded_species.csv: Lepidoptera species excluded from the database (primarily adventive or micro-moths).
- excluded_subspecies.csv: Lepidoptera subspecies/forms excluded from the database.
- hostplant_list_stacked.csv: raw data on larvae host plant preferences; multiple rows per species for multiple hostplants; hostplants named per Stace (2019).
- hostplant_list_unstacked.csv: table-formatted hostplant data; single row per species with hostplants as columns; 1 indicates known use.
- ReadMe.docx: metadata descriptions, data derivation notes, column criteria, and references used; provides detailed provenance and guidance.

## Data structure and metadata (highlights)
- Headers and data structure in ecological_traits.csv are described in Table 2; some categories are merged for compactness (e.g., monthly egg stage represented across 12 monthly columns in the data).
- Geographic boundaries defined in metadata:
  - Great Britain: England, Scotland, Wales
  - United Kingdom: GB plus Northern Ireland
  - Ireland: island including Northern Ireland and Republic of Ireland
  - Republic of Ireland, Isle of Man, Channel Islands noted where relevant for trends
- Key trait and status fields include:
  - presence/absence and distribution in specified political areas
  - occupancy and abundance trends (long/short term, significant tests)
  - life-stage timing: diurnal/nocturnal, larval/pupal/adult stages by month
  - overwintering strategies, larval/pupal overwintering details, and overwintering multiplicity
  - habitat and breeding habitat categories (broad and subcategories)
  - hostplant associations (monophagous, oligophagous, polyphagous; main/occasional/also reported; native/non-native)
  - hostplant characteristics (Ellenberg light, moisture, reaction, nitrogen, salt tolerance)
  - broad host-plant category and host-plant section allocations
  - common hostplants and habitat associations
  - morphological data points (e.g., forewing measurements, body mass estimates with caution)
- Source data come from multiple schemes and publications (BNM, NMRS, MothsIreland, UKBMS, Rothamsted Insect Survey, Henwood et al., Stace, etc.) and are compiled with explicit references listed in ReadMe and the References section.

## Provenance, sources, and citation
- Dataset assembled from established monitoring and taxonomic sources; primary citation:
  Cook, P.M., Tordoff, G.M., Davis, A.M., Parsons, M.S., Dennis, E.B., Fox, R., Botham, M.S., Bourn, N.A.D., 2021. A traits database for the Butterflies and Macro-moths of Great Britain and Ireland. Butterfly Conservation & Centre for Hydrology and Ecology, United Kingdom.
- Acknowledgments note collaboration with Henwood, Sterling, Lewington and others for hostplant data and guidance on interpretation of biomass estimates.
- Users must cite the dataset as above in publications.

## How the data can be used (outputs and applications)
- Standardized trait data to analyze environmental health indicators, species responses to environmental change, and policy performance over time.
- Enables analyses linking species traits (phenology, host-plant use, habitat) with distribution and abundance trends.
- Supports creation of reports, maps, and charts for monitoring programs and decision-making.
- Facilitates cross-dataset integration by providing underlying trait dimensions alongside occupancy and trend data.

## Data quality, governance, and accessibility
- Data are quality-assured and derived from recognized sources; ReadMe documents column derivation, criteria, and data provenance.
- The database stores and provisions data likely for upload to appropriate portals (as per the “How they meet their aims” archetype).
- Clear guidance provided on boundaries, data coverage, and the need to account for variation in political-boundary reporting in different components.

## Practical considerations for analysts
- Data integration potential: designed to be combined with other monitoring datasets to enhance the value of presence, occupancy, and abundance information.
- Underlying data provenance is explicit; monthly phenology, stage- specific presence, and hostplant data allow nuanced cross-species and cross-region analyses.
- Limitations and cautions:
  - Some fields (e.g., biomass estimates) are model-derived and should be treated with caution; best for cross-species comparisons rather than precise mass estimates.
  - Latitudinal differences in phenology are not fully accounted in egg/larval/pupal monthly data.
  - Some status fields (extinct/immigrant/resident) rely on historical and source-specific definitions; users should review metadata for boundary and year coverage.
- Accessibility and reuse:
  - The dataset is designed for reuse by researchers and practitioners; a formal citation is required for publications.
  - Hostplant data include both stacked and unstacked formats to support different analysis approaches.

## Summary for analysts monitoring the environment
- This six-file database provides a comprehensive, citable suite of Lepidoptera traits (ecology, phenology, habitat, hostplants, morphology) plus occupancy and trend data from established GB/Ireland monitoring programs.
- It enables consistent, time-aware assessment of environmental health through standardized outputs and supports integration with additional environmental datasets to enhance monitoring and policy evaluation.
- Proper use requires attention to metadata on boundaries, data sources, temporal coverage, and cautions around model-based estimates.