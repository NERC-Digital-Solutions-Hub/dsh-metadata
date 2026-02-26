# CLC2006 technical guidelines

- Aims to update Corine land cover data for 2006 by integrating the land cover map from 2000 (CLC2000) with a new database of land cover changes (CLC-Changes) derived from IMAGE2006 (two-date satellite imagery). Managed by EEA, Eionet NRCs, and ETC LUSI within the GMES Fast Track Service Precursor for Land Monitoring.

## Key concepts and parameters

- Scale and classes
  - Mapping scale: 1:100,000
  - Minimum Mapping Unit (MMU): 25 ha for CLC2000/CLC2006; 5 ha MMU for CLC-Changes
  - Hierarchy: 44 land cover classes in a three-level structure; five level-one groups (artificial surfaces, agricultural areas, forests and semi-natural areas, wetlands, water bodies)
- Methodology
  - Computer-assisted visual interpretation of satellite imagery
  - Consistent national nomenclature; Addendum 2006 updates for definitions
- Data quality targets
  - Thematic accuracy: typically ≥ 85%
  - Geometric accuracy: ≤ 25 m for IMAGE2000/2006 reference data
  - Edge-matching and seamless European coverage

## IMAGE2006 imagery and interpretation

- Satellites and data
  - SPOT-4 and IRS P6 (LISS III) provided for multi-temporal coverage
  - Two dates per area (two acquisitions in the 2006 +/- 1 year window)
  - Panchromatic band availability differs from CLC2000 (no pan for IMAGE2006)
- Photo-interpretation guidance
  - Two images per area to improve discrimination (e.g., irrigated vs non-irrigated arable land)
  - Color composites and recommended band combinations provided
  - Use of ancillary data (topographic maps, orthophotos) and LUCAS data to ground-truth interpretation

## CLC-Changes database and change mapping

- Purpose and scope
  - Primary product for CLC2006: changes in land cover between 2000 and 2006
  - MMU for changes: 5 ha (minimum) and 100 m boundary displacement; all changes > 5 ha mapped
  - All changes > 5 ha must be delineated, regardless of position (including island-like changes)
- Updating approach
  - Change mapping first: interpret changes directly from IMAGE2000 vs IMAGE2006, generating CLC-Changes polygons
  - CLC2006 derived as: CLC2006 = CLC2000 rev + CLC-Changes through a defined intersection/replace process
  - Unlike CLC2000, CLC-Changes polygons are created directly from imagery for real changes
- Change types and typology
  - Eight theoretical change types (A–H) based on existence/absence in CLC2000, CLC-Changes, and CLC2006
  - Technical changes (T) used to avoid misclassifications when MMU differences create artifacts; these are identified and later removed from CLC-Changes
  - Landscape- and heterogeneous-class edits are addressed with dedicated rules (e.g., 243-211) to reflect real landscape changes
- Handling of boundary and mosaicking
  - Changes must be delineated using CLC2000 polygons as a basis to avoid slivers
  - Two-code attribution per change polygon: code 2000 and code 2006, reflecting the real process
- Source data and border considerations
  - Uses edge-matched CLC2000 as the basis for change delineation
  - Border strips (2 km) considered; border similarity checks performed; edge-matching simplifies CLC2006 border integration

## Participating countries and governance

- 38 European countries participate (EEA members and collaborators)
- GMES FTSP Land Monitoring governance
  - National Reference Centres (NRCs) organize national implementation
  - Steering Committee with DG ENV, EEA, ESTAT, JRC, ESA, and participating countries
  - GMES LMCS Implementation Group provides advisory linkage to other GMES services
- Work packages
  - Seven work packages (WP1–WP7) define roles (satellite data, ortho-correction, mosaicking, in-situ/ancillary data, CLC-Change mapping, CLC2006 mapping, validation, data dissemination, project management)
  - WP3 (Corine land cover mapping 2006) is central to production; national teams execute national plans

## Production workflow for CLC2006

- Two-track data integration
  - CLC2006 production uses CLC2000 rev (corrected where needed) plus CLC-Changes
  - Because MMU differs (25 ha for CLC2000/CLC2006 vs 5 ha for CLC-Changes), an exact automatic equation cannot always be used
  - Semi-automatic integration with photo-interpretation input and generalisation guidance
