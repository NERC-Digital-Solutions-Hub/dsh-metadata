# River Habitat Survey - spot-check data

## Overview
- Data describe the River Habitat Survey (RHS) spot-check component, containing sections E, F and G of the RHS (Environment Agency, 2003) as part of the Glastir Monitoring & Evaluation Programme (GMEP) in Wales.
- GMEP is a Welsh Government initiative (2013–2016 rollout) to monitor environmental outcomes from agri-environment schemes (AES) and to quantify status and trends related to climate, biodiversity, soil, water quality, and woodland expansion.
- The programme uses a consistent, ecosystem-based approach with standardized field methods, multi-metric integration, and a common 1 km square spatial unit across Wales.

## Datasets and schemas
- GMEP_STREAM_DIATOMS_2013_16.csv
  - Diatom species counts per 1 km square, expressed as percent of sample. Includes SQ_ID, SPECIES_NAME, COUNT, year, and 10 km grid coordinates. Only samples summing to 100% ±1% are included.
  - Taxonomic references and identification methods described; analyzed by Bowburn Consultancy.
- GMEP_STREAM_INVERTS_2013_16.csv
  - Stream invertebrate abundance by species per square. Includes SQ_ID, SPECIES_NAME, COUNT, coordinates, and year. Sorting and identification follow standard QA procedures.
- GMEP_STREAM_SITE_INFO_INVERTS_2013_16.csv
  - Site information for headwater sampling (RIVPACS context). Includes SQ_ID, LC, coordinates, SAMPLE_DATE, METHOD, habitat metrics, and various habitat descriptors.
- GMEP_STREAM_RHS_MAIN_2013_16.csv
  - Core RHS data (sections A, B, C, D, J, K, L, M, N, O, P, Q) for field survey details. Includes SQ_ID, coordinates, SAMPLE_DATE, PART_OF_RIV_OR_ART, ADV_COND, and extensive field notes on site conditions.
- GMEP_STREAM_RHS_BANK_2013_16.csv
  - RHS sections H and I (bank-related attributes) including LEFT/RIGHT bank materials, land use within banks, banktop structures, vegetation types, substrate, and related RHS indicators.
- GMEP_STREAM_RHS_WATER_CHEMISTRY_2013_16.csv
  - Stream water chemistry data for headwater streams. Includes SQ_ID, SITE_TYPE, DETERMINAND, VALUE, UNITS, DATE, and notes (LOD, detection limits). Includes conductivity, pH, PO4-P, TDN, alkalinity, etc.
- GMEP_STREAM_RHS_SPOTCHECK_2013_16.csv
  - RHS spot-check data (Sections E, F, G) focusing on notable nuisance plants and RHS-characteristic features. Includes HOGWEED_FACE/TOP, HIMALAYAN_BF/TO P, JAP_KNOTWEED_FACE/TOP, OTHER_FACE/TOP, major/minor RHS features, and related comments.
- GMEP_STREAM_MACROPHYTES_MTR_2013.csv
  - Macrophyte data from 2013 using Mean Trophic Rank (MTR) system. Includes SQ_ID, plant name, type, cover (on a 9-point scale), year, and location metadata.
- Additional RHS metadata fields
  - Various RHS-related fields (e.g., RHS spotcheck descriptors, site geography, vegetation, and habitat classifications) are provided to support comprehensive habitat assessments across years.

- Common data elements across datasets
  - SQ_ID: 1 km square identifier
  - EASTING_10km / NORTHING_10km: OSGB 1936 coordinates (10 km resolution)
  - LC: Land Classification code
  - YEAR: Survey year (2013–2016)
  - Various habitat, substrate, and vegetation descriptors
  - -9999/-9 markers denote missing or not-relevant data in several tables

## Sampling design and scope
- 4-year rolling survey cycle (2013–2016 for the first cycle)
- 300 x 1 km squares sampled over the cycle
  - Wider Wales squares: randomly sampled within strata defined by Land Classification (GB-wide framework)
  - Targeted squares: selected to focus on Glastir priority areas
- Exclusions: squares with >75% urban land or >90% sea (per LCM2007 data and census sea extent)
- Sampling aims: maximize site visits nationally and capture temporal and spatial variation to detect trends

## Data collection and analysis methods
- Field methods: standardized data collection described in Field Handbook (O’Hare et al., 2013)
- Diatoms: sample digestion with hydrogen peroxide, mountants, microscopy (Nikon BX40, 100x), alignment with established diatom taxonomic references; results expressed as percentage composition
- Invertebrates: sorting and counting invertebrates from sieved samples; identification to species level where possible with standard microscopes; QA includes random re-analysis
- Water chemistry: samples analyzed at UK Centre for Ecology & Hydrology (UKCEH) Lancaster using accredited methods; determinations include PO4-P, TDN, alkalinity, and conductivity/pH (field measurements)
- Community and habitat data: RHS main, RHS bank, RHS spot-check components collected per RHS methodology; 3-part RHS spot-check (E-F-G) covers nuisance species and habitat attributes
- Macrophytes: 2013 macrophyte data collected with MTR system; not extended to subsequent years

## Quality assurance and provenance
- DEFRA Joint Codes of Practice (JCoPR) followed for quality and research processes
- UKAS-accredited laboratories (UKCEH Lancaster) used for chemical analyses
- QA processes include re-analysis: one randomly selected sample per twenty re-analyzed by a different analyst
- Data are accompanied by extensive metadata describing units, data types, and field methods
- Nomenclature and taxonomic references are explicitly documented for diatoms
- Data tables include detailed field definitions, measurement units, and data provenance notes

## Metadata, documentation, and accessibility
- Field Handbook and references cited (O’Hare et al., 2013; Emmett et al., 2014/2017; various taxonomic references)
- Data descriptions include explicit field definitions, units, and data quality notes
- Notation such as -9999/-9 used to indicate missing data across tables
- Data are designed to support integration across metrics and future GB-wide analyses via common grid units

## Governance, access, and reuse
- Data produced under the Glastir Monitoring & Evaluation Programme for Welsh Government, with formal QA and standards adherence
- Rich metadata and standardized formats facilitate reuse, cross-dataset integration, and temporal/spatial trend analyses
- Researchers and data stewards should note the multi-table, multi-year architecture and ensure consistent interpretation of fields, units, and coding (e.g., missing value codes)

## Challenges and considerations for data stewards
- Incomplete or evolving user needs for multi-metric environmental datasets
- Timely collection and transfer of data across year cycles
- Ensuring data creators/collectors meet metadata and standardization requirements across diverse datasets
- Managing integration across many systems/formats and large volumes of data
- Interoperability across GB-wide and Welsh-specific data frameworks
- Handling legacy 2013 macrophyte data alongside 2014–2016 RHS datasets

## References and key sources
- Field Handbook: Glastir Monitoring & Evaluation Programme FIELD HANDBOOK Freshwater (2013)
- O’Hare et al. (2013) Field Handbook Freshwater
- Bunce et al. (2007) ITE Land Classification of Great Britain
- DEFRA/Environment Agency methodologies and QA guidelines
- UKCEH, JCoPR QA framework and UKAS accreditation
- Glastir Monitoring & Evaluation Programme (Emmett et al.; 2014–2017) final reports and annual summaries