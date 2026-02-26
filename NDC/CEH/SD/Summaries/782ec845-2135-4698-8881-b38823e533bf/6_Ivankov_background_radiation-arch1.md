# Metadata for 6_Ivankov_background_radiation.csv

- Purpose of the metadata: Describes the structure and meaning of columns in the associated CSV dataset that captures background radiation measurements around Ivankov.
- Location data
  - latitude: Site latitude in decimal degrees; GPS data captured with Garmin GPSmap 78S using the WGS-84 system; stated accuracy of 10 m or less.
  - longitude: Site longitude in decimal degrees; same GPS/WGS-84 details and accuracy.
- Site identification and sampling scope
  - Explanation.Site identifier: Indicates the location of the sampling site (used in both latitude and longitude rows for context).
  - Sampling_site_description: Habitat type for the site; note that seven sites were inaccessible but are retained in the data for completeness.
- Analysis configuration
  - Analysis_type_1_or_2: Indicates whether the site is for both dose measurement and soil sampling (1) or for dose measurement only (2).
- Dose measurement details
  - at_0.1m: Ambient equivalent dose rate measured at 0.1 meters above ground; measured with certified gamma-beta irradiation dosimeters (RKS-01, Stora-TU, Ukraine).
  - at_1m: Ambient equivalent dose rate measured at 1 meter above ground; measured with the same dosimeters as at_0.1m.
- Data quality and methodology notes
  - All latitude and longitude values are decimal degrees.
  - Dosimetry details specify the measurement height, dosimeter type, and source of the dosimeters.
  - The “Notes” fields accompanying columns largely indicate n/a, except for the GPS/data source notes and the site accessibility remark for habitat description.