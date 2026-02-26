# CLC2006 technical guidelines

- Aims to update Corine land cover data for 2006 (CLC2006) by integrating CLC2000 with land cover changes from 2000-2006 (IMAGE2006), managed by Eionet NRCs and coordinated by EEA with ETC-LUSI. Delivers CLC2006 and CLC-Changes to support GMES/FTSP Land Monitoring.

## 1. Key context and scope
- CLC2006 builds on CLC1990 and CLC2000; introduces a dedicated CLC-Changes database for real changes between 2000 and 2006.
- Focus is on timely, quality-assured, Europe-wide land cover data; improvements over CLC2000 where needed; changes >5 ha mandatory to map.
- 38 participating countries; part of GMES FTSP Land Monitoring.

## 2. Main technical parameters
- Scale: 1:100,000; MMU for CLC = 25 ha; minimum width for linear elements = 100 m.
- Nomenclature: 44 land cover classes in a three-level hierarchy; five level-one groups (artificial, agricultural, forests/semi-natural, wetlands, water).
- Mapping method: computer-assisted visual interpretation of satellite imagery; higher geometric accuracy with IMAGE2000, orthophotos, and topographic maps.
- Data quality and consistency targets maintained across CLC1990/2000/2006 updates.

## 3. CLC2006 in the GMES framework
- CLC2006 is part of the GMES Fast Track Service Precursor (FTSP) Land Monitoring; complements other core GMES components.
- Key differences from prior rounds:
  - No major geometry/content overhaul of CLC2000; focus on 2000-2006 changes.
  - All changes >5 ha must be mapped (not only those linked to existing polygons).
  - Change mapping is largely automatic, with human oversight; integrates CLC2000 and CLC-Changes to form CLC2006.

## 4. CHANGE database and change mapping approach
- CLC-Changes: dedicated database for real land cover changes >5 ha (MMU 5 ha; 100 m boundary); independent from CLC2000/CLC2006.
- Updating approach (favoured for CLC2006): interpret changes directly from IMAGE2000 vs IMAGE2006; then merge with CLC2000 to create CLC2006.
- Each change polygon carries a 2000 code and a 2006 code to reflect actual processes; “technical changes” (T) are used only to resolve MMU/aggregation issues and are not real land cover changes.
- Changes are delineated using CLC2000 as the baseline to avoid slivers; all changes >5 ha must be captured, including isolated patches.

## 5. Change typology and interpretation guidance
- Eight change types (A–H) defined by the presence/absence and size in CLC2000, CLC-Changes, and CLC2006; guidance and examples provided to handle complex cases.
- Emphasis on avoiding false changes (seasonal, transient, or non-persistent changes) and handling heterogeneous/landscape-level classes appropriately.
- Landscape-level changes for certain heterogeneous classes (e.g., mosaics) may be mapped at landscape level when character of the area changes.

## 6. Source data, and ancillary information
- IMAGE2006: multi-temporal data using SPOT-4 and IRS P6 (LISS III); two dates per area within 2005-2006 window to aid interpretation; no panchromatic band in this cycle.
- Ancillary data recommended: topographic maps (1:50,000+ digital if available), orthophotos, and additional high/medium-resolution imagery; LUCAS data support photo-interpretation.

## 7. LUCAS data and field truth
- LUCAS land use/cover data and field photographs (from 2001/2002 and 2006 cycles) available to national teams; used to improve CLC2000 and support CLC2006 change delineation.
- Annexes provide LUCAS nomenclature and examples of usage.

## 8. Production of the CLC2006 database
- Overall method: “change mapping first” approach; CLC2006 = CLC2000 rev + CLC-Changes for changes >25 ha; for changes <25 ha, generalisation steps apply.
- Two-part process:
  - Computerized processing: integration of >25 ha changes, generalisation/amalgamation for small changes, semi-automatic where possible.
  - Non-automated processing: photointerpreter decisions for near-threshold cases and ambiguous generalisations.
- Resulting relationship: CLC2000, CLC-Changes, and CLC2006 are treated as three largely independent databases due to differing MMUs.

## 9. Metadata and data quality
- Two levels of metadata: working unit (for CLC-Changes production) and country level (for CLC-Changes, CLC2006, and revised CLC2000 when applicable).
- Metadata standards: European Environment Agency Metadata Standard for Geographic Information (EEA-MSGI); use of EEA metadata editor where possible.
- Verification: ETC-LUSI technical team performs photo-interpretation verification; two verification missions per country; uses InterCheck software; aims to harmonise European outputs.

## 10. Verification and quality assurance
- Verification focuses on topological consistency, thematic accuracy, and proper coding and delineation of changes.
- QA checks cover formal specifications, mapping, topology, and metadata; includes error location annotations and recommendations.
- Emphasis on corrected data prior to European integration to minimize iterations.

## 11. Deliverables and delivery workflow
- Deliverables to EEA Central Data Repository (CDR):
  - CLC-Changes 2000-2006 (CHA06)
  - Revised CLC2000 (CLC00) where applicable
  - CLC2006 (CLC06)
  - Working unit level metadata (MWU_xx_nn)
  - Country level metadata for CLC-Changes (MCOCH_xx) and CLC2006 (MCO06_xx)
- File naming conventions and formats:
  - Default format: ESRI Arc/INFO Export Interchange File (E00); optional MDB (Esri Personal Geodatabase)
  - File naming pattern: CHA06_xx.e00, CLC06_xx.e00, CLC00_xx.e00, with two-letter ISO country codes
- Coordinate reference system: national projections aligned with IMAGE2006; if confidential, use European CRS
- Delivery flow: upload to CDR envelopes, automated notifications, and acceptance checks; iterative improvements if needed

## 12. Technical specifications and quality checks
- Data formats and topology: E00 (default) or MDB; strict topology rules (no gaps, no dangles, closed polygons, unique codes, no overlapping or adjacent same-code polygons).
- MMU and mapping: CHA06 (5 ha) for changes; CLC06 and CLC00 (25 ha) for status layers.
- Metadata and attribute conventions: strict field definitions, unique IDs, two CLC codes per change polygon, correct area calculations, and cross-dataset compatibility.
- Quality check reports: Database Technical Acceptance (DBTA) reports documenting formal, mapping, topology, and metadata checks, plus a summary of acceptance or required improvements.

## 13. Annexes and references
- Annexes include approaches for updating CLC data, LUCAS nomenclature, priority tables for generalisation, and contact information.
- Annex 3 outlines two update approaches (update-first vs change-mapping-first) with rationale for adopting the change-mapping-first approach in CLC2006.
- Annexes provide detailed LUCAS nomenclature mappings (Annexes 4 and 5), generalisation priority (Annex 6), and contacts (Annex 7).