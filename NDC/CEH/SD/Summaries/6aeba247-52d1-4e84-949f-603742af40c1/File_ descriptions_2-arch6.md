# Eurasian pollen data from 21 kiloannum to the present

## Overview
- Data collection workshop (Winchester, April 2008) inviting contributors from the Former Soviet Union to add unpublished pollen data to a new database.
- Objective: define the most likely vegetation types (biomes) represented by fossil pollen from the Last Glacial Maximum (21 ka) to the present.
- Dataset scope: 96 sites spanning from 24°E (western Ukraine/Belarus) to eastern Siberia, north of 40°N; 99 entities (reflecting multiple cores or sections at some sites).
- Contributors conducted fieldwork, prepared and analyzed pollen/spore identifications and counts, and provided site context (e.g., bog vs lake, surrounding vegetation).

## Data collection and quality control
- Radiocarbon dating and age modelling: CLAM v1.2 used to calibrate dates and construct age models; age assignments include error estimates (Sample Table).
- Data quality and taxonomy: TaxonName (original identification) paired with TaxonClean (taxonomy harmonized to ITIS); regional synonyms noted; non-pollen identifications removed (e.g., Dyadosporites).
- Taxonomy harmonization: consistent, redundancy-free taxonomy produced (Taxonomy table); TaxonClean used for analyses, with TaxonName preserved for provenance.
- Data preservation: complete database planned for Southampton University website; dataset to be published in Quaternary Science Reviews (2017, in press).

## Data structure and contents
- Site Table: SiteID, SiteName, DataSubmitter, SurfaceSample, Elevation, LatDD, LonDD, Notes.
- Entity Table: SiteID, SiteName, EntityID, EntityName, LocalVeg, Age_model_ID, Age_model, SampleUsage, No_of_rc_dates, Outliers, Site_Description_notes.
- Sample Table: SiteID, SiteName, EntityID, EntityName, SampleID, DepthCM, Cal yr BP, Error, AgeSlice, SampleUsage.
- Pollen Table: SiteID, SiteName, EntityID, EntityName, SampleID, DepthCM, TaxonName, TaxonClean, ITIS, PollenCount.
- Age Model Table: Age Model ID, Age Model description.
- Taxonomy Table: TaxonName, TaxonClean.
- Dataset characteristics: 96 sites and 99 entities; includes multiple core locations or discrete terrestrial sections at certain sites.

## Age modelling and methods
- Age modelling framework described; radiocarbon dates calibrated and age models constructed using CLAM v1.2 (Blauuw 2010).

## Access and outputs
- The complete database will be accessible via the Southampton University website.
- Publication status: data prepared for publication in Quaternary Science Reviews (2017).

## References
- Blauuw, M. 2010. Methods and code for ‘classical’ age modelling of radiocarbon sequences. Quaternary Geochronology, 5, 512-518.