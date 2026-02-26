# File Uploaded to EIDC: hydroscape_lakedistrict_core_metadata.csv

## Overview
- Metadata file describing hydroscape lake district sediment core samples uploaded to EIDC.
- Captures essential identifiers, geographic context, sampling details, core characteristics, dating status, and internal lab codes.
- Designed to support discovery, reuse, and governance of palaeolimnology core data.

## Dataset contents and key fields
- WBID (Waterbody Identification number) with a link to the lakes index, enabling lake-level linking.
- Hydroscape: name of the Hydroscape region used.
- Lake Name: specific lake identifier.
- General_location_of_core: designation of core location within a lake (deep, littoral, intermediate).
- OSGB36_E and OSGB36_N: UK Ordnance Survey Easting and Northing coordinates (OSGB36 datum) for geolocation.
- Water_depth_at_core_site_(m): water depth from surface to sediment at the core site; measured with a hand-held echo sounder; littoral depth confirmed with a Secchi disc approach.
- Secchi_disc_depth_(m): water clarity measured before coring; mean depth from three readings, taken at the deepest position of the lake.
- Core_length_and_type: core length in metres and the corer type used (Tapper, Big Ben, Livingstone, Renberg) with references clarifying operation.
- Date_core_collected: date of fieldwork and core collection (dd/mm/yyyy).
- UCL_Code: internal UCL code used on bags/database.
- UCL_Sample_ID: internal Amphora code for the entire sample core (unique ID).
- 210 Pb-dated_Y_N_for_Hydroscape: whether the core was dated by 210Pb (Yes/No).

## Metadata, provenance, and methods
- Core and lake metadata are tied to specific field collection details and core systems, enabling reproducibility and provenance tracing.
- Methods details included for depth and Secchi measurements:
  - Water depth measured with a handheld echo sounder; littoral depth cross-checked with Secchi disc method.
  - Secchi depth derived from three measurements, averaged.
- Core type references provided for reproducibility of coring technique.
- Coordinates and regional naming support integration with other datasets (e.g., lake inventories, Hydroscape regions).

## Data governance and sharing
- Dataset uploaded to EIDC (Environmental Information Data Centre) for discovery and access, with a clear data record and portal deployment.
- Uses internal organizational identifiers (UCL_Code, UCL_Sample_ID) to maintain traceability across bags and databases.
- Includes an explicit field on 210Pb dating status, aiding data interpretation and potential embargo or sharing considerations.
- Linkable to waterbody records via WBID and to Hydroscape region data for cross-dataset analyses.

## Quality and caveats
- Units are specified (meters for depths and lengths; coordinates in OSGB36 Easting/Northing).
- Some fields rely on free-text references (corer operation literature) to document methods, which may require standardization for interoperability.
- Dating status (210 Pb) is a binary flag; users may need to consult accompanying results to interpret dating quality and chronology.
- Data completeness depends on field collection conditions and timely data entry (noted stewardship challenges around timely data provision).

## Challenges and considerations for Data Stewards
- Incomplete picture of user needs and priorities may affect dataset curation and discoverability.
- Ensuring timely data intake from multiple data creators and field teams.
- Achieving standardization across diverse systems and formats, including legacy corer metadata and references.
- Managing interoperability between OSGB36 coordinates and other geographic systems; ensuring accurate georeferencing during portal integration.
- Handling updates and ensuring mechanisms are in place to reflect revised core data, dates, or dating results.

## Recommendations for data stewardship
- Validate and standardize critical fields (WBID, OSGB36_E/N, dates, core length, depth measurements, and dating flag) for consistency across datasets.
- Attach and maintain provenance: ensure Core_length_and_type references are consistently linked to the cited literature and accessible.
- Confirm metadata completeness before sharing (e.g., all cores have WBID, Hydroscape, lake name, core collection date, UCL identifiers).
- Maintain data governance around updates: establish a clear process for updating dating results (210Pb) and any revised core metadata.
- Ensure discoverability: maintain cross-references to lake inventories and Hydroscape region datasets; support geospatial queries using OSGB36 coordinates.
- Document data usage rights and any sharing limitations, including embargoes or proprietary considerations.
- Consider adopting or mapping to a standard palaeolimnology metadata schema to improve interoperability with other repositories.