# Copernicus land CORINE metadata 2012

## Overview
- Metadata for three Corine Land Cover (CLC) datasets at the UK and Channel Islands level.
- Datasets capture CLC 2012 and 2006-2012 changes; produced under the Copernicus programme.
- Includes details on data structure, coordinate systems, and licensing/usage conditions.

## Datasets included
- Dataset 1: Corine land cover 2006 (revised), 2012 and changes (2006-2012) for the UK
  - Filename: CLC2012_UK.mdb
  - Layers: CLC-Changes (2006-2012), CLC2006revised, CLC2012
  - Projection: British National Grid; Transverse Mercator; GCS_OSGB_1936; Datum D_OSGB_1936
- Dataset 2: Corine land cover 2006 (revised), 2012 and changes (2006-2012) for Guernsey
  - Filename: CLC2012_UK.mdb
  - Layers: CLC-Changes (2006-2012), CLC2006revised, CLC2012
  - Projection: Guernsey Grid; Transverse Mercator; GCS_WGS_1984; Datum D_WGS_1984
- Dataset 3: Corine land cover 2006 (revised), 2012 and changes (2006-2012) for Jersey
  - Filename: CLC2012_UK.mdb
  - Layers: CLC-Changes (2006-2012), CLC2006revised, CLC2012
  - Projection: Transverse Mercator; GCS_ETRF_1989; Datum D_ETRF_1989

## Metadata and standards
- Metadata language: English (eng)
- Hierarchy level: Dataset
- Abstract: CLC 2012 and 2006-2012 change data produced within Copernicus; balance between land cover mapping and change detection.
- Keywords: Land cover, Land use, UK
- Spatial extent: UK, Guernsey, Jersey (bounding box West -8.62, East 1.76, South 49.88, North 60.84)
- Spatial resolution: Denominator 100000
- Lineage: Updated UK CLC for reference year 2012; based on 2011–2013 satellite imagery, supported by Google Earth for interpretation; no up-to-date national LCM available; followed EEA technical guidelines using InterChange for CLC changes; last LCM prior to 2012 was 2007 (LCM2007)
- Metadata compliance: INSPIRE-compliant metadata with some extended elements (country-level metadata)
- Metadata author: University of Leicester (Originator)
- Date stamp: 2015-01-09
- Resource constraints: File includes licensing with a mix of open access and restrictions under EU and Copernicus regulations; data access governed by EU Regulation 1159/13 (and related amendments), with conditions for informing users of data source, not implying EU endorsement, and clearly stating any adaptations

## Data governance and access
- Access and licensing: Free, full, and open access under specified conditions; users must acknowledge data source and EU ownership; explicit guidance on not implying official Union endorsement; adaptations must be clearly stated
- Ownership and responsibility: Originator (University of Leicester); Custodian (Defra); Owner (European Commission DG ENTR); Project context: Copernicus/GMES
- Availability and updates: Datasets reflect 2012 reference year and 2006-2012 changes; lineage notes indicate data come from satellite imagery (2011–2013) with supporting aerial imagery; acknowledges lack of a fully up-to-date national LCM in this update and use of national/intermediate products

## Geographic and technical details
- Coordinate reference systems vary by dataset (UK, Guernsey, Jersey); each with appropriate projection, grid, and datum
- Data are provided as a multi-layer MDB (Microsoft Access) databases for the UK and Crown dependencies
- Coverage and purpose align with wide-scale environmental monitoring, land cover classification, and change detection within the Copernicus framework

## Contact and resources
- Point of contact: The University of Leicester (Originator); Defra (Custodian); European Environment Agency (Owner); European Commission - DG ENTR
- Online resource/link: http://cdr.eionet.europa.eu/gb/eea/clc/envvlpnwa/
- Acknowledgments: Defra and EEA support; project by University of Leicester, Centre for Landscape and Climate Research, and Specto Natura

## Practical implications for Data Stewards
- Ensure metadata remains INSPIRE-compliant and clearly documents data lineage, spatial extent, coordinate systems, and licensing
- Maintain clear data provenance for updates and changes (2006-2012 changes, 2012 reference)
- Monitor and communicate data access restrictions and licensing conditions to data users
- Align dataset storage and sharing practices with governance requirements, including attribution and licensing notices
- Plan for interoperability across UK and Channel Islands datasets given differing projections and datums
- Document any adaptations or transformations performed when distributing data to downstream users