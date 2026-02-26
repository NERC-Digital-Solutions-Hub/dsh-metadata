# A traits database for the Butterflies and Macro-moths of Great Britain and Ireland

## Overview
- A dataset describing traits for butterflies and macro-moths in Great Britain and Ireland, covering life cycle ecology, phenology, host plant preferences, breeding habitats, morphology, distribution, and abundance trends.
- Composed of six files: ecological_traits.csv, excluded_species.csv, excluded_subspecies.csv, hostplant_list_stacked.csv, hostplant_list_unstacked.csv, ReadMe.docx.
- Primary citation for use: Cook, P.M., et al., 2021. A traits database for the Butterflies and Macro-moths of Great Britain and Ireland.

## File contents and structure (what the data contain)
- ecological_traits.csv
  - 970 rows, 293 KB.
  - Traits include life cycle ecology, phenology, host plant specificity and characteristics, breeding habitat, and morphological characteristics.
  - Contains presence/absence data by political boundary (Great Britain, United Kingdom, Ireland) and trends (occupancy and abundance) drawn from multiple recording schemes and literature.
  - Includes extensive columns on life stages (egg, larval, pupal, adult) across monthly timeframes, overwintering strategies, diurnal/nocturnal activity, disturbance sensitivity, habitat usage, and hostplant relationships (monophagous, oligophagous, polyphagous, hostplant columns, and hostplant categories).
  - Several derived fields (e.g., red list status, 10 km squares occupancy, long/short term distribution trends, abundance trends, and significance indicators for trends).
  - Notes on header merging (Table 2) and on political boundary definitions used in the data.
  - Key caution: some fields are derived or model-based (e.g., estimated dry mass) and latitudinal differences in phenology were not accounted for in some monthly columns.

- excluded_species.csv
  - 2022 rows.
  - List of Lepidoptera species excluded from the database (mainly adventive or micro-moth taxa).
  - Columns include ABH number, b&f number, scientific_name, vernacular_name, family.

- excluded_subspecies.csv
  - 276 rows.
  - List of Lepidoptera subspecies and forms excluded from the database.
  - Columns include ABH number, b&f number, scientific_name, vernacular_name, family.

- hostplant_list_stacked.csv
  - 4955 rows, raw data.
  - Raw, stacked format for butterfly/macro-moth larvae host plant preferences; species may appear on multiple rows per hostplant.
  - hostplants named according to Stace (2019); data originates from Henwood, Sterling & Lewington (2020).

- hostplant_list_unstacked.csv
  - 798 rows, unstacked format.
  - Each species appears in a single row with hostplants represented as columns; cells marked with 1 indicate known use of that hostplant.

- ReadMe.docx
  - Detailed metadata guidance for ecological_traits.csv, excluded_species.csv, excluded_subspecies.csv, hostplant_list_stacked.csv, and hostplant_list_unstacked.csv, including derivation criteria and references.
  - Table 1: Files in the repository; Table 2: Headers of ecological_traits.csv; Table 3–6: Headers for other files.
  - Provides criteria for numbering, data provenance, and acknowledgement of data sources.

## Data provenance and metadata
- Primary sources and references feeding the dataset include:
  - Agassiz, Beavan & Heckford (2013); Henwood, Sterling & Lewington (2020); Waring & Townsend (2017); Hill et al. (1999) for Ellenberg values; Stace (2019); Rothamsted Insect Survey; UKBMS; NMRS; MothsIreland; and national red list assessments (Ireland and GB).
  - Specific data streams include Butterflies for the New Millennium (BNM 2021), National Moth Recording Scheme (NMRS 2021), and MothsIreland, among others.
- The dataset explicitly notes boundary definitions:
  - Great Britain: England, Scotland, Wales.
  - United Kingdom: England, Scotland, Wales, Northern Ireland.
  - Ireland: island including Northern Ireland and the Republic of Ireland.
  - Additional notes reference the Republic of Ireland, Isle of Man, and Channel Islands where relevant to trend data.

## Usage, citation, and caveats
- Usage: The dataset is designed to support data discovery, combination, analysis, and the creation of data products for exploration (e.g., dashboards, self-serve analyses) in line with Data Support aims.
- Citation: Cook, P.M., Tordoff, G.M., Davis, A.M., Parsons, M.S., Dennis, E.B., Fox, R., Botham, M.S., Bourn, N.A.D., 2021. A traits database for the Butterflies and Macro-moths of Great Britain and Ireland. Butterfly Conservation & Centre for Hydrology and Ecology, United Kingdom.
- Notable caveats for data users:
  - Some headers are merged to save space (Table 2 in ecological_traits.csv) with explicit notes on the relationships between columns (e.g., monthly egg/larval/pupal/adult stages).
  - Data are drawn from multiple sources and may use different political boundaries for reporting presence/absence and trends.
  - Certain numerical fields (e.g., estimated dry mass) are model-derived and should be treated with caution.
  - Phenology and overwintering data may not be consistently latitudinally adjusted across all species and time periods.
  - Some fields may contain missing or uncertain values (e.g., '?') and trend significance indicators (Y/N) reflect the statistical treatment described in the ReadMe.

## Practical takeaways for Data Support work
- The ecological_traits.csv file provides a comprehensive, multi-dimensional trait matrix suitable for cross-species comparisons, trend analyses, and habitat/hostplant research.
- The stacked vs unstacked hostplant lists enable flexible data integration strategies:
  - Stacked format is useful for aggregations across hostplants.
  - Unstacked format is convenient for species-centric queries with binary hostplant indicators.
- The ReadMe and header documentation are essential for accurate interpretation, data cleaning, and reproducible analyses.
- The dataset supports dashboard-style self-service exploration of presence, trends, life cycle stages, hostplant associations, and habitat associations across GB and Ireland.