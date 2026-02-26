# CLC2006 technical guidelines

- Purpose: Provide guidelines for updating Corine land cover data for 2006 (CLC2006) by integrating the land cover map from 2000 (CLC2000) with land cover changes between 2000 and 2006 (CLC-Changes), produced from IMAGE2006 data.

- Context: Part of GMES Fast Track Service Precursor (FTSP) Land Monitoring; coordinated by EEA with national NRCs and the ETC-LUSI; data sharing and integration supported through Eionet and the CDR.

- Scope of outputs: 
  - CLC2006 database (land cover in 2006)
  - CLC-Changes database (land cover changes 2000-2006, MMU 5 ha)
  - Revised CLC2000 (where applicable) used for generating CLC-Changes and CLC2006
  - Metadata at working unit and country levels

- Key differences from earlier CLC projects:
  - Focus shifted to capturing real changes between 2000 and 2006; not an extensive improvement of CLC2000.
  - All changes larger than 5 ha must be mapped; changes smaller than 5 ha generally not delineated unless part of a complex change.
  - Change mapping is largely direct interpretation from IMAGE2000 vs IMAGE2006; aims for higher accuracy and realism.
  - CLC2006 is produced mostly automatically (with human oversight) by combining CLC2000 and CLC-Changes.

- Data and inputs:
  - IMAGE2006: multi-temporal satellite data (two dates) from SPOT-4 and IRS P6 (LISS III) to enable refined photo-interpretation.
  - IMAGE2000: used as the baseline for CLC2006.
  - Ancillary data: topographic maps, orthophotos, LUCAS data (ground truth for photointerpretation).

- LUCAS data:
  - Ground-truth land use/land cover codes and photographs; supports improvement of CLC2000 and delineation of changes.
  - LUCAS 2001/2002 and 2006 availability varies by country.

- Nomenclature and parameters:
  - Scale: 1:100,000; MMU for CLC: 25 ha; minimum width for linear elements: 100 m.
  - CLC uses 44 classes organized in a three-level hierarchy; five level-1 categories.
  - CLC-Changes MMU: 5 ha; two-date change polygons carry codes for 2000 and 2006.
  - For heterogeneous landscape classes (e.g., 242, 243, 313), landscape-level changes may be mapped when warranted.

- Change concept and typology:
  - CLC-Changes database contains change polygons > 5 ha (real changes), including “technical changes” to resolve MMU inconsistencies between databases.
  - Change types are categorized (A–H) based on existence and size in CLC2000, CLC-Changes, and CLC2006; examples include Simple change, New polygon, Disappearing polygon, Change only, and Technical change.
  - Technical change polygons are auxiliary, used to allow correct creation of CLC2006 polygons and are removed from final CLC-Changes.

- Change delineation methodology:
  - Updating approach: CLC2006 = CLC2000 rev + CLC-Changes (or alternative update-first approaches). CLC2006 is produced using change mapping first to capture actual processes.
  - Change polygons are delineated directly from IMAGE2000 vs IMAGE2006 in a dual-window setup; each change polygon is labelled with 2000 and 2006 codes.
  - Changes must be visualized against CLC2000 boundaries to avoid slivers; use of ground-truth data (LUCAS) and ancillary data recommended.

- Data integration and generalisation:
  - Because MMUs differ (25 ha for CLC, 5 ha for CLC-Changes), automated combination is not perfect; generalisation (amalgamation or neighbour-based) is applied per Annex 6 guidance.
  - Some cases require non-automatic, photointerpreter-driven decisions (under 25 ha changes, or ambiguous situations).
  - The three databases (CLC2000 rev, CLC-Changes, CLC2006) cannot be perfectly reconciled with a single mathematical formula; they are treated as nearly independent.

- Ancillary data and landscape considerations:
  - Proposed ancillary data types to support interpretation (topographic maps, orthophotos, and additional high/medium resolution imagery).
  - Annex 4/5 LUCAS nomenclatures provide ground-truth references for photointerpretation.

- Metadata and documentation:
  - Two levels of metadata: Working unit level metadata (MWU) and Country level metadata (MCOCH, MCO06); aligned with EEA-MSGI/ISO19115 standards.
  - Metadata delivery supported via EEA metadata editor or an XML form; detailed templates provided in Annexes.
  - Metadata accompany data deliveries and are checked during technical quality checks.

- Verification and quality assurance:
  - ETC-LUSI CLC Technical Team verifies CLC2000 rev and CLC-Changes; two verification missions per country (2nd and 4th quarters), with InterCheck software support.
  - Quality checks cover formal specification, mapping and topology, metadata, and cross-layer consistency.
  - Technical Acceptance (DBTA) reports summarize data and metadata checks; used to accept data or request improvements.

- Deliverables and delivery process:
  - Deliverables to EEA Central Data Repository (CDR): CHA06 (CLC-Changes 2000-2006), CLC00 (revised CLC2000), CLC06 (CLC2006), plus MWU_xx_nn, MCOCH_xx, MCO06_xx metadata.
  - File formats: default ESRI Arc/INFO E00 (Arc/Info export interchange) with optional MDB (ESRI Personal Geodatabase).
  - File naming conventions: CHA06_xx.e00, CLC06_xx.e00, CLC00_xx.e00; country codes from ISO 3166-1 alpha-2 (xx).
  - Coordinate reference system: national projection; national CRS updates to TT with description in country metadata.
  - Topology requirements: no gaps, no dangling boundaries, closed polygons, single label per polygon, no overlapping or adjacent polygons with same codes; no artificial map boundaries; 1 km sea buffer recommended to ensure seamless European coverage.
  - MMU: CHA06 5 ha, CLC06 25 ha, CLC00 25 ha.
  - Delivery workflow: national teams upload to CDR, TT verifies, and final acceptance/rejection communicated; iterative corrections allowed; pre-delivery QA support available.

- Delivery schedule and responsibilities:
  - Delivery follows national project proposals; schedule coordinated with ETC-LUSI; two verification missions planned.
  - National teams or ETC-LUSI may perform CLC2006 integration; script support available to assist data integration.

- Access and distribution:
  - Data in CDR not intended for public dissemination; CDR provides controlled access; unified notification service informs relevant stakeholders upon delivery and acceptance.

- Annexes and references:
  - Annexes include metadata templates, LUCAS nomenclatures, change typology explanations, and generalisation priorities.
  - Key references and contacts provided for technical guidance and support.

- Summary for data support practitioners:
  - CLC2006 builds on CLC2000 by explicitly mapping real land cover changes that occurred between 2000 and 2006, using IMAGE2006 and ancillary data.
  - Produces two main data products: CLC2006 (land cover map for 2006) and CLC-Changes (mmu 5 ha; changes > 5 ha mapped).
  - Requires careful data governance, standardized metadata, and rigorous QA/verification; data delivery is formalized through the CDR with strict file naming, formats, and topology requirements.
  - Ancillary data and LUCAS provide essential support for accurate interpretation and change detection.
  - The process emphasizes transparency of change processes, landscape-level considerations for heterogeneous classes, and robust documentation to enable European-scale integration and reuse.