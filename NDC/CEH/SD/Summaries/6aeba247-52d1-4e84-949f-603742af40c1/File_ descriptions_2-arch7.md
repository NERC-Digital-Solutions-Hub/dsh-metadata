# Eurasian pollen data from 21 kiloannum to the present

## Overview
- Data collection workshop held in Winchester, April 2008; contributors mainly from the Former Soviet Union.
- Purpose: collate unpublished pollen data to define the most likely vegetation types (biomes) represented by fossil pollen since the Last Glacial Maximum (21 ka) to the present.

## Dataset scope and geography
- 96 sites with 99 entities (e.g., multiple cores at a lake or multiple sections at a terrestrial exposure).
- Sites span from 24°E (western Ukraine/Belarus) to eastern Siberia, north of 40°N.
- Each site/entity includes context such as whether the sampling location was a bog or lake and surrounding vegetation.

## Data collection, dating, and age models
- Fieldwork and analyses conducted by participants; workshop added site-level context where possible.
- Radiocarbon dates and age models calibrated with CLAM v1.2; age assignments and errors recorded in the Sample Table.
- Age-related data are organized with explicit age slices (kyr BP) and error estimates.

## Taxonomy, data quality, and standardization
- TaxonName reflects original identifications; TaxonClean provides standardized taxonomy aligned with ITIS (with regional differences noted).
- Some non-pollen identifications were removed; taxonomy checked for consistency, producing a redundancy-free taxonomy (Table 6).
- Both TaxonName and TaxonClean retained for provenance; unidentifiable entries may be marked with question marks, with TaxonClean indicating deletions (DELETE) not used in analyses.

## Data structure and content (key tables)
- Site Table: SiteID, SiteName, DataSubmitter, SurfaceSample, Elevation, LatDD, LonDD, Notes.
- Entity Table: SiteID, SiteName, EntityID, EntityName, LocalVeg, Age_model_ID, Age_model, SampleUsage, No_of_rc_dates, Outliers, Site_Description_notes.
- Sample Table: SiteID, SiteName, EntityID, EntityName, SampleID, DepthCM, Cal yr BP, Error, AgeSlice, SampleUsage.
- Pollen Table: SiteID, SiteName, EntityID, EntityName, SampleID, DepthCM, TaxonName, TaxonClean, ITIS, PollenCount.
- Age Model Table: Age Model ID, Age Model description.
- Taxonomy Table: TaxonName, TaxonClean.

## Access and publication
- Complete database planned for publication on the Southampton University website.
- Data set anticipated to appear in Quaternary Science Reviews (2017, in press).
- Reference: Blauuw, 2010 (methods for classical radiocarbon age modeling).

## GIS relevance and potential use
- Provides precise coordinates (LatDD, LonDD) enabling spatial visualization of pollen data across Eurasia.
- Facilitates map-based analyses of vegetation types (biomes) through time, using standardized taxonomy and integrated age models.
- Supports multi-site, multi-entity spatial analyses by linking Site, Entity, and Sample information with pollen counts and taxa.
- Site context (bog vs lake, local vegetation) aids habitat and landscape-scale mapping and interpretation.