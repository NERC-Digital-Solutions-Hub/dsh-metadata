# Project: Historical lake sediment metal concentrations from Greater Glasgow File Uploaded to EIDC: hydroscape_glasgow_core_metadata.csv

## Overview
- Metadata file describing core samples for a project on historical lake sediment metal concentrations from Greater Glasgow.
- Uploaded to the EIDC; dataset identified as hydroscape_glasgow_core_metadata.csv.
- Captures core metadata to support discovery, interpretation, and reuse within data governance and sharing workflows.

## Metadata schema (core fields)
- WBID: Waterbody Identification number; reference link to lake database (https://eip.ceh.ac.uk/apps/lakes/index.html).
- Hydroscape: Name of the Hydroscape region used.
- Name: Lake name.
- General location of core: Categorical location of core within the lake (deep, littoral, intermediate).
- OSGB36_E: Easting coordinate (OSGB36 datum).
- OSGB36_N: Northing coordinate (OSGB36 datum).
- Water depth at core site (m): Depth from water surface to sediment surface at the core site.
- Secchi disc depth (m): Water clarity measurement prior to coring.
- Core length and type: Core length in metres and core type.
- Corer types: Types of corers used (e.g., Tapper, Chambers); reference cited (Date core collected).
- Date core collected: Field collection date (dd/mm/yyyy).
- UCL_Code: Internal University College London code used on bags/database.
- UCL Sample ID: Internal Amphora code for the entire core sample (unique ID).
- 210 Pb-dated (Y/N) for Hydroscape: Whether the core was dated using ^210Pb.

## Data quality, provenance, and governance
- Emphasizes alignment with data management best practices: accuracy, consistency, metadata completeness, and standardised formats.
- Coordinates use a defined spatial reference system (OSGB36); implications for interoperability with other geospatial datasets.
- Clear provenance through field collection date and internal coding (UCL codes) to support traceability.
- 210Pb dating flag indicates dating status, affecting age models and downstream analyses.
- Metadata supports data availability decisions, including potential disclosure or embargo considerations and update mechanisms.
- Quality assurance steps expected: QA, cleaning, and transformation of metadata prior to sharing; documentation of work performed on datasets.

## Data access, sharing, and lifecycle
- Dataset is uploaded to an external portal (EIDC) for discoverability and reuse.
- File naming and descriptive fields are aligned to enable catalogue and user discovery.
- Updates and ongoing availability should be governed by data-sharing policies and any embargo or proprietary constraints; mechanisms should be in place to reflect data updates.

## Challenges and considerations for Data Stewards
- Potential gaps in user needs and metadata completeness; ensure the schema captures all user-relevant attributes.
- Timely ingestion of data from creators and ensuring adherence to standards (metadata, formats, units).
- Interoperability across systems and formats; consider harmonising coordinate systems and date formats.
- Handling large or complex datasets and legacy databases requiring bespoke solutions.
- Ensuring consistent documentation for data lineage and transformations.

## Recommendations / next steps for Data Stewards
- Verify completeness and consistency of all fields (especially coordinates, depth, core length, dating status).
- Confirm units and reference systems (OSGB36 for coordinates) are documented and maintained.
- Maintain clear data lineage: original field notes, processing steps, and any transformations.
- Establish update workflow for new cores or revised measurements; communicate changes via versioning in the EIDC portal.
- Provide or update user guidance on dataset usage, limitations (e.g., dating status, potential embargoes), and crosswalks to related datasets (e.g., metal concentration results).
- Ensure accessibility and discoverability by aligning with portal metadata standards and linking to related datasets (e.g., hydroscape regions, lake metadata).