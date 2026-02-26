# Technical Report Metadata for Corine Land Cover data 2018. UK.

## Executive scope
- Metadata for three UK Corine Land Cover (CLC) datasets:
  - CLC2018_UK.shp (CLC2018)
  - CLC2012rev_UK.shp (CLC2012rev)
  - CLC_CHA12-18_UK.shp (CLC-Changes 2012-2018)
- UK coverage includes Isle of Man, Channel Islands, Guernsey, Jersey, and Northern Ireland.
- Attribute tables include: CLC level-3 classification codes, area (hectares), feature length, feature area, remarks, and a unique ID.

## Datasets and main specifications

- Dataset 1: Corine land cover 2018 (CLC2018_UK.shp)
  - Description: Final UK status map for 2018.
  - Projection: British National Grid (Transverse Mercator), GCS_OSGB_1936, Datum OSGB 1936.

- Dataset 2: Corine land cover 2012 (revised) (CLC2012rev_UK.shp)
  - Description: Updated CLC2012 map for the UK, revised during 2018 change-mapping.
  - Projection: British National Grid (Transverse Mercator), GCS_OSGB_1936, Datum OSGB 1936.

- Dataset 3: Corine land changes (2012-2018) (CLC_CHA12-18_UK.shp)
  - Description: Changes between 2012 and 2018, mapped directly.
  - Projection: British National Grid (Transverse Mercator), GCS_OSGB_1936, Datum OSGB 1936.

## Copernicus metadata and purpose
- Datasets provided under Copernicus Land Monitoring (CLC). UK component of Europe.
- CLC baseline: 44 classes, MMU for status layers 25 hectares; MMU for linear elements 100 m; MMU for LCC changes 5 hectares.
- Purpose: supporting environmental monitoring, indicators, EU policy reporting (biodiversity, climate change, agriculture, Water Framework Directive, etc.).
- Base methodology: photointerpretation of Sentinel-2 and Landsat-8 (2017 imagery); supported by aerial imagery (Google Earth); following EEA guidelines; production with InterChange mapping package.

## Metadata and access
- Metadata language: English; metadata compliant with the EEA Metadata Profile (INSPIRE-compliant with extensions).
- Online resource: http://cdr.eionet.europa.eu/gb/eea/clc/envvlpnwa/
- File identifier: CLC_metadata_UK
- Contact and roles:
  - Originator: University of Leicester
  - Custodian: Defra
  - Point of contact: European Environment Agency
  - Owner: European Commission - DG ENTR

## Geographic scope and resolution
- Geographic bounding box: West -8.62, East 1.76, South 49.88, North 60.84
- Spatial resolution: 1:100,000 denominator (map scale)

## Lineage and processing
- Lineage: UK update for 2018; focus on detecting and mapping land cover changes >5 ha; Sentinel-2 and Landsat-8 2017 used as the base; Google Earth imagery used for support; adherence to EEA production guidelines; InterChange used for mapping CLC changes and revising the 2012 map.

## Data quality and verification
- Quality control:
  - Internal: University of Leicester performed dual-interpretation (two interpreters per Work Unit) with InterCheck software; feedback loops via exported shapefiles.
  - External: European Technical Team (CTT) completed two remote verifications (Feb 2018, Jun 2018) across multiple WUs to ensure harmonised UK CLC2018 results; errors documented as points with attributes and returned with verification reports.

## Access constraints and licensing
- Use limitation: Access governed by EU Regulation 1159/2013 (GMES) with registration/licensing conditions; although Regulation 911/2010 superseded, provisions remain; open, free access with attribution, notification of source, no implication of EU endorsement, and clear statement if data or outputs are modified. EU ownership/grant conditions apply to Copernicus-derived outputs.

## Administrative metadata
- Metadata language: English; character set: UTF-8
- Metadata author: University of Leicester (originator)
- Date stamp: 2021-06-01
- Acknowledgments: Project by University of Leicester, Centre for Landscape and Climate Research, and Specto Natura; funded by European Environment Agency under Grant EEA/IDM/R0/16/009/UK (Copernicus Programme).

## Additional notes
- Keywords: Land cover, Land use, UK, imagery base maps/earth cover
- Version and access details: Dataset status and lineage reflect 2012-2018 change mapping and 2018 revision integrated into a seamless European dataset.