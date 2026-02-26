# Technical Report Metadata for Corine Land Cover data 2018. UK.

## Datasets described
- Dataset 1: Corine land cover 2018
  - Filename: CLC2018_UK.shp
  - Description: Final UK status map for 2018; includes CLC level 3 codes, area (ha), length, and area per feature; remarks and a unique ID
  - Projection: Transverse Mercator
  - Geographic Coordinate System: GCS_OSGB_1936
  - Datum: D_OSGB_1936
  - Coordinate system: British National Grid
- Dataset 2: Corine land cover 2012 (revised) for the UK
  - Filename: CLC2012rev_UK.shp
  - Description: Updated CLC2012 map for the UK, revised during 2018 change mapping
  - Projection: Transverse Mercator
  - Geographic Coordinate System: GCS_OSGB_1936
  - Datum: D_OSGB_1936
- Dataset 3: Corine land changes (2012-2018) for the UK
  - Filename: CLC_CHA12-18_UK.shp
  - Description: Final changes layer for 2012-2018, mapped directly
  - Projection: Transverse Mercator
  - Geographic Coordinate System: GCS_OSGB_1936
  - Datum: D_OSGB_1936

## Copernicus metadata and compliance
- Metadata language: English (eng)
- Hierarchy level: Dataset
- Metadata standard: INSPIRE-compliant with extended elements
- Online resource link: http://cdr.eionet.europa.eu/gb/eea/clc/envvlpnwa/
- File identifier: CLC_metadata_UK
- Keywords: Land cover; Land use; UK
- Extent: Geographic bounding box
  - West: -8.62, East: 1.76, South: 49.88, North: 60.84
- Spatial resolution: Denominator 100000

## Online resource and contacts
- Point of contact: 
  - Originator: The University of Leicester (Centre for Landscape and Climate Research)
  - Custodian: Defra
  - Owner: European Environment Agency; European Commission - DG ENTR
- Topic categories: Environment; Imagery base maps earth cover
- Acknowledgement and provenance notes
- File includes: Metadata language (eng), UTF-8 character set
- Access conditions: Free, full, and open access with attribution and usage notes

## Extent and coverage
- Geographic coverage includes the UK and dependencies: Isle of Man, Channel Islands, Guernsey, Jersey, and Northern Ireland
- Spatial reference: British National Grid; standard mapping at 1:100000 denominator

## Lineage and methodology
- Updated for reference year 2018; objective to detect/mapping land cover changes above 5 ha
- Imagery sources: Sentinel-2 and Landsat-8 (2017) for image interpretation
- Supporting imagery: Aerial imagery from Google Earth
- Production follows European Environment Agency guidelines using InterChange for CLC mapping and revision of the 2012 map

## Usage constraints and licensing
- Data access governed by Commission delegated regulation EU No 1159/13 (with updates) relating to GMES/Copernicus data
- Conditions for public distribution:
  - Acknowledge data source and EU funding
  - Do not imply official EU endorsement of user activities
  - Clearly state if data have been adapted or modified
- Data remains EU property under grant and related terms

## Metadata specifics
- File identifier: CLC_metadata_UK
- Metadata language: English
- Character set: UTF-8
- Metadata author: University of Leicester (Originator)

## Quality control and verification
- Internal quality control:
  - Two-person interpretation for each Work Unit (WU)
  - InterCheck software to verify imagery and ancillary data
  - Feedback loop: comments returned as shapefiles and incorporated
- External quality control:
  - European Technical Team (CTT) conducted two remote verifications in Feb 2018 and Jun 2018
  - Sample checks covered multiple WUs and interpreters
  - Verification included detailed error logging and feedback reports

## Acknowledgments
- Project carried out by University of Leicester (Centre for Landscape and Climate Research) and Specto Natura
- Funded by the European Environment Agency under Grant Agreement EEA/IDM/R0/16/009/UK, within the Copernicus Programme
- Acknowledges EU funding and collaboration across national teams for harmonised CLC2018 data

## Practical takeaway for data support
- Provides three UK-specific CORINE datasets with consistent spatial reference and attribution suitable for cross-border analyses
- Clear lineage and methodology enable reproducibility and updates
- Access is open with licensing considerations; ensure attribution and note any adaptations in downstream products
- Quality control history supports confidence in harmonisation with other European CLC datasets