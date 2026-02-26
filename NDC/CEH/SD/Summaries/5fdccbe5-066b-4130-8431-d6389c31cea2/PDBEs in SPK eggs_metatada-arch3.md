# EXPERIMENTAL SECTION

- Study context and sample source
  - Sparrowhawk eggs were collected from nests by licensed egg collectors and archived as part of the Predatory Bird Monitoring Scheme (PBMS) in the UK.
  - Sampling focused on the longest temporal period within the smallest geographical area: eastern England within 250 km of the Welsh border.
  - Sampling years spanned 1985–2007; for each year, 3–5 eggs from different nests were analysed, with random selection when multiple eggs existed from the same nest.
  - A total of 10 sampling years provided sufficient eggs for analysis.

- Egg measurement and preparation
  - Measured egg weight, length, and breadth; eggs were blown or cracked for contents.
  - Shells were washed, air-dried, and reweighed; contents were homogenised and stored at -20°C until analysis.
  - Egg weight and lipid content: mean wet weight = 1.98 ± 0.34 g; mean lipid content = 8.35 ± 6.30% (n = 43).

- PBDE analysis
  - Eggs were analysed for 27 PBDE congeners (tri-Octa BDEs) using Gas Chromatography–Mass Spectrometry (GC-MS) with a 30 m CPSIL-8 CB column.
  - Calibration used seven PBDE standards (2.5–250 pg/μL); instrument LODs ranged from 2.5 pg/μL (tri-hexa BDEs) to 12.5 pg/μL (Octa BDEs), corresponding to egg LODs of 0.0631–0.316 pg/g wet weight.
  - Five procedural blanks were run per batch; samples were blank-corrected.
  - Mean recoveries for 13128 C12-labelled congeners (28, 47, 99, 100, 153, 154, 183) ranged 73.4–95.6%; concentrations were recovery-corrected.
  - Quality control (QC) standard containing five PBDEs (tri-hepta homologues) analysed at 2.5–250 pg/μL; batches passed QC if concentrations were within ±10% of expected values.
  - During analysis, three additional potential octa-BDEs (BDEs 201, 202, 203) were detected within a distinctive pattern along with known octa homologues (196 and 197). These were tentatively identified as BDEs 201, 202, 203 and treated as such; due to lack of calibration standards for these three, their concentrations were semi-quantified using calibration curves for BDEs 196 and 197.

- Data handling and corrections
  - PBDE concentrations (congeners and ΣPBDE) were expressed on a wet-weight basis and desiccation-corrected by multiplying by the total egg weight/volume ratio.
  - Egg volume was estimated using V = 0.51 × LB² (L = length, B = breadth); if eggs were damaged and volumes could not be calculated, the mean volume/weight ratio from other eggs that year was used.
  - Shell index (shell thickness proxy) was calculated as shell weight (mg) divided by (shell length × breadth in mm).

- Handling of measurements below detection limits
  - For congeners with concentrations below the LOD across some eggs, values below the LOD were interpolated only when the proportion of below-LOD observations was ≤20%; for congeners with >20% below-LOD observations, those datasets were not analysed.
  - For ΣPBDE calculations, concentrations below the LOD were assigned a value of zero.

- Statistical treatment and modelling
  - Data for individual congeners and ΣPBDE were skewed; Box-Cox transformations were applied to achieve normality for statistical tests.
  - Relationships between ΣPBDEs, individual congeners, and shell index were assessed using Pearson correlation.
  - Temporal trends were evaluated with linear, quadratic, or split-line regressions; model selection guided by Akaike Information Criterion (AIC).
  - Models incorporated potential explanatory variables including time, land use, and human population density, using linear or polynomial regression approaches.
  - Population density near nest sites was estimated using a sphere-of-influence approach at 200 m resolution based on the 2001 UK census. The exposure metric A was calculated as A = Σ(pop_i / r_i^2), where r_i is the distance from the nest to population centroids.
  - Land use around the nest (within a 10 km radius) was classified from the 2000 UK Land Cover Map (1 km resolution) into five groups (urban, arable, grassland, woodland, semi-natural). Analyses used both the percentages of each class and the dominant class within the radius.
  - The land-use and population-density variables were used to model associations with ΣPBDE and individual congeners to understand spatial and temporal drivers of exposure.