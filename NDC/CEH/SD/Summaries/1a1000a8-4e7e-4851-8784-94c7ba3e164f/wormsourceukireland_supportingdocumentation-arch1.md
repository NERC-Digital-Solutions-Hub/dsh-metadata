# A compendium of earthworm data sources and associated information from the UK and Ireland 1891-2021 Supporting Information

## Overview
- Presents a compendium of field-based earthworm data sources and associated metadata from the UK and Ireland (WormSource), compiled up to 2021 and dating back to 1891.
- Metadata cover quantitative earthworm data types (incidence, abundance, biomass, taxa), sampling methods, locations, habitat/land-use, climate data, and basic soil properties.
- Data collected via literature searches (Web of Science, Google Scholar) and direct data holders; intended to support earthworm abundance and niche models and a modelling framework for earthworm impacts on soil processes.
- Part of the Soil Organic Carbon Dynamics (SOC-D) project funded by NERC UK-SCAPE (Grant NE/R016429/1).

## Data Sources and Coverage
- 257 data sources compiled from systematic searches and author/dataset contacts.
- Most common data types: incidence (82%), abundance (68%), taxa (68%), biomass (49%).
- Soil data included in 43% of sources; climate data included where available.
- Habitat distribution across data sources: grasslands (62%), arable (32%), woodland (22%); other habitats also present.
- Geographic distribution: England most represented (51%), Republic of Ireland (ROI) 21%, Scotland 18%, Wales 13%, Northern Ireland 4%; many data sources span multiple locations/countries.
- Figure 1 (not shown here) maps the number of data sources by country.
- Original documents could not be obtained for 17 potential data sources, limiting extra metadata.

## Data Structure and Metadata
- Core dataset: WormSource.UKIreland.csv containing structured metadata for each data source.
- Key fields include:
  - Source_ID and Study_ID: unique identifiers
  - Source and Source_Type: publication type (paper, book chapter, thesis, report, dataset)
  - DOI and Publication_Year: bibliographic identifiers
  - Data_Specific_Location: availability of precise farm/forest/field-level coordinates (Yes/No; some data available on request)
  - Sampling_Methods and subfields (Method_Hand_Sorting, Method_Chemical_Extractant, etc.)
  - Data indicators (Data_Incidence, Data_Abundance, Data_Biomass, Data_Taxa, Data_Species_Specific)
  - Data_Climate and Data_Soil: presence of climate/soil data (Yes/No)
  - Habitat indicators (Habitat_Arable, Habitat_Grassland, Habitat_Wooded, Habitat_Wetland_Upland, Habitat_Brownfield, Habitat_Coastal, Habitat_Freshwater_Shoreline, Habitat_Urban, Habitat_Horticulture, Habitat_Other)
  - Habitat_Notes on natural vs. experimental data
  - Spatial_Extent and General_Location: sampling extent (Single Site, Multiple sites within a region, etc.)
  - Country and Number_Of_Sites: geographic scope and sampling intensity
  - Plot_Types_Sampled: total plot types per site
  - First_Sampling_Year and Sampling_Years: temporal coverage
- Data fields may be missing or vary in availability across sources; newer datasets may offer finer location data upon request.

## Sampling Methods and Data Availability
- Predominant sampling methods: hand-sorting (55%) and chemical extractants (42%), with 16% using both.
- Data coverage across data types varies by source; incidence and abundance are common, biomass less so; taxa data commonly recorded in a substantial subset.
- Environmental data (soil, climate) available for a portion of sources; habitat classification widely captured.
- Location data may be precise (farm/field-level) or generalized; precise data often require author data managers or direct access.

## Temporal and Geographic Coverage
- Temporal span: data from 1891 through 2021.
- England is the most sampled region; ROI, Scotland, Wales, and Northern Ireland follow in descending order.
- Many sources include sampling across multiple locations or regions, enabling broader-scale analyses but also introducing heterogeneity in methods and contexts.

## Uses, Gaps, and Considerations for Analysts
- Designed to support analyses of earthworm abundance and niche modeling, and to inform soil process modelling and SOC dynamics.
- Strengths: broad temporal span, a wide range of data types, and integration of environmental and habitat metadata.
- Challenges: variable data quality and standardization across sources; missing original documents for 17 sources; uneven geographic and habitat coverage; location data accessibility restrictions for some datasets.
- Considerations for modelling: harmonize methodological differences, address spatial/temporal biases, and integrate available soil/climate data where present.
- Data accessibility: location data may require direct contact with data holders; some data are available only in older publications or as summarized metadata.

## Funding and Purpose
- SOC-D project funded by NERC UK-SCAPE (Grant NE/R016429/1) supports the compilation and use of this dataset for earthworm-related soil process modelling.