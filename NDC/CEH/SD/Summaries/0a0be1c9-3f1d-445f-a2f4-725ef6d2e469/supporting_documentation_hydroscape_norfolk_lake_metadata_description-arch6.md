# File Uploaded to EIDC: hydroscape_norfolk_core_metadata.csv

## Overview
- Provides metadata for Hydroscape Norfolk lake core samples, intended to support palaeolimnology research.
- Data is stored as an EIDC CSV with a set of standardized fields describing each core and its context.
- Core information includes location, depth, sampling details, dating status, and internal identifiers.

## Key Data Fields and Descriptions
- EIDC File Name: File name uploaded to EIDC (.csv).
- WBID: Waterbody Identification number; links to lake records (e.g., via CEH Lakes index).
- Hydroscape: Name of the Hydroscape region used for the sample.
- Name: Lake Name.
- General location of core: Indicates cores were collected from the central (often deepest) area of the lake.
- OSGB36_E / OSGB36_N: Easting and Northing coordinates in UK OSGB36 datum.
- Water depth at core site (m): Depth from water surface to sediment surface at the core site.
- Core length and type: Length of the core in metres and its type.
- Corer types: References for corer types used (e.g., Big Ben, Livingstone) with full literature citations.
- Date core collected: Fieldwork date; if precise date is unknown, only the year may be shown.
- UCL_Code: Internal University College London code used on bags/database.
- UCL Sample ID: Internal Amphora code for the entire sample core (unique ID).
- 210 Pb-dated (Y/N) for: Indicates whether the core is dated by 210Pb.
- Hydroscape (additional field): [Description cut off in the provided text; appears to be a secondary reference field.]

## Data Quality and Provenance
- Standardized structure: clearly defined fields intended to support data discovery and cross-referencing (e.g., WBID, OSGB36 coordinates).
- Coordinate system: OSGB36 for spatial references.
- Dating information: Includes explicit indicator for 210Pb dating, enabling assessment of chronology reliability.
- Internal identifiers: UCL_Code and UCL Sample ID facilitate tracking within data custody and analyses.
- Documentation depth: Field descriptions are present for most items, but the Hydroscape field description is incomplete in the provided text, indicating potential gaps in metadata coverage.
- Data variation: Information spans multiple cores and potentially multiple dates, corer types, and sampling schemes, requiring careful harmonization when merging with other datasets.

## How This Data Supports the Data Support Archetype
- Enables data discovery and self-service exploration: core metadata can be mapped, filtered, and visualized (e.g., by Hydroscape region, lake, depth, or dating status).
- Facilitates data combination: common keys (WBID, UCL_Code, UCL Sample ID) allow joining with other datasets (e.g., lake characteristics, core analyses, or dating results).
- Supports data products: can underpin dashboards and reports showing core locations, sampling depth distributions, and dating coverage across Norfolk Hydroscape lakes.
- Encourages data quality improvements: explicit documentation of corer types and dating enables cross-referencing with literature and replication of sampling methods.

## Potential Uses and Applications
- Spatial analyses and mapping of core locations within the Hydroscape Norfolk region.
- Linking core metadata to palaeolimnological results (e.g., sediment proxy data, 210Pb dating outcomes).
- Tracking data provenance and internal coding schemes for data governance.
- Building user-friendly dashboards (self-serve) to explore cores by lake, region, depth, and dating status.

## Challenges and Considerations for Users
- Incomplete field descriptions: some metadata (e.g., Hydroscape description) appears truncated, which may require consultation of original records or additional documentation.
- Varied data formats: data spans multiple cores with different sampling histories and corer types; harmonization may be needed for comparative analyses.
- Data freshness and provenance: reliance on EIDC uploads means ongoing updates may occur; verify versioning and source references when performing longitudinal studies.

## Recommendations for Data Consumers
- Use WBID and UCL identifiers to join with supplementary datasets (e.g., lake characteristics, regional metadata).
- Validate coordinates against OSGB36 GIS layers and consider reprojecting if integrating with other coordinate systems.
- Check 210Pb dating status before chronological interpretation; annotate analyses with the presence or absence of dating.
- Seek or request complete metadata for any fields with incomplete descriptions (notably Hydroscape field) to ensure full contextual understanding.
- Consider creating a dashboard or pivoted reports that allow self-service exploration by Hydroscape region, lake name, core depth, and dating status.