# CLC2006 technical guidelines

- Purpose: provide guidelines to update Corine land cover data for 2006 (CLC2006) by integrating CLC2000 with land cover changes (CLC-Changes) identified via IMAGE2006 imagery.
- Scope: GMES Fast Track Service Precursor (FTSP) Land Monitoring; national teams map changes (2000-2006) and produce CLC2006 for Europe; data governance via EEA, ETC-LUSI, and NRCs.

## Key outputs and workflow

- Primary products:
  - CLC2006: updated land cover map for 2006.
  - CLC-Changes: changes between 2000 and 2006 (MMU 5 ha).
  - Revised CLC2000 (where needed) to support CLC2006 production.
- Production approach: “change mapping first” to map real changes >5 ha, then fuse with CLC2000 to build CLC2006.
- Data integration rule: CLC2006 = CLC2000 rev + CLC-Changes (subject to MMU differences; >25 ha changes can be integrated automatically; smaller changes require generalisation).

## Technical parameters and nomenclature

- Scale and detail:
  - Map scale: 1:100,000
  - MMU: 25 hectares for CLC2000/CLC2006; 5 ha for CLC-Changes
  - Five level-1 categories; 44 land cover classes in a three-level hierarchy
- Methodology:
  - Computer-assisted photo interpretation of satellite imagery
  - Use of ortho-rectified imagery and ancillary data to ensure accuracy
- Classes and terminology updates:
  - Updated definitions in Addendum 2006; guidance on several class interpretations (e.g., forest, plantations, urban fabric)

## Data sources and imagery

- IMAGE2006 data:
  - Multitemporal coverage with two dates (two dates per area) to aid photo-interpretation
  - Primary sensors: SPOT-4 (HRVIR) and IRS P6 (LISS III); no panchromatic in IMAGE2006
  - Two dates separated by at least ~6 weeks; closest-to-current image preferred for changes
- IMAGE2006 image interpretation:
  - Recommended color composites to match interpreters’ screen displays
  - Ground-truth data (e.g., LUCAS) and ancillary data encouraged

## CLC-Changes (land cover changes 2000-2006)

- MMU and scope:
  - Change mapping MMU: 5 ha (minimum)
  - Changes >5 ha must be mapped regardless of position
- Approach and detection:
  - Changes identified by direct visual interpretation comparing IMAGE2000 with IMAGE2006 (two-date imagery)
  - Changes must refer to real evolution processes; avoid false changes
  - Delineation uses CLC2000 polygons as the basis to avoid slivers; each change polygon carries a 2000/2006 code pair
- Technical changes:
  - Technical change polygons (T) used to bridge MMU gaps (<25 ha but created to enable correct GIS delineation)
  - Technical changes are flagged and later removed from CLC-Changes; they ensure inclusion of real changes in CLC2006
- Landscape-level changes:
  - For heterogeneous classes (e.g., mosaic landscapes), changes may be delineated at landscape level when warranted by the overall shift in character
- Change typology:
  - Eight theoretical types (A–H) based on existence in CLC2000, CLC-Changes, and CLC2006
  - Detailed guidelines and examples explain how to handle each type (simple change, small changes, disappearance, new polygons, etc.)

## Participating countries and GMES context

- 38 countries (EEA members plus collaborators) participate in GMES FTSP Land Monitoring.
- CLC2006 is a direct continuation of previous CLC mapping efforts (CLC1990 and CLC2000) with refinements:
  - Focus on robust 2000-2006 change data
  - Greater emphasis on capturing all changes >5 ha
  - Most changes will be produced automatically with some human oversight

## Organization and governance

- Work packages (WP): seven defined; national NRCs coordinate at the country level
- Project governance:
  - Steering Committee (Commission, ESA, EEA, participating countries)
  - GMES LMCS Implementation Group provides advisory linkages
- Roles include satellite data acquisition, ortho-correction, in-situ data, change mapping, validation, data dissemination, and project management

## Verification and quality assurance

- Verification by the ETC-LUSI CLC Technical Team (TT)
- Two verification missions per country (partial and near-complete coverage)
- Use of InterCheck software for automated checks; Unix-based QA/QC guidance
- Verification focuses on topological integrity, thematic consistency, and metadata completeness
- Verification feedback used to trigger improvement deliveries to national teams

## Metadata and delivery

- Metadata levels:
  - Working unit level metadata ( Annex 1): for CLC-Changes production
  - Country level metadata ( Annex 2): for CLC-Changes, CLC2006, and revised CLC2000
- Metadata standards: European Environment Agency Metadata Standard for Geographic Information (EEA-MSGI), with an emphasis on INSPIRE alignment
- Deliverables and delivery process:
  - CHA06 (CLC-Changes 2000-2006), CLC06 (CLC2006), CLC00 (revised CLC2000, if applicable)
  - MWU (Working unit level) and MCOCH / MCO06 (country level) metadata
  - Deliver via the European Environment Agency Central Data Repository (CDR); use of envelopes and versioning for corrections
- Data formats:
  - Default: ESRI Arc/INFO Export Interchange File (E00) with no compression
  - Optional MDB (ESRI Personal Geodatabase) for richer dataset management
- File naming and coding conventions:
  - Standard 8-character country-specific file names; versioning with suffixes (e.g., CHA06_MT02, CLC06_MT02)
  - Attributes include codes for 2000/2006, change type, area, and other metadata fields
- CRS and projection:
  - Data to be delivered in national projection used for IMAGE2006; updates must be documented in country metadata

## Technical specifications and quality checks (high-level)

- MMU mapping thresholds:
  - CHA06 (CLC-Changes): 5 ha
  - CLC06 (CLC2006): 25 ha
  - CLC00 (revised CLC2000): 25 ha
- Topology:
  - No dangles, no gaps, no overlapping polygons, single label per polygon, no artificial boundaries, cross-layer consistency
- Metadata and documentation:
  - Complete WU and country-level metadata in the specified formats
- Technical quality check reports (DBTA):
  - Summary of data and metadata checks; acceptance status or requests for improvements
- Data governance:
  - Clear process for acceptance, revisions, and multiple iterations as needed to achieve final integration

## Additional resources and references

- Annexes include detailed approaches for updating, LUCAS nomenclature, and priority tables for generalisation
- LUCAS data (land use/cover area frame survey) used to support photointerpretation and ground-truth processes
- Key references and contact information for TT coordinators and national liaisons

Note: The document provides extensive technical detail, with annexes offering templates for metadata, coding schemes, and guidelines for handling edge cases, validation, and data exchange.