- Change-first vs update-first approaches
  - The project adopts the change-mapping-first approach for better reflection of real changes
  - CLC2006 = CLC2000 rev + CLC-Changes (with subsequent generalisation as needed)
- Generalisation and amalgamation
  - Small changes (< 25 ha) require generalisation to neighbours or amalgamation to maintain consistent MMU
  - Special handling for complex or unclear cases where exact automatic mapping would be misleading

## Ancillary data and LUCAS support

- Ancillary data
  - Topographic maps (scale 1:50,000 or better), orthophotos, and additional high/medium resolution imagery
- LUCAS data
  - Ground-truth land use and land cover codes with field photographs from LUCAS 2001/2002 and 2006
  - Used to improve CLC2000 (LUCAS 2001/2002) and to support CLC2006 photo-interpretation
  - Nomenclatures for LUCAS LC and LU provided in Annexes 4 and 5

## Metadata and verification

- Metadata
  - Two levels: working unit level metadata (Annex 1) and country level metadata (Annex 2)
  - Metadata aligned with European standards (EEA-MSGI, ISO19115, INSPIRE guidance)
  - EEA Metadata Editor recommended for ArcGIS users; forms available for non-ArcGIS users
- Verification and quality assurance
- Verification by ETC-LUSI Technical Team
  - Two verification missions; use InterCheck software
  - Checklists cover formal specifications, mapping/topology, metadata, and overall data quality
- Deliverables and validation
  - CLC-Changes (2000-2006), revised CLC2000, CLC2006, and associated metadata
  - Technical Quality Check Reports (DBTA) accompany each deliverable
  - Deliverables to be submitted to the EEA Central Data Repository (CDR)

## Data delivery, formats, and technical specifications

- File formats
  - Default: ESRI Arc/INFO Export Interchange File (E00) with no compression
  - Optional: ESRI Personal Geodatabase (MDB)
- File naming conventions
  - CHA06_xx.e00 for CLC changes (2000-2006)
  - CLC06_xx.e00 for CLC2006 status
  - CLC00_xx.e00 for revised CLC2000
  - Example: CHA06_MT02, CLC06_MT02, CLC00_MT02
- Coordinate Reference System (CRS)
  - Use national projection for IMAGE2006; report any deviations or updates to the TT
  - If national CRS parameters are confidential, provide data in a European CRS
- Attribute and data definitions
  - Detailed field definitions for Area, Perimeter, Code_00/Code_06, Change, Chtype, etc. included
  - Chtype indicates the type of change (real vs technical)
- Topology and data integrity
  - Requirements include no gaps, no dangles, polygons closed, single label per polygon, no overlapping polygons, and consistent cross-layer delineation
  - 1 km sea buffer along coastlines to ensure seamless edge matching
- MMU and mapping thresholds
  - CHA06 MMU = 5 ha for changes; CLC06/CLC00 MMU = 25 ha
  - Complex/elementary changes may have special treatment under the established rules

## Change interpretation guidelines and landscape mosaics

- Landscape-level changes
  - For heterogeneous classes (e.g., mosaics within 243, 242, 313), determine if landscape-level change warrants a polygon-level change (e.g., 243-211)
  - If changes alter the landscape character significantly, the change polygon may cover the whole area (e.g., 243-211)
- Real vs technical changes
  - Real changes reflect actual land cover evolution
  - Technical changes (T) are auxiliary constructs to enable mapping and are removed from the final CLC-Changes dataset

## Deliverables, contacts, and references

- Deliverables include:
  - CHA06 (CLC-Changes 2000-2006)
  - CLC00 (revised CLC2000)
  - CLC06 (CLC2006)
  - Working unit metadata and country-level metadata
- Key contacts and organizational roles are listed (TT coordinator, project manager, etc.)
- References and annexes provide nomenclature details (LUCAS), update approaches, priority generalisation tables, and metadata templates

- This document provides practical, end-to-end guidance for GIS-focused teams to produce, validate, and deliver a harmonised European CLC2006 dataset, with emphasis on change-driven mapping, data quality, metadata rigor, and standardized delivery to the European Central Data Repository.