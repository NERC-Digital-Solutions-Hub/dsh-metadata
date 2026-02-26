# CLC2006 technical guidelines

- Comprehensive guidelines for updating Corine land cover data for 2006 (CLC2006)
- Objective: produce CLC2006 by integrating CLC2000 with land cover changes (CLC-Changes) between 2000 and 2006 using IMAGE2006 data

## 1. Purpose and context
- Update strategy: merge CLC2000 with CLC-Changes derived from IMAGE2006 (two dates 2005/2006) to create CLC2006
- Hosted within GMES Fast Track Service Precursor (FTSP) Land Monitoring; coordinated by EEA with ETC-LUSI support
- Readers: national teams, for practical data production and European harmonisation

## 2. Key concepts and parameters
- Scale and detail
  - MMU: 25 hectares for CLC; 5 hectares for CLC-Changes (new)
  - 44 land cover classes in a three-level hierarchy (level-one: artificial, agricultural, forests/semi-natural, wetlands, water)
- Update methodology
  - Change mapping first approach: interpret LCC changes directly from IMAGE2000/IMAGE2006; then build CLC2006 as CLC2000 rev plus CLC-Changes
  - Distinct MMUs imply careful handling to avoid propagation of prior errors
- Change data
  - CLC-Changes: separate product with 5 ha MMU; focuses on real changes >5 ha and >100 m boundary displacement
  - All changes >5 ha are mapped, even if isolated from existing polygons
  - Change polygons carry two codes: 2000 and 2006 to reflect real processes
  - Technical changes (T): auxiliary polygons used to avoid MMU-related artefacts; named and flagged to be removed from final CLC-Changes

## 3. IMAGE2006 and data sources
- Satellite data: SPOT-4 and IRS P6 (LISS III); no Landsat-7 pan imagery
- Multi-temporal imagery: two dates per area, with at least 6 weeks separation
- Photo-interpretation: two dates to aid interpretation; recommended color composites and band combinations
- Ground truth and ancillary data: use topographic maps, orthophotos, and LUCAS data for ground truth where available

## 4. Land cover change mapping (CLC-Changes) and interpretation
- Change types and rules
  - Eight typologies (A–H) defined to guide interpretation based on presence/absence in CLC2000, CLC-Changes, and CLC2006
  - Landscape-level changes considered for heterogeneous classes (e.g., 242, 243, 313) when warranted
- Change interpretation workflow
  - Delineate changes directly in the image/interpretation environment
  - Use CLC2000 as the reference boundary to avoid slivers; assign 2000/2006 codes representing real processes
  - Distinguish real changes vs. technical changes; document with appropriate codes
- Examples and guidance
  - Simple change: >25 ha change linked to existing polygon
  - New polygon: emergence of a patch >25 ha; requires technical change polygon for the non-changed portion if needed
  - Change-only or displacement-only cases handled via code logic and generalisation as appropriate
- Landscape-level mosaics
  - For certain heterogeneous landscapes, delineation may occur at landscape level when the overall character shifts

## 5. Ancillary data and LUCAS integration
- Ancillary data: topographic maps, orthophotos, and additional high-resolution imagery recommended
- LUCAS data: ground-truth reference for photo-interpretation (2001/2002 and 2006); used to improve CLC2000 and delineate changes
- LUCAS nomenclatures (Annex 4/5) provide standardized LU/LC codes and field photos to assist interpretation

## 6 Production of the CLC2006 database
- Core approach: change mapping first, then integrate
- Integration logic
  - CLC2006 = CLC2000 rev + CLC-Changes
  - For changes >25 ha, integration is straightforward (automatic)
  - For changes <25 ha, generalisation/amalgamation rules apply (guided by Annex 6)
- Automation and human input
  - Most of CLC2006 generation is automatic, with photointerpreter decisions for threshold cases and under-definition cases
  - 6 main steps: (a) automatic processing, (b) integration for >25 ha, (c) generalisation for small changes, (d) possible neighbour-based generalisation, (e) handling borderline polygons (under 25 ha), (f) unresolved cases require interpreter input
- Output formats and metadata
  - Deliverables: CHA06 (CLC-Changes 2000-2006), CLC06 (CLC2006), CLC00 (revised CLC2000, if applicable)
  - Metadata: working unit level (Annex 1) and country level (Annex 2)

## 7 Metadata
- Two levels: Working unit metadata and Country level metadata
- Compliance: European Environment Agency Metadata Standard for Geographic Information (EEA-MSGI), with optional EEA Metadata Editor
- Contents include: data origin, data sources, ancillary data, photointerpreters, border matching, topology checks, verification, and delivery details

## 8 Verification and quality assurance
- Verification by CLC2006 Technical Team (ETC-LUSI)
- Two verification missions per country: 25–50% area and 75–100% area
- Verification checks cover:
  - Topological integrity (no dangles, gaps, or overlaps; unique polygon labeling)
  - Consistency across CLC2000 rev, CHA06, and CLC2006
  - Metadata completeness and correctness
- Tools: InterCheck software for automated checks; detailed feedback provided to national teams

## 9 Deliverables and delivery process
- Deliverables
  - CHA06 (CLC-Changes 2000-2006)
  - CLC00 (revised CLC2000, where applicable)
  - CLC06 (CLC2006)
  - Working unit metadata (MWU_xx_nn)
  - Country metadata for CHA06 (MCOCH_xx) and CLC2006 (MCO06_xx)
- Delivery to European Environment Agency (EEA) via Central Data Repository (CDR)
- File naming conventions (example: CHA06_MT02, CLC06_MT02, CLC00_MT02)
- File formats
  - Default: ESRI Arc/INFO Export Interchange File (E00) with no compression
  - Optional: ESRI Personal Geodatabase (MDB)
- Attribute, CRS, and topology requirements
  - Consistent with MMU, valid CLC codes, topology integrity, 1 km sea buffer, and national projections
- Delivery workflow and verification
  - Pre-delivery QC and ongoing verification
  - If severe issues are found, iterative corrections are required
  - Post-acceptance steps include DBTA (Database Technical Acceptance) reports

## 10 Delivery – technical specifications
- File formats
  - E00 as default; MDB optional
- File naming and structure
  - CHA06_xx.e00, CLC06_xx.e00, CLC00_xx.e00
  - MDB equivalents with corresponding dataset names and auxiliary topology files
- Attribute and code conventions
  - Unique IDs, two date codes per change polygon (00 and 06)
  - Area, Perimeter, Code_00, Code_06, Change, Chtype, Area_ha, Remarks
- Coordinate reference system
  - Delivered in each country’s national projection; document any use of European CRS if needed
- MMU and mapping standards
  - CHA06: MMU = 5 ha; CLC06 and CLC00: MMU = 25 ha
- Topology and metadata
  - Full topological checks; no gaps or artificial boundaries; cross-layer consistency
  - Metadata files (working unit and country level) accompanying data

## 11 Annexes and supporting guidance (highlights)
- Annex 3: Approaches for updating CLC data
  - Update-first vs change-mapping-first; CLC2006 uses change-mapping-first
- Annex 4 & 5: LUCAS nomenclature
  - Detailed LU/LC codes and examples for 2001/2002 and 2006
- Annex 6: Priority table for generalising CLC classes
  - Coding priorities to guide generalisation when MMU differences arise
- Annex 7: Contacts
  - Key points of contact for TT coordinator, project manager, and verification teams

## 12 References
- Core literature and prior CLC2000/1990 guidelines, technical reports, and supporting GMES context