# EXPERIMENTAL SECTION Egg sampling and analysis

- Study and sample collection
  - Eggs collected from sparrowhawk nests as part of the Predatory Bird Monitoring Scheme (PBMS) in the UK.
  - Selection criteria aimed to cover the longest temporal period within the smallest possible geographic area: east England within 250 km of the Welsh border.
  - Timeframe: 1985–2007, with 10 sampling years available.
  - For each sampling year, 3–5 eggs from different nests; if multiple eggs were from the same nest, one egg was chosen at random (laying order unknown).
  - Measured egg metrics: wet weight, length, breadth; eggs were blown/cracked, shells washed and reweighed; contents homogenised and stored at -20°C.

- Laboratory analysis (PBDEs)
  - Samples homogenised and analysed for 27 PBDE congeners (tri- to octa-BDEs: 17, 28, 32, 35, 37, 47, 49, 51, 66, 71, 75, 77, 85, 99, 100, 118, 119, 126, 128, 138, 153, 154, 166, 183, 190, 196, 197).
  - GC-MS method with a 30 m CPSIL-8 CB column; calibration with seven PBDE standards (2.5–250 pg/μL range).
  - Instrument LoD ranged from 2.5 pg/μL (tri-hexa BDEs) to 12.5 pg/μL (Octa BDEs); equivalent to egg wet-weight LoDs of 0.063–0.316 pg/g.
  - Blank-corrected data; recoveries for 13128 C12-labelled congeners: 73.4–95.6% (recovery-corrected).
  - Quality control: included a QC standard with five PBDEs; pass if concentrations within ±10% of expected.

- Identification of additional congeners
  - During analysis, three additional potential octa-BDEs (BDEs 201, 202, 203) were detected alongside known octa congeners (including BDE-196/197).
  - Confirmation based on distinctive mass fragments and qualifier ions; concentrations for 201–203 were semi-quantified using calibration curves for BDEs 196/197 (calibration standard not available for 201–203).

- Data processing and corrections
  - PBDE concentrations reported on a wet weight basis and corrected for desiccation using total egg weight/volume.
  - Egg volume estimated as V = 0.51 × L × B^2 (L = length, B = breadth); damaged eggs used the mean volume/weight ratio from undamaged eggs of that year when needed.
  - Shell index calculated as shell weight (mg) / (shell length × breadth).
  - Handling concentrations below the detection limit
    - For congeners with <20% below LoD across all eggs: interpolate missing values.
    - For congeners with ≥20% below LoD: do not conduct statistical analyses on those datasets.
  - ΣPBDE calculated as the sum of detected congeners; concentrations below LoD assigned a value of zero in this sum.
  - Data distributions were skewed; Box-Cox transformations applied to enable normality assumptions for statistical tests.

- Statistical analyses
  - Relationships among ΣPBDEs, individual congeners, and shell index assessed with Pearson’s rank correlation.
  - Temporal trends analyzed with linear, quadratic (second-order), or split-line regressions.
  - Models relating concentrations to time, land-use, population density, and eggshell thickness implemented via linear/polynomial regression.
  - Model suitability evaluated using Akaike Information Criterion (AIC).
  - Analyses involving shell index restricted to eggs with reliably calculated shell index (undamaged eggs).

- Population density and land-use context
  - Human population density near nest sites estimated using the sphere of influence approach at 200 m resolution, based on the 2001 UK census.
  - Land use within a 10 km² area around each nest (foraging range) classified via GIS from the 2000 UK Land Cover Map at 1 km resolution.
  - Land-use categories condensed to five groups: urban, arable, grassland, woodland, semi-natural; inputs used as both:
    - Percent composition within the area
    - Overall majority land-use class

- Notes and references
  - Descriptions and criteria include sampling year availability, nest-based sampling, and region focus.
  - References cited for methods and contextual data (sampling design, analytical methods, and land-use/population data frameworks).