# Eurasian pollen data from 21 kiloannum to the present

## Overview
- Results of a data collection workshop held in Winchester (April 2008) to add previously unpublished data to a new pollen database.
- Aim: define the most likely vegetation types (biomes) represented by fossil pollen data from the Last Glacial Maximum (21 ka) to the present.
- Contributors mainly from the Former Soviet Union; data include site-level fieldwork and laboratory pollen counts.

## Data scope and geographic coverage
- 96 sites spanning from 24°E (western Ukraine/Belarus) to eastern Siberia.
- North of 40°N latitude; 99 entities (e.g., multiple cores at a lake or multiple sections at a terrestrial exposure).
- Data include site characteristics (e.g., bog vs lake) and surrounding local vegetation.

## Data collection and provenance
- Participants collected samples, performed pollen/spore identification and counts.
- Additional site information added at the workshop (habitat, surrounding vegetation).
- Radiocarbon dating dates calibrated and age models created using CLAM v1.2; age assignments include error estimates.

## Data structure and schema
- Complete database organized into six tables:
  - Site Table: SiteID, SiteName, DataSubmitter, SurfaceSample, Elevation, LatDD, LonDD, Notes.
  - Entity Table: SiteID, SiteName, EntityID, EntityName, LocalVeg, Age_model_ID, Age_model, SampleUsage, No_of_rc_dates, Outliers, Site_Description_notes.
  - Sample Table: SiteID, SiteName, EntityID, EntityName, SampleID, DepthCM, Cal yr BP, Error, AgeSlice, SampleUsage.
  - Pollen Table: SiteID, SiteName, EntityID, EntityName, SampleID, DepthCM, TaxonName, TaxonClean, ITIS, PollenCount.
  - Age Model Table: Age Model ID, Age Model description.
  - Taxonomy Table: TaxonName, TaxonClean.
- Data relationships allow multiple samples per site/entity; taxonomy harmonized to ensure consistent analyses.

## Taxonomy, quality control, and data standards
- TaxonName contains original identifications; TaxonClean provides standardized names aligned to ITIS.
- Non-pollen identifications were removed (e.g., Dyadosporites fungus).
- Taxonomy cleaned to produce redundancy-free taxonomy (Table 6) for reliable analysis; unresolved or non-identifiable entries marked (e.g., question marks) and removed from analyses where appropriate.

## Age modelling and dating
- CLAM v1.2 used for radiocarbon calibration and constructing age models.
- Age assignments include an error term (Cal yr BP and Error) and are organized by Age_model and AgeSlice in the dataset.

## Publication, access, and reuse
- The complete database will be available via the Southampton University website.
- Data planned publication in Quaternary Science Reviews (in press, 2017).
- Reference to Blauuw (2010) for methods and code on classical age modelling of radiocarbon sequences.

## Implications for Data Leaders
- Demonstrates end-to-end data stewardship: provenance, metadata, and documentation (Site, Entity, Sample, Pollen, Age Model, and Taxonomy tables) to support discoverability and reuse.
- Emphasizes data standardization (taxonomy alignment to ITIS) and transparent age modelling to enable cross-study comparability.
- Highlights the importance of making the full dataset available online and in a peer-reviewed venue to maximize impact and collaborative potential across networks.