# A compendium of earthworm data sources and associated information from the UK and Ireland 1891-2021 Supporting Information

## Overview
- Compendium of field-based earthworm data sources and metadata across the UK and Ireland (WormSource), compiled up to 2021 (dating back to 1891).
- Metadata covers quantitative data types (incidence, abundance, biomass, taxa), sampling methodologies, locations, sampling years, and environmental context (habitat/land-use, climate data availability, soil properties).
- Data collection aimed at enabling earthworm abundance and niche modelling and developing a framework for earthworm impacts on soil processes.
- Part of the Soil Organic Carbon Dynamics (SOC-D) project funded by NERC UK-SCAPE (Grant NE/R016429/1).

## Data collection and scope
- Systematic literature search conducted in June–July 2020 using Web of Science and Google Scholar.
- Searches yielded 364 (WoS) and 38,000+ (Google Scholar) results; approximately 750 articles screened after deduplication and country-specific filtering.
- Publications selected if they contained location information and at least one earthworm species or field-derived abundance/biomass data; additional sources found via reviews and direct contact with authors.
- Total of 257 data sources compiled.
- Some sources (17 potential data sources) could not be obtained as original documents, limiting access to additional information.

## Data content and metadata
- Data sources include:
  - Data types: incidence (82%), abundance (68%), taxa (68%), biomass (49%).
  - Environmental context: climate data (Data_Climate), soil data (Data_Soil) present in 43% of sources.
  - Habitat information: grasslands (62%), arable (32%), woodland (22%); additional habitat categories captured via binary fields (e.g., coastal, urban, wetland, etc.).
- Sampling methods (most common):
  - Hand-sorting (55%)
  - Chemical extractant (42%)
  - Combination of hand-sorting and chemical extractant (16%)
- Data sources dominated by England (51%), with ROI (21%), Scotland (18%), Wales (13%), Northern Ireland (4%). Many sources include sampling across multiple locations or regions.
- Some original documents could not be obtained, constraining metadata depth for those sources.
- Figure 1 (not reproduced here) illustrates the number of data sources per country.

## Data structure (WormSource.UKIreland.csv)
- Core fields include:
  - Source_ID, Study_ID, Source_Summary, FirstAuthor_LastName, Source, Source_Type, DOI, Publication_Year
  - Data_Specific_Location (location precision; field-level data available if Yes)
  - Sampling_Methods (and subfields: Method_Hand_Sorting, Method_Chemical_Extractant, Method_Under_Feature_Search, Method_Electrical_Octet, Method_Pitfall_Traps, Method_Surface_Or_Cast_Counting, Method_Other)
  - Data_Incidence, Data_Abundance, Data_Biomass, Data_Taxa, Data_Species_Specific, Data_Climate, Data_Soil
  - Habitat_Arable, Habitat_Grassland, Habitat_Wooded, Habitat_Wetland_Upland, Habitat_Brownfield, Habitat_Coastal, Habitat_Freshwater_Shoreline, Habitat_Urban, Habitat_Horticulture, Habitat_Other, Habitat_Notes Natural_Or_Experimental
  - Spatial_Extent, General_Location, Country
  - Number_Of_Sites, Plot_Types_Sampled
  - First_Sampling_Year, Sampling_Years
- Data_Specific_Location indicates whether precise site coordinates are available (Yes) or not readily available (No; general location like town or county level). Newer datasets may be accessible on request.
- The fields enable GIS-ready attributes linked to sampling effort, habitat type, data type, and potential environmental covariates (climate, soil).

## Geographic distribution and sampling coverage
- England accounts for about half of data sources; ROI, Scotland, Wales, and Northern Ireland comprise the remainder with smaller shares.
- Many data sources involve sampling across multiple locations, regions, or countries, enabling broader spatial analyses.

## Data availability and access
- Metadata and data sources compiled to facilitate integration into GIS and modelling workflows.
- Location data availability varies by source; precise site-level data may be restricted or require author/data manager access.
- Some data sources lack full original documentation, potentially limiting reproducibility for certain records.

## GIS applications and use cases
- Enables mapping of data source locations, sampling density, and habitat associations for earthworms.
- Supports spatial analyses of earthworm incidence, abundance, biomass, and taxa in relation to habitat types, soil properties, and climate data.
- Facilitates development of earthworm abundance and niche models, and integration into soil process modelling frameworks.

## Limitations and caveats
- Potential geographic bias toward England and English-language literature; underrepresentation of some regions.
- Incomplete access to original documents for some data sources; missing metadata for those sources.
- Variability in sampling methods, data types, and taxonomic resolution across sources, which may affect cross-source comparability.
- Location precision is not uniform; some records provide only coarse location data.

## Provenance and funding
- Data compiled as part of the SOC-D project under the UK-SCAPE programme (Grant NE/R016429/1).