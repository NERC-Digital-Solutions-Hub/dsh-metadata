# UK Environmental Change Network (http://www.ecn.ac.uk) Vegetation: Fine Grain (VF)

## Overview
- ECN Vegetation: Fine Grain (VF) dataset managed by a multi-institution program; data stored in an Oracle database with a site-centric, multi-table schema.
- Data governance emphasizes discoverability, reuse, provenance, and appropriate attribution/citation.
- Site coverage uses codes T01–T12 with location and date-range metadata; data are structured for interoperability across sites.

## Data Model and Structure
- Oracle-based, multi-table schema:
  - D1VF_xxx: Plot and site-level descriptors
  - D2VF_xxx: Environmental/management information (e.g., PEDATE, LANDUSE, SLOPE, ASPECT, NVCCLASS)
  - D3VF_xxx: Cell-level and feature data
- Core fields:
  - SITECODE, SYEAR, PLOTPID, CELLID, FIELDNAME, VALUE
- Sampling design:
  - At least two 10m x 10m plots per NVC type per site
  - Species presence recorded in 40cm x 40cm cells
  - Vegetation surveys repeated every three years; some sites conduct annual subsampling
- Metadata and protocol documents accompany the dataset; data usage should include acknowledgement and reprint of citing publications.

## Taxonomy, Codes, and Metadata
- Extensive cross-referenced codes for:
  - Species and taxa (Latin names, synonyms, and groupings; broad thesaurus coverage)
  - Land use (Hodgson codes 1–22)
  - Slope, slope form, aspect, NVCCLASS, and site features (path, hedge, stream, etc.)
- Detailed mappings link numeric species codes to accepted names and taxonomic concepts, enabling cross-reference and reuse across analyses.
- Site-specific metadata and measurement details are organized by site (T01–T12), with location coordinates and site date ranges.

## Quality, Availability, and Updates
- Quality information is essential for analysis; users should consult accompanying quality metadata.
- ECN quality codes exist to flag data issues; a special code 999 captures unusual events with accompanying free-text in quality documentation.
- Update governance:
  - Clear disclosure and embargo constraints for data sharing
  - Processes to provide updated datasets while preserving provenance and traceability

## Governance and Stewardship Considerations for Data Stewards
- Provenance and attribution:
  - Maintain clear records of dataset origin, site ownership, and sponsorship; enforce acknowledgement and data citation requirements.
- Metadata and discoverability:
  - Keep core metadata and site-specific protocol details current and accessible; preserve quality metadata for proper analysis.
- Data structure and interoperability:
  - Manage the Oracle-based D1VF/D2VF/D3VF schema with consistent site codes; retain comprehensive code mappings for plots, land use, features, and taxonomy.
- Access and updates:
  - Document embargoes/disclosure constraints; provide updated data with change logs across sites and tables.
- Citation and reuse:
  - Ensure users cite ECN data and provide reprints to support traceability and impact assessment.

## Practical Implications and Next Steps for Data Stewards
- Regularly audit and update site-level metadata, protocol details, and code mappings to maintain interoperability.
- Ensure robust quality metadata is available and used in analyses; monitor and manage quality code 999 text for unusual events.
- Implement and communicate data-sharing policies, including attribution requirements and data revision procedures.
- Prepare clear documentation for end users on how to navigate the three-tier VF data schema (D1VF, D2VF, D3VF) and the associated code thesauri.
- Plan for scalable data transfers and storage considerations given the large species code mappings and multi-site structure.