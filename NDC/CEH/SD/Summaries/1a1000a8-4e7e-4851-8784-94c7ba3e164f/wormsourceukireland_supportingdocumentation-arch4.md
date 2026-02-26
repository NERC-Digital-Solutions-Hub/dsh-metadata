# A compendium of earthworm data sources and associated information from the UK and Ireland 1891-2021 Supporting Information

## Overview and purpose
- Compiles field-based earthworm data sources and metadata from the UK and Ireland (1891–2021), titled "WormSource".
- Aims to gather quantitative earthworm data (incidence, abundance, biomass, taxa) and associated environmental information to support earthworm abundance and niche modelling and a modelling framework for earthworm impacts on soil processes.
- Part of the Soil Organic Carbon Dynamics (SOC-D) project funded by the NERC UK-SCAPE programme (Grant NE/R016429/1).

## Data sources, scope, and coverage
- 257 data sources compiled to date.
- Data sources identified through systematic literature searches (Web of Science and Google Scholar) and direct outreach to authors/data managers.
- Original documents could not be obtained for 17 potential data sources.
- Geographic coverage within the UK and Ireland includes multiple countries and regions, with England contributing the largest share of sources (51%), followed by the Republic of Ireland (ROI) 21%, Scotland 18%, Wales 13%, and Northern Ireland 4%.
- Habitat coverage across data sources: grasslands (62%), arable (32%), woodland (22%), with other habitats represented as available.

## Data content and metadata
- For each data source, metadata captures:
  - Type of quantitative earthworm data: incidence, abundance, biomass, taxa.
  - Methodological details: sampling methods, locations, whether plots were natural or experimental, sampling years.
  - Environmental context: habitat/land-use, climate data availability, basic soil properties.
- Data are structured to enable model development, including information about location precision and data availability.
- Most common data types across sources: incidence (82%), abundance (68%), taxa (68%), biomass available in 49% of sources.
- Soil data present in 43% of sources (e.g., texture, bulk density, pH, moisture, organic matter, C/N content).
- Habitat categories across sources are broadly diverse, but legible grouping includes grassland, arable, and woodland.
  
## Data structure and access
- The dataset WormSource.UKIreland.csv contains structured fields such as:
  - Source_ID, Study_ID, Source_Summary, FirstAuthor_LastName, Source, Source_Type, DOI, Publication_Year
  - Data_Specific_Location (farm/forest/field-level data available; otherwise general location)
  - Sampling_Methods (including combinations)
  - Specific sampling method indicators (Hand_Sorting, Chemical_Extractant, Under_Feature_Search, Electrical_Octet, Pitfall_Traps, Surface_Or_Cast_Counting, Other)
  - Data indicators (Incidence, Abundance, Biomass, Taxa, Species_Specific)
  - Climate_Data and Soil_Data availability
  - Habitat indicators (Arable, Grassland, Wooded, Wetland/Upland, Brownfield, Coastal, Freshwater/Shoreline, Urban, Horticulture, Other)
  - Habitat_Notes, Natural_Or_Experimental, Spatial_Extent, General_Location, Country, Number_Of_Sites, Plot_Types_Sampled
  - First_Sampling_Year, Sampling_Years, and related fields for temporal coverage
- Newer datasets may have location data available upon request.

## Methodology of data compilation
- Literature search conducted in June–July 2020 using terms related to earthworms and UK/Ireland geography.
- Searches included separate country-focused queries on Google Scholar due to term length limitations.
- Screening process: approximately 750 articles screened; 257 data sources ultimately compiled.
- Data collection prioritised sources with location information and earthworm data from field sampling, including published and unpublished datasets.

## Implications for data strategy and governance (Data Leaders perspective)
- Demonstrates the value of a centralized, queryable meta-dataset to support data discovery, provenance, and reuse across institutions.
- Highlights the importance of rich metadata to enable cross-dataset integration, reproducibility, and model development.
- Underlines ongoing needs for data standardization (uniform definitions of data types, sampling methods, and habitat categories) to improve interoperability.
- Points to access and equity considerations (some original documents unavailable; some location data may require direct contact) as areas to address for smoother data sharing.
- Supports a collaborative, community-driven approach to data collection and sharing, aligning with broader data-system co-ownership and stewardship goals.

## Challenges and opportunities
- Fragmented data sources and scattered availability impede quick data discovery and integration.
- Paywalls and data protection barriers can hinder access to certain datasets.
- Gaps in data granularity and standardized metadata across sources present obstacles to rapid benchmarking and comparison.
- Potential opportunities to strengthen cross-sector communities of practice and to extend the dataset with new, standardized data streams for enhanced soil-process modelling.