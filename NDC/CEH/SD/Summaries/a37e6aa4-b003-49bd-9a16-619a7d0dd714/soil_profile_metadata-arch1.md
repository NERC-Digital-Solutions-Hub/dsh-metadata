# soil_profile_data.csv

- Overview
  - A soil profile dataset collected along a transect in the Siksik catchment, North West Territories, Canada.
  - Samples collected in September 2014; data describe soil profile properties across depths and locations.
  - Includes identifiers for samples and soil profiles, presence of 14C analysis indicators, and dominant plant community names (P1–P10).

- Data fields (columns)
  - sample: Sample identification number (1 to 64).
  - location: Soil profile identification; indicates whether 14C analyses were carried out; associated dominant plant community names.
  - depth_1: Upper depth of the sampling interval (cm).
  - depth_2: Lower depth of the sampling interval (cm).
  - ph: pH (method described below).
  - Bulk_density_gcm3: Bulk density (g/cm3).
  - longitude: Location of sampling within the Siksik catchment (arc or projected coordinate).
  - latitude: Location of sampling within the Siksik catchment.
  - elevation (m): Elevation in metres.
  - column_heading: Explanatory label for the column (contextual metadata).
  - units: Units corresponding to the column (e.g., centimetres, grams per cubic centimetre).
  - Notes indicate that some fields are placeholders or require explanation (e.g., “Explanation of data sheet - soil_profile_data.csv”).

- Sampling and measurement methods
  - Bulk density: Determined according to Blake and Hartge (1986).
  - pH: Measured using a 1:5 soil:water suspension method (reference to NSW soils test methods provided).
  - Sampling design: Soil samples collected along a transect; sampling location recorded by latitude/longitude and sediment depth ranges.

- Location and metadata
  - Country: Canada (some entries show placeholders, e.g., “Country, = .”).
  - State/Region: North West Territories (some entries show placeholders, e.g., “State, = .”).
  - Coordinate details: Longitude 133.26.26"W and Latitude 68.44.17"N (as example values); Elevation around 85 m.
  - Additional context: The data sheet notes that soil profiles along a transect are identified as P1–P10 by dominant plant community.

- References
  - Blake, G., Hartge, K. (1986). Bulk density: part of Methods of Soil Analysis, Part 1 (Blake and Hartge method cited in Klute, A., Ed.).
  - Method details for bulk density are from standard soil analysis literature (Klute 1986).

- Potential uses and considerations
  - Analyses of how soil properties (pH, bulk density) vary with depth and along the transect.
  - Opportunities to explore correlations between soil properties and plant community context or location within the catchment.
  - Data can support predictive modeling of soil carbon/nutrient dynamics across depths and spatial locations.
  - Data quality considerations: some fields appear to contain placeholders or incomplete entries (e.g., country/state), and clear documentation of column meanings is present but may require alignment when combining with other datasets.
  - Provenance and reproducibility: methods referenced enable replication or cross-study comparison; coordinates and sampling details facilitate spatial analyses.