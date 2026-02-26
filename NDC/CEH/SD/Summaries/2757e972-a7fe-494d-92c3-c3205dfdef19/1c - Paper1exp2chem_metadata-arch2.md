# Soil Core Sample Dataset Description

- Overview
  - A dataset describing soil core/sample measurements with identifiers for each sample and treatment.
  - Includes key chemical and physical properties such as pH, carbon and nitrogen content, inorganic nitrogen forms, bulk density, and soil moisture metrics.
  - Some fields appear with placeholders indicating missing descriptions.

- Key fields and meanings
  - soilcorenumber: Individual number assigned to the soil sample/core.
  - soilcorename: Name of the individual soil sample.
  - treatmentfullname: Full name of the soil treatment (biochar and wetted).
  - pH.water: pH of the soil in water at a 1:2.5 ratio.
  - total.C.percent: Total carbon content of the soil as a percentage.
  - total.N.percent: Total nitrogen content of the soil as a percentage.
  - CN ratio: Ratio of total carbon to nitrogen content in the soil.
  - extract.nh4-n.mgkg: Extractable ammonium in the soil (mg/kg).
  - extract.no3-n.mgkg: Extractable nitrate in the soil after the start of incubation (mg/kg).
  - bulkdensitygcm3: Bulk density of the soil (g/cm^3).
  - wfpsproportion: Water-filled pore space (gravimetric water content × (bulk density / total porosity)).
  - whcproportion: Proportion of the maximum water holding capacity of the soil at the time of gas sampling.
  - Additional fields with empty descriptions indicate missing metadata.

- Measurements and outputs
  - Captures soil chemical status (pH, C, N, CN ratio, inorganic N forms) and physical/educational properties (bulk density, moisture metrics) to assess soil health.
  - Data intended for quality assurance, cleaning, and transformation to support standardized analysis.

- Data quality, workflow, and storage
  - Analysts verify data from established sources, perform quality assurance, clean and transform data.
  - Outputs are presented in clear formats (reports, maps, charts).
  - Datasets should be stored properly and uploaded to appropriate data portals to ensure accessibility and reuse.

- Use for environmental monitoring
  - Provides standardized soil health indicators for monitoring environmental conditions and policy performance over time.
  - Facilitates comparison against standards and integration with other environmental datasets.

- Data integration and accessibility (particular challenges)
  - Opportunity to increase dataset value by combining with other relevant data sources (avoiding single-use).
  - Emphasizes enabling access to the underlying data used to produce final outputs.