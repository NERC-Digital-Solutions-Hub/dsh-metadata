# CLC2006 technical guidelines

## Overview
- Guidelines for updating Corine land cover data for 2006 (CLC2006) by integrating land cover changes (2000–2006) with the CLC2000 map.
- Part of the GMES Fast Track Service Precursor (FTSP) on Land Monitoring; national teams map changes and produce CLC2006 databases.
- Readers: national CLC teams, ETC-LUSI, and related partners involved in production and delivery.
- Emphasizes data quality, openness, metadata, and harmonised European product delivery.

## Context and aims
- Build CLC2006 by combining CLC2000 with a dedicated CLC-Changes database derived from IMAGE2006 imagery.
- Establish a European coverage of real land cover changes > 5 ha, based on multi-temporal satellite data (two dates) and photo-interpretation.
- Correct and harmonise earlier CLC products; avoid propagating errors from CLC2000 into CLC2006.
- Ensure timeliness, traceability, and data governance across participating countries.

## Data structures and products
- CLC2006 database: updated land cover map for 2006 (based on CLC2000 plus CLC-Changes).
- CLC-Changes database: a separate, higher-resolution change layer (MMU 5 ha) capturing real changes between 2000 and 2006; used to update CLC2006.
- IMAGE2006: multi-temporal satellite data (two dates) used for photo-interpretation; two images acquired per area to aid interpretation.
- CLC2000 rev: revision of CLC2000 used to correct errors prior to integration.
- Data integration is largely semi-automatic; final delineation involves human interpretation.

## Main technical parameters
- Scale: 1:100,000; MMU for CLC mapping: 25 ha; minimum width for linear elements: 100 m.
- 44 land cover classes organized in a three-level hierarchy; five level-one categories: artificial surfaces, agricultural areas, forests and semi-natural areas, wetlands, water bodies.
- Mapping methodology: computer-assisted photo-interpretation; ortho-corrected imagery; higher geometric accuracy achieved via IMAGE2000/2006 data.
- CLC2006 focuses on changes between 2000 and 2006; CMU for changes is 5 ha (with some complex/elementary cases).

## Change mapping and typology (CLC-Changes)
- All changes larger than 5 ha must be delineated, irrespective of their position.
- Change polygons are created directly by photo-interpretation in a dual-window environment comparing IMAGE2000 and IMAGE2006.
- Each change polygon has two codes: code2000 and code2006, representing land cover at each date.
- Technical changes (T) may be introduced to avoid errors due to MMU differences; technical changes are marked and later removed from the CLC-Changes database.
- Eight change types (A–H) describe scenarios across the three databases (CLC2000, CLC-Changes, CLC2006) and guide handling of updates, with detailed examples in figures and annexes.
- Landscape-level changes for heterogeneous classes may be mapped if the change affects landscape character (e.g., 243 to 211 scenarios).

## Participating bodies and governance
- 38 countries participate in GMES FTSP Land Monitoring (EEA member and collaborating countries).
- National Reference Centres (NRCs) for spatial analysis and land cover coordinate national work; ETC-LUSI supports integration and methodology.
- Steering Committee includes the Commission, ESA, EEA, and participating countries; LMCS Implementation Group provides advisory input.

## IMAGE2006 basics and data requirements
- New imagery sources: SPOT-4 HRVIR and IRS P6 LISS III used (instead of Landsat-7 ETM used in CLC2000).
- Two-date, multi-temporal imagery per area to improve photo-interpretation; avoid single-date limitations.
- Recommended color composites align with Landsat and SPOT/IRS sensor characteristics to aid interpretation.
- If changes occur between the two IMAGE2006 dates, the most recent image is used as reference for interpretation in most cases.

## Ancillary data and ground-truth support
- Proposed ancillary data to support interpretation: up-to-date topographic maps (1:50,000), orthophotos, and additional high/medium-resolution imagery.
- LUCAS data (land use/cover area frame survey) available for several countries to support photointerpretation and ground truth; LUCAS LC and LU nomenclatures provided in annexes.

