# A compendium of earthworm data sources and associated information from the UK and Ireland 1891-2021 Supporting Information

## Overview
- A centralized, field-based dataset (WormSource) compiling earthworm data sources and metadata from the United Kingdom and Ireland up to 2021, with records dating back to 1891.
- Aims to gather quantitative earthworm data (incidence, abundance, biomass, taxa) and associated methodological and environmental information to support earthworm abundance and niche modelling, and a broader modelling framework for earthworm impacts on soil processes.
- Generated as part of the Soil Organic Carbon Dynamics (SOC-D) project funded by the NERC UK-SCAPE programme (Grant NE/R016429/1).

## Data scope and sources
- Systematic literature search (Web of Science and Google Scholar) conducted around June–July 2020; supplementary data obtained directly from authors/data managers when possible.
- 257 data sources compiled, spanning 1891–2021, across the UK and Ireland; many sources include multiple locations or regions within countries.
- Most sources located in England (51%), followed by ROI (21%), Scotland (18%), Wales (13%), and Northern Ireland (4%); a map (Figure 1) illustrates country distribution.
- Some original documents could not be obtained for 17 potential data sources, resulting in gaps in extra metadata.

## Data content and metadata
- Metadata categories for each data source include:
  - Data type: incidence, abundance, biomass, taxa (and sometimes data at species level or entire community).
  - Methodology: sampling methods (e.g., hand-sorting, chemical extractants, combinations), and whether plots were natural or experimental; additional methods like electrical octets, pitfall traps, surface/cast counting, or other methods.
  - Environmental context: climate data and basic soil properties if available.
  - Habitat/land-use: habitat type(s) sampled (grassland, arable, woodland, wetland, brownfield, coastal, freshwater/shores, urban, horticulture, other).
  - Sampling details: sampling year(s), location details, spatial extent (single site, regional, or broader), number of sites, plot types sampled, and whether data are incidence, abundance, biomass, or taxa data.
- Data across sources show:
  - Data types: incidence (82%), abundance (68%), taxa (68%), biomass (49%).
  - Soil data availability: 43% of sources include some soil data (e.g., texture, pH, moisture, bulk density, organic matter, carbon/nitrogen content).
  - Habitat distribution: grasslands (62%), arable (32%), woodland (22%); other habitats represented in smaller proportions.
  - Common sampling methods: hand-sorting (55%), chemical extractants (42%), with 16% using both methods.
- Structure and access:
  - The primary data structure is the dataset WormSource.UKIreland.csv, containing fields such as Source_ID, Study_ID, Source_Summary, FirstAuthor_LastName, Source, Source_Type, DOI, Publication_Year, Data_Specific_Location, Sampling_Methods, and multiple binary indicators for data types, climate/soil data, and habitat categories.
  - Location data availability is variable; newer datasets may have location data available upon request.

## Data structure and accessibility
- Dataset fields cover unique identifiers, bibliographic details, data availability at site-level coordinates, sampling methods, and presence/absence of climate, soil, and habitat information.
- Location specificity ranges from precise site coordinates to more general town/county levels; newer entries may provide finer detail upon request.
- Acknowledges gaps where original documents are missing, limiting the depth of metadata for some sources.

## Methodological context
- Data sources vary in sampling scope and methodology, with many sources spanning multiple sites or regions.
- The compilation supports building earthworm abundance and niche models and contributes to broader soil-process modelling efforts.

## Limitations and considerations for monitoring
- Gaps due to unavailable original documents for some sources and incomplete metadata for others.
- Biomass data are less frequently reported compared with incidence and abundance.
- Inconsistent metadata quality across centuries and studies may affect comparability.
- The need for standardized metadata and data governance to enable transparent sharing, replication, and reuse.

## Relevance for monitoring frameworks
- Provides a comprehensive inventory of earthworm data sources and rich metadata essential for:
  - Selecting indicators (incidence, abundance, taxa, biomass) and modelling approaches.
  - Assessing data availability, gaps, and biases across habitats, climates, and geographies.
  - Designing data workflows with explicit provenance, quality checks, and provenance trails.
  - Informing data governance, openness, and metadata standards to facilitate data sharing and reuse.

## Practical implications for policy and decision-making
- Enables evidence-based monitoring design for soil biodiversity and soil health with earthworms as key indicators.
- Highlights where data are robust (e.g., grasslands in England) and where data gaps exist (certain habitats, regions, or data types like biomass).
- Supports development of modelling frameworks to predict earthworm-driven soil process dynamics under varying environmental conditions.

## Funding and provenance
- Project funded under SOC-D by NERC UK-SCAPE (Grant NE/R016429/1).