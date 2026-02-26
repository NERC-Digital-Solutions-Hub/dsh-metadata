# Soil Core Dataset Metadata and Measurements

- Overview
  - A dataset describing individual soil core samples, including treatment status (biochar amendment and wetted treatment), field site, sampling depth, replicate, and sampling time, along with a set of soil chemical and physical measurements collected around incubation.
  - Records are organized by core identifiers and capture both pre-incubation properties and some post-incubation nutrient measurements (e.g., extractable NO3-N after incubation).

- Key variables and descriptions
  - soilcorenumber: Unique identifier for each soil core sample.
  - biocharamendment: Indicates whether the sample is un-amended or amended with biochar.
  - wettedtreatment: Indicates whether the sample was periodically wetted to a high water content.
  - site: Field site where the sample is located.
  - depth: Depth of the soil sample from the soil surface.
  - replicate: Replicate number within the same treatment.
  - timesample: Time at which the sample was taken.
  - pH.water: Soil pH measured in water at a 1:2.5 soil-to-water ratio.
  - total.C.percent: Total carbon content as a percentage.
  - total.N.percent: Total nitrogen content as a percentage.
  - CN ratio: Carbon-to-nitrogen ratio (C/N).
  - extract.nh4-n.mgkg: Extractable ammonium (NH4-N) in mg/kg.
  - extract.no3-n.mgkg: Extractable nitrate (NO3-N) in mg/kg after the start of incubation.
  - drysoilweightg: Dry soil weight in grams.
  - gravwatercontproportion.before: Gravimetric soil water content before incubation (proportion).
  - bulkdensitygcm3.before: Bulk density before the start of incubation (g/cm3).
  - particledensitygcm3: Particle density (g/cm3).
  - totalporosityproportionbefore: Total porosity before incubation, calculated as 1 - (bulk density / particle density).
  - wfpsproportionbefore: Water-filled pore space before incubation, calculated from gravimetric water content, bulk density, and total porosity.

- Structure and scope
  - The dataset spans multiple field sites, depths, times of sampling, and replicates, with clear treatment annotations (biochar amendment and wetted treatment).
  - Focuses on foundational soil properties (chemical and physical) that can be related to treatments and environmental conditions.

- Derived metrics and analysis opportunities
  - CN ratio, total porosity, and water-filled pore space (WFPS) enable analysis of nutrient cycling potential and soil moisture dynamics.
  - Potential analyses include: comparing treatment effects (biochar vs none, wetted vs not) on carbon, nitrogen, pH, and extractable nutrients; exploring how soil physical properties relate to nutrient availability and moisture status; modeling interactions across depth, site, and time.

- Data quality and usability considerations
  - Values include both pre-incubation measurements and post-incubation nutrient data (NO3-N after incubation), requiring careful handling of temporal aspects.
  - Unit consistency is essential (e.g., percent for C/N, mg/kg for nutrients, g/cm3 for densities).
  - Data may be integrated with other datasets; tracking the provenance and metadata is important for reproducibility.

- Practical use for analysts
  - Generate correlations and predictive models linking biochar amendment and wetted treatment to soil chemistry and physical properties.
  - Compare across sites, depths, and sampling times to identify robust treatment effects.
  - Create derived datasets (e.g., standardized CN ratios, porosity-based moisture indices) to inform practical decisions in soil management or environmental studies.