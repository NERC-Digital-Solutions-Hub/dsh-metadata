# CLC2006 technical guidelines

- A comprehensive guide for updating Corine land cover data for 2006 (CLC2006) by integrating 2000-era data with land cover changes (CLC-Changes) derived from IMAGE2006 imagery.
- Primary audience: national teams and organisations producing CLC updates; aims to enable consistent, timely, quality-assured data across Europe within the GMES Fast Track Service Precursor.

## Purpose, scope and readers
- Produce CLC2006 by combining CLC2000 with CLC-Changes (2000-2006).
- Use IMAGE2006 (two-date, satellite imagery) for change interpretation; NATIONAL REFERENCE CENTRES coordinate national work; ETC LUSI supports data integration.
- Document practical production steps, quality checks, and delivery to the European Environment Agency (EEA).

## Main technical parameters
- Scale: 1:100,000; MMU for standard CLC: 25 ha; minimum width of linear elements: 100 m.
- Nomenclature: 44 land cover classes, organized in a three-level hierarchy; five level-one categories (artificial, agricultural, forests/semi-natural, wetlands, water).
- Change database: CLC-Changes MMU: 5 ha; designed to capture real changes between 2000 and 2006, with large emphasis on mapping all changes >5 ha.
- Change interpretation is performed via direct photointerpretation using IMAGE2000/IMAGE2006 data, and then integrated with CLC2000 to form CLC2006.

## Change mapping and data structure
- CLC-Changes is a separate product from CLC2000/CLC2006, created by direct interpretation of changes between 2000 and 2006.
- Two MMUs differ (5 ha for CHANGEs vs 25 ha for CLC2000/CLC2006); results in a higher-resolution change dataset.
- CLC2006 = CLC2000 rev + CLC-Changes for changes > 25 ha; for smaller changes (<25 ha), generalisation and amalgamation are used (not a simple arithmetic merge).
- The 2006 workflow emphasizes “change mapping first” to capture real processes; this yields more accurate changes than simply intersecting revised inputs.
- For landscape-level heterogeneous classes (e.g., mosaic vegetation), changes may be mapped at landscape level if the overall character shifts significantly.

## Data sources and imagery
- IMAGE2006 provides multitemporal data (two dates) to improve photo-interpretation; SPOT-4 and IRS P6 sensors used (no panchromatic data planned as in 2000).
- Two images per area: intended to be not closer than 6 weeks apart; sequences and dates documented in filenames (e.g., IMAGE2006 dates).
- Color composites and band combinations recommended to align with interpreters’ expectations (NIR/SWIR emphasis).

## Ancillary data and ground truth
- Ancillary data to support interpretation: up-to-date topographic maps (1:50,000), orthophotos, and additional higher-resolution imagery.
- LUCAS data (land use/cover area frame survey) support photo-interpretation and ground-truth validation; LUCAS 2001/2002 data used for CLC2000 improvements; LUCAS 2006 supports change interpretation.

## Data production and project organization
- Seven work packages (WP) structure; national NRCs coordinate at-country work; EEA/ESA/JRC provide cross-border coordination and data integration.
- WP3 focused on CLC2006 mapping; other WPs cover data acquisition, ancillary data, validation, dissemination, and project management.
- Verification: two major verification missions per country; use of InterCheck software for quality assurance; feedback provided to national teams.

## Metadata, quality assurance, and formats
- Dual metadata levels: Working unit metadata (Annex 1) for data producers; Country-level metadata (Annex 2) for users; aligned with EEA-MSGI/ISO19115 standards.
- Topological and thematic quality checks: no gaps, no dangles, closed polygons, unique labels, no identical neighboring codes; cross-layer consistency between CLC2000, CLC2006, and CHA06.
- Deliverables require standardized formats (default: ESRI Arc/INFO E00 exchanges; MDB optional for geodatabase delivery); strict file naming conventions (CHA06_xx.e00 and CLC06_xx.e00; CLC00_xx.e00 for revised 2000 where applicable).
- Coordinate reference system: national projections (consistent with IMAGE2006); if national CRS is confidential, deliver in European CRS with documented notes.

## Deliverables, delivery, and workflow
- Deliverables include:
  - CHA06: Corine Land Cover Change 2000-2006
  - CLC06: CLC2006 status
  - CLC00: revised CLC2000 (if ETC-LUSI generates CLC2006 on behalf of a country)
  - Working unit metadata (MWU_xx_nn)
  - Country-level metadata for CLC-Changes (MCOCH_xx) and CLC2006 (MCO06_xx)
- Delivery to EEA Central Data Repository (CDR) via standardized envelopes; notifications trigger acceptance checks.
- Technical Acceptance Reports (DBTA) document formal specification conformance, mapping/topology checks, metadata completeness, and any required improvements.
- Data integration realities: CLC2006 and CHANGEs are treated as nearly independent datasets due to differing MMUs; three datasets (CLC2000 rev, CHA06, CLC2006) are used in analyses and indicator development with cross-references.

## Annexes, methodology and support tools
- Annex 3: Describes updating approaches; the project adopts “change mapping first” for optimal change capture.
- Annexes 4-5: LUCAS nomenclatures for land cover and land use to support interpretation and ground truthing.
- Annex 6: Priority table guiding generalisation of CLC classes during amalgamation.
- Annex 7: Contacts for technical coordination and delivery.

## Metadata and references
- Metadata standards: EEA-MSGI profile of ISO 19115; EEA metadata editor tools recommended; country-level metadata templates provided.
- References and prior guidelines (CLC1990/2000) contextualize improvements in 2006 update and validation frameworks.