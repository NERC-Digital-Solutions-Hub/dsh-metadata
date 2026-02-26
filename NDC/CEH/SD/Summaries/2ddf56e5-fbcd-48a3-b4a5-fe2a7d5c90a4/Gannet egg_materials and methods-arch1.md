# 2.1. Egg sampling and analysis

- Study design
  - Fresh eggs collected from ten gannet nests across two Scottish colonies (Ailsa Craig and Bass Rock) in two sampling years.
  - Measurements: egg weight, length, breadth; eggshells washed, air-dried, reweighed; contents homogenised and stored at -20 °C.
  - PBDE analysis: a random sub-group of five eggs per sampling year for each colony selected for PBDE analysis.

- PBDE analytical workflow
  - Sub-sample preparation: 2 g sub-sample of egg homogenate; spiked with 13C12-labelled recovery standard (final 50 pg/µL).
  - Extraction and cleanup: soxhlet extraction in dichloromethane; lipid content determined gravimetrically; two-step cleanup (acidified silica column elution with hexane; followed by gel permeation chromatography with biobeads; final fraction concentrated and placed in GC vial with keeper).
  - Instrumental analysis: GC-MS (EI mode) with a CPSIL-8 CB column; calibration with seven PBDE standards (2.5–250 pg/µL range); analyzed for 25 PBDE congeners (list includes 17, 28, 32, 35, 37, 47, 49, 66, 71, 75, 77, 85, 99, 100, 119, 138, 153, 154, 166, 183, 190, 196, 197) plus two additional congeners (51, 128 from AccuStandard).
  - Sensitivity and quality: instrument LODs ranged from 2.5 to 12.5 pg/µL; average egg LOD-equivalents in ng/g wet weight per congener (0.061–0.305 ng/g). Fourteen procedural blanks per batch; blank concentrations below LOD. Recovery for 13C12-labelled congeners 28, 47, 99, 100, 153, 154, 183 ranged 68–83%. Concentrations corrected for recovery using deuterated analogue.
  - Quality controls: QC standard (five PBDEs across tri-hepta homologues) run with unknowns; batches deemed acceptable if QC concentrations within ±10% of expected.
  - Notes on scope: Nona BDEs and BDE209 not measured due to poor recovery with the method used. DecaBDE data from PBMS archive existed for a sub-series of 12 gannet eggs and were below detection in all samples.

- Data handling and reporting
  - Concentrations reported on a wet weight basis and desiccation-corrected by multiplying by total egg weight/volume ratio.

- References for methods
  - Hoyt (1979) for volume estimation
  - Decabromodiphenylether and hexabromocyclododecane studies and related PBDE work cited for context

# 2.2. Statistical analyses

- Data preparation
  - PBDE concentrations (congeners and ΣPBDE) treated on a wet weight basis and corrected for desiccation.
  - Egg volume estimated via V = 0.51 × L × B^2 (L = length, B = breadth).
  - Damaged eggs adjusted using mean volume/weight ratios when possible; three eggs excluded where volume/weight ratios exceeded 3 standard deviations.
  - Shell index defined as shell weight (mg) divided by (shell length × shell breadth) (mm).

- Congener sums and value handling
  - ΣPBDE calculated as the sum of all 25 determined congeners; concentrations below LoD set to zero.
  - All data log10-transformed to satisfy homogeneity of variance and normality assumptions.

- Analyses
  - Temporal trends: General Linear Model (GLM) with year and colony effects; post-hoc Tukey pairwise comparisons for colony/year interactions.
  - Inter-congener associations: Pearson correlation coefficients.
  - Overall associations: multiple regression models relating ΣPBDE and individual congeners to shell index and to egg volume.
  - Shell index analyses: performed only on samples with calculable shell index (Bass Rock n=46; Ailsa Craig n=35).

- Software
  - Analyses conducted in Minitab 16.