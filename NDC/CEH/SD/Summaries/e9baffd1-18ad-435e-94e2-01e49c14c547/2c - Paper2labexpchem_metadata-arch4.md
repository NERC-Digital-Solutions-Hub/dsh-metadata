# Soil Core Sample Data Dictionary

- Purpose: Defines the fields that describe soil core samples used in an incubation context, enabling tracking of sample identity, treatments, location, depth, timing, and chemical/physical properties before incubation.

- Key variables and meanings
  - soilcorenumber: Unique identifier for the soil sample/core
  - biocharamendment: Indicates if the sample is un-amended or amended with biochar
  - wettedtreatment: Indicates if the sample is periodically wetted to a high water content
  - site: Field site where the sample is located
  - depth: Depth of the soil sample from the soil surface
  - replicate: Replicate number within the same treatment
  - timesample: Time of sampling
  - pH.water: Soil pH measured in water at a 1:2.5 ratio
  - total.C.percent: Total carbon content as a percentage
  - total.N.percent: Total nitrogen content as a percentage
  - CN ratio: Ratio of total carbon to total nitrogen
  - extract.nh4-n.mgkg: Extractable ammonium in mg/kg
  - extract.no3-n.mgkg: Extractable nitrate in mg/kg after incubation start
  - drysoilweightg: Dry soil weight in grams
  - gravwatercontproportion.before: Gravimetric water content as a proportion before incubation
  - bulkdensitygcm3.before: Bulk density before incubation (g/cm3)
  - particledensitygcm3: Particle density (g/cm3)
  - totalporosityproportionbefore: Total porosity before the incubation (computed as 1 - (bulk density / particle density))
  - wfpsproportionbefore: Water-filled pore space before incubation (gravimetric water content × (bulk density / total porosity))

- Data structure and units
  - Mix of percentages, mg/kg, grams, and dimensionless proportions
  - Many pre-incubation metrics provide context for subsequent analyses

- Data quality and governance considerations for Data Leaders
  - Ensure consistent naming, units, and comprehensive metadata for discoverability
  - Validate for missing values and clearly document any derived fields (e.g., CN ratio, total porosity)
  - Capture provenance: site, depth, replicate, timesample, and treatment details (biochar status, wetted) for reproducibility
  - Promote standardization of measurement methods (e.g., pH in water at specified ratio) to enable cross-site comparisons

- Practical uses and implications
  - Assess how biochar amendment and moisture regimes influence soil chemistry and physical properties
  - Enable cross-site, depth-specific, and time-point comparisons in incubation studies
  - Inform data-driven decisions in soil management and research networks through well-documented data products