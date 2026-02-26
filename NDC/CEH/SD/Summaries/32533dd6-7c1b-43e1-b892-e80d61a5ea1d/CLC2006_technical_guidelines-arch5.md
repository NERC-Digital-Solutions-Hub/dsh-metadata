# CLC2006 technical guidelines

- Aims: Provide guidelines for updating Corine land cover data for 2006 (CLC2006) by integrating land cover changes from 2000-2006 with the CLC2000 map, to produce a timely, quality-assured European land cover database within the GMES Fast Track Service Precursor (FTSP) for Land Monitoring.
- Governance: Production managed by Eionet National Reference Centres (NRCs) with data integration by EEA and ETC-LUSI; Steering Committee and GMES LMCS advisory group coordinate cross-service links.

## Key concepts and products

- CLC2006: Updated land cover map for 2006, created from CLC2000 plus CLC-Changes (land cover changes 2000-2006) derived from IMAGE2006.
- CLC-Changes: A separate change database (MMU 5 ha) detailing real land cover changes between 2000 and 2006, including changes not tied to existing polygons; intended to be integrated with CLC2000 to form CLC2006.
- Nomenclature and scale: Uses 44 land cover classes in a three-level hierarchy; mapping scale is 1:100,000; MMU 25 ha for CLC, 5 ha for CLC-Changes; emphasis on improving geometry and thematic accuracy.
- Photos and imagery: IMAGE2006 provides two-date, multitemporal SPOT-4 and IRS P6 imagery to support photo-interpretation; time windows are country-specified but kept within a 6-week separation constraint between images.

## From CLC1990/CLC2000 to CLC2006

- Background: CLC updates built on earlier CORINE programs, with improved geometry and metadata; CLC2006 focuses specifically on 2000-2006 changes.
- Differences versus earlier updates: No broad revision of CLC2000 needed; emphasis on detecting all real changes > 5 ha; all changes > 5 ha must be mapped; updates rely on a predominantly automatic workflow with expert interpretation.

## Project organization and work packages

- Seven work packages (WP) structure to deliver the FTSP Land Monitoring service.
- NRCs organize national activities; EEA and ETC-LUSI coordinate cross-border and integration tasks.
- Steering Committee includes Commission, ESA, EEA, and participating countries; LMCS Implementation Group provides advisory linkage.

## IMAGE2006 basics and data requirements

- Data sources: SPOT-4 and IRS P6 provide multitemporal coverage; two dates per area (with seasonality considerations).
- Photo-interpretation guidance: recommended color composites and display settings to align with historical interpretation when needed; two dates help distinguish certain land cover changes (e.g., irrigated vs non-irrigated arable land).

## Mapping land cover changes (CLC-Changes)

- Core product: CLC-Changes database records real changes > 5 ha, > 100 m displacement, between 2000 and 2006; can be island-like or connected to existing polygons.
- Updating approach: direct change mapping using IMAGE2000 vs IMAGE2006 in a dual-window environment; CLC2000 polygons serve as the basis for delineation to avoid slivers.
- Change delineation: each change polygon must carry two codes: 2000 and 2006, representing the land cover status in the two dates.
- Change types: Eight typologies (A–H) across three databases (CLC2000 25 ha MMU, CLC-Changes 5 ha, CLC2006 25 ha MMU) to handle simple, complex, new, disappearing, and “technical” changes. Technical changes are used to resolve MMU/accuracy gaps and are flagged accordingly.
- Landscape-level changes: for heterogeneous landscape classes (e.g., 243, 242, 313), changes may be mapped at landscape level if the landscape character changes significantly.

## Ancillary data and ground-truth support

- Ancillary data: topographic maps (1:50,000+), orthophotos, and additional high/medium-resolution imagery recommended to support photo-interpretation.
- LUCAS data: ground-truth land use and land cover codes with field photos available to support photo-interpretation and validation (varies by country and year). LUCAS data aids in improving CLC2000 interpretation and delineating changes (CLC2006).

## Production of CLC2006 database

- Integration approach: CLC2006 = CLC2000 rev + CLC-Changes; but due to MMU differences (25 ha vs 5 ha), exact mathematical combination is valid mainly for changes > 25 ha; smaller changes require generalisation rules.
- Change-first workflow: national teams interpret all LCCs > 5 ha; identify and correct errors in CLC2000; integrate CLC-Changes, then generate CLC2006.
- Semi-automatic process: includes computer processing for >25 ha changes and generalisation/amalgamation for smaller changes; some manual interpretation is required for under-25 ha cases.
- Three databases treated as nearly independent for some analyses due to MMU differences.

## Metadata

- Two levels: Working Unit (WU) metadata for CLC-Changes; Country-level metadata for CLC-Changes and CLC2006 (and revised CLC2000 when applicable).
- Standards: metadata aligned with EEA-MSGI/ISO19115; EEA Metadata Editor available for ArcGIS environments; country metadata templates provided.

## Verification and quality assurance

- Verification by CLC2006 Technical Team (ETC-LUSI) to ensure consistent interpretation and harmonization across Europe.
- Two verification missions per country (mid-phase and late-phase); use of InterCheck tooling and a structured set of criteria to check topology, accuracy, and metadata completeness.
- Key QA areas: topological consistency, no dangles, no gaps, metadata completeness, and consistent delineation across CLC2000, CLC-Changes, and CLC2006.

## Deliverables and delivery process

- Deliverables: CHA06 (CLC-Changes 2000-2006), revised CLC2000 (CLC00_xx) where applicable, CLC2006 (CLC06_xx), working unit metadata (MWU_xx_nn), country metadata (MCOCH_xx, MCO06_xx).
- Delivery to Central Data Repository (CDR) of the EEA; national coordinators manage envelopes and versions; notifications via Unified Notification Service.
- File formats and naming: default ESRI Arc/INFO E00 format; MDB (ESRI Personal Geodatabase) optional; file naming uses 8-character country codes with versioning (e.g., CHA06_AT, CLC06_AT, CLC00_AT; MDB variants as applicable).
- Attribute conventions: unique IDs, 3-letter CLC codes for 2000/2006, change codes, and a Chtype indicator (change type) to capture whether a change is real or technical.
- Coordinate reference system: deliver in national projection aligned with IMAGE2006 production; provide CRS parameters for integration to European dataset if national projection is confidential.

## Technical specifications (highlights)

- Minimal Mapping Unit (MMU): CHA06 (CLC-Changes) MMU = 5 ha; CLC06 (CLC2006) and CLC00 (revised CLC2000) MMU = 25 ha.
- Topology: strict requirements for topology, no gaps, no artificial boundaries, no duplicated lines, polygons closed, single code per polygon, and cross-layer consistency.
- Data formats: E00 as default; MDB optional for modern geodatabase workflows; file naming, attribute definitions, and CRS documentation outlined.
- Metadata and documentation: comprehensive metadata requirement (WU and country levels) with templates; verification results feed into acceptance reports.

## Annexes and references

- Annexes cover updating approaches (Annex 3), LUCAS nomenclature (Annex 4/5), generalisation priority tables (Annex 6), and contact information (Annex 7).
- References include foundational CORINE guides, LUCAS references, and methodological papers detailing change mapping and verification practices.
- Key contacts provided for CLC2006 TT coordination, technical acceptance, and project management.

Note: The guidelines emphasize robust data governance, standardized metadata, controlled change-tracking, harmonized delivery processes, and transparent QA to ensure that CLC2006 and associated products meet European data-sharing and interoperability needs.