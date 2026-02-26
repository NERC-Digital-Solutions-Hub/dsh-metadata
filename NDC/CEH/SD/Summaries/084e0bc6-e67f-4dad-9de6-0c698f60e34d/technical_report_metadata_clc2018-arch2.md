# Technical Report Metadata for Corine Land Cover data 2018. UK.

## Overview
- Documents metadata for three UK Corine Land Cover (CLC) datasets:
  - CLC2018_UK.shp (CLC2018)
  - CLC2012rev_UK.shp (CLC2012 revised)
  - CLC_CHA12-18_UK.shp (CLC changes 2012–2018)
- Geographic coverage includes the UK and associated territories (Isle of Man, Channel Islands, Guernsey, Jersey, Northern Ireland).
- Attribute tables include: CLC Level 3 codes, feature area (hectares), length, area, remarks, and a unique ID.

## Datasets Details
- Dataset 1: Corine land cover 2018 (CLC2018_UK.shp)
  - Status map for 2018 (UK)
  - Projection: British National Grid; Projection: Transverse Mercator
  - Geographic CS: GCS_OSGB_1936; Datum: D_OSGB_1936
- Dataset 2: Corine land cover 2012 (revised) (CLC2012rev_UK.shp)
  - Updated 2012 map (revised in 2018)
  - Same projection/CS and datum as 2018 dataset
- Dataset 3: Corine land changes 2012–2018 (CLC_CHA12-18_UK.shp)
  - Changes mapped directly for 2012–2018
  - Same projection/CS and datum as above

## Metadata & Standards
- Metadata language: English; hierarchy level: Dataset
- Metadata aligned with INSPIRE/EEA metadata profiles; available via European portals
- Online resource: link provided to Copernicus/CLC metadata portal
- Keywords: Land cover, land use, UK
- Extent: geographic bounding box (West -8.62, East 1.76, South 49.88, North 60.84)
- Spatial resolution: denominator 100000 (scale ~1:100,000)
- File identifier: CLC_metadata_UK; Character set: UTF-8

## Abstract and Purpose
- CLC data provide consistent European land cover information; UK components include 2018 status, 2012 revised, and 2012–2018 changes.
- 44 hierarchical land cover classes; MMU for status layers is 25 hectares; MMU for change layers is 5 hectares.
- Grounded in photointerpretation of Sentinel-2 and Landsat-8 imagery (2017) with supporting aerial imagery (Google Earth).
- Supports land change research, environmental indicators, climate tracking, agriculture developments, and EU policy instruments (e.g., Water Framework Directive).

## Lineage and Methodology
- Objective: detect, identify, and map land cover changes above 5 ha for 2018 revision.
- Method: image interpretation guided by EEA technical guidelines; InterChange mapping package used for CLC changes; 2012 map revised accordingly.
- Data integrated into a seamless Europe-wide land cover dataset.

## Access, Use, and Licensing
- Use is governed by EU regulatory frameworks; general access is free, full, and open under conditions:
  - Acknowledge data source and funding source when distributing or publishing
  - Do not imply EU endorsement of user activities
  - Clearly state if data/products have been modified
- Data are part of Copernicus Land Monitoring, with licensing constraints and attribution requirements.

## Quality Control
- Internal QC: University of Leicester conducted rigorous checks; each Working Unit (WU) interpreted by two people; use InterCheck software; iterative feedback to interpreters.
- External QC: European Technical Team (CTT) conducted remote verifications (Feb and Jun 2018) to ensure harmonised UK outputs.
  - Sampling included ~1,500 km² areas and later additional WUs; errors recorded as shapefiles with descriptive attributes.

## Provenance and Acknowledgments
- Originator: University of Leicester; Custodian: Defra; Point of contact: European Environment Agency; Owner: European Commission DG ENTR.
- Acknowledged collaboration with Specto Natura; funded by the European Union under Copernicus Programme (Grant EEA/IDM/R0/16/009/UK).
- Metadata authored by the University of Leicester; date stamp: 2021-06-01.

## Practical Implications for Environmental Monitoring
- Provides standardized, harmonised UK CLC datasets suitable for longitudinal environmental health monitoring and policy performance assessment.
- Enables integration with additional datasets for expanded environmental indicators and cross-border analyses.
- Facilitates transparent quality assurance and traceable lineage from imagery to final land cover outputs.