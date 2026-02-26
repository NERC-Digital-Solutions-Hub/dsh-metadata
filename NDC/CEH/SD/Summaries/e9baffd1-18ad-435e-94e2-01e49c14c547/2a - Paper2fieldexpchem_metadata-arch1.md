# Soil Core Sample Dataset Description

- Purpose
  - Defines the variables for a soil core/gas flux dataset, detailing sample identification, field site, biochar treatment status, depth, timing, and key soil chemical properties.

- Key variables (with concise descriptions)
  - soilcorenumber: Unique identifier for the soil sample/core.
  - site: Field site where the sample is located.
  - biocharamendment: Indicates whether the sample was amended with biochar.
  - depth: Depth of the soil sample from the soil surface.
  - treatmentfullname: Full name of the soil treatment (biochar and wetted).
  - dayfromstart: Days from the start of measurements.
  - date: Date of the soil gas flux analysis.
  - pH.water: pH of the soil in water at a 1:2.5 ratio.
  - total.C.percent: Total carbon content as a percentage.
  - total.N.percent: Total nitrogen content as a percentage.
  - CN ratio: Carbon-to-nitrogen ratio.
  - extract.nh4-n.mgkg: Extractable ammonium (mg/kg).
  - extract.no3-n.mgkg: Extractable nitrate after incubation (mg/kg).
  - drysoilweightg: Weight of the dry soil in grams.
  - gravwatercontproportion: Gravimetric water content as a proportion.
  - bulkdensitygcm3: Bulk density of the soil (g/cm^3).
  - bulkdensitygcm3SE: Standard error of the bulk density (g/cm^3).

- Data collection and structure
  - Likely combines field measurements (site, depth, date) with laboratory analyses (pH, C, N, CN ratio, extractable N forms, bulk density).
  - Includes treatment information to compare amended versus unamended samples (biochar).

- Data quality and provenance considerations
  - Data may require cleaning and standardization when integrating with other datasets.
  - Tracking sources and metadata is important to ensure reproducibility and discoverability.

- Analytical uses and potential analyses
  - Assess correlations between biochar amendment and soil chemical properties (C, N, CN ratio, pH, extractable N, bulk density).
  - Explore temporal trends using dayfromstart and date.
  - Inform models of soil gas flux responses to treatment and soil properties.

- Practical challenges for analysts (perspective aligned with data-centric work)
  - Ensuring data at appropriate local scales and consistent units across fields.
  - Accessing complete datasets and linking this schema to actual gas flux measurements.
  - Managing missing data and integrating with other environmental datasets.