# CLC2006 technical guidelines

- Purpose and scope
  - Provide guidelines to update Corine land cover data for 2006 (CLC2006) by integrating the land cover map from 2000 (CLC2000) with the land cover changes between 2000 and 2006 (CLC-Changes).
  - Produce a European 2006 land cover map and a Europe-wide database of land cover changes (LCC) to support GMES Fast Track Service on Land Monitoring.

- Key data products
  - CLC2006: updated land cover map for 2006 (from 2000 plus changes).
  - CLC-Changes: database of real land cover changes between 2000 and 2006 (MMU 5 ha).
  - Revised CLC2000: corrected version used for CLC-Changes/CLC2006 as needed.
  - Ancillary data and LUCAS-based ground-truth inputs to support photo-interpretation and validation.

- Data sources and imagery
  - IMAGE2006 uses multi-temporal imagery from SPOT-4 and IRS P6 (LISS III) to provide two dates within 2006 +/- 1 year.
  - IMAGE2006 supports two dates to improve photo-interpretation and change detection; no panchromatic data.
  - For context, IMAGE2000 (Landsat-7) was used in previous cycles; CLC2006 builds on CLC2000 and CLC-Changes.

- Change mapping methodology
  - Change mapping first approach: interpret CLC-Changes directly using IMAGE2000/IMAGE2006 comparison, then integrate with CLC2000 to form CLC2006.
  - All real changes > 5 ha must be delineated in CLC-Changes; CLC2006 has an MMU of 25 ha.
  - Change polygons carry two codes (2000 and 2006) describing the real process; technical changes (T) are used only to enable proper inclusion and are removed from final CLC-Changes.
  - Changes > 5 ha must be captured regardless of position (connected to existing polygons or island-like).
  - Delineation uses CLC2000 as the basis to avoid slivers; two dates are visualised and interpreted in a dual-window environment; ground-truth data (e.g., LUCAS) and ancillary data are strongly recommended.

- Data structure and comparability
  - CLC2006 = CLC2000 rev + CLC-Changes (with specific integration rules).
  - Due to MMU differences (25 ha vs 5 ha), direct mathematical relationships between CLC2000, CLC-Changes, and CLC2006 exist only for changes > 25 ha; smaller changes require generalisation/amalgamation.
  - Changes in heterogeneous/landscape-class mosaics may be mapped at landscape level if the landscape characteristic has truly changed.

- Participating countries and GMES context
  - 38 countries participate in GMES FTSP Land Monitoring (EEA member states plus collaborators).
  - CLC2006 is part of GMES, with collaboration among EEA, ESA, JRC, and national NRCs.

- Organization, governance and work packages
  - Seven work packages (WP1–WP7) define data acquisition, ortho-correction, mosaics, in-situ data, change mapping, validation, data dissemination, and project management.
  - National Reference Centres (NRCs) coordinate national activities; a Steering Committee and GMES LMCS Implementation Group provide governance and interlinking with other GMES services.

- IMAGE2006 basics
  - Two-date, multi-temporal imagery is required to support photo-interpretation and detect changes more reliably.
  - SPOT-4 and IRS P6 provide suitable data; recommended color composites align with Landsat TM/ETM conventions for interpretability.
  - Consistency in date windows and image-sequence is emphasized to ensure reliable change detection.

- Production and integration workflow
  - CLC2006 production is semi-automatic, combining CLC2000 rev with CLC-Changes, plus targeted human interpretation.
  - For > 25 ha changes, straightforward automatic integration is possible; for smaller changes, generalisation and amalgamation rules apply ( Annex 6 guides generalisation priorities ).
  - The workflow yields three potentially independent datasets: CLC2000 rev, CLC-Changes, and CLC2006; users should treat them as related but not trivially interchangeable.

- Handling complex and landscape-scale changes
  - For heterogeneous landscapes (e.g., mosaics with patches of natural vegetation and arable land), changes may be mapped at landscape level when the overall character shifts significantly (e.g., from mosaic natural/agricultural to predominantly agricultural).

- Ancillary data and LUCAS support
  - Ancillary data types proposed: up-to-date topographic maps (1:50,000 or better), orthophotos, and additional high-/medium-resolution imagery.
  - LUCAS data (land use/land cover area frame survey) provides ground-truth and ground-based photos to support interpretation and ground-truthing; LUCAS availability varies by country and project year.

- Metadata and documentation
  - Two levels of metadata: working unit metadata (for CLC-Changes) and country-level metadata (for CLC-Changes, CLC2006, and revised CLC2000 if applicable).
  - Metadata formats align with the European Environment Agency Metadata Standard for Geographic Information (EEA-MSGI), with support from the EEA metadata editor.
  - Annexes provide templates and examples for working unit and country-level metadata.

- Verification and quality assurance
  - ETC-LUSI CLC Technical Team conducts photo-interpretation verification; two verification missions per country are planned (partial and near-complete area coverage).
  - Verification checks address topology, coding, MMU compliance, accuracy of delineation, and cross-dataset consistency.
  - InterCheck software supports verification; a Database Technical Acceptance (DBTA) report documents acceptance or requests for improvement.

- Deliverables and delivery process
  - Deliverables include:
    - CHA06 (CLC-Changes 2000-2006)
    - CLC00 rev (revised CLC2000)
    - CLC06 (CLC2006)
    - Working unit metadata (MWU_xx_nn)
    - Country metadata for CLC-Changes (MCOCH_xx) and CLC2006 (MCO06_xx)
  - Deliveries go to the EEA Central Data Repository (CDR) in standardized envelopes and file formats.
  - File formats: default ESRI Arc/INFO E00 (uncompressed) with optional MDB (ESRI Personal Geodatabase).
  - File naming conventions include country codes and version numbers (e.g., CHA06_MT02, CLC06_MT02, CLC00_MT02).
  - Coordinate Reference System (CRS) must be the national projection used for IMAGE2006, with documentation of any deviations to ensure accurate European integration.

- Technical specifications (summary)
  - MMU thresholds: CHA06 (5 ha) for CLC-Changes; CLC06/CLC00 (25 ha) for status layers.
  - Topology: strict requirements for closed polygons, single labels, no dangles, no overlaps, no gaps, no artificial boundaries; cross-layer consistency across CLC00, CLC06, and CHA06.
  - Data must be edge-matched across borders; a 1 km sea/coast buffer is required to ensure seamless European coverage.
  - Attribute definitions include codes for 2000/2006 status, change type, area, and metadata fields; specific field definitions are provided in tables within the guidelines.

- Annexes and supporting material (highlights)
  - Annex 3: Approaches for updating CLC data (update-first vs change-mapping-first; preferred approach is change-mapping-first).
  - Annex 4–5: LUCAS land cover and land use nomenclature.
  - Annex 6: Priority table for generalising CLC classes (guides how to handle small changes during generalisation).
  - Annex 7: Contacts for CLC2006 coordination and technical teams.

- Delivery and contact details
  - Responsible bodies include the European Environment Agency (EEA), European Space Agency (ESA), and national coordinators; detailed contact points are provided for the CLC2006 TT coordinator, project manager, and technical acceptance lead.

- Practical considerations for monitoring framework authors
  - Emphasizes the importance of standardized, open metadata and data formats to enable governance and reuse across agencies.
  - Highlights the need to manage data quality, transparency of change processes, and governance around public data sharing and data accessibility.
  - Demonstrates how to handle data integration with differing MMUs, including explicit rules for generalisation and technical changes to preserve real change information.
  - Provides a concrete, auditable workflow for delivering timely, quality-assured environmental monitoring data at continental scale, with clear verification and accountability mechanisms.