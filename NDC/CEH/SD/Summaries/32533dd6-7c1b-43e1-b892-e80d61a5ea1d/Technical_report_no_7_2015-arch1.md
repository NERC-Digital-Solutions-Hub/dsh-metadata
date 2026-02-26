# Technical Report No. 7

- Executive focus: metadata for Corine Land Cover (CLC) datasets for the UK, Guernsey, and Jersey; three layers per dataset; aims to support land cover monitoring and change detection under the Copernicus framework.

## Datasets and layers

- Dataset 1: Corine land cover 2006 (revised), 2012 and changes (2006-2012) for the UK
  - File: CLC2012_UK.mdb
  - Three layers: CLC-Changes (2006-2012), CLC2006revised, CLC2012
- Dataset 2: Corine land cover 2006 (revised), 2012 and changes (2006-2012) for Guernsey
  - File: CLC2012_UK.mdb
  - Three layers: CLC-Changes (2006-2012), CLC2006revised, CLC2012
- Dataset 3: Corine land cover 2006 (revised), 2012 and changes (2006-2012) for Jersey
  - File: CLC2012_UK.mdb
  - Three layers: CLC-Changes (2006-2012), CLC2006revised, CLC2012

## Projections and coordinate systems

- UK: British National Grid, Transverse Mercator; GCS_OSGB_1936; Datum D_OSGB_1936
- Guernsey: Guernsey Grid, Transverse Mercator; GCS_WGS_1984; Datum D_WGS_1984
- Jersey: New JTM, Transverse Mercator; GCS_ETRF_1989; Datum D_ETRF_1989

## Dataset purpose and content

- Copernicus/CORINE metadata for 2012 updates; LCC changes detected for areas >5 ha
- Imagery basis: 2011-2013 satellite images; support from Google Earth imagery
- Previously available national LCM updated only up to 2007 (LCM2007); this update follows EEA technical guidelines using InterChange for CLC changes

## Metadata and compliance

- Metadata aligned with the EEA Metadata Profile; INSPIRE-compliant metadata with extensions
- Online resource and linkage provided for metadata access
- File identifier: CLC_metadata_UK
- Metadata language: English (UTF-8)

## Access, licensing, and provenance

- Use and access governed by Commission delegated regulation (EU) No 1159/13 (amending GMES access and licensing)
- Despite changes in regulation, data are described as free, full, and open under conditions:
  - Acknowledge data source when distributing/publicizing
  - Do not imply EU endorsement of user activities
  - State if data/products have been adapted or modified
- Acknowledgment of collaboration and funding:
  - University of Leicester; Centre for Landscape and Climate Research; Specto Natura
  - Defra and European Environment Agency (Grant 3541/B2012/R0-GIO/EEA.55055)

## Geographic extent and resolution

- Geographic bounding box (UK-focused): West -8.62, East 1.76, South 49.88, North 60.84
- Spatial resolution: Denominator 100000 (map scale context)

## Lineage and methodology

- Objective: update UK CLC to 2012; detect and map changes >5 ha
- Data inputs: satellite imagery from 2011-2013; aerial imagery from Google Earth to support interpretation
- Note: No up-to-date national land cover map available at update time; relies on LCM2007 as reference point
- Production guidelines: EEA technical guidelines; InterChange tool used for mapping CLC changes

## Practical considerations for analysts

- Data availability may be constrained by licensing; ensure proper attribution and note of modification if applicable
- When integrating with other datasets, account for differing coordinate systems across UK, Guernsey, and Jersey layers
- MMU details: changes layer focuses on >5 ha; status layers use a 25 ha minimum mapping unit
- Consider the gap since 2012 for current analyses; if up-to-date land cover is needed, supplemental sources may be required

## Documentation and contact

- Metadata author: University of Leicester; Originator
- Date stamp: 2015-01-09
- Acknowledgments: Defra and EEA support; project collaboration with Specto Natura
- Point of contact: University of Leicester (Originator); Custodian: Defra; Owner: European Commission DG ENTR
- Online access: metadata and dataset references available via linked resources