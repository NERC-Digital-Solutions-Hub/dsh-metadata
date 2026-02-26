# PBDE concentrations in sparrowhawk eggs from the Predatory Bird Monitoring Scheme (PBMS) in the UK: Experimental methods and statistical analyses

- Objective
  - Describe the sampling, analytical methods, and statistical approaches used to assess PBDE concentrations in sparrowhawk eggs from the PBMS archive (1985–2007) and to examine relationships with nest environment and temporal trends.

- Sampling and egg handling
  - Eggs were from failed or abandoned sparrowhawk nests collected by licensed egg collectors and archived under the PBMS.
  - Selection aimed to cover the longest temporal span with the smallest geographic area (east England within ~250 km of the Welsh border).
  - Ten sampling years (1985–2007) with 3–5 eggs per year, each from a different nest; random selection if multiple eggs existed per nest.
  - Egg contents homogenised; aliquots stored at -20°C after shell washing, air-drying, and reweighing.

- PBDE analysis and congeners
  - Analyzed 27 PBDE congeners using GC-MS with a 30 m CPSIL-8 CB column; calibration with seven PBDE standards (2.5–250 pg/μL).
  - Instrument detection limits (LoD) ranged from 2.5 pg/μL for tri-hexa BDEs to 12.5 pg/μL for Octa BDEs; corresponding egg wet-weight LoDs calculated.
  - Five C12-labeled PBDE recoveries (congeners 28, 47, 99, 100, 153, 154, 183) ranged 73.4–95.6% and were used to correct concentrations.
  - Quality control (QC) standard with five PBDEs tested in each batch; pass criteria within ±10% of expected values.
  - During the study, five additional potential octa-BDEs were detected (BDEs 201, 202, 203) alongside known octa homologues (196, 197); pattern supported identification; concentrations of 201–203 were semi-quantified using calibration curves for 196/197 due to lack of standards.

- Data quality and handling below detection
  - Concentrations below LoD were recorded; for statistical analyses, values below LoD were interpolated for congeners with <20% below-LoD across eggs; not interpolated if >20%.
  - Sum of PBDEs (ΣPBDE) calculated from detected congeners, with below-LoD values assigned zero for the sum.
  - Some eggs were damaged, so volume/weight adjustments used year-wide mean values when needed.

- Desiccation and shell measurements
  - Wet-weight concentrations corrected for desiccation by multiplying by total egg weight/volume ratio.
  - Egg volume estimated as V = 0.51 × LB^2 (L = length, B = breadth).
  - Shell index (shell thickness proxy) calculated as shell weight (mg) / (shell length × breadth).

- Statistical analyses and modeling
  - Data transformed for normality (Box-Cox) due to skewness.
  - Associations assessed with Pearson’s correlation for ΣPBDE and congeners against shell index.
  - Temporal trends evaluated with linear, second-order polynomial, or split-line (segmented) regression; model fit assessed using AIC.
  - Relationships with time, land use, and human population density modeled via linear or polynomial regression.
  - Analyses including shell index restricted to undamaged eggs.
  - Population density around nest sites estimated with a “sphere of influence” approach (200 m resolution) using 2001 UK census data:
    - A = sum(pop_i / r_i^2), where r_i reflects Euclidean distance components from nest to population cell centroids.
  - Land use around nests (within a 10 km radius, approximating foraging range) classified from the 2000 UK Land Cover Map:
    - Five classes: urban, arable, grassland, woodland, semi-natural.
    - Used as both: (i) percentages of the area by class, and (ii) a majority-class indicator.
  - Land-use data and population density used to model ΣPBDE and individual congeners.

- Context and references
  - Methods draw on established PBDE analytical and statistical practices, with cited sources for LC methods, calibration, quality control, handling below-detection data, and ecological context of sparrowhawk foraging and nesting.

- Key notes and limitations
  - Identification of novel octa-BDE congeners relied on chromatographic patterns and qualifier ions rather than full standards.
  - Data handling for damaged eggs and missing volumes required approximations, potentially contributing to uncertainty in shell index and volume-related calculations.
  - The study integrates environmental exposure data with spatial-temporal context (population density and land use) to explore drivers of PBDE patterns in top avian predators.