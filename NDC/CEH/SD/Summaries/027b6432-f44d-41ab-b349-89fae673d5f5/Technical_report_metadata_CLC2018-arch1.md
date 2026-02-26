# Technical Report Metadata for Corine Land Cover data 2018. UK.

## Overview
- Metadata and descriptions for three UK CORINE Land Cover (CLC) datasets: CLC2018_UK.shp, CLC2012rev_UK.shp, and CLC_CHA12-18_UK.shp.
- Coverage includes the UK and neighboring territories (Isle of Man, Channel Islands, Guernsey, Jersey, Northern Ireland).
- Datasets include CLC classifications (level 3), area (hectares), length, remarks, and a unique ID for each feature.

## Datasets and What They Represent
- Dataset 1: Corine land cover 2018 (CLC2018_UK.shp)
  - Status map for 2018 for the UK.
  - Coordinate system: British National Grid; Projection: Transverse Mercator; Geographic CRS: GCS_OSGB_1936; Datum: D_OSGB_1936.
- Dataset 2: Corine land cover 2012 (revised) for the UK (CLC2012rev_UK.shp)
  - Updated CLC2012 map produced during 2018 change-mapping process.
  - Same projection and datum as Dataset 1.
- Dataset 3: Corine land changes (2012–2018) for the UK (CLC_CHA12-18_UK.shp)
  - Direct mapping of changes between 2012 and 2018.
  - Same projection and datum as above.

## Metadata, Standards and Access
- Copernicus CORINE metadata 2018; three datasets form part of the Copernicus land monitoring program.
- Landscape coverage: 44 hierarchical land cover classes; minimum mapping units (MMU) of 25 ha for status layers; MMU for land cover changes (LCC) of 5 ha; minimum width for linear elements 100 m.
- Aim: provide consistent land cover and change information to support environmental monitoring, policy, biodiversity, climate tracking, agriculture, and EU directives.
- Metadata format: INSPIRE-compliant with ENGLISH language metadata; online resource and contact points provided.
- Extent and scale: geographic bounding box West -8.62 to East 1.76; South 49.88 to North 60.84; spatial resolution denominator 100000 (1:100,000 scale).

## Lineage and Methodology
- Update objective: detect, identify, and map land cover changes above 5 ha.
- Imagery: Sentinel-2 and Landsat-8 images from 2017 used for interpretation; Google Earth imagery supported interpretation.
- Process: following EEA technical guidelines; InterChange support package used for mapping CLC changes; revision of the 2012 map.
- The metadata notes the production and harmonization efforts to ensure comparability across Europe.

## Access, Use and Licensing
- Access governed by Commission delegated regulation (EU) No 1159/13; promotes free, full, and open access with conditions.
- Users must: (1) acknowledge the data source; (2) avoid implying EU endorsement of user activities; (3) clearly state if data or outputs have been adapted or modified.
- EU ownership and funding acknowledgment obligations apply for outputs produced under the Copernicus program.

## Quality Control and Verification
- Internal quality control by the University of Leicester: each working unit interpreted by two different interpreters; use of InterCheck software; feedback loop to adjust shapefiles.
- External verification by the European Technical Team (CTT) in February and June 2018: sampling multiple working units to ensure harmonized UK production for CLC2018; errors logged as points with descriptive attributes and accompanied by verification reports.

## Provenance, Contacts and Acknowledgments
- Originator: University of Leicester; Custodian: Defra; Owner: European Environment Agency; EU governing bodies including European Commission DG ENTR acknowledged.
- Acknowledgments: University of Leicester, Centre for Landscape and Climate Research, Specto Natura; supported by the European Environment Agency under Copernicus funding (Grant EEA/IDM/R0/16/009/UK).

## Key Takeaways for Analysts
- The datasets provide standardized UK-specific CLC2018, revised 2012, and 2012–2018 change layers with consistent projection (OSGB 1936) suitable for cross-temporal analyses and EU-wide harmonization.
- Data quality is reinforced by dual-interpretation internal checks and external European verification, increasing reliability for detecting correlations and predicting impact of land-cover changes.
- Licensing and attribution requirements should be followed, with clear documentation of any data modifications when used for decision-support, reporting, or academic research.