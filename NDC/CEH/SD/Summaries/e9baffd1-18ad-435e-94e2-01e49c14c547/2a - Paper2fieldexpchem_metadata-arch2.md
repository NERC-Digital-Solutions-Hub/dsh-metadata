# Soil core sample data fields and descriptions

- Purpose and use
  - A standardized set of field descriptions for soil core samples, enabling monitoring of soil health and environmental conditions over time through consistent data collection and analysis.

- Core identifiers and site metadata
  - soilcorenumber: Unique identifier for each soil sample/core.
  - site: Field site where the sample is located.
  - depth: Depth of the soil sample from the soil surface.
  - biocharamendment: Indicates whether the sample is un-amended or amended with biochar.
  - treatmentfullname: Full name of the soil treatment (biochar and wetted).
  - dayfromstart: Day from the start of measurements.
  - date: Date of the soil gas flux analysis.

- Context and sampling timing
  - These fields capture when and how the sampling occurred in relation to the experimental timeline (dayfromstart, date, and treatment information).

- Chemical properties
  - pH.water: Soil pH measured in water at a 1:2.5 ratio.
  - total.C.percent: Total carbon content as a percentage of soil mass.
  - total.N.percent: Total nitrogen content as a percentage of soil mass.
  - CN ratio: Ratio of total carbon to total nitrogen in the soil.
  - extract.nh4-n.mgkg: Extractable ammonium (NH4+) in mg/kg.
  - extract.no3-n.mgkg: Extractable nitrate (NO3-) in mg/kg after incubation.

- Physical properties
  - drysoilweightg: Dry weight of the soil in the core (grams).
  - gravwatercontproportion: Gravimetric water content as a proportion.
  - bulkdensitygcm3: Bulk density of the soil (g/cm3).
  - bulkdensitygcm3SE: Standard error of the bulk density (g/cm3).

- Overall data structure
  - The fields collectively describe each soil core’s identity, treatment, sampling context, chemical composition, and physical properties, facilitating standardized analysis and cross-site comparisons.