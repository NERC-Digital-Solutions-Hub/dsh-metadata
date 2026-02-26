# Explanation of data sheet - soil_profile_data.csv

- Purpose and scope
  - Documents soil profile data collected along a transect in the Siksik catchment, North West Territories, Canada.
  - Includes sample identifiers, location (latitude/longitude), depth ranges, pH, bulk density, and related metadata.
  - Indicates that some samples have had 14C analyses conducted.

- Geographic and temporal context
  - Country: Canada; region: North West Territories.
  - Coordinates: approximately 133°26'26"W, 68°44'17"N.
  - Elevation: 85 m.
  - Sampling date: September 2014.

- Dataset structure and key fields
  - sample: sample identification number (1 to 64).
  - location: soil profile identification; note that 14C analysis may be linked to specific samples.
  - depth_1: upper depth of sampling depth (cm).
  - depth_2: lower depth of sampling depth (cm).
  - ph: pH measured using a 1:5 soil:water suspension method.
  - bulk_density_gcm3: soil bulk density (g/cm^3), determined per Blake and Hartge (1986).
  - longitude: location within the Siksik catchment (transect context).
  - latitude: location within the Siksik catchment (transect context).

- Measurement methods and standards
  - Bulk density measured following Blake and Hartge (1986) in the Methods of Soil Analysis Part 1.
  - pH measured via 1:5 soil:water suspension method; reference provided to NSW soil testing method for pH.
  - Column headings and units explicitly defined in the data sheet (Explanation vs. Units).

- Data provenance and references
  - Materials and Methods specify sampling along a transect and recording of depth and geographic coordinates.
  - Key reference: Blake, G., Hartge, K., 1986. Bulk density: 13. In Klute, A. (Ed.), Methods of Soil Analysis: Part 1.
  - Additional reference for pH method: NSW soil test methods (phw.pdf).

- Metadata and usage notes for data leaders
  - The sheet includes explicit metadata fields (sample, location, depth_1, depth_2, ph, bulk_density_gcm3, longitude, latitude) with definitions and units.
  - Indicates the broader aim of documenting soil properties along transects for later analysis and potential cross-reference with 14C data.
  - Useful for ensuring data discoverability, proper attribution, and alignment with data standards (clear definitions, units, and provenance).