# CLC2006 technical guidelines

- Purpose: Provide guidelines for updating Corine land cover data for 2006 (CLC2006) by integrating the 2000 baseline (CLC2000) with a new Land Cover Changes database (CLC-Changes) derived from IMAGE2006 imagery.
- Context: Part of the GMES Fast Track Service Precursor (FTSP) for Land Monitoring. National Reference Centres (NRCs) coordinate production; ETC/LUSI supports data integration and metadata.

## Data architecture and key parameters

- Data model and scale
  - Map scale: 1:100,000; Minimum Mapping Unit (MMU): 25 hectares for CLC datasets; 5 ha MMU for CLC-Changes (policy requirement to capture real changes).
  - 44 land cover classes in a three-level hierarchy; five level-1 categories: artificial surfaces, agricultural areas, forests and semi-natural areas, wetlands, and water bodies.
  - Methodology: computer-assisted photo interpretation; imagery sources include ortho-corrected SPOT, IRS, and Landsat history; emphasis on improving geometric and thematic accuracy.
- Change-focused approach
  - CLC-Changes database captures real land-cover changes between 2000 and 2006 (MMU 5 ha; minimum 100 m boundary displacement).
  - All changes > 5 ha must be mapped, including isolated changes not tied to existing polygons.
  - Change delineation is performed directly (not solely by overlaying two databases), with two dates per change polygon (code 2000 and code 2006) representing the change process.
  - Technical changes (T): auxiliary polygons used to avoid >5 ha and <25 ha errors; later removed from the final CLC-Changes product.
  - Landscape/heterogeneous classes (e.g., 242, 243, 313) can be mapped at landscape level when changes affect overall landscape character.
- Data sources and coverage
  - 38 participating countries; national teams (NRCs) coordinate national-level data collection and interpretation; border areas are edge-matched for Europe-wide consistency.
  - Ancillary data and ground-truth elements (e.g., LUCAS data) support interpretation and validation.

## Data production and workflow

- IMAGE2006 imagery
  - Multi-temporal two-date coverage to enable robust photointerpretation.
  - Primary sensors: SPOT-4 HRVIR and IRS P6 LISS III (two dates, +/-1 year window).
  - Color composites and band choices recommended to optimize interpretation; two dates per area to detect changes.
- Change mapping workflow
  - The update uses a "change first" approach: interpret CLC-Changes (2000-2006) and then integrate with CLC2000 rev to form CLC2006.
  - For changes > 25 ha, integration is largely automatic; for changes < 25 ha, generalisation or amalgamation is applied (guided by a priority table).
  - Change polygons reference CLC2000 boundaries to minimize sliver creation; interpreter assigns two codes per change polygon (2000 and 2006) describing the real process.
  - Photointerpretation uses ancillary data (topographic maps, orthophotos) and LUCAS as ground truth where available.
- Ancillary data and ground-truth
  - Proposed ancillary data include topographic maps, orthophotos, and additional high-resolution imagery.
  - LUCAS data (land use/land cover and photographs) support photo-interpretation for various countries, improving interpretation quality and providing ground-truth context.

## Metadata, verification, and quality assurance

- Metadata
  - Two levels: working unit level metadata (Annex 1) for CLC-Changes and country-level metadata (Annex 2) for each delivered dataset.
  - Metadata standards: EU/EEA guidelines (EEA-MSGI, a profile of ISO 19115; INSPIRE alignment). Tools available include the EEA Metadata Editor and metadata templates.
- Verification and quality assurance
  - ETC-LUSI CLC Technical Team verifies CLC2000 rev and CLC-Changes; two verification missions per country (2nd and 4th quarters of production).
  - Verification uses InterCheck software; checks cover topological consistency, coding validity, geometry accuracy, and metadata completeness.
  - Deliverables include a Database Technical Acceptance (DBTA) report detailing checks, corrections, and acceptance status.
