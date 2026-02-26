# Glastir Monitoring & Evaluation Programme

- The Glastir Monitoring & Evaluation Programme (GMEP) in Wales collects evidence on the effectiveness of Glastir management interventions and general environment status, focusing on climate, biodiversity, soil, water quality, and woodland expansion.
- GMEP uses a four-year rolling survey (2013–2016) with two integrated components:
  - Wider Wales component for baseline estimation, national trends, and national reporting.
  - Targeted component focused on Glastir priority areas.
- A single common spatial unit of 1 km x 1 km squares is used to integrate data across components and enable future analyses with GB-wide surveys.

## Sampling design and coverage

- A total of 300 x 1 km squares are sampled over the four-year cycle.
  - Half are Wider Wales squares, randomly sampled within strata defined by the Land Classification of Great Britain to maximise environmental heterogeneity between strata.
  - The other half are targeted at Glastir priority areas.
- Exclusions: any square with more than 75% urban land or more than 90% sea is excluded.
- The sampling frame and method align with the Countryside Survey of Great Britain to enable future data integration.
- The national scale sampling supports robust indicators at national and sub-national levels across Wales and GB.

## Field data collection and sampling methods

- Up to 300 1 km squares are sampled using standardized field methods described in the Field Handbook (O’Hare et al., 2013).
- Data collection aims to capture multiple measures and metrics in a single snapshot visit, enabling an ecosystem-based approach and cross-scalar analyses.

## Data types and analyses

- Diatoms (GMEP_STREAM_DIATOMS_2013_16.csv)
  - Diatom counts presented as percentages of the sample; microscopy and taxonomy follow standard references; slides prepared with hydrogen peroxide digestion and mounting medium.
- Diatoms for river ecological status (GMEP_STREAM_DARES_2013_16.csv)
  - DARES dataset describing diatom-based assessments; includes 1 km square identifiers and year.
- Stream invertebrates (GMEP_STREAM_INVERTS_2013_16.csv)
  - Abundance counts by species; includes spacing and sampling metadata; QA includes random re-analysis.
- Invertebrate site information (GMEP_STREAM_SITE_INFO_INVERTS_2013_16.csv)
  - Site details for headwater stream sampling (RIVPACS context); includes sampling method and habitat proportions.
- Macrophytes (GMEP_STREAM_MACROPHYTES_MTR_2013.csv)
  - Macrophyte species and cover data from 2013 (Mean Trophic Rank system); includes taxonomic and coverage information.
- Water chemistry (GMEP_STREAM_WATER_CHEMISTRY_2013_16.csv)
  - Field measurements (conductivity, pH) and laboratory analyses (phosphate, TDN, alkalinity); QA via DEFRA Joint Codes of Practice; UKAS-accredited labs.
- River Habitat Survey (RHS) main data (GMEP_STREAM_RHS_MAIN_2013_16.csv)
  - Comprehensive RHS sections A–Q covering site details, river habitat features, river morphology, substrate, and related attributes.
- RHS spot-check data (GMEP_STREAM_RHS_SPOTCHECK_2013_16.csv)
  - Spot-check-based RHS data for E–G sections, including nuisance species observations and habitat features.
- RHS spot-check site data (GMEP_STREAM_RHS_SPOTCHECK_2013_16.csv)
  - Specific spot-check observations such as nuisance plant species (e.g., giant hogweed, Himalayan balsam, Japanese knotweed) and site-level remarks.
- RHS bank data (GMEP_STREAM_RHS_BANK_2013_16.csv)
  - River Habitat Survey sections H and I (sweep-up) focusing on bank materials, substrates, modifications, bank geometry, channel features, land use near banks, and RHS-scale descriptors.
- RHS site and bed features (implied by tables such as RHS_BANK and RHS_MAIN)
  - Rich set of fields describing channel morphology, vegetation, bank structure, embankments, water width/depth, and spatially explicit layout.

- All datasets include spatial identifiers (1 km square SQ_ID with Easting/Northing at 10 km resolution) and a consistent geographic reference (OSGB 1936). Years covered: 2013–2016.

## Data quality assurance and standards

- Quality assurance follows DEFRA Joint Codes of Practice (JCoPR) for robust science quality, repeatability, and auditability.
- UK Centre for Ecology & Hydrology (UKCEH) laboratories used for chemical analyses are UKAS accredited.
- Invertebrate data quality controlled via re-analysis of a random sample (1 in 20) by a different analyst.

## GIS and data integration considerations

- The 1 km square unit enables integration with other national surveys (e.g., Countryside Survey of Great Britain) and facilitates national and sub-national analyses.
- Data are distributed across multiple datasets and methods (diatoms, invertebrates, macrophytes, RHS, and water chemistry), requiring cross-dataset harmonization and careful metadata handling.
- Coordinates provided at 10 km resolution for privacy, with site-specific data linked by 1 km SQ_IDs.

## Implementation implications for data products

- GIS specialists can build map-based visualizations that show:
  - National and regional trends in biodiversity and ecosystem condition derived from multi-metric RHS and biological datasets.
  - Spatial distribution of Glastir priority areas versus Wider Wales baselines.
  - Relationships between land classification, habitat features, water chemistry, and biotic communities.
- The standardized 4-year rolling cycle supports temporal trend analyses and early prototype testing with feedback during development.

## Challenges and considerations

- Data are held in many places and across diverse formats, requiring careful data management and standardization.
- Gaps in data availability or resolution (especially high-resolution data) may limit certain analyses.
- Consistency in data standards across datasets is essential for successful integration.
- Large or complex datasets (spanning multiple taxa, habitats, and chemical parameters) require packaging into manageable components and thorough data cleaning and transformation.
- Building and maintaining teams with sufficient GIS, data management, and domain-specific expertise is critical.