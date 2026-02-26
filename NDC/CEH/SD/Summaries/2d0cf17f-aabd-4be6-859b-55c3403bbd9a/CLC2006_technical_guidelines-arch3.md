CLC2006 technical guidelines

## Overview
- Guidelines for updating Corine land cover data for reference year 2006 (CLC2006).
- Produces CLC2006 by integrating CLC2000 with Land Cover Changes (CLC-Changes) for 2000-2006.
- Managed by EEA with national contributions via Eionet NRCs; part of GMES Fast Track Service Precursor (FTSP) Land Monitoring.
- Readers: national CLC teams and organizations involved in production; aims to guide practical production and ensure data quality and consistency.

## Key technical parameters and data products
- Scale and classes:
  - CLC mapping at 1:100,000 scale; minimum mapping unit (MMU) 25 ha; minimum width of linear elements 100 m.
  - Standard nomenclature includes 44 land cover classes organized in a three-level hierarchy (five level-1 categories).
- Change data:
  - CLC-Changes database uses MMU 5 ha and 100 m minimum width.
  - All real changes larger than 5 ha should be mapped; not limited to existing polygons.
- Methodology:
  - Change mapping first approach: CLC2006 derived from CLC2000 rev + CLC-Changes (for >25 ha) or via integrated editing for smaller changes.
  - Photo-interpretation of IMAGE2000 and IMAGE2006 to detect changes; supports use of ancillary data and LUCAS ground-truth data.

## Data sources and ancillary information
- IMAGE2006 satellite data: two dates, using SPOT-4 and IRS P6 (LISS III); aims for multi-temporal imagery to improve interpretation.
- IMAGE2000 data: Landsat-7 ETM used for baseline.
- Ancillary data: topographic maps (1:50,000+), orthophotos, additional high-resolution imagery; LUCAS data (2001/2002 and 2006) for ground-truth support and improved photo-interpretation.

## Change mapping and interpretation rules
- All changes > 5 ha are delineated; changes can be island-like or connected.
- Change polygons in CLC-Changes carry two codes: 2000 and 2006, representing pre- and post-change classes.
- Technical changes (T) may be used to reconcile MMU differences and are removed from final CLC-Changes; they require a special attribute to identify them.
- Landscape-level changes: for certain heterogeneous landscape classes (e.g., 242, 243, 313), changes may be mapped at landscape level if they alter the overall character.
- Relationship with CLC2000:
  - CLC2006 = CLC2000 rev + CLC-Changes for changes > 25 ha (automatic).
  - For changes < 25 ha, generalisation and amalgamation rules apply; exact mathematical relation between databases is not strictly fulfilled.

## Annexes and methodological approaches
- Annex 3 outlines two update approaches:
  - Update first: revise CLC2000 using IMAGE2000, then apply changes to produce CLC2006 (not preferred for this project).
  - Change mapping first: interpret changes directly from IMAGE2000 vs IMAGE2006, then derive CLC2006; this is the chosen approach for CLC2006.
- Annexes also cover LUCAS nomenclature, generalisation priority, and more detailed change typologies.

## Ancillary data and LUCAS support
- LUCAS land use/cover data provide ground-truth support for photo-interpretation and change delineation.
- Annexes 4 and 5 provide LUCAS 2001/2002 and 2006 nomenclatures (land cover and land use) used for interpretation and verification.

## Metadata and verification
- Metadata:
  - Two levels: working unit level metadata for CLC-Changes (Annex 1) and country-level metadata for CLC-Changes and CLC2006 (Annex 2).
  - Follows European Environment Agency Metadata Standard for Geographic Information (EEA-MSGI); preferred use of EEA Metadata Editor with ArcGIS.
- Verification and quality assurance:
  - ETC-LUSI CLC Technical Team verifies CLC2000 and CLC-Changes; two verification missions planned per country.
  - InterCheck software used for verification; checks cover topological consistency, geometry, coding, and metadata completeness.
  - Technical Quality Check Reports (DBTA) accompany each deliverable, documenting checks and acceptance status.

## Deliverables and data flow
- Deliverables:
  - CHA06: CLC-Changes (2000-2006) data.
  - CLC00 rev: revised CLC2000 (for countries not producing CLC2006 themselves).
  - CLC06: CLC2006 database (for countries producing CLC2006 with support).
  - Working unit metadata for CLC-Changes (MWU_xx_nn).
  - Country metadata for CLC-Changes (MCOCH_xx) and CLC2006 (MCO06_xx).
- Delivery mechanism:
  - All deliveries via the EEA Central Data Repository (CDR).
  - File packaging: each delivery in one envelope; separate compressed files inside (E00 format by default; MDB as optional).
  - File naming: CHA06_xx.e00, CLC06_xx.e00, CLC00_xx.e00 with 8-character country codes; versioning indicated in names (e.g., MT02).
- File formats and schemas:
  - Default data format: ESRI Arc/INFO Export Interchange File (E00) with build polygon topology.
  - Optional format: ESRI Personal Geodatabase (MDB).
  - Coordinate reference systems: national projections used in IMAGE2006; cross-border buffer and sea buffer guidance to ensure seamless European integration.
  - Attribute and topology requirements specified (e.g., valid CLC codes, MMU adherence, 100 m width for lines, no gaps, consistent delineation across layers).

## Delivery process and quality control
- Delivery schedule aligned with national project plans; deviations coordinated with ETC-LUSI.
- Pre-delivery QA/QC supported by TT; in case of issues, iterative deliveries (improvement cycles) until acceptance.
- After delivery, TT performs a technical quality check; accepted data trigger final acceptance notes and data upload back to CDR; severe issues trigger improvement cycles.

## Governance, roles, and coordination
- GMES FTSP Land Monitoring framework with EEA, ESA, JRC, and participating countries; Steering Committee oversees and coordinates.
- NRCs (National Reference Centres) organize national work; ETC-LUSI provides technical support and data integration guidance.
- Metadata standards and data sharing are emphasized to avoid data silos and ensure openness and interoperability.

## Practical considerations and challenges
- Data gaps and access limitations are acknowledged as ongoing challenges.
- Siloing between organizations, data becoming out-of-date, and metadata inadequacies are barriers to timely, usable monitoring data.
- Ensuring data governance, standardised metadata, and transparent delivery processes are central to enabling consistent, Europe-wide environmental health monitoring.

## Contacts and references
- CLC2006 TT coordinator and project management contacts listed for coordination and support.
- References include EEA/GMES documentation, methodology guides, and annexed metadata standards and nomenclatures.