# Eurasian pollen data from 21 kiloannum to the present

## Purpose and scope
- Collate unpublished pollen data from a data collection workshop (Winchester, April 2008) to define the most likely vegetation types (biomes) represented by fossil pollen since the Last Glacial Maximum (21 ka) to the present.
- Dataset covers 96 sites across 24°E to eastern Siberia, north of 40°N, comprising 99 entities (multiple cores or sections per site in some cases).
- Contributors were mostly from the Former Soviet Union; additional site information (e.g., bog vs lake) added at the workshop.

## Data collection and workflow
- Participants conducted fieldwork and prepared/analyzed pollen samples before the workshop; workshop supplemented site details where possible.
- Age modelling and radiocarbon calibration used CLAM v.1.2 (Blauuw, 2010) to generate age models; calibrated ages with error estimates are provided in the Sample Table.
- Taxonomic nomenclature retained original taxa (TaxonName) with regional variations; a harmonized TaxonClean column offers standardized taxonomy (aligned with ITIS). Non-pollen identifications were removed.

## Data structure and content
- Six interlinked tables define the dataset:
  - Site Table: SiteID, SiteName, DataSubmitter, SurfaceSample, Elevation, LatDD, LonDD, Notes.
  - Entity Table: SiteID, SiteName, EntityID, EntityName, LocalVeg, Age_model_ID, Age_model, SampleUsage, No_of_rc_dates, Outliers, Site_Description_notes.
  - Sample Table: SiteID, SiteName, EntityID, EntityName, SampleID, DepthCM, Cal yr BP, Error, AgeSlice, SampleUsage.
  - Pollen Table: SiteID, SiteName, EntityID, EntityName, SampleID, DepthCM, TaxonName, TaxonClean, ITIS, PollenCount.
  - Age Model Table: Age Model ID, Age Model description.
  - Taxonomy Table: TaxonName, TaxonClean.
- Taxonomy ensures consistency (TaxonClean) while preserving original identifications (TaxonName).

## Data quality and taxonomy
- Taxonomy cleaned to conform with ITIS; deletes non-pollen identifications (e.g., fungal Dyadosporites).
- TaxonClean records how uncertain identifications were handled (e.g., deletion where appropriate).
- Original identifications (TaxonName) are retained for reference.

## Data availability and publication
- The complete database will be available via the Southampton University website.
- Publication planned in Quaternary Science Reviews (2017, in press).
- Cited methods include Blauuw (2010) for age modelling methods and Quaternary Geochronology (2010) for related calibration approaches.

## Relevance for environmental monitoring and policy analysis
- Provides a standardized, quality-assured palaeo-vegetation dataset suitable for long-term environmental health assessments and policy performance reviews.
- Facilitates cross-site comparisons and biome reconstruction over time.
- Supports increasing the value of datasets by enabling access to underlying data and integration with other environmental datasets.