# A compendium of earthworm data sources and associated information from the UK and Ireland 1891-2021 Supporting Information

## Overview
- A comprehensive compilation of field-based earthworm data sources across the United Kingdom and Ireland up to 2021, with records dating back to 1891.
- Metadata includes data type (incidence, abundance, biomass, taxa), sampling methods, locations, whether plots were natural or experimental, sampling years, and environmental context (habitat/land-use, climate data, soil properties).
- Aims to support development of earthworm abundance and niche models and a modelling framework for earthworm impacts on soil processes under the Soil Organic Carbon Dynamics (SOC-D) project (NERC UK-SCAPE grant NE/R016429/1).

## Data sources and collection methodology
- Data sources were identified via systematic searches of Web of Science and Google Scholar in June–July 2020, supplemented by direct contact with original authors/data holders.
- Searches yielded thousands of results; publications were included if they contained location information and at least one earthworm species or field-derived abundance/biomass data.
- In total, 257 data sources were compiled, including published papers, book chapters, theses, reports, and datasets.
- 17 potential data sources could not be accessed via original documents at the time of compilation.

## Content and coverage of the data
- Data types captured: incidence (82%), abundance (68%), taxa (68%), biomass (49%).
- Environmental context: climate data and basic soil properties included in 43% of sources.
- Habitat coverage: grasslands (62%), arable land (32%), woodland (22%), with various other habitats represented.
- Geographic distribution of data sources: England dominates (51%), followed by Republic of Ireland (ROI) (21%), Scotland (18%), Wales (13%), Northern Ireland (NI) (4%). Many sources include multiple locations or regions.
- Some original documents could not be obtained for 17 potential data sources, resulting in missing supplementary information.

## Data structure and metadata schema
- Core dataset: WormSource.UKIreland.csv with fields such as:
  - Source_ID, Study_ID, Source, Source_Type (paper, book chapter, thesis, report, dataset), DOI, Publication_Year
  - Data_Specific_Location (Yes/No) and availability of precise coordinates
  - Sampling_Methods and method-specific indicators (Hand_Sorting, Chemical_Extractant, Under_Feature_Search, Electrical_Octet, Pitfall_Traps, Surface_Or_Cast_Counting, Other)
  - Data types (Data_Incidence, Data_Abundance, Data_Biomass, Data_Taxa)
  - Data_Climate, Data_Soil
  - Habitat indicators (Habitat_Arable, Habitat_Grassland, Habitat_Wooded, Habitat_Wetland_Upland, Habitat_Brownfield, Habitat_Coastal, Habitat_Freshwater_Shoreline, Habitat_Urban, Habitat_Horticulture, Habitat_Other)
  - Habitat_Notes and Natural_Or_Experimental
  - Spatial_Extent (Single Site, Multiple site within a region, Multiple site across regions)
  - General_Location (approximate site location or broader region)
  - Country, Number_Of_Sites, Plot_Types_Sampled
  - First_Sampling_Year and Sampling_Years (data availability across years)
- Note: Location data availability varies; newer datasets may be obtainable upon request.

## Implications for data governance and stewardship
- Emphasizes the importance of standardized, rich metadata to enable reuse across studies and portals.
- Highlights the need for consistent documentation of sampling methods, data types, locations, and environmental covariates to support data discovery and interoperability.
- Underlines the role of data stewards in cataloguing, updating, and sharing datasets, and in documenting work performed on datasets.
- Points to the necessity of maintaining data provenance and clear notes on data limitations (e.g., missing original documents, restricted location data).

## Challenges and considerations for archiving
- Heterogeneity of data sources, formats, and metadata; many studies used older or bespoke methodologies.
- Incomplete or inaccessible original documents for a subset of sources.
- Location data may be limited or require permission/request to access more precise coordinates.
- Potentially large and multi-site datasets that require careful transfer and storage solutions.

## Relevance to Data Stewards
- Provides a ready-to-use, richly annotated catalogue of earthworm data sources that can be ingested into data portals and repositories.
- Demonstrates practical metadata fields and data-type classifications valuable for governance, quality assurance, and data discovery.
- Serves as a case study for standardizing data schemas, documenting methods and environmental context, and planning updates and data sharing protocols.

## Funding and provenance
- Part of the Soil Organic Carbon Dynamics (SOC-D) project funded by the NERC UK-SCAPE programme (Grant NE/R016429/1).