# CLC2006 technical guidelines

## Executive summary
- Guidelines for updating Corine land cover data for 2006 (CLC2006) by integrating CLC2000 with land cover changes (LCC) 2000-2006.
- Key products: CLC2006, CLC-Changes (2000-2006). Change mapping is the primary focus; integration with CLC2000 is constrained by different minimum mapping units (MMUs).
- Quality assurance, metadata, and delivery standards are defined for European-wide harmonization and data sharing.

## Aim and scope
- Produce CLC2006 by combining CLC2000 with LCC data for 2000-2006 using IMAGE2006 imagery (two dates, 2006 +/- 1 year).
- Managed by Eionet National Reference Centres (NRCs) with data integration by EEA and ETC-LUSI.
- Readers are national CLC teams and related organisations; focus is practical production guidance and overview of theory.

## Data standards and parameters
- MMU and scale: CLC uses 1:100,000 scale; MMU 25 ha for CLC, 5 ha for CLC-Changes; minimum width for linear elements 100 m.
- Nomenclature: 44 land cover classes in a three-level hierarchy; five level-one categories (artificial surfaces, agricultural areas, forests and semi-natural areas, wetlands, water bodies).
- Methodology: computer-assisted visual interpretation with ortho-corrected imagery; CLC2006 builds on improvements from CLC2000; CLC2006 emphasizes change mapping and real-world processes.
- Change databases: CLC-Changes created for 2000-2006 with MMU 5 ha; CLC2006 uses CLC2000 and CLC-Changes to produce the updated map.

## Imagery and data sources
- IMAGE2006 imagery: SPOT-4 HRVIR and IRS P6 LISS III (two dates for each area); multi-temporal pairs aid interpretation.
- Comparable references: IMAGE2000 used Landsat-7 ETM; IMAGE1990 used Landsat.
- Colour composites and image timing guidelines provided for consistent photo-interpretation.

## Change mapping and data integration
- Change mapping first approach is used for CLC2006: interpret LCCs > 5 ha directly, derive CLC-Changes, then combine with CLC2000 rev to form CLC2006.
- Larger-than-25-ha changes can be integrated automatically; smaller changes (<25 ha) require generalisation and may involve technical changes to preserve accuracy.
- The updating process accounts for real processes (e.g., new development, conversion) rather than simple differences between dated maps.
- Important: changes must be delineated using CLC2000 boundaries to avoid slivers; each change polygon carries a 2000/2006 code pair.

## Change typology and handling rules
- Eight change types (A–H) defined based on existence, size, and whether it creates a new polygon or alters an existing one.
- Technical changes (T) may be used to avoid inaccuracies caused by MMU differences; these are marked with a technical flag and later handled to ensure final CLC2006 accuracy.
- Special attention to heterogeneous or landscape-level classes (e.g., mosaic landscapes) where landscape-level changes may supersede patch-level delineation.

## Ancillary data and ground truth
- Ancillary data proposed: up-to-date topographic maps (1:50,000), orthophotos, and additional high-resolution imagery.
- LUCAS data (land use/cover area frame survey) provided to support photo-interpretation; LUCAS 2001/2002 aids CLC2000 improvements, LUCAS 2006 supports change delineation.

## Production and workflow
- Seven work packages (WPs) structure the GMES FTSP Land Monitoring; NRCs coordinate national activities; ETCLUSI/EEA/JRC share responsibilities.
- IMAGE2006 basics described; data integration is semi-automatic with human oversight.
- Border regions: use edge-matched CLC2000; a 2 km border strip analyzed; ensures seamless Europe-wide data; sea edge adjustments applied.

## Metadata and delivery requirements
- Two levels of metadata: Working Unit (Annex 1) and Country-level (Annex 2); metadata must follow EEA-MSGI (ISO19115 profile) with an editor tool available for ArcGIS.
- Deliverables include:
  - CHA06_xx.e00 (CLC change layer 2000-2006)
  - CLC06_xx.e00 (CLC2006)
  - CLC00_xx.e00 (revised CLC2000, if applicable)
  - Working unit metadata (MWU_xx_nn)
  - Country metadata for CLC-Changes (MCOCH_xx) and CLC2006 (MCO06_xx)
- File formats: default ESRI Arc/INFO E00 (uncompressed) with optional ESRI Personal Geodatabase MDB; 8-character file names with country codes; strict attribute and topology requirements.
- Coordinate reference systems: national projections (with documentation of CRS); for confidential national projections, European CRS may be required.

## Quality assurance and verification
- Verification by the CLC Technical Team (ETC-LUSI) to ensure harmonization and high quality.
- Two verification missions planned; InterCheck software used for automated checks; checklists and DBTA (Database Technical Acceptance) reports document issues and resolutions.
- Topology and data integrity checks include: no dangles, no gaps, polygons closed with one label, no duplicate lines, and consistent cross-layer delineation.

## Deliverables and delivery process
- Deliverables to the EEA Central Data Repository (CDR); delivery envelopes with standardized file naming; versioning for iterative improvements.
- Delivery schedule and change management governed by national projects; notifications via Unified Notification Service.
- Technical acceptance can result in final acceptance or requests for improvements with re-delivery.

## Annexes and supporting materials
- Annex 3: Approaches for updating CLC data (update-first vs change-mapping-first; CLC2006 uses change-mapping-first).
- Annex 4/Annex 5: LUCAS land cover/use nomenclature (2001/2002 vs 2006 differences).
- Annex 6: Priority table for generalising CLC classes (guides generalisation decisions).
- Annex 7: Contacts for CLC2006 coordination and TT.
- References and glossary of abbreviations for consistent terminology.

## Practical implications for Data Stewards
- Enforce standardized MMU and class definitions; maintain data provenance across CLC1990/CLC2000/CLC2006 and CLC-Changes.
- Ensure robust metadata at both working-unit and country levels; use EEA-MSGI and the provided editors.
- Manage data delivery workflows through the CDR with strict file naming, formats, CRS documentation, and topology checks.
- Oversee quality assurance workflows, including verification missions and DBTA reporting.
- Coordinate use of ancillary data (topographic maps, orthophotos, LUCAS) and LUCAS-based ground truth to improve interpretation accuracy.
- Monitor handling of heterogenous/landscape-level classes to avoid misclassification in change mapping.
- Maintain border continuity and coastal sea-buffer requirements to ensure seamless European datasets.