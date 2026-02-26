# CLC2006 technical guidelines

- Aimed at providing guidelines for updating Corine land cover data for 2006 (CLC2006) by combining the 2000 base map (CLC2000) with land cover changes from 2000-2006 (CLC-Changes) using IMAGE2006 imagery.

- Managed by EEA with national NRCs and ETC-LUSI within the GMES Fast Track Service Precursor (FTSP) on Land Monitoring.

## Overview and context

- CLC2006 continues the Corine mapping series, focusing on changes between 2000 and 2006 and producing a seamless European CLC2006 database.

- IMAGE2006 is based on two-date satellite imagery (SPOT-4 and IRS P6) to support photo-interpretation; two dates per area help distinguish changes.

- National teams collect, verify, and interpret data; ETC-LUSI supports integration and standardization.

## Key technical parameters

- Scale: 1:100,000; MMU for CLC mapping: 25 ha; minimum width for lines: 100 m.

- Nomenclature: 44 land cover classes, organized in a three-level hierarchy; five level-one categories (artificial surfaces, agricultural areas, forests and semi-natural areas, wetlands, water bodies).

- Methodology: computer-assisted photo interpretation; ortho-corrected imagery; CLC2000 corrections, then integration with CLC-Changes to form CLC2006.

- Change database: CLC-Changes has MMU of 5 ha; used to capture real changes between 2000 and 2006.

## Data products and structure

- CLC2006: updated land cover map for 2006, produced by combining CLC2000 rev with CLC-Changes.

- CLC-Changes: dedicated changes database capturing real changes > 5 ha (and up to 25 ha where needed), including technical changes to bridge MMU differences.

- Relationship: CLC2006 = CLC2000 rev (+) CLC-Changes (but with special handling for changes < 25 ha and MMU differences).

- Changes in 2000-2006 are mapped directly (not inferred solely by GIS difference), to better reflect real processes.

## Imagery and data sources

- IMAGE2006: two-date multitemporal coverage to aid interpretation; SPOT-4 HRVIR and IRS P6 LISS III.

- Color composites and band choices recommended to align with interpreters’ prior experience (Landsat vs SPOT/IRS equivalents).

- Two dates per area; if changes occur between dates, the most recent image is used as reference.

## Change mapping methodology and typology

- Approach: change mapping first (chosen for more accurate reflection of real changes).

- Process: interpret changes directly from IMAGE2000 vs IMAGE2006; delineate change polygons; assign codes for 2000 and 2006; align with CLC2000 boundaries to avoid slivers.

- Technical changes: used to avoid gaps when changes push a polygon across 25 ha MMU; identified with a special attribute to distinguish them.

- Landscape-level changes: for heterogeneous classes (notably 242, 243, 313), changes may be mapped at landscape level when the landscape character shifts significantly.

- Change types (high-level): simple change, small change, disappearing polygon, new polygon, new polygon with small change, change-only, island changes, and small-change-only cases. Technical changes and landscape-level cases are documented with specific rules.

## Ancillary data and LUCAS support

- Ancillary data recommended: up-to-date topographic maps (1:50,000), orthophotos, additional high-resolution imagery, and other supporting data.

- LUCAS data: ground-truth LU and LC codes with field photographs available to support photointerpretation and change delineation. LUCAS coverage varies by country and is used to improve CLC2000 and change delineation (examples in annexes).

## Production and project organization

- Seven Work Packages (WPs); national NRCs coordinate at the national level; a Steering Committee and GMES LMCS Implementation Group provide governance.

- WP3 (Corine land cover mapping 2006) is described in detail; other WPs referenced for context.

## Metadata and quality assurance

- Metadata: two levels
  - Working unit level metadata (Annex 1): documents production steps for CLC-Changes; provided by national teams.
  - Country level metadata (Annex 2): describes main product parameters for CLC-Changes, CLC2006, and revised CLC2000 where applicable; follows EEA-MSGI/ISO19115 standards; EEA Metadata Editor recommended.

- Verification and QA: ETC-LUSI CLC Technical Team verifies CLC2000 and CLC-Changes; two verification missions planned; InterCheck software used; checks cover topology, mmu, codes, geometry, and metadata completeness.

## Deliverables and data delivery

- Deliverables to EEA Central Data Repository (CDR):
  - CHA06_xx: CLC-Changes 2000-2006
  - CLC00_xx: revised CLC2000 (if not produced as CLC2006 by national team)
  - CLC06_xx: CLC2006 products (if produced by national team)
  - Working unit metadata (MWU_xx_nn)
  - Country-level metadata for CLC-Changes (MCOCH_xx)
  - Country-level metadata for CLC2006 (MCO06_xx)

- File formats and naming:
  - Default: ESRI Arc/INFO Export Interchange File (E00) with no compression
  - Optional: ESRI Personal Geodatabase (MDB)
  - File naming: CHA06_xx.e00, CLC06_xx.e00, CLC00_xx.e00 (xx = ISO country code)
  - MDB equivalents: CHA06_xx.mdb, CLC2006_xx.mdb, etc. with specific internal naming for datasets and topology

- Coordinate reference system: data in national projections used for IMAGE2006; updates to CRS parameters must be reported; European CRS used if national parameters are confidential.

- Minimal mapping units (MMU) by dataset: CHA06 5 ha; CLC06 and CLC00 25 ha.

- Topology and data integrity: strict requirements for closed polygons, no dangles, no overlaps, single label per polygon, no artificial boundaries, cross-layer consistency.

- Data integration: CLC2006 = CLC2000 rev + CLC-Changes (for changes > 25 ha) with automatic and semi-automatic steps; for changes < 25 ha, generalisation and amalgamation rules apply; national teams or ETC-LUSI can perform integration with ArcInfo scripts.

## Delivery and quality assurance flow

- After delivery, technical quality checks (DBTA) determine acceptance or need for improvement; iterative corrections until acceptance.

- A delivery envelope approach and Unified Notification Service are used to manage data transfer and status updates.

## Metadata and documentation requirements

- Comprehensive documentation of data lineage, methodology, and parameter choices; annexes provide:

  - Annex 3: approaches for updating CLC data (update-first vs change-mapping-first; change-mapping-first chosen)
  - Annex 4/5: LUCAS nomenclature (LC and LU codes)
  - Annex 6: priority table for generalising CLC classes
  - Annex 7: contacts for CLC2006 TT and project management

## Practical implications for GIS specialists

- Implementing CLC2006 requires integrating two data streams with different MMUs (25 ha for CLC2006 and 5 ha for CLC-Changes) and ensuring topological integrity across three datasets (CLC2000 rev, CLC-Changes, CLC2006).

- Emphasis on direct interpretation of changes from multitemporal imagery, supported by ancillary data and LUCAS ground-truth data.

- Adoption of standardized metadata and delivery formats to ensure European-wide data integration.

- Use of automated scripts (ArcInfo/ArcGIS) for integration, with human oversight for complex or borderline cases.