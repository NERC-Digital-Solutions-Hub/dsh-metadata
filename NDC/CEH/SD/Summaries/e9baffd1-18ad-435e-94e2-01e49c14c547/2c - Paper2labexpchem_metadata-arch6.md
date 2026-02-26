# Soil Core Sample Dataset Variable Descriptions

- Purpose of dataset
  - Aims to capture soil core sample data across treatments (biochar amendment, wetted vs not), sites, depths, and timepoints to enable exploration, analysis, and data products (dashboards, reports) for end users.

- Key data structure
  - Metadata
    - soilcorenumber: Unique identifier for each soil core sample.
    - biocharamendment: Indicates whether the sample is amended with biochar.
    - wettedtreatment: Indicates whether the sample underwent periodic wetting to a high water content.
    - site: Field site where the sample is located.
    - depth: Soil depth from the soil surface for the sample.
    - replicate: Replicate number within the same treatment group.
    - timesample: Timepoint at which the sample was collected.
  - Physical and chemical measurements
    - pH.water: Soil pH measured in water at a 1:2.5 soil-to-water ratio.
    - total.C.percent: Total carbon content of the soil as a percentage.
    - total.N.percent: Total nitrogen content of the soil as a percentage.
    - CN ratio: Ratio of total carbon to total nitrogen in the soil.
    - extract.nh4-n.mgkg: Extractable ammonium (NH4+-N) in mg/kg.
    - extract.no3-n.mgkg: Extractable nitrate (NO3--N) in mg/kg after incubation starts.
    - drysoilweightg: Dry soil weight in grams for the core sample.
  - Pre-incubation physical properties (baseline measurements)
    - gravwatercontproportion.before: Gravimetric water content as a proportion before incubation.
    - bulkdensitygcm3.before: Bulk density of the soil before incubation (g/cm3).
    - particledensitygcm3: Particle density of the soil (g/cm3).
    - totalporosityproportionbefore: Total porosity of the soil before incubation, computed as 1 - (bulk density / particle density).
    - wfpsproportionbefore: Water-filled pore space before incubation, calculated as gravimetric water content × (bulk density / total porosity).

- Key insights enabled by the data
  - Compare chemical and physical soil properties across biochar treatments, wetted vs non-wetted treatments, sites, depths, and timepoints.
  - Assess relationships such as CN ratio with extractable N forms (NH4+-N, NO3--N) and how these relate to porosity and water content.
  - Support creation of self-serve data products (dashboards, pivot tables) to monitor soil health indicators and treatment effects over time.
  - Facilitate quality assurance and data transformations, including unit consistency, handling missing values, and deriving additional metrics as needed.

- Data quality and use considerations for data support
  - Ensure consistent units across samples (e.g., percent for C/N, mg/kg for inorganic N, g/cm3 for densities).
  - Verify alignment of timesample with incubation start points and treatment labels (biochar amendment, wetted treatment).
  - Pay attention to potential missing values in any of the measurements and metadata fields, especially for replicate and site/depth combinations.
  - Maintain clear provenance for derived variables (e.g., how totalporosityproportionbefore and wfpsproportionbefore were computed) to support reproducibility.