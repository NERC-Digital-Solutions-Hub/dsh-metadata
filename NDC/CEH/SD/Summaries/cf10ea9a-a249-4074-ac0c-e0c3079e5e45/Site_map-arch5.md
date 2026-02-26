# Site codes and site names

## Overview
- A mapping of site codes (e.g., Tm, Ra, Ch, Ev, TS, TN, Wi, Le, Cl, Cn, Oc, Pa, Tso, Lo, Cu, TR, Wy, TW, TH, Ke, En, Ju, Cs) to human-readable site names.
- Sites cover a network of rivers and locations, including Thame, Ray, Cherwell, Evenlode, several Thames sites (Swinford, Newbridge, Sonning, Runnymede, Wallingford, Hannington Wick), Windrush, Leach, Cole, Coln, Ock, Pang, Loddon, The Cut, Kennet, Emborne, Jubilee River, Wye, and Colne.
- Indicates a dataset that systematically documents multiple monitoring sites within a geographic hydrological network.

## Data governance and standards (how Data Stewards meet aims)
- Maintain an authoritative crosswalk between site codes and site names to ensure consistent discovery and use.
- Define and enforce metadata standards for each site (e.g., coordinate reference, river, location, site type).
- Align data collection and presentation across diverse systems and formats to support interoperability.
- Identify data availability, usage restrictions, embargo periods, and any proprietary constraints for individual sites.
- Receive site data from creators, including chasing up when datasets are incomplete.
- Perform quality assurance, cleaning, and transformation of site data before sharing.
- Ensure sharing limitations are respected and establish update mechanisms across the network.
- Upload and catalogue site data in relevant data portals and catalogues.
- Document the processing, decisions, and changes made to datasets.

## Metadata, provenance, and schema considerations
- Capture core metadata for each site: code, name, river system, location (coordinates), datum, start/end dates of monitoring, units, parameters measured, and data quality flags.
- Maintain provenance: source of the data, collection methods, processing steps, and version history.
- Use controlled vocabularies for site types and river identifiers to enable interoperability.

## Data access, sharing, and licensing
- Ensure datasets are discoverable via designated portals and catalogues.
- Apply clear licensing and usage terms to site data.
- Communicate any embargoes or access restrictions at the site level.

## Data quality and validation
- Validate accuracy and consistency between site codes and site names.
- Check for missing or inconsistent metadata (e.g., coordinates, river names, site type).
- Validate data formats and units across sites to enable reliable cross-site comparisons.
- Implement routine quality checks post-ingestion and prior to publication.

## Operational workflow and roles
- Data creators: provide raw site data with sufficient metadata.
- Data stewards: perform quality assurance, metadata curation, format standardization, and governance oversight.
- Data publishers: upload to portals, manage catalog metadata, and communicate updates.

## Challenges
- Incomplete understanding of user needs across stakeholders.
- Timely delivery of data from diverse site operators.
- Encouraging data creators to meet metadata and standardization requirements.
- Managing data from many systems and heterogeneous formats.
- Transferring and handling large datasets from numerous sites.
- Dealing with outdated databases requiring bespoke, non-interoperable solutions.

## Recommendations and next steps for Data Stewards
- Establish and maintain a single authoritative site code-to-name crosswalk with version control.
- Develop a minimum metadata schema per site, including provenance and data quality indicators.
- Create standardized templates and validation rules to facilitate consistent data submission from creators.
- Implement automated ingestion and validation pipelines where possible to reduce delays.
- Document all transformations and decisions to support traceability and reproducibility.
- Ensure clear publication workflows, licensing, and update notifications for all site data.
- Regularly review site coverage against user needs to identify gaps and priorities.