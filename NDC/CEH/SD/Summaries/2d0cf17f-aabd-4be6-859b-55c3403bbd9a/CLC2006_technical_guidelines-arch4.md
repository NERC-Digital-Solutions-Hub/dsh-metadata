# CLC2006 technical guidelines

- Purpose: Guidelines for updating Corine land cover data for 2006 by integrating the CLC2000 map with land cover changes (2000-2006) derived from IMAGE2006 imagery, produced under GMES Fast Track Service Precursor (FTSP) Land Monitoring.
- Scope and beneficiaries: Aimed at national teams, EEA, ETC LUSI, ESA, JRC, and NRCs; focuses on practical production guidance, metadata, and delivery to the European database.

## Key context and frame

- Transition from CLC1990 to CLC2000 and then to CLC2006
  - CLC2006 continues from CLC2000, with a new emphasis on mapping land cover changes (2000-2006) using IMAGE2006 data.
  - IMAGE2006 provides multitemporal SPOT-4 and IRS P6 imagery to support photo-interpretation.
- GMES fast-track framing
  - CLC2006 is part of the GMES Land Monitoring Fast Track Service Precursor; partners include EEA, NRCs, ETC-LUSI, ESA, JRC.
  - Differences from CLC2000: reduced need to revise CLC2000 data; primary focus on changes; all changes >5 ha to be mapped; change mapping now more directly tied to real processes.

## Technical parameters and nomenclature

- Scale and accuracy
  - Map scale: 1:100,000
  - Minimum Mapping Unit (MMU): 25 hectares for CLC2000/CLC2006; 5 ha MMU for CLC-Changes
  - Minimum width for linear elements: 100 meters
- Classes
  - 44 land cover classes organized in a three-level hierarchy; five level-one groups: artificial surfaces, agricultural areas, forests and semi-natural areas, wetlands, water bodies
- Mapping methodology
  - Computer assisted photo interpretation; ortho-corrected imagery (IMAGE2006); high geometric accuracy (≤25 m) using SPOT-4 and IRS data
  - Two dates per area (two IMAGE2006 dates) to support change detection
- CLC-Changes
  - New database focusing on real changes >5 ha, ≤100 m width; intended to capture “island” changes and avoid false changes
  - Change polygons are delineated directly in image space and linked with 2000 and 2006 codes to reflect real processes
- Comparability
  - CLC-Changes 1990-2000 and 2000-2006 are not directly comparable due to different MMUs and methodologies; comparisons are meaningful mainly for changes >25 ha

## Project organization and delivery framework

- Work packages
  - Seven work packages (WP 1.1–WP 7) with roles assigned to NRCs, EEA, ESA, JRC, and data providers; national plans required
- Project governance
  - Steering Committee with reps from Commission, ESA, EEA, and participating countries
  - GMES LMCS Implementation Group provides advisory linkage to other GMES services

## IMAGE2006 basics

- Data sources
  - SPOT-4 HRVIR and IRS P6 LISS III provide multitemporal data for mapping
- Imagery characteristics
  - Comparable spectral coverage to Landsat but with distinct sensor characteristics; two dates per area with no panchromatic band
- Photo-interpretation guidance
  - Recommended color composites to align with interpreters’ experience; two images per area to enhance interpretation; date-coded file naming recommended to show sequence and season

## Mapping land cover changes (CLC-Changes)

- Updating approach
  - Changes are interpreted directly from IMAGE2000/IMAGE2006 in a dual-window setup; CLC2000 polygons serve as the basis for delineating changes
  - Two-code system for each change polygon: status in 2000 and 2006
  - Technical changes (T) may be used to resolve MMU gaps (<25 ha) but are removed from final CLC-Changes
- Source data and working units
  - Use edge-matched CLC2000 as baseline; border regions aligned to ensure seamless European coverage
  - Working units are defined by national workflows; similarity with edge-matched borders validated
- Change typology and landscape-level mapping
  - Eight change types (A–H) based on presence/absence in CLC2000, CLC-Changes, and CLC2006; examples include Simple Change, New Polygon, Change Only, and Landscape-level changes
  - For heterogeneous landscapes (e.g., mosaics with 243, 242, 313 classes), changes may be mapped at landscape level when the overall character shifts

