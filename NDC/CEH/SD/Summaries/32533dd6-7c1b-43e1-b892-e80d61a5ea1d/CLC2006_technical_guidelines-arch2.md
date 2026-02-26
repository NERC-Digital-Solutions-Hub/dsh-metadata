# CLC2006 technical guidelines

- Aims to update Corine land cover data for 2006 by integrating the land cover map from 2000 (CLC2000) with land cover changes detected between 2000 and 2006 (CLC-Changes), using IMAGE2006 imagery.
- Part of GMES Fast Track Service Precursor (FTSP) Land Monitoring; 38 countries participate.
- Intended for national CLC teams and related organizations; emphasizes practical production guidance and standardised outputs.

## Key data products and outputs

- CLC2006 database: European land cover map for 2006 at 1:100,000 scale; MMU of 25 hectares; 44 land cover classes; built by combining CLC2000 with CLC-Changes.
- CLC-Changes database: records real land cover changes between 2000 and 2006; MMU of 5 hectares; polygons include paired codes for 2000 and 2006 to reflect actual processes.
- CLC2000 rev: revised 2000 dataset used to correct errors before integration into CLC2006.
- Outputs are delivered as standardized datasets with complete metadata to the European Environment Agency (EEA) Central Data Repository (CDR).

## Data sources and imagery

- IMAGE2006: multi-temporal two-date satellite imagery (SPOT-4 and IRS P6 LISS III) for 2006 +/- 1 year to support photo-interpretation; no panchromatic band in 2006.
- IMAGE2000: Landsat-7 ETM used for the 2000 reference; high geometric accuracy (≤25 m) and ortho-corrected mosaics.
- Ancillary data: topographic maps, orthophotos, and other high-resolution imagery; LUCAS data (land use/cover area frame survey) provide ground-truth-like references for photo-interpretation.

## Change mapping methodology

- Change mapping first approach: primary method for CLC2006 production.
  - Identify and delineate all real land cover changes > 5 ha between 2000 and 2006, regardless of location or connection to existing polygons.
  - Derive CLC2006 by intersecting CLC2000 rev with CLC-Changes and reclassifying; in practice, CLC2006 = CLC2000 rev + CLC-Changes (with alignment and generalisation to 25 ha MMU for final map).
  - Changes are delineated directly on IMAGE2000/IMAGE2006 in a dual-window setup; use CLC2000 polygons as baselines to avoid spurious changes.
- Change typology and handling (types A–H) guide interpretation when integrating three databases: CLC2000, CLC-Changes, CLC2006.
- Technical changes (T) may be introduced to manage edge effects or MMU disparities; technical changes are removed from final CLC-Changes but help ensure inclusion of real changes in CLC2006.
- Landscape-level changes are considered for heterogeneous classes (e.g., mosaics) where the landscape character changes fundamentally.

## Data governance and project organization

- Seven work packages (WPs) structure the GMES FTSP Land Monitoring; WP3 focuses on CLC-Changes mapping (2000–2006) and CLC2006 production.
- National Reference Centres (NRCs) organise national work; ETC-LUSI provides support and data integration tools; a Steering Committee coordinates across DGs, EEA, ESA, JRC and participating countries.
- Data integration logic recognises that CLC2000, CLC-Changes, and CLC2006 are three (nearly) independent datasets due to different MMUs and processing histories.

## Quality assurance and verification

- Verification by ETC-LUSI Technical Team (TT) mirrors CLC2000 verification approaches; two verification missions per country (partial and near-complete areas) ensure consistency and harmonisation.
- Verification checks cover geometry, topology, coding, and metadata completeness; use of InterCheck software and DBTA (Database Technical Acceptance) reports to document acceptance or improvements.

## Metadata and data delivery

- Two metadata levels: working unit level (for changes) and country level (for all datasets).
- Metadata standards follow the European Environment Agency Metadata Standard for Geographic Information (EEA-MSGI); EEA-MSGI metadata editor is recommended.
- Deliverables to EEA Central Data Repository (CDR) include:
  - CHA06 (CLC-Changes 2000–2006)
  - CLC00 (revised CLC2000, if applicable)
  - CLC06 (CLC2006)
  - Working unit and country level metadata
- File formats: default ESRI Arc/Info Export Interchange File (E00) with no compression; MDB (ESRI Personal Geodatabase) optional.
- File naming conventions: 8-character country codes; versioned envelopes (e.g., CHA06_MT02, CLC06_MT02, CLC00_MT02) for updates; many attribute naming and data integrity requirements apply.
- Coordinate reference systems (CRS): national projections used during IMAGE2006; provider must indicate any deviations or use of European CRS.

## Technical specifications and data integrity

- MMU thresholds: CHA06 changes = 5 ha; CLC06 map = 25 ha; CLC00 = 25 ha.
- Topology requirements: no dangles, no gaps, polygons closed, consistent labeling, and cross-layer consistency between CLC00, CHA06, and CLC06.
- 1 km buffer around national borders and 1 km sea buffer along coastlines are recommended to ensure seamless European coverage.
- Data are treated as three nearly independent datasets for analysis and indicators due to differing MMUs and processing histories.

## Ancillary data and LUCAS

- Ancillary data: topographic maps, orthophotos, and additional high-resolution imagery to aid interpretation.
- LUCAS data: ground truth-like land use and land cover nomenclature and field photos for 2001/2002 and 2006; used to improve CLC2000 and delineate changes; availability varies by country.

## Practical implications for analysts monitoring the environment

- Provides a consistent, time-grounded European land cover dataset for 2006, enabling monitoring of land cover dynamics and policy performance over time.
- Recognises and addresses changes in data structure (two MMUs) by treating CLC2000, CLC-Changes, and CLC2006 as distinct datasets while enabling integrated analysis.
- Emphasises transparent, reproducible workflows with explicit change types and metadata to support scrutiny and policy evaluation.
- Highlights the value of linking datasets (e.g., CLC data with LUCAS and ancillary data) to improve dataset quality and interpretability, aligning with the archetype’s aim to maximize dataset value and accessibility.