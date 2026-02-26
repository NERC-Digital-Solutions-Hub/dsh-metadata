CLC2006 technical guidelines

## Overview
- Technical guidelines for updating Corine land cover data for the reference year 2006 (CLC2006).
- Objective: produce a 2006 land cover map by integrating CLC2000 with land cover changes (CLC-Changes) identified between 2000 and 2006 using IMAGE2006 data.
- Managed by Eionet NRCs for spatial analysis and land cover, with ETC/LUSI coordination; part of the GMES Fast Track Service Precursor (FTSP) – Land Monitoring.

## Aim and context
- Provide timely, quality-assured, European-scale information on land cover to support environmental monitoring and policy assessment (2006-2008 timeline).
- CLC2006 focuses on real land cover changes between 2000 and 2006, and on updating the CLC2000 base map.
- CLC2006 is a component of GMES FTSP Land Monitoring; complements other core GMES land monitoring components.
- Previous CLC2000 improvements remain valid; revisions to CLC2000 are not released as new products, but may be used for CLC-Changes and CLC2006 production.

## Key parameters and nomenclature
- Scale: 1:100,000; Minimum Mapping Unit (MMU) for CLC: 25 ha; minimum width for lines: 100 m.
- 44 land cover classes organized in a three-level hierarchy; five Level-1 categories: artificial surfaces, agricultural areas, forests and semi-natural areas, wetlands, and water bodies.
- Mapping method: computer-assisted visual interpretation of satellite imagery; CLC2000 used ortho-corrected Landsat-7 ETM data; CLC2006 uses multi-temporal imagery (SPOT-4 and/or IRS LISS III) from IMAGE2006, with two dates per area to improve interpretation.
- Accuracy and quality expectations updated over time; the 2006 Addendum and nomenclature guide provide refined definitions.

## Data sources and imagery (IMAGE2006)
- Two-date imagery (SPOT-4 and/or IRS P6) for each area to enable multi-temporal interpretation; no panchromatic band expected.
- Band combinations recommended to align display with interpreters’ experience (R: band 3 for Landsat-like, G: band 4, B: band 2, etc.; specifics in the guidelines).
- IMAGE2006 supports two dates within the 2006 +/- 1 year window to enable detection of changes; if changes occur between the two dates, the most recent image is used as reference.

## Land Cover Changes (LCC) and CLC-Changes database
- Main novelty in CLC2000 was creation of CLC-Changes (LCC database with MMU 5 ha).
- For CLC2006, all changes > 5 ha must be mapped, regardless of their position (connected or island-like); larger than 5 ha and detectable on satellite imagery.
- CLC-Changes is produced directly via computer-assisted visual interpretation; used to derive CLC2006 by combining with CLC2000.
- Two data flows for updating:
  - CLC2006 = CLC2000 rev + CLC-Changes (intersections and code updates)
  - or, the preferred approach for CLC2006: CLC2006 = CLC2000 (+) CLC-Changes (change mapping first approach)
- For CLC2006, two problems are mitigated:
  - Edge-matching and border consistency via edge-matched CLC2000 as a basis; border 2 km strip similarity analyses
  - Reduced propagation of errors by addressing real change processes rather than solely polygon differences
- Change types and typology (eight types) guide interpretation, including simple changes, new polygons, disappearing polygons, technical changes, and complex cases. Technical changes (T) may be used for algorithmic gating to avoid errors when MMU differences would otherwise cause gaps; these are not real land cover changes and are removed from final CLC-Changes, but may be used to build CLC2006.
- Changes in heterogeneous/landscape-level classes (e.g., mosaics in 242, 243, 313) may be mapped at landscape level if whole landscape character shifts.

## Participating countries and governance
- 38 GMES FTSP Land Monitoring participating countries (EEA member states + collaborators); strong coordination through EEA, ESA, JRC, and national RCs.
- National Reference Centres (NRCs) responsible for national implementation plans; data integration centralized by EEA with ETC-LUSI support.
- A Steering Committee and the GMES LMCS Implementation Group oversee cross-service integration.

## Ancillary data and LUCAS
- Ancillary data: topographic maps, orthophotos, and other medium/high-resolution imagery to support interpretation.
- LUCAS data (land use/cover area frame survey) provide ground-truth and photo-interpretation support:
  - LUCAS 2001/2002 and LUCAS 2006 available to national teams.
  - LUCAS LC/LULC nomenclatures included in Annexes 4 and 5; ground-truth photos help confirm classifications and changes.

