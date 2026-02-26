# Eurasian pollen data from 21 kiloannum to the present

## Overview
- Results of a data collection workshop held in Winchester in April 2008.
- Contributors, mostly from the Former Soviet Union, added unpublished pollen data to a new database.
- Objective: define the most likely vegetation types (biomes) represented by fossil pollen from the Last Glacial Maximum (21 ka) to the present.
- Dataset includes 96 sites across 24°E (western Ukraine and Belarus) to eastern Siberia, north of 40°N, with 99 entities (reflecting multiple cores or sections at sites).

## Provenance, sampling, and site information
- Fieldwork was conducted prior to the workshop; analysts prepared and identified pollen and spores.
- At the workshop, additional site information was added (e.g., bog vs lake, surrounding local vegetation).
- Site-level details capture location, environment, and sampling context.

## Dating, age modelling, and data quality
- Radiocarbon dates calibrated and age models constructed using CLAM v1.2 (Blauuw, 2010).
- Age assignments for samples provided with error estimates (Table 3).
- Age model descriptors summarized in Table 5.
- Taxonomic data include both original taxon names (TaxonName) and taxonomy-cleaned names (TaxonClean) to support consistent analyses.

## Taxonomy, data cleaning, and annotations
- TaxonName reflects initial identifications; regional taxonomy differences noted (e.g., Duschekia fruticosa vs Alnus fruticosa).
- Non-pollen identifications (e.g., Dyadosporites as a fungus) deleted from analyses.
- Taxonomy is standardized to ITIS via TaxonClean; TaxonClean and the original TaxonName are both available for reference.
- Taxonomy table (Table 6) documents the mapping between TaxonName and TaxonClean.

## Data structure and content
- Site Table: SiteID, SiteName, DataSubmitter, SurfaceSample, Elevation, LatDD, LonDD, Notes.
- Entity Table: SiteID, SiteName, EntityID, EntityName, LocalVeg, Age_model_ID, Age_model, SampleUsage, No_of_rc_dates, Outliers, Site_Description_notes.
- Sample Table: SiteID, SiteName, EntityID, EntityName, SampleID, DepthCM, Cal yr BP, Error, AgeSlice, SampleUsage.
- Pollen Table: SiteID, SiteName, EntityID, EntityName, SampleID, DepthCM, TaxonName, TaxonClean, ITIS, PollenCount.
- Age Model Table: Age Model ID, Age Model description.
- Taxonomy Table: TaxonName, TaxonClean.

## Availability and publication status
- The complete database will be available from the Southampton University website.
- The dataset is slated for publication in Quaternary Science Reviews in 2017 (in press).
- References: Blauuw (2010) for age modelling methodology; Blauw 2010 methods and code for classical radiocarbon sequence modelling.

## Potential analytical uses and considerations
- Enables reconstruction of Eurasian past vegetation biomes from 21 ka to present.
- Facilitates cross-site comparisons through standardized taxonomy (TaxonClean) and harmonized age models.
- Data can be used to explore correlations between pollen assemblages and local vegetation, climate proxies, or site environments (bog vs lake).
- Important to account for age model uncertainties and differences in sampling depth and site context when aggregating across sites.