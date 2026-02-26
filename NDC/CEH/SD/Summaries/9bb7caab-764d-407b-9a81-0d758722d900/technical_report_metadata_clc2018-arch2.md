# Metadata for Corine Land Cover data 2018. UK.

- Overview
  - Metadata for three UK CORINE Land Cover (CLC) datasets: CLC2018_UK.shp, CLC2012rev_UK.shp, and CLC_CHA12-18_UK.shp.
  - Coverage includes the UK plus Isle of Man, Channel Islands (Guernsey, Jersey) and Northern Ireland.
  - Datasets contain CLC level-3 codes, area (ha), length, feature area, remarks, and a unique ID.

- Datasets and Descriptions
  - Dataset 1: Corine land cover 2018 (CLC2018_UK.shp)
    - Final status map for the UK for 2018.
    - Projection: British National Grid (Transverse Mercator); GCS_OSGB_1936; Datum: D_OSGB_1936.
  - Dataset 2: Corine land cover 2012 (revised) (CLC2012rev_UK.shp)
    - Updated UK CLC2012 map revised during 2018 change mapping.
    - Same projection and datum as Dataset 1.
  - Dataset 3: Corine land changes 2012–2018 (CLC_CHA12-18_UK.shp)
    - Changes between 2012 and 2018 mapped directly.
    - Same projection and datum as above.

- Context and Purpose
  - Part of Copernicus Land Monitoring (CORINE) datasets for Europe.
  - Provides consistent land cover and land cover change information to support environmental monitoring, indicators, and EU policy (biodiversity, climate, agriculture, Water Framework Directive).

- Technical Characteristics
  - Base parameters: 44 classes in the CORINE nomenclature; minimum mapping units (MMU) of 25 ha for status layers and 5 ha for change layers.
  - Data formats: Shapefiles with attribute tables (CLC level-3 codes, area/length metrics, remarks, IDs).

- Data Lineage and Methodology
  - Creation relied on Sentinel-2 and Landsat-8 imagery from 2017; supported by Google Earth imagery.
  - Followed EEA technical guidelines using InterChange for CLC change mapping; revision of the 2012 map.
  - Outputs integrated into a seamless European land cover dataset.

- Quality Control and Verification
  - Internal quality control by University of Leicester: each work unit interpreted independently by two people; results checked and reworked using InterCheck software.
  - External quality control by European Technical Team (CTT) in 2018: two remote verifications (Feb and Jun 2018) covering multiple work units; issues reported as shapefiles with descriptive attributes for corrective actions.

- Access, Use, and Legal Context
  - Data access governed by EU Regulation 1159/2013 (and related provisions); free, full, and open access with conditions.
  - Requirements: acknowledge the source, avoid implying EU endorsement, and state any adaptations/modifications.
  - Ownership: EU data produced under Copernicus; data and results remain EU property with appropriate attribution.

- Metadata Details
  - Language: English; metadata aligned with INSPIRE/compliant European metadata practices.
  - Online resource and contact points provided (including EEA, Defra, DG-ENTR, and University of Leicester as originator/custodian/owner).
  - Geographic extent: West -8.62 to East 1.76; South 49.88 to North 60.84.
  - Spatial resolution indicator: denominator 100000 (map scale context).
  - File identifier: CLC_metadata_UK; date stamp: 2021-06-01.

- Relevance to Environmental Analysts
  - Demonstrates how UK CLC datasets are produced, updated, and quality-assured to support long-term environmental monitoring and policy performance.
  - Provides a clear data lineage, standardized classifications, and robust QA/validation suitable for monitoring change in land cover and informing environmental indicators.