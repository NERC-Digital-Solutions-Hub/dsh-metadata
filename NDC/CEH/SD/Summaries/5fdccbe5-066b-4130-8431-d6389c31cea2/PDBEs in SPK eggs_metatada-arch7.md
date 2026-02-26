# EXPERIMENTAL SECTION Egg sampling and analysis

## Overview
- Investigates PBDEs in sparrowhawk eggs from the Predatory Bird Monitoring Scheme (PBMS) archive in England, focusing on a region east of England within 250 km of the Welsh border.
- Temporal window: 1985–2007; sampling years chosen based on archive availability to cover the longest period with eggs from different nests (3–5 eggs per year).
- Random selection of eggs when multiple eggs existed from the same nest (laying order not known).

## Sampling and sample processing
- Eggs collected from licensed collectors as part of PBMS monitoring.
- Measurements: wet weight, length, breadth; shells were washed, air-dried, and reweighed; contents homogenised and stored at -20°C.
- From the PBMS archive, eggs were selected to maximize temporal coverage within the specified geographic area.
- Sample size: 43 eggs with mean wet weight 1.98 ± 0.34 g and mean lipid content 8.35 ± 6.30%.

## Laboratory analysis
- PBDEs extracted, cleaned, and analysed by Gas Chromatography-Mass Spectrometry (GC-MS) using defined equipment and a 30 m CPSIL-8 CB column.
- Analyzed for 27 PBDE congeners (tri-Octa BDEs: 17, 28, 32, 35, 37, 47, 49, 51, 66, 71, 75, 77, 85, 99, 100, 118, 119, 126, 128, 138, 153, 154, 166, 183, 190, 196, 197).
- Calibration with seven PBDE standards; instrument LoD ranged from 2.5 pg/μL (tri-hexa BDEs) to 12.5 pg/μL (Octa BDEs); LoD converted to pg/g wet weight.
- Five procedural blanks per batch; sample concentrations blank-corrected.
- Recovery for 13128 C12 labelled congeners 28, 47, 99, 100, 153, 154, 183 ranged 73.4–95.6% and were recovery-corrected.
- QC standard with five PBDEs (2.5–250 pg/μL) used to ensure precision; batches passed QC if concentrations were within ±10% of expected values.
- During the study, three additional potential octa-brominated PBDEs detected (BDEs 201, 202, 203) with characteristic mass fragments; semi-quantified using calibration curves for BDEs 196 and 197 due to absence of calibration standards.

## Data handling and quality control
- Concentrations corrected for desiccation using total egg weight/volume ratio; egg volume estimated as V = 0.51 × L × B².
- Damaged eggs led to using mean volume/weight ratio from other eggs that year when possible.
- Eggshell index calculated as shell weight (mg) / (shell length × breadth in mm).
- Values below the LoD were interpolated for congeners with <20% below-LoD observations; not interpolated for congeners with >20% below-LoD or for analyses on those datasets.
- ΣPBDE concentrations computed by summing detected congeners; concentrations below LoD treated as zero in the sum.
- Data skew addressed with Box-Cox transformation prior to statistical analyses.

## Statistical analyses
- Associations between ΣPBDEs/congeners and shell index assessed with Pearson’s rank correlation.
- Temporal trends evaluated using linear, quadratic, or split-line regressions.
- Relationships with time, land-use, human population density, and eggshell thickness modelled with linear or polynomial regression.
- Model suitability assessed via Akaike Information Criterion (AIC).
- Analyses involving shell index restricted to samples with reliably calculated shell index (undamaged eggs).

## GIS data and spatial covariates
- Human population density near nest sites estimated using the sphere-of-influence approach at 200 m resolution, based on the 2001 UK census.
- Land use within a 10 km radius around each nest derived from the UK Land Cover Map (2000) at 1 km resolution; five classes condensed to urban, arable, grassland, woodland, semi-natural.
- Land-use metrics used both as percentages (within the 10 km radius) and as the dominant land-use class for modelling ΣPBDE and individual congeners.

## Notes on data and reproducibility
- PBMS archive provided nest-level spatial context; QC and recovery standards ensured measurement reliability.
- Identification of additional octa-BDEs (201, 202, 203) acknowledged with semi-quantification due to calibration gaps.