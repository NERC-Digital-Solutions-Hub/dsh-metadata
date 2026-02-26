# File Uploaded to EIDC: hydroscape_norfolk_core_metadata.csv

- Metadata file uploaded to EIDC documenting core sample information for the Hydroscape region in Norfolk.
- Core-related fields capture identification, location, and collection details, plus data provenance and dating status.

## Overview of the Data Asset

- Contains core metadata for lake sediments, including file name, waterbody ID, Hydroscape region, lake name, and core location context.
- Spatial coordinates are captured in OSGB36 (Easting and Northing) to enable mapping of core sites.
- Key physical measurements included: water depth at the core site and core length/type.
- Corer types referenced with bibliographic citations:
  - Big Ben: a wide-bore piston corer (citation provided)
  - Livingstone: lightweight piston sampler (citation provided)
- Sample identifiers and lab codes: UCL_Code and UCL_Sample_ID.
- Dating status: whether the core is 210Pb-dated (Yes/No).
- Date of core collection noted, with formatting guidance (full date or year only if precise date is unknown).
- The dataset links to external resources (e.g., UK CEH Lakes index) and uses standard lake-specific naming conventions (Hydroscape, Lake Name).

## Metadata Fields and Purpose

- EIDC File Name: name of the CSV file uploaded to EIDC.
- WBID: Waterbody Identification number for cross-referencing with external lake inventories.
- Hydroscape: regional context within the Hydroscape dataset.
- Name: Lake Name.
- General location of core: description of core site placement (typically central, deepest area).
- OSGB36_E / OSGB36_N: spatial coordinates for mapping and GIS integrations.
- Water depth at core site (m): surface-to-sediment depth at collection.
- Core length and type: physical dimensions and type of the retrieved core.
- Corer types: references to the coring equipment used, with bibliographic citations.
- Date core collected: date of field collection (specific day/month/year or year only when unknown).
- UCL_Code / UCL_Sample ID: internal identifiers for sample tracking.
- 210 Pb-dated (Y/N): indicates dating status which informs age-model capabilities.
- Hydroscape (additional context): region-specific metadata (note: field appears truncated in provided extract).

## Data Provenance and Access

- Data originate from lake core sampling within the Hydroscape Norfolk region.
- Metadata is stored as a CSV file uploaded to EIDC, facilitating centralized access and discovery.
- Some fields reference external data sources (e.g., CEH Lakes index) for broader context and validation.

## Data Quality, Standards, and Gaps

- Coordinate data are provided in a standard OSGB36 system (facilitates GIS use).
- Core-specific details (depth, length, dating status) are included, supporting basic quality assessment.
- Some fields show incomplete fulfillment in the extract (e.g., Hydroscape field truncated), indicating potential gaps in metadata completeness.
- Inferred need for standardized vocabularies (e.g., controlled terms for corer types) and consistent date formatting to improve interoperability.

## Discoverability and Data Asset Management

- Centralized in EIDC, with explicit identifiers (WBID, UCL_Code, UCL_Sample_ID) to enable tracking and linking to related datasets.
- Cross-referencing potential with external lakes inventories enhances discoverability and integration across systems.

## Challenges and Considerations for Data Leaders

- Understanding user needs: metadata should support diverse users (policy colleagues, researchers) by clarifying data context and usage.
- Gaining an overview of available data: multiple data sources require centralization and clear linking between internal and external datasets.
- Data granularity and completeness: ensure all core-related fields are complete and standardized.
- Access barriers: anticipate and address data protection or sharing constraints that could impede external access.
- Verifying data content/format quickly: rely on dating status, corer type citations, and consistent units; maintain clear provenance.
- Data standards and metadata clarity: adopt controlled vocabularies and consistent metadata practices to reduce ambiguity.
- Sector coordination: foster communities of practice to align metadata standards and improve cross-dataset interoperability.

## Recommendations for Data Leaders

- Standardize metadata fields and adopt controlled vocabularies (e.g., for corer types, units, date formats).
- Link metadata to external inventories (e.g., CEH Lakes index) to improve context and discoverability.
- Ensure metadata completeness and accuracy, with explicit data quality notes and update procedures.
- Implement clear data governance, versioning, and provenance documentation for updates.
- Provide user guidance, licensing, and usage notes to facilitate broader, responsible data reuse.
- Facilitate feedback loops with data users to align metadata with evolving needs (policy, research, and practice communities).