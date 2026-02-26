# CLC2006 technical guidelines

## Aim and context
- Guidelines for updating Corine land cover data for 2006 (CLC2006) by integrating land cover changes 2000-2006 with the 2000 map (CLC2000).
- Production overseen by Eionet National Reference Centres (NRCs) for spatial analysis and land cover; data integration supported by the European Topic Centre on Land Use and Spatial Information (ETC-LUSI) and GMES Fast Track Service Precursor (FTSP) Land Monitoring.
- Readers: national CLC teams and organisations involved in production; focus on practical production issues with overview of theory.

## Key outputs and structure
- Primary products: CLC2006 database, CLC-Changes database (LCC changes 2000-2006), revised CLC2000 when applicable.
- Metadata: working unit and country level metadata; delivered via the European Central Data Repository (CDR).
- Deliverables include CHA06 (CLC-Changes 2000-2006), CLC06 (CLC2006), CLC00 (revised CLC2000), plus associated metadata and working-unit records.

## Data sources and GMES context
- IMAGE2006 provides multitemporal satellite data (two dates) to support photo-interpretation; SPOT-4 and IRS P6 (LISS III) used as primary sensors.
- Two dates per area within 2006 +/- 1 year to improve interpretation; colour composites and band combinations guided for consistency with historical data.
- Ancillary data support includes topographic maps, orthophotos, and LUCAS ground-truth data (2001/2002 and 2006).

## Technical parameters and nomenclature
- Corine parameters: MMU of 25 ha for CLC, 5 ha for CLC-Changes; minimum width of 100 m for linear features remains.
- The standard CLC nomenclature comprises 44 classes across five major groups; class definitions enhanced with Addendum 2006.
- CLC2006 aims to map only changes larger than 5 ha; but changes > 5 ha must be delineated regardless of position.

## Change mapping framework and methodology
- Change mapping first approach: changes between 2000 and 2006 are interpreted directly from IMAGE2000 vs IMAGE2006, producing CLC-Changes, which are then combined with CLC2000 to yield CLC2006.
- Change polygons carry two codes (2000 and 2006) describing the real process; two dates help distinguish genuine changes from errors.
- Change typology (Table 7) outlines eight types (A–H), including simple changes, small changes, disappearing polygons, new polygons, and technical changes to bridge MMU gaps.
- Technical changes (T) are auxiliary polygons (<25 ha but >5 ha) used to avoid larger errors; they are removed from the final CLC-Changes database.
- Specialized considerations for heterogeneous/landscape-level classes (e.g., 242, 243, 313) to decide when to delineate changes at landscape level vs patch level.

## Data integration and evolution
- CLC2006 = CLC2000 rev + CLC-Changes (for changes > 25 ha, straightforward automatic integration). For changes < 25 ha, generalisation and amalgamation are required.
- Because CLC2000, CLC-Changes, and CLC2006 use different MMUs (25 ha vs 5 ha), exact mathematical reconciliation is not possible; three datasets are treated as nearly independent for some applications.
- Annexes provide approaches for updating data (Annex 3) and generalisation rules (Annex 6).

## Ancillary data and LUCAS support
- Proposed ancillary data include up-to-date topographic maps, orthophotos, and additional high/medium-resolution imagery.
- LUCAS ground-truth data (land use and land cover codes with photos) are available to support photo-interpretation and can improve CLC2000 and CLC-Changes delineation (Annex 4, Annex 5).

## Metadata and quality assurance
- Two levels of metadata: working unit level (Annex 1) and country level (Annex 2).
- Metadata follow the European Environment Agency Metadata Standard for Geographic Information (EEA-MSGI); use of the EEA Metadata Editor is recommended.
- Verification: ETC-LUSI technical team conducts two verification missions, with checks on topological consistency, code validity, and cross-dataset coherence. InterCheck software used for verification; DBTA reports document acceptance or areas for improvement (Section 8).

## Deliverables and delivery process
- Deliverables to the EEA Central Data Repository (CDR) include CHA06, CLC06, CLC00, MWU (working unit metadata), MCOCH (country metadata for CHA06), MCO06 (country metadata for CLC06).
- Delivery flow involves envelopes in CDR, with notifications to coordinators; pre-delivery QA/QC support is available.
- Technical specifications cover:
  - File formats: ESRI Arc/INFO Export Interchange File (E00) as default; ESRI Personal Geodatabase (MDB) as an optional delivery.
  - File naming: CHA06_xx.e00, CLC06_xx.e00, CLC00_xx.e00 (xx = ISO country code); versioning via suffixes (e.g., MT02).
  - Coordinate reference: national projections, with updates to reflect IMAGE2006 CRS where needed.
  - MMU and topology: strict adherence to MMU thresholds, 100 m minimum width for lines, valid CLC codes, no gaps, proper topology, and cross-border edge matching.
- Anomalies and corrections are tracked via DBTA; iterative improvement is allowed but the aim is to minimize cycles.

## Delivery schedule and contacts
- Delivery schedule aligned with national project plans; coordination through national focal points and TT (Technical Team) at ETC-LUSI.
- Key contacts: CLC2006 TT coordinator, project manager, and support teams; detailed contact information provided in Annex 7.

## Annexes and supporting material
- Annexes include LUCAS nomenclature (Annex 4 and Annex 5), approaches for updating data (Annex 3), priority generalisation table (Annex 6), and contacts (Annex 7).
- Annexes provide detailed coding schemes, generalisation rules, and data structure guidance.

## Implications for analysts monitoring the environment
- Establishes a rigorous, standardized workflow for updating land cover across Europe with explicit change detection, documentation, and quality control.
- Enables comparability over time while addressing changes in data resolution (MMU differences) through explicit generalisation rules and a detailed change typology.
- Highlights data integrity and traceability via layered metadata, verification, and formal delivery procedures; emphasizes combining CLC data with ancillary information (e.g., LUCAS) to improve interpretation and data value.
- While primarily oriented to European institutional workflows, the framework demonstrates how to harmonize multi-source, multi-date land cover information for environmental monitoring and policy assessment.