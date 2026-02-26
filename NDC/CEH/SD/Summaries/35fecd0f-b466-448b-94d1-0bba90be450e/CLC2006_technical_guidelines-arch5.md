# CLC2006 technical guidelines

- Aims to update Corine land cover data for 2006 by integrating CLC2000 with land cover changes (LCC) 2000-2006, using IMAGE2006 imagery for change interpretation.
- Managed by Eionet National Reference Centres (NRCs) with support from ETC LUSI and EEA/JRC within GMES Fast Track Service Precursor (FTSP) Land Monitoring.

## Governance and Stakeholders

- National teams coordinate at the country level; data integration handled by EEA with ETC LUSI support.
- Steering Committee includes Commission, ESA, EEA, participating countries; LMCS Implementation Group provides advisory linkage.
- Deliverables flow through the Central Data Repository (CDR) of the EEA; clear roles for delivery, verification, and technical acceptance.

## Data Standards and Nomenclature

- 44 land cover classes in a three-level hierarchy; five level-one groups (artificial surfaces, agricultural areas, forests/semi-natural, wetlands, water bodies).
- MMU: 25 ha for CLC2000/CLC2006; 5 ha MMU for CLC-Changes.
- Consistent geometry and semantics; emphasis on standard metadata (EEA-MSGI/ISO19115) and country-level metadata.
- LCC database (CLC-Changes) uses MMU of 5 ha and is separate from CLC2006; CLC2006 derives from CLC2000 plus CLC-Changes.

## Data Sources and Change Mapping

- IMAGE2006 uses two dates from SPOT-4 and IRS P6 (LISS III) to enable multitemporal photo-interpretation.
- IMAGE2006 imagery chosen to maximize two-date comparison within a 2006 +/- 1 year window.
- LCC creation focuses on real changes (>5 ha, >100 m displacement) across Europe; inclusive of changes near or connected to existing polygons and island-like changes.

## Production and Integration Workflow

- Change mapping first: interpret all changes >5 ha; CLC2006 = CLC2000 rev + CLC-Changes (with caveats for small changes).
- Two parallel approaches to updating CLC2000 discussed; CLC2006 adopts a "change mapping first" approach for more accurate, real-change representation.
- Integration rules:
  - For changes > 25 ha, straightforward automatic integration: CLC2006 = CLC2000 rev + CHA06.
  - For changes < 25 ha, require generalisation/amalgamation to reach 25 ha in the final product; sometimes use technical changes to preserve real change information.
- LUCAS data (ground-truth) and ancillary data (topographic maps, orthophotos) recommended to support interpretation.
- Annexes provide detailed approaches for updating data and handling heterogeneous/landscape-level changes.

## Metadata and Documentation

- Two levels of metadata:
  - Working Unit (WU) metadata for CLC-Changes (Annex 1).
  - Country-level metadata for CLC-Changes, CLC2006, and revised CLC2000 (Annex 2).
- Metadata aligned with EEA-MSGI/ISO19115; metadata tooling includes an EEA Metadata Editor for ArcGIS.
- Metadata must accompany data deliveries to ensure traceability and reuse.

## Quality Assurance and Verification

- ETC-LUSI CLC Technical Team validates photo-interpretation; two verification missions per country (early and late in production).
- InterCheck software used for automatic and manual checks; DBTA (Database Technical Acceptance) reports document acceptance or requests for improvement.
- Checks cover topological consistency, geometry, coding, and metadata completeness; emphasis on harmonisation across Europe.

## Delivery, Access and Data Management

- Deliverables include:
  - CHA06 (CLC-Changes 2000-2006)
  - CLC06 (CLC2006)
  - CLC00 (revised CLC2000, if applicable)
  - Working Unit metadata (MWU_xx_nn)
  - Country-level metadata (MCOCH_xx, MCO06_xx)
- Deliveries via EEA Central Data Repository (CDR); use ZIP envelopes with standardized file naming:
  - CHA06_xx.e00, CLC06_xx.e00, CLC00_xx.e00
  - Optional MDB deliveries (ESRI Personal Geodatabase)
- File naming includes country ISO codes; 8-character names for primary data, versioned names for iterative deliveries (e.g., CHA06_AT02, CLC06_AT02).
- Data formats: default ESRI Arc/INFO Export Interchange File (E00); optional MDB deliveries for modern GIS workflows.
- Coordinate Reference System (CRS): national projections used in IMAGE2006, with documentation of CRS parameters; national provision for European integration.

## Ancillary Data and Ground Truth

- Ancillary data (topographic maps, orthophotos, high-resolution imagery) recommended to support interpretation.
- LUCAS data (land use/cover area frame survey) provided for ground-truth and to support photo-interpretation (LC/LU nomenclatures in Annexes 4 and 5).
- LUCAS 2006 and earlier versions used to validate and improve CLC2000, with examples showing corrections to CLC2000 interpretations.

## Change Typology and Landscape Considerations

- Change types defined to handle complex scenarios (A–H) based on size thresholds and whether they involve existing polygons.
- Special handling for heterogeneous/landscape-level classes (e.g., mosaic landscapes) to determine when to map changes at landscape level versus patch level.
- Technical changes (T) may be used to reconcile MMU differences and ensure inclusion of real changes while maintaining dataset integrity.

## Technical Specifications

- Minimal Mapping Unit (MMU) for CHA06: 5 ha; for CLC06 and CLC00: 25 ha.
- Topology: strict requirements (no dangles, no overlaps, single label per polygon, no gaps, seamless across borders).
- Data must be edge-matched across countries; 1 km coastal buffer recommended to ensure seamless European coverage.
- Attribute definitions and naming conventions tailored for both E00 and MDB deliveries; key fields include 2000/2006 codes, area, change, and change type.

## Deliverables Schedule and Contacts

- Documentation includes timelines, verification schedules, and delivery processes; responsibilities clearly defined for national coordinators and TT.
- Annexes provide contacts for the CLC2006 TT, project manager, and technical/metadata support.

## Annexes and References

- Annexes cover updating approaches (Annex 3), LUCAS nomenclatures (Annex 4/5), priority table for generalising classes (Annex 6), and contacts (Annex 7).
- References to prior CLC guidelines, LUCAS references, metadata standards, and GMES-related documentation.