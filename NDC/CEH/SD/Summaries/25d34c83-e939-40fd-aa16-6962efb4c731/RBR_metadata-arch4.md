# Water temperature measurements from Durleigh Reservoir 2018 - RBR SoloT

- Overview
  - Metadata and basic characteristics of water temperature measurements from Durleigh Reservoir in 2018 using an RBR SoloT temperature chain.
  - Data are organized as a depth-variant temperature record with 10-minute sampling intervals over the study period.

- Data details
  - Location: latitude 51.1210, longitude -3.0403
  - Instrumentation: RBR SoloT thermistors positioned at 1 m depth intervals along a chain from surface (0 m) to bottom (6 m)
  - Sampling cadence: every 10 minutes
  - Time period: 22/02/2018 to 05/10/2018
  - Time format: dd/mm/yyyy HH:MM
  - Units: degrees Celsius (°C)
  - Depth coverage: includes depths from 0 m to 6 m; reported at each 1 m interval
  - Data missing: missing data for thermistors at 1 m, 2 m, and 3 m depths due to corrupted files downloaded from the thermistors
  - Deployment and authorship: deployed by Emily Slavin and Danielle Wain
  - Reference: Slavin, E.I., Wain, D.J. 2018. Water temperature measurements from Durleigh Reservoir 2018

- Data quality and gaps
  - Gaps exist specifically at depths 1–3 m due to corrupted downloads
  - Indicates potential data availability issues at mid-depths and highlights the need for data integrity checks during ingestion and download

- Provenance and metadata
  - Clear attribution to the two deployers and a formal citation for the dataset
  - Provides precise location, instrumentation setup, depth coverage, sampling interval, and temporal window

- Implications for data strategy (Data Leaders)
  - Ensure robust data integrity workflows to prevent loss of mid-depth data during downloads
  - Maintain comprehensive metadata for each depth channel and sensor to support discovery and reuse
  - Implement validation checks for completeness across all depth intervals before release
  - Consider redundancy or backup procedures for critical measurements to avoid data gaps
  - Facilitate access pathways to raw and processed data, accounting for potential file corruption issues
  - Document provenance and deployment details to support reproducibility and collaboration with partners (e.g., the original deployers)