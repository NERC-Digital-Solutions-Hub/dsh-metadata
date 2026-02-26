# Eurasian pollen data from 21 kiloannum to the present

## Overview
- Results of a 2008 data collection workshop aimed at compiling unpublished pollen data into a new database to define likely vegetation types (biomes) since the Last Glacial Maximum (21 ka) to today.
- 96 sites across 24°E (western Ukraine/Belarus) to eastern Siberia, north of 40°N; 99 entities (site/entity combinations).
- Contributors were primarily from the Former Soviet Union; data include pollen counts, site context, and sampling details.

## Data Content and Structure
- Tables and fields
  - Site Table: SiteID, SiteName, DataSubmitter, SurfaceSample, Elevation, LatDD, LonDD, Notes.
  - Entity Table: SiteID, SiteName, EnitityID, EntityName, LocalVeg, Age_model_ID, Age_model, SampleUsage, No_of_rc_dates, Outliers, Site_Description_notes.
  - Sample Table: SiteID, SiteName, EnitityID, EntityName, SampleID, DepthCM, Cal yr BP, Error, AgeSlice, SampleUsage.
  - Pollen Table: SiteID, SiteName, EnitityID, EntityName, SampleID, DepthCM, TaxonName, TaxonClean, ITIS, PollenCount.
  - Age Model Table: Age Model ID, Age Model description.
  - Taxonomy Table: TaxonName, TaxonClean.
- Data provenance
  - Data collected and initially prepared by field researchers; workshop added contextual site information (e.g., bog vs. lake surroundings).
  - CLAM v. 1.2 used to calibrate radiocarbon dates and construct age models; age assignments and error estimates recorded (Table 3).
- Taxonomy and naming
  - Original TaxonName vs standardized TaxonClean to harmonize regional taxonomy differences (e.g., Duschekia fruticosa vs Alnus fruticosa).
  - Non-pollen identifications removed (e.g., Dyadosporites) and not used in analyses.
  - Taxonomy cleaned to be consistent with ITIS; TaxonClean kept alongside TaxonName for reference.
  - Instances where material was unidentifiable recorded with question marks; TaxonClean notes deletions (DELETE) for such entries.

## Data Quality, Standards and Provenance
- Quality assurance and standardization
  - Taxonomy harmonization to create a redundancy-free taxonomy (Table 6) while preserving the original identifications for reference.
  - Verification against ITIS to ensure consistent nomenclature.
- Metadata and documentation
  - Comprehensive metadata across Site, Entity, Sample, Pollen, Age model, and Taxonomy tables.
  - Detailed notes on sampling site context and age-model methodology.
- Data integrity and usability
  - Clear indication of data that could not be identified or used (e.g., DELETE entries in TaxonClean).
  - Age models and associated error estimates provided to support robust analyses.

## Access, Availability and Publication
- Availability
  - Complete database planned for publication on the Southampton University website.
  - Data set to be published in Quaternary Science Reviews in 2017 (in press).
- Supporting references
  - Blauuw, M. 2010. Methods and code for 'classical' age modelling of radiocarbon sequences. Quaternary Geochronology.
- Data submission and collaboration
  - Data submitters (contributors) are credited in the Site Table; workshop aggregated and expanded the data with additional site-level details where possible.

## Governance Considerations and Challenges for Data Stewards
- Data completeness and timeliness
  - Potential incomplete picture of user needs and priorities; reliance on timely submission from diverse data creators.
- Standardization across diverse systems
  - Harmonizing taxonomy across regional naming conventions; ensuring ITIS-aligned taxonomy while preserving original identifiers for traceability.
- Handling large and heterogeneous datasets
  - Managing multiple tables with relational links (Site, Entity, Sample, Pollen, Age Model, Taxonomy) and integrating radiocarbon age models with error propagation.
- Data access and updates
  - Ensuring ongoing availability of the complete database via the project site; documenting updates post-publication and maintaining provenance across versions.
- Embargoes and usage restrictions
  - While not explicitly stated, awareness of potential embargo periods or usage restrictions tied to publication timelines and data submitter preferences.