## Production of the CLC2006 database
- The update uses a “change mapping first” approach:
  - Interpret LCCs > 5 ha and map changes directly; correct thematic and geometric errors in CLC2000 as needed (CLC2000 rev).
  - Produce CLC-Changes; then derive CLC2006 by combining CLC2000 rev and CLC-Changes.
- For changes > 25 ha, integration of CLC2000 and CLC-Changes is straightforward. For changes < 25 ha, generalisation and amalgamation rules are applied (Annex 6).
- Two levels of processing:
  - Computerised processing: integration of >25 ha changes; generalisation of small changes; amalgamation logic.
  - Non-automated processing: human decisions for close cases (under 25 ha) and ambiguous generalisations.
- Outputs remain three largely independent datasets for analysis: CLC2000 rev, CLC-Changes, and CLC2006.

## Metadata and verification
- Metadata is produced at two levels:
  - Working unit level metadata (Annex 1) for CLC-Changes processes.
  - Country level metadata (Annex 2) for CLC-Changes, CLC2006, and revised CLC2000 if applicable.
- Metadata standards: EEA-MSGI (ISO19115-based) with an accompanying EEA Metadata Editor; national metadata templates provided.
- Verification and quality assurance:
  - ETC-LUSI CLC Technical Team verifies CLC2000 and CLC-Changes; two verification missions per country (2nd and 4th quarters).
  - InterCheck software used; detailed verification tables (Table 9) cover topological, thematic, and metadata checks.
- Technical Quality Check Report (DBTA) documents acceptance status or improvement needs; two primary deliverables: CLC-Changes (2000-2006), revised CLC2000, and CLC2006, plus metadata sheets.

## Deliverables and data delivery
- Deliverables to be submitted to the EEA Central Data Repository (CDR):
  - CHA06_xx (CLC-Changes 2000-2006)
  - CLC06_xx (CLC2006)
  - CLC00_xx (revised CLC2000) for countries not producing CLC2006 themselves
  - Working unit metadata (MWU_xx_nn)
  - Country-level metadata (MCOCH_xx for CHA06; MCO06_xx for CLC06)
- File formats:
  - Default: ESRI Arc/INFO Export Interchange File (E00) with no compression; optional: ESRI Personal Geodatabase (MDB)
  - E00 supports topology; MDB offers modern relational structure with topology
- File naming conventions:
  - CHA06_xx.e00 (CLC change layer for 2000-2006)
  - CLC06_xx.e00 (CLC status layer for 2006)
  - CLC00_xx.e00 (revised CLC2000)
  - Versioning via two-letter country ISO code (xx) and version numbers
- Attributes and metadata schema:
  - Each CHANGEs polygon has 2000/2006 codes; CLC2006 polygons have 3-letter CLC codes
  - Change type indicator (Chtype) to distinguish real vs. technical vs. other changes
  - Area fields, IDs, and other attributes as defined in Tables 13, 14
- Coordinate reference system:
  - National projections used for IMAGE2006; where needed, European CRS may be used; national CRS parameters must be provided to TT

## Delivery and workflow logistics
- Delivery schedule aligned with national CLC2006 project plans; deviations communicated to ETC-LUSI TT
- Data delivery follows a defined envelope process via the CDR; notifications sent to key stakeholders
- Pre-delivery quality control (QA/QC) support provided by TT; delivery envelope management, release, and final acceptance steps outlined

## Verification and quality metrics
- Topology and geometry checks: no dangles, no gaps, polygons closed, single label per polygon, no overlapping polygons, no artificial boundaries, cross-layer consistency
- Geometric accuracy: alignment with input imagery; linear features at least 100 m wide
- Thematic accuracy: adherence to CLC nomenclature and updated addenda
- Metadata completeness and conformance to EEA-MSGI

## Ancillary information and references
- Annexes provide detailed approaches for updating data, LUCAS nomenclature, and generalisation rules (Annexes 3–6)
- Annex 7 provides contact points for the CLC2006 project management and technical teams
- Key references include the original CLC technical guides, addenda, and GMES documentation

## Practical implications for Analysts Monitoring the Environment
- CLC2006 delivers a harmonised, Europe-wide view of land cover and land cover change between 2000 and 2006, enabling temporal comparisons and policy assessment.
- The change-first approach emphasizes real change processes and improves the value of datasets by producing a high-resolution CLC-Changes layer and a coherent CLC2006 map.
- Data are produced with standardized formats, robust metadata, and rigorous verification, while allowing national teams to manage integration and documentation.
- The methodology supports linking CLC data with other environmental datasets and ancillary information, facilitating broader analyses of environmental health, land use dynamics, and policy performance over time.