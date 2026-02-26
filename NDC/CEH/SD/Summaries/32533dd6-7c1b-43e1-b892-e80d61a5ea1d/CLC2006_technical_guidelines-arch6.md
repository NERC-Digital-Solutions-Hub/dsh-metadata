# CLC2006 technical guidelines

- Overview and purpose
  - Guidelines for updating Corine land cover data for 2006 (CLC2006) by integrating the CLC2000 map with land cover changes between 2000 and 2006 (IMAGE2006).
  - Produced and managed by Eionet National Reference Centres (NRCs) for spatial analysis and land cover, with data integration coordinated by EEA and ETC LUSI, under GMES Fast Track Service Precursor (FTSP) Land Monitoring.
  - Readers are primarily national CLC teams and allied organisations; aims to support practical production and European data harmonisation.

- Key technical parameters and structure
  - Scale: 1:100,000; Minimum Mapping Unit (MMU): 25 ha; minimum width of linear elements: 100 m.
  - Nomenclature: 44 land cover classes, in a three-level hierarchy; five level-1 categories: artificial surfaces, agricultural areas, forests & semi-natural areas, wetlands, water bodies.
  - Mapping methodology: computer-assisted photo-interpretation of satellite imagery; ortho-corrected imagery (target RMS error ≤ 25 m for IMAGE2000/CLC2000 lineage; similar expectations for CLC2006).
  - Change database: CLC-Changes with MMU 5 ha, intended to capture real evolution processes between 2000 and 2006 (including changes not tied to existing polygons).
  - New focus for CLC2006: heavy emphasis on land cover change data (2000-2006); aims to map all changes > 5 ha; improves over previous approaches that relied on simple intersections of older databases.

- Data sources and imagery
  - IMAGE2006 uses SPOT-4 and IRS P6 (LISS III) imagery, providing two dates per area for robust photo-interpretation.
  - Two dates per area help separate land-cover changes (e.g., irrigation, development) from seasonal or transient effects.
  - Image naming and band-combination guidance to support consistent photo-interpretation; multi-temporal imagery favored for difficult separations.

- Change mapping approach and typology
  - Change mapping first: interpreters delineate real changes >5 ha directly, then integrate with CLC2000 to form CLC2006.
  - All changes > 5 ha must be delineated, regardless of whether they touch existing polygons; includes island-like changes.
  - Interchange between CLC methods: updated CLC2000, CLC-Changes, and CLC2006 are not a single automatic pipeline; some human interpretation remains required.
  - Change typology (eight types A–H) guides interpretation when combining three data layers: revised CLC2000, CLC-Changes, and CLC2006.
  - Technical changes (T) may be used to avoid processing gaps, but are not real land-cover changes; they are documented and later removed from the final CLC-Changes product.
  - Landscape-level and heterogeneous-class considerations: some landscape-level changes may require representing changes at the landscape level (e.g., 243 to 211) rather than mapping many small patches individually.

- Ancillary data and ground truth
  - Proposed ancillary data: topographic maps (≥1:50k), orthophotos, and additional high-resolution imagery to support interpretation.
  - LUCAS data (ground-truth land use/cover codes and field photos) are available to support photo-interpretation and ground truth, aiding change delineation and validation (Annexes 4–5).

- Data model and integration
  - Three interrelated databases:
    - CLC2000 rev (revised CLC2000)
    - CLC-Changes (new change polygons; MMU 5 ha)
    - CLC2006 (final updated map; MMU 25 ha)
  - Integration rule:
    - For changes > 25 ha: straightforward automatic integration: CLC2006 = CLC2000_rev + CLC-Changes.
    - For changes < 25 ha: require generalisation and potential manual decisions to ensure consistency; exact mathematical relation among databases is not strictly fulfilled.
  - Annexed generalisation rules (Annex 6) guide how to amalgamate small changes and resolve borderline cases.

- Governance, work packages and organisation
  - Seven GMES FTSP Land Monitoring work packages (WP) with national and European-level coordination.
  - NRCs organise national implementation; a Steering Committee and an LMCS Implementation Group provide governance and inter-service linkages.
  - ETC-LUSI provides technical support and, if needed, ArcInfo scripting assistance for data integration.

- Metadata and documentation
  - Two levels of metadata: working unit level (Annex 1) and country level (Annex 2), aligned with EEA-MSGI/ISO19115 metadata standards and INspire recommendations.
  - Metadata delivered via formal templates; national teams prepare country metadata for CLC-Changes, CLC2006, and revised CLC2000 datasets.
  - Metadata editing tools include the EEA Metadata Editor for ArcGIS environments.

- Verification and quality assurance
  - ETC-LUSI Technical Team verifies CLC2000 and CLC-Changes; two verification missions per country (2nd and 4th quarters) to ensure harmonised European results.
  - Verification uses InterCheck software and standardized checklists for topology, codes, and metadata (Tables 9, 16–18).
  - Emphasis on topological consistency, absence of gaps, correct coding, correct polygon closures, and cross-layer consistency.

- Deliverables and delivery process
  - Deliverables to the European Central Data Repository (CDR) include:
    - CHA06: Corine land cover change 2000-2006
    - CLC00: revised CLC2000 (where applicable)
    - CLC06: CLC2006
    - Working unit metadata (MWU_xx_nn)
    - Country metadata for CLC-Changes (MCOCH_xx) and CLC2006 (MCO06_xx)
  - File formats and naming:
    - Default: ESRI Arc/INFO Export Interchange File (E00) with no compression
    - Optional: ESRI Personal Geodatabase (MDB)
    - File naming follows country codes (CHA06_xx.e00, CLC06_xx.e00, CLC00_xx.e00)
  - Coordinate reference: national projections used for IMAGE2006; updates to country CRS should be reported.
  - Data quality checks are documented in a Database Technical Acceptance (DBTA) report; multiple iterations may occur if severe issues are found.
  - Data should be delivered in a seamless European dataset with 1-km buffer around borders to ensure consistency across countries.

- Metadata and data standards references
  - Documentation and annexes provide detailed attribute definitions, topological rules, and data quality criteria.
  - Annexes include LUCAS nomenclature (Annexes 4–5), updating approaches (Annex 3), and a priority table for generalising CLC classes (Annex 6).
  - Annex 7 lists key contacts for the CLC2006 team.

- Practical implications for data support
  - Enables a consistent, multi-country European land cover update by combining updated data, change detection, and rigorous metadata/QA processes.
  - Supports data exploration and reuse through standardized formats, detailed provenance, and accessibility via the EEA/CDR.
  - Provides a structured workflow to manage data quality, versioning, and integration challenges arising from dual MMUs and complex change scenarios.

- Reference and scope notes
  - Includes references to prior CLC iterations (CLC1990, CLC2000) and related addenda, as well as coordination with GMES and EC/JRC mechanisms.
  - Contains a built-in framework for ongoing improvement, validation, and harmonisation across Europe.