- Deliverables and delivery process
  - Deliverables: CHA06 (CLC-Changes 2000-2006), CLC00 (revised 2000), CLC06 (CLC2006), working-unit metadata (MWU_xx_nn), country metadata for CLC-Changes and CLC2006.
  - Delivery via the EEA Central Data Repository (CDR) with standardized ZIP envelopes and file naming (CHA06_xx.e00, CLC06_xx.e00, CLC00_xx.e00; MDB option available for geodatabases).
  - File naming uses ISO country codes; guidance on metadata formats and structure is provided.
  - A formal acceptance process determines if data are accepted or require improvements; multiple iterative deliveries may occur until acceptance.
- Data integration and relationships
  - CLC2006 = CLC2000 rev + CLC-Changes for changes > 25 ha; for smaller changes, integration relies on generalisation and amalgamation rules.
  - The exact mathematical relationship among CLC2000, CLC-Changes, and CLC2006 is not strictly fixed due to MMU differences; datasets should be used as nearly independent but harmonized products.

## Technical specifications and data quality

- Data formats and topology
  - Default delivery: ESRI Arc/INFO Export Interchange File (E00) with no compression; optional ESRI Personal Geodatabase (MDB).
  - Topology and coding requirements: valid CLC codes, 25 ha changes for CLC2000; 5 ha changes for CHA06; linear features must be at least 100 m wide; no gaps or artificial boundaries; seamless, edge-matched national datasets.
  - Coordinate reference systems: national projections consistent with IMAGE2006; national CRS metadata must be provided to ensure proper European integration.
- Attribute and dataset structure
  - Detailed attribute definitions and naming conventions are specified for CHA06, CLC06, and CLC00 datasets (e.g., code fields for 2000/2006 statuses, area, change type, and metadata references).
  - Additional annexes provide LUCAS nomenclatures for land use/cover and guidance on generalisation priorities.
- Delivery quality checks
  - Formal specifications, mapping specifications (MMU and coding), topology checks, and metadata completeness are audited in a structured format (DBTA and checklists).

## Governance, collaboration, and program context

- Governance and partnerships
  - Steering Committee with representatives from the European Commission, ESA, EEA, and participating countries; GMES LMCS Implementation Group provides advisory input.
  - Roles distributed across NRCs, ETC-LUSI, JRC, and national data providers; annual updates and cross-border coordination are emphasized.
- Program context and objectives
  - CLC2006 aims to deliver timely, quality-assured land-cover data to policy makers; aligns with GMES core products for environmental monitoring and assessment.
  - Distinct from CLC2000, CLC2006 emphasizes accurate, high-resolution change detection and cross-border consistency, supporting indicators and policy analysis.

## Practical implications for Data Leaders

- Strategic data workflow
  - Maintain a change-first, multi-database update cycle with explicit governance for data quality and cross-border harmonization.
  - Leverage ancillary data and LUCAS to improve change interpretation and metadata fidelity.
- Data governance and quality
  - Implement standardized metadata (EEA-MSGI), formal verification steps, and robust topological checks to ensure data integrity and interoperability.
  - Manage versioning, delivery envelopes, and acceptance processes via the Central Data Repository with clear responsibilities and escalation paths.
- Data sharing and standards
  - Adhere to common data formats (E00 as default; MDB option), consistent naming conventions, MMU thresholds, and landscape-level mapping when appropriate.
  - Ensure transparent documentation of methodologies, change typologies, and generalisation rules to facilitate comparability across countries and over time.
- Operational considerations
  - Coordinate with NRCs and ETC-LUSI for data integration and European seamless database construction; plan for iterative improvements based on verification feedback.
  - Anticipate the need for bilingual or multi-format metadata reviews and training for local photointerpreters to maintain consistency.

- Deliverables overview (for reference)
  - CHA06 (CLC-Changes 2000-2006), CLC06 (CLC2006), CLC00 (revised CLC2000, if applicable), working-unit metadata, country-level metadata, and technical quality acceptance reports; all delivered to the EEA CDR with appropriate documentation and versioning.