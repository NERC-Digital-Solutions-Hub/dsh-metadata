# A compendium of earthworm data sources and associated information from the UK and Ireland 1891-2021 Supporting Information

- Overview
  - A dataset compiling field-based earthworm data sources across the United Kingdom and Ireland up to 2021, including sources dating back to 1891 (the WormSource dataset).
  - Aims to gather quantitative earthworm data (incidence, abundance, biomass, taxa) and associated metadata to support earthworm abundance and niche modelling and a broader modelling framework for earthworm impacts on soil processes.
  - Part of the Soil Organic Carbon Dynamics (SOC-D) project funded by the NERC UK-SCAPE programme (Grant NE/R016429/1).

- Data Sources and Methodology
  - Systematic literature search in June–July 2020 using Web of Science and Google Scholar.
  - Search terms targeted earthworms and UK/Ireland geography; Google Scholar searches were country-specific to manage term length.
  - Screening process involved approximately 750 articles, focusing on sources with location data and field-obtained earthworm data; additional sources found via reviews and direct contact with authors/data managers.
  - Ultimately 257 data sources were compiled.
  - Metadata captured include: data type (incidence, abundance, biomass, taxa), sampling details (methods, locations, natural vs. experimental), and environmental information (habitat/land-use, climate data, soil properties).

- Key Data Characteristics
  - Sampling methods: hand-sorting (55%), chemical extractants (42%), with 16% using both methods.
  - Data types across sources: incidence (82%), abundance (68%), taxa (68%), biomass (49%).
  - Environmental data: soil data present in 43% of sources (e.g., texture, bulk density, pH, organic matter).
  - Habitats represented: grasslands (62%), arable (32%), woodland (22%).
  - Geographic coverage: England (51%), Republic of Ireland (ROI) (21%), Scotland (18%), Wales (13%), Northern Ireland (4%); many sources cover multiple locations.
  - Access to original documents: 17 potential data sources lacked accessible original documents at the time of compilation.

- Data Structure and Metadata
  - Core dataset: WormSource.UKIreland.csv containing structured metadata for each data source, with fields such as:
    - Source_ID, Study_ID, Source, Source_Type (Paper, Book chapter, Thesis, Report, Dataset)
    - DOI, Publication_Year
    - Data_Specific_Location ( farm/forest/field-level coordinates if available; otherwise broader location)
    - Sampling_Methods (combinations like hand-sorting + chemical extractant)
    - Method flags: Hand_Sorting, Chemical_Extractant, Under_Feature_Search, Electrical_Octet, Pitfall_Traps, Surface_Or_Cast_Counting, Other
    - Data flags: Incidence, Abundance, Biomass, Taxa, Species_Specific, Climate, Soil
    - Habitat flags: Arable, Grassland, Wooded, Wetland_Upland, Brownfield, Coastal, Freshwater_Shoreline, Urban, Horticulture, Other
    - Habitat_Notes: Natural_Or_Experimental
    - Spatial_Extent, General_Location, Country
    - Number_Of_Sites, Plot_Types_Sampled
    - First_Sampling_Year, Sampling_Years
  - The classification supports distinguishing data scope (natural vs. experimental), spatial scale, and the breadth of environmental context available with each data source.

- Coverage and Accessibility
  - Data span: up to 2021, encompassing historical and more recent field data.
  - Diversity of data types and environments enables broad analyses of earthworm communities and their environmental correlates.
  - Some data sources may require direct access requests to authors or data managers for detailed coordinates or unpublished data; 17 sources lacked accessible original documents at the time of compilation.

- Applications and Value for Data Support
  - Enable data combine-and-compare workflows across studies to build comprehensive earthworm abundance and niche models.
  - Facilitate the creation of self-serve data products (dashboards, pivot tables, charts) for end users to explore earthworm distributions, habitat associations, and temporal trends.
  - Support integration with climate and soil datasets to model earthworm responses and their implications for soil processes and carbon dynamics.
  - Help identify data gaps, promote data creation, and encourage data sharing among researchers and data holders.