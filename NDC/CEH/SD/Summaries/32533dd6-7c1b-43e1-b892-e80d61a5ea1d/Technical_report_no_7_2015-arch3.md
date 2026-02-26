# Technical Report No. 7

## Overview
- Metadata and documentation for Copernicus CORINE Land Cover (CLC) datasets covering the UK (including Northern Ireland and Isle of Man) and crown dependencies Guernsey and Jersey.
- Focus on three layers per dataset: CLC-Changes (2006-2012), CLC2006revised, and CLC2012.
- Datasets produced under the Copernicus programme; intended to support environmental monitoring, policy analysis, and indicator development.

## Datasets and Structure
- Dataset 1: Corine land cover 2006 (revised), 2012 and changes (2006-2012) for the UK
  - Filename: CLC2012_UK.mdb
  - Layers: CLC-Changes (2006-2012), CLC2006revised, CLC2012
  - Projection: British National Grid (Transverse Mercator); Geographic CS: GCS_OSGB_1936; Datum: D_OSGB_1936
- Dataset 2: Corine land cover 2006 (revised), 2012 and changes (2006-2012) for Guernsey
  - Filename: CLC2012_UK.mdb
  - Layers: CLC-Changes (2006-2012), CLC2006revised, CLC2012
  - Projection: Guernsey Grid (Transverse Mercator); Geographic CS: GCS_WGS_1984; Datum: D_WGS_1984
- Dataset 3: Corine land cover 2006 (revised), 2012 and changes (2006-2012) for Jersey
  - Filename: CLC2012_UK.mdb
  - Layers: CLC-Changes (2006-2012), CLC2006revised, CLC2012
  - Projection: New Jersey Transverse Mercator (JTM); Geographic CS: GCS_ETRF_1989; Datum: D_ETRF_1989
- Metadata and context
  - Copernicus Land - CORINE metadata for UK; 2012 updates with 2006-2012 changes
  - 44 land cover classes; minimum mapping unit (MMU) for status layers 25 ha; MMU for change layers 5 ha

## Metadata Standards and Access
- Metadata language: English
- Metadata profile: INSPIRE-compliant (EEA metadata profile with extended elements)
- Online resources and links provided for metadata and data access
- Data lineage notes emphasize the update process and methodologies

## Methodology and Lineage
- Basis: CORINE Land Cover (CLC) 2012 with 2006-2012 change detection
- Imagery: Satellite images from 2011-2013; supported by aerial imagery (e.g., Google Earth)
- Methodology: InterChange-based mapping following EEA technical guidelines
- Context: UK national map not fully up-to-date at the time; 2007 LCM used as a reference point for comparison
- Purpose: Detection and mapping of land cover changes above 5 ha for change layers; consistent Europe-wide integration

## Geographic, Temporal, and Technical Details
- Geographic extent: UK (including NI and Isle of Man) plus Guernsey and Jersey; bounding coordinates specified
- Spatial resolution: Nominal scale of 1:100,000
- Change and status layers provide both current land cover (2012) and historical revisions (2006)

## Access, Licensing, and Data Governance
- Use limitation: Access governed by EU Regulation 1159/2013 (and successor regulations); conditions for distribution and public communication
- Open access stance: Free, full, and open access with requirements
  - Must acknowledge data source
  - Must not imply Union endorsement
  - Must clearly state if data have been adapted or modified
- Provenance and stewardship
  - Originator: University of Leicester
  - Custodian: Defra
  - Owner: European Commission - DG Enterprise and Industry (DG-ENTR) / European Environment Agency (EEA)
  - Point of contact: Coordinated by The University of Leicester; additional coordination with Defra and EEA
- Acknowledgments: Project supported by Defra and EEA under specific grant agreement; EU-funded Copernicus program

## Implications for Monitoring Frameworks
- Provides standardized, Europe-wide land cover data and change information suitable for environmental health monitoring, trend analysis, and policy evaluation.
- Useful for indicators related to ecosystems, biodiversity, land-use change, climate impact assessment, and alignment with EU directives (e.g., Water Framework Directive) and environment programs.
- Enables cross-border comparability (UK and crown dependencies) due to harmonized metadata and classification scheme.

## Practical Considerations and Limitations
- Data currency: UK base map not up-to-date at the time; reliance on 2011-2013 imagery for 2012 reference
- Access constraints: Licensing and data sharing conditions may affect rapid or broad public dissemination
- Metadata quality and consistency: Requires attention to ensure metadata alignment and transformation for local monitoring systems
- Data transformation: Coordinate system differences across UK, Guernsey, and Jersey layers may require transformation for integrated dashboards

## Acknowledgments and Provenance
- Acknowledged collaboration among The University of Leicester, Defra, and Specto Natura
- Funded under EU Copernicus program; grant agreement noted
- Documentation and metadata prepared to support reuse and transparency in monitoring activities