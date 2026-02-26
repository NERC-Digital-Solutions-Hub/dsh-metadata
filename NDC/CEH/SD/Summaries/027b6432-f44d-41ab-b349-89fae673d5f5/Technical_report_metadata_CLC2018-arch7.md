# Metadata for Corine Land Cover data 2018. UK.

## Overview
- Metadata for three UK Corine Land Cover (CLC) datasets: CLC2018_UK.shp, CLC2012rev_UK.shp, CLC_CHA12-18_UK.shp.
- Coverage includes the UK and Crown dependencies (Isle of Man, Channel Islands, Guernsey, Jersey, Northern Ireland).
- Attribute tables include: CLC classification codes at level 3, area (hectares), length, area of each feature, remarks, and a unique ID.

## Datasets

- Dataset 1: Corine land cover 2018 (CLC2018_UK.shp)
  - Final UK status map for 2018
  - Projection: British National Grid; Transverse Mercator
  - Geographic Coordinate System: GCS_OSGB_1936; Datum: D_OSGB_1936

- Dataset 2: Corine land cover 2012 (revised) for the UK (CLC2012rev_UK.shp)
  - Updated CLC2012 map for the UK (revision during 2018 change mapping)
  - Projection/Geography: same as Dataset 1

- Dataset 3: Corine land changes (2012-2018) for the UK (CLC_CHA12-18_UK.shp)
  - Final database for the UK changes between 2012 and 2018
  - Projection/Geography: same as Dataset 1

## Spatial Reference and Data Model
- Coordinate system: British National Grid; Projection: Transverse Mercator; Geographic: GCS_OSGB_1936; Datum: D_OSGB_1936
- Spatial resolution: 1:100,000
- Extent: West -8.62, East 1.76, South 49.88, North 60.84
- Classification: Corine Land Cover with 44 classes; status layers with MMU of 25 ha; change layers with MMU of 5 ha
- File identifiers and metadata: CLC_metadata_UK; metadata language: English; UTF-8

## Content and Classification
- Level-3 CLC codes in attributes
- Area and length fields for each feature
- Remarks and a unique ID per feature
- Data designed for map-based visualization and analysis of land cover and land cover change

## Lineage and Production
- 2018 update aim: detect and map land cover changes above 5 ha
- Basis imagery: Sentinel-2 and Landsat-8 (2017) with support from Google Earth imagery
- Production follows EEA technical guidelines; interChange package used for mapping CLC changes and revising the 2012 map

## Quality Assurance
- Internal quality control by University of Leicester
  - Two interpreters per work unit (WUs); InterCheck software; cross-checks with feedback to interpreters
- External quality control by European Technical Team (CTT)
  - Verifications in Feb 2018 and Jun 2018
  - Sampled WUs (areas ~1,500 km² initially; later coverage across interpreters)
  - Error points recorded in shapefiles with descriptive attributes; verification reports provided

## Access, Use and Licensing
- Access governed by EU regulation 1159/2013 (GMES) with licensing conditions; free, full, open access with restrictions
  - Users must attribute the source and not imply EU endorsement
  - If data are adapted or modified, this must be clearly stated
  - Intellectual property remains with the EU for data produced under Copernicus
- Originator/Custodian/Owner/Contact
  - Originator: University of Leicester
  - Custodian: Defra
  - Owner: European Environment Agency; DG European Commission - ENTR
  - Online resource link provided for metadata and data access

## Metadata and Contact
- Metadata language: English
- Online resource: http://cdr.eionet.europa.eu/gb/eea/clc/envvlpnwa/
- Point of contact: University of Leicester (Originator), Defra (Custodian), EEA (Owner), DG ENTR
- File identifier: CLC_metadata_UK
- Date stamp: 2021-06-01

## Acknowledgments
- Project conducted by University of Leicester (Centre for Landscape and Climate Research) and Specto Natura
- Funded by the European Environment Agency under Grant EEA/IDM/R0/16/009/UK, Copernicus Programme
- Collaboration aimed at harmonised European CLC2018 data production