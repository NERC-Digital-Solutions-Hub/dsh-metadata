# Metadata for Corine Land Cover data 2018. UK.

- Purpose and scope
  - Metadata for three UK CORINE datasets: CLC2018_UK.shp, CLC2012rev_UK.shp, and CLC_CHA12-18_UK.shp.
  - Coverage includes the UK and Crown dependencies (Isle of Man, Channel Islands, Guernsey, Jersey, Northern Ireland).
  - Attributes include CLC classification codes at level 3, area (hectares), length, area of features, remarks, and a unique ID.
  - Intended to support consistent land cover mapping, land cover change detection (2012–2018), and integration into European-wide CLC products.

- Dataset details
  - Dataset 1: Corine land cover 2018
    - Filename: CLC2018_UK.shp
    - Description: Final UK status map for 2018
    - Projection: British National Grid (Transverse Mercator); GCS_OSGB_1936; Datum D_OSGB_1936
  - Dataset 2: Corine land cover 2012 (revised)
    - Filename: CLC2012rev_UK.shp
    - Description: Updated 2012 map for the UK, revised during 2018 change-mapping
    - Projection: British National Grid; Transverse Mercator; GCS_OSGB_1936; Datum D_OSGB_1936
  - Dataset 3: Corine land changes (2012–2018) for the UK
    - Filename: CLC_CHA12-18_UK.shp
    - Description: Changes between 2012 and 2018, mapped directly
    - Projection: British National Grid; Transverse Mercator; GCS_OSGB_1936; Datum D_OSGB_1936

- Context and methodology
  - CORINE Land Cover (CLC) provides consistent European land cover data; UK component included here.
  - Time series initiated in 1990 with updates in 2000, 2006, and 2012; 2018 update described.
  - Mapping approach: photointerpretation of satellite imagery (Sentinel-2, Landsat-8, 2017 imagery used); aerial imagery (Google Earth) support.
  - Mapping parameters: 44 classes in a three-level nomenclature; minimum mapping unit (MMU) for status layers is 25 hectares; MMU for land cover changes (LCC) is 5 hectares; minimum width for linear elements is 100 m.
  - National inventories are integrated into a seamless European land cover map.
  - Uses: land cover and land use information support environmental change monitoring, indicators, and policy areas (EU Environment Action Programmes, biodiversity, climate change, agriculture, Water Framework Directive).

- Metadata and standards
  - Metadata language: English
  - Compliance: INSPIRE-compatible metadata profile (EEA metadata framework with extended elements)
  - Online resources: provided link to the Copernicus CORINE metadata portal
  - File identifier: CLC_metadata_UK
  - Geographic extent and data characteristics: bounding box West -8.62, East 1.76, South 49.88, North 60.84; spatial resolution denominator 100,000

- Lineage and data provenance
  - Lineage: 2018 update of the UK CLC; basis on 2017 imagery; uses InterChange mapping package; revision of 2012 map
  - Data production overseen with adherence to EEA technical guidelines; external validation to ensure harmonised European CLC2018

- Access, rights, and use constraints
  - Use limitation: data access governed by EU Regulation 1159/2013 (GMES) and related frameworks; conditions for open data distribution include attribution to source, avoidance of implying EU endorsement, and clear notation if data are modified
  - Despite regulatory changes, this metadata indicates a framework for free, full, and open access under defined terms

- Quality control and validation
  - Internal quality control by University of Leicester; each Work Unit interpreted and checked by a second interpreter
  - External quality control by European Technical Team (CTT) in Feb and June 2018; error tagging and feedback via shapefiles and verification reports
  - Quality checks used InterCheck software with identical imagery and ancillary data

- Stakeholders and custodians
  - Originator: University of Leicester (Centre for Landscape and Climate Research)
  - Custodian: Defra
  - Owner/Point of contact: European Environment Agency; DG-Enterprise and Industry (European Commission)
  - Topic categories: Environment; Imagery base maps / earth cover

- Supporting information
  - Keywords: Land cover; Land use; UK
  - Geographic scope: UK and dependencies
  - Acknowledgments: project led by University of Leicester with Specto Natura; funded under the European Union Copernicus Programme (Grant EEA/IDM/R0/16/009/UK)

- Date and documentation
  - Metadata authoring: University of Leicester
  - Date stamp: 2021-06-01

- Implications for monitoring frameworks
  - Provides standardized, quality-assured land cover data and change detection for policy evaluation and planning
  - Clear lineage and provenance support reproducibility and governance of monitoring outputs
  - Explicit data quality controls and access conditions aid in transparent reporting and data governance for environmental health monitoring initiatives