## Production of the CLC2006 database
- Change mapping first approach: national teams interpret LCCs > 5 ha; CLC2006 is produced by integrating CLC2000 rev and CLC-Changes.
- Integration nuances:
  - For changes > 25 ha, CLC2006 = CLC2000 rev + CLC-Changes straightforwardly.
  - For changes < 25 ha, generalisation and priority rules are applied; exact mathematical relations between CLC2000, CLC-Changes, and CLC2006 may not hold.
- Two main processing parts:
  - Computerised processing: automatic integration for changes > 25 ha; generalisation/amalgamation for small changes.
  - Non-automated processing: photointerpreter decisions for borderline cases (e.g., 23–25 ha), unclear generalisation, and complex scenarios.
- Outputs include CLC2006, CLC-Changes, and revised CLC2000 where applicable.

## Metadata and data provenance
- Two levels of metadata: working unit level (MWU) and country level (MCOCH, MCO06).
- Metadata standards aligned with EEA-MSGI (ISO19115 profile) and INSPIRE; EEA metadata editor recommended.
- Documentation accompanies data deliveries to ensure traceability and harmonisation.

## Verification and quality assurance
- CLC Technical Team (ETC-LUSI) verifies both CLC2000 rev and CLC-Changes; ensures harmonisation and data quality across Europe.
- Verification missions cover topological consistency, accuracy, and metadata completeness; InterCheck software used for QA.
- Verification scope includes both formal specification checks and thematic/geometric checks; results fed back to national teams to guide corrections.

## Deliverables and delivery process
- Deliverables:
  - CHA06: CLC-Changes 2000–2006
  - CLC00: revised CLC2000 (for countries not producing CLC2006 themselves)
  - CLC06: CLC2006 product
  - Working unit metadata (MWU_xx_nn)
  - Country-level metadata for CLC-Changes (MCOCH_xx) and CLC2006 (MCO06_xx)
- Delivery via the European Environment Agency Central Data Repository (CDR); standardized file naming conventions (e.g., CHA06_xx.e00, CLC06_xx.e00, CLC00_xx.e00).
- Optional MDB (ESRI Personal Geodatabase) delivery available; both E00 and MDB formats support topology.
- File naming includes ISO country codes; file attributes and structure conform to detailed specifications (Tables 11–13 in the guidelines).
- Coordinate reference system (CRS) must match national projections used for IMAGE2006; updates to CRS parameters should be reported.

## Technical specifications and quality criteria
- MMU: 5 ha for CHA06; 25 ha for CLC06 and CLC00; allows complex cases with elementary changes under 5 ha.
- File formats: default E00 (Arc/Info export interchange); MDB optional; topology maintained.
- Topology: no dangles, no gaps, polygons closed, single label per polygon, no overlapping polygons, no artificial boundaries, cross-layer consistency.
- Metadata and data checks: formal specifications, mapping specifications, topology specifications, and metadata checks are documented; DBTA reports used to document acceptance or requests for improvement.
- Attribute definitions and code lists detailed in annexes; code consistency and change pairs are essential.

## Delivery workflow and contacts
- After delivery, technical quality checks determine acceptance or need for improvement.
- If improvements are needed, new deliveries follow a versioning scheme (e.g., version_02).
- Notifications and verification flow managed via the Unified Notification Service; TT coordinators, national coordinators, and relevant parties are alerted upon data readiness.
- Primary contacts for CLC2006 TT, project management, and data dissemination are provided in annexes.

## Endnotes and references
- The document references substantial background on CLC1990/CLC2000 updates, LUCAS nomenclature, and related annexes that define metadata templates, update approaches, and generalisation rules.
- Annexes provide working unit metadata templates, country metadata structures, LUCAS nomenclature, priority generalisation tables, and contact information.