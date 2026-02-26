# File Uploaded to EIDC: hydroscape_norfolk_core_metadata.csv

## Overview
- Metadata record uploaded to EIDC describing hydroscape_norfolk core data from the UK Centre for Ecology & Hydrology.
- Purpose: enable discovery, sharing, and reuse of lake core metadata with standardized fields covering identification, location, sampling details, and dating.
- Focuses on core sampling in Norfolk within the Hydroscape region, with references to core types and field collection details.

## Key Fields and Data Model
- EIDC File Name: File name uploaded to EIDC (.csv).
- WBID: Waterbody Identification number (link to lakes index).
- Hydroscape: Hydroscape region name (regional context for the dataset).
- Name: Lake name.
- General location of core: Where cores were collected (typically central/deep area of the lake).
- OSGB36_E / OSGB36_N: Easting and Northing coordinates in the UK OSGB36 datum (spatial positioning for mapping and discovery).
- Water depth at core site (m): Depth from water surface to sediment surface at the core site (units in metres).
- Core length and type: Length of the core and its type.
- Corer types: References to corer systems used (e.g., Big Ben, Livingstone) with bibliographic references.
- Date core collected: Date of fieldwork and core collection (format: dd/mm/yyyy; year shown if precise date is unknown).
- UCL_Code: Internal University College London code used on bags/database.
- UCL Sample ID: Internal Amphora code for the entire sample core (unique identifier).
- 210 Pb-dated (Y/N) for: Indicates whether the core has 210Pb dating.
- Hydroscape: (Field appears but description is truncated in the provided text; intended to describe the Hydroscape context or dataset linkage.)
- Description (associated fields): Descriptions of the corresponding fields, with some entries partially shown in the document (e.g., corer references, location details).

## Data Governance and Quality Considerations
- Standards and consistency: Metadata follows a structured layout (identifiers, spatial data, sampling details, and dating status) to support interoperability and discoverability.
- Provenance and traceability: Internal codes (UCL_Code, UCL Sample ID) support traceability back to physical samples and lab workflows.
- Geospatial accuracy: Use of OSGB36_E/N coordinates enables precise mapping within the Hydroscape/norfolk context.
- Temporal clarity: Date collected field enables temporal sequencing; when precise dates are unavailable, year-level resolution is captured.
- Dating status: 210Pb dating flag documents dating methodology applicability and limitations for each core.
- Potential gaps: Some field descriptions (e.g., Hydroscape) are incomplete in the provided record, indicating a need for complete metadata field definitions and data dictionary alignment.

## Data Availability, Provenance, and Access
- Data uploaded to a central repository (EIDC), facilitating portal-based discovery and sharing.
- Metadata includes fields to manage data availability and update processes (e.g., core collection date, dating status, internal codes).
- Sharing limitations and embargo considerations are acknowledged in the data governance context, though explicit embargo details are not provided in the extract.

## Practical Implications for Data Stewards
- Ensure completeness: Verify that all metadata fields have complete, unambiguous values (e.g., Hydroscape description, corer references, and dating status).
- Validate standards: Confirm units (metres for depth/length), coordinate system (OSGB36), and date formats (dd/mm/yyyy).
- Maintain provenance: Keep internal codes synchronized with physical sample records and laboratory data.
- Improve interoperability: Consider adding a formal data dictionary, controlled vocabularies for corer types, and cross-links to external references.
- Plan updates: Establish procedures for updating core metadata as new data become available or corrections are needed; ensure portal uploads reflect changes.

## Recommendations and Next Steps
- Complete and harmonize all field descriptions, especially the Hydroscape field, to avoid ambiguity.
- Implement a controlled vocabulary for corer types and link references to standardized bibliographic entries.
- Publish a concise metadata dictionary outlining field definitions, units, and acceptable values to support reuse by data users.
- Establish versioning and change-tracking for the metadata record to support governance and audit trails.
- Align with user needs by verifying essential fields for common discovery queries (location, dating status, core depth/length) and adjust metadata accordingly.