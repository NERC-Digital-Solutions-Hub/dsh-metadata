# CLC2006 technical guidelines

- Purpose: Guidelines for updating Corine land cover data for 2006 (CLC2006) by combining CLC2000 with land cover changes (CLC-Changes) identified from IMAGE2006 imagery.
- Context: Part of GMES Fast Track Service Precursor (FTSP) Land Monitoring; coordinated by EEA with ETC LUSI support; National Reference Centres (NRCs) lead national production.

## Key concepts and outputs
- Primary products:
  - CLC2006: updated land cover map for 2006.
  - CLC-Changes: detailed database of land cover changes between 2000 and 2006 (MMU = 5 ha).
  - CLC2000 rev: revised CLC2000 data used to support CLC2006 production.
- Data integration principle:
  - CLC2006 = CLC2000 rev + CLC-Changes (with automatic and manual steps). Changes > 25 ha integrate more directly; changes < 25 ha require generalisation and may involve technical changes.
- Timeframe and scope:
  - IMAGE2006 uses two dates (two-temporal imagery) to support robust photo-interpretation; changes interpreted directly in many cases to reflect real processes.

## Technical parameters and nomenclature
- Scale and mapping thresholds:
  - Base mapping MMU: 25 hectares; linear elements minimum width: 100 m.
  - CLC-Changes MMU: 5 hectares (with some exceptions for complex cases).
- Classification:
  - 44 land cover classes organized in a three-level hierarchy; five level-1 groups: artificial surfaces, agricultural areas, forests and semi-natural areas, wetlands, water bodies.
- Methodology:
  - Computer-assisted photo interpretation; IMAGE2006 orthorectified data; improved geometric accuracy (≤ 25 m) compared to earlier cycles.
- Change vs landscape: special rules for heterogeneous/landscape-level classes (e.g., 242/243/313) when changes alter landscape character.

## Participating organisations and governance
- 38 countries participated (EEA member states plus partners).
- Structure:
  - Eionet National Reference Centres (NRCs) coordinate national activities.
  - European Topic Centre on Land Use and Spatial Information (ETC-LUSI) supports integration.
  - Steering Committee and GMES Land Monitoring Core Service (LMCS) Implementation Group provide governance.

## IMAGE2006 basics and data needs
- Sensors and data:
  - SPOT-4 HRVIR and IRS P6 LISS III used; two-date, multi-temporal imagery for each area.
- Photo-interpretation guidance:
  - Use two dates within defined windows (2006 +/- 1 year; second date helps separate changes).
  - Recommended color composites per Table suggestions (e.g., R=band 4/3, G=band 5/4, B=band 3/2 depending on sensor).
- File naming and sequencing:
  - Include acquisition dates; maintain sequence awareness for interpretation.

## Change mapping approach and rules
- Change mapping first (Annex 3 describes two approaches; CLC2006 adopts change mapping first):
  - Identify and delineate all real land cover changes > 5 ha, using IMAGE2000/IMAGE2006 comparison, with attention to avoiding false changes.
  - Use CLC2000 as the base, then delineate changes directly in CLC-Changes; assign 2000/2006 codes to reflect real processes.
- Technical change polygons:
  - Used to avoid >5 ha and <25 ha errors; polygons labeled as technical (with a flag) are temporary and removed from final CLC-Changes.
- Change typology guidance:
  - Eight theoretical types (A–H) based on presence/absence and size in CLC2000, CLC-Changes, and CLC2006; examples and decision logic provided to handle complex cases.
- Landscape-level changes:
  - For mosaic/heterogeneous classes (243, 242, 313), changes may be mapped at landscape level if the overall character shifts substantially.

## Ancillary data and ground truth
- Ancillary data:
  - Topographic maps (≥1:50,000), orthophotos, and additional high/medium-resolution imagery recommended to support interpretation.
- LUCAS data:
  - Ground-truth data from LUCAS (land use/cover area frame survey) used to support photointerpretation and change interpretation (where available; Annexes 4 and 5 detail nomenclatures).

## Metadata and documentation
- Metadata levels:
  - Working unit level metadata (Annex 1) for CLC-Changes production.
  - Country level metadata (Annex 2) for CLC-Changes, CLC2006, and revised CLC2000 where applicable.
- Standards:
  - Metadata aligned with EEA-MSGI/ISO19115 (INSPIRE guidance); EEA Metadata Editor recommended for ArcGIS environments.

## Verification and quality assurance
- Verification framework:
  - ETC-LUSI CLC Technical Team verifies CLC2000 and CLC-Changes; two verification missions per country (2nd and 4th quarters).
  - InterCheck software used; emphasis on topological integrity, logical code usage, and cross-layer consistency.
- Quality checks:
  - Topology: no dangles, no gaps, polygons closed, unique labels, no overlaps.
  - Thematic accuracy and geometric accuracy checks are documented in DBTA (Database Technical Acceptance) reports.

## Deliverables and data delivery
- Deliverables:
  - CHA06 (CLC-Changes 2000-2006)
  - CLC00 (revised CLC2000, if applicable)
  - CLC06 (CLC2006)
  - Working unit level metadata (MWU_xx_nn)
  - Country level metadata for CLC-Changes (MCOCH_xx) and CLC2006 (MCO06_xx)
- Delivery process:
  - Delivered to EEA Central Data Repository (CDR) in envelopes; follow national schedules; use Unified Notification Service for alerts.
- File formats and naming:
  - Default: ESRI Arc/INFO E00 (export/interchange) with no compression; MDB as optional delivery format.
  - File naming: CHA06_xx.e00, CLC06_xx.e00, CLC00_xx.e00; with country ISO codes; versions labeled (e.g., MT02 for Malta second delivery).
  - Attribute and topology conventions detailed (e.g., Change field with 2000/2006 codes; Chtype; Area_ha; etc.).
- Coordinate reference system:
  - Data delivered in national projections (as used for IMAGE2006); provide country CRS parameters to TT; European integration uses consistent reference baselines.

## Production workflow and guideline structure
- Production is semi-automatic with human intervention:
  - Automated integration for changes > 25 ha; generalisation/amalgamation for smaller changes.
  - Non-automatic, photointerpreter-driven handling for certain edge cases and near-threshold areas.
- Working units and borders:
  - Edge-matched basis from CLC2000; border regions adjusted to ease Europe-wide mesh; 1 km buffer along borders for consistency.

## Annex highlights (for GIS work implications)
- Annex 3: Approaches for updating CLC data (update-first vs change-mapping-first); CLC2006 uses change-mapping-first for better change representation.
- Annex 4/5: LUCAS land cover and land use nomenclature (supporting ground-truth coding).
- Annex 6: Priority table for generalising CLC classes to manage amalgamation consistently.
- Annex 7: Contacts for CLC2006 TT and project management.

## References and standards
- Core references include: Corine land cover guides, Addendum 2006 nomenclature, CLC2000/2006 methodological papers, and GMES-related implementation plans.
- Metadata and data standards align with EEA-MSGI/ISO19115 and INSPIRE guidelines.