## Ancillary data and ground-truth support

- Proposed ancillary data
  - Topographic maps (1:50,000) and orthophotos; additional high-/medium-resolution imagery to support interpretation
- LUCAS data
  - Ground truth data for photo-interpretation from LUCAS 2001/2002 and 2006; available to national teams for improved CLC2000 interpretation and change delineation
  - LUCAS provides land use and land cover codes plus field photographs to support interpretation and validation

## Production of the CLC2006 database

- Integration approach
  - Change mapping first: produce CLC-Changess 2000-2006 and then derive CLC2006
  - CLC2006 = CLC2000 rev + CLC-Changes, with different handling for >25 ha vs <25 ha changes
- Automatic and manual components
  - Semi-automatic processing for integration and generalisation; photointerpreter decisions required for under-25 ha changes and ambiguous cases
- Data model and generalisation
  - Generalisation rules (amalgamation or neighbour transfer) guided by a priority table; exact mathematical relationships among CLC2000, CLC-Changes, and CLC2006 may not hold in all cases
- Outputs and interoperability
  - CLC2006, CHA06 (CLC-Changes 2000-2006), and revised CLC2000 are treated as nearly independent data sets for many applications

## Metadata and verification

- Metadata
  - Two levels: Working unit metadata (Annex 1) and Country-level metadata (Annex 2); aligned with EEA-MSGI metadata standard (ISO19115-based) and INSPIRE guidance
  - Metadata delivered via standard editors (EEA Metadata Editor) or forms; includes documentation of data provenance, processing steps, and CRS
- Verification and quality assurance
  - ETC-LUSI technical team verifies CLC2000 rev and CLC-Changes; two verification missions per country; use of InterCheck software
  - Verification checks cover topology, codes, MMU adherence, metadata completeness, and cross-layer consistency
  - A DBTA (Database Technical Acceptance) report summarizes checks and indicates acceptance or need for improvement

## Deliverables and data delivery

- Deliverables
  - CHA06: CLC-Changes 2000-2006
  - CLC00: revised CLC2000 (for countries not producing CLC2006 themselves)
  - CLC06: CLC2006 database
  - Working unit metadata (MWU_xx_nn); country-level metadata for CHA06 and CLC2006
- Delivery process
  - Deliveries to EEA via the Central Data Repository (CDR); use delivery envelopes and versioning (e.g., CHA06_xx, CLC06_xx, CLC00_xx)
  - Notifications via CDR; revised data can be requested for improvement
  - Helpdesk support available for delivery issues
- Technical specifications
  - File formats: default ESRI Arc/INFO E00 (Arc coverage); optional MDB geodatabase
  - File naming: eight-character country code; versioned envelopes labeled CHA06_xx, CLC06_xx, CLC00_xx
  - Attributes: include feature IDs, codes for 2000/2006, Change codes, CHTYPE (real vs technical change), area, and metadata fields
  - Coordinate reference system: national projection used for IMAGE2006; report any national CRS changes
  - MMU and topology: MMU 5 ha for CHA06, 25 ha for CLC06/CLC00; robust topology checks; no gaps, no dangles, consistent coding
- Quality and metadata acceptance
  - Detailed quality checks and acceptance criteria documented; non-conforming deliveries trigger improvement cycles

## Deliverables and reference materials

- Annexes and references
  - Annexes cover updating approaches (Annex 3), LUCAS nomenclature (Annexes 4–5), priority generalisation table (Annex 6), and contacts (Annex 7)
- Contacts
  - CLC2006 TT coordinator, project manager, and technical acceptance contacts provided for coordination and support

## References and context

- Key sources include EEA technical reports on Corine land cover, LUCAS, and GMES Fast Track Service documentation; ongoing emphasis on harmonization, metadata standards, and cross-border data consistency
- Overall objective: enable timely, quality-assured, and comparable European land cover data for policy, reporting, and environmental assessment through rigorous change mapping, standardized metadata, and robust delivery mechanisms