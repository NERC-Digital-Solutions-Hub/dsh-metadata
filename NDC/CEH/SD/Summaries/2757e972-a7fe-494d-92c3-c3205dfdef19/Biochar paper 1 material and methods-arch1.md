# The effect of biochar addition on N2O and CO2 emissions from a sandy loam soil - the role of soil aeration

- Objective: Assess how biochar addition influences soil N2O and CO2 emissions, focusing on the role of soil aeration controlled by moisture and wetting events, using a data-driven, factorial experimental approach.

## Context and materials

- Soil source: Bare soil from a Miscanthus field in Lincolnshire, UK.
  - Soil type: dense, compacted sandy loam (53% sand, 32% silt, 15% clay).
  - Bulk density: 1.68 ± 0.03 g cm-3.
  - Low total C (14.7 ± 0.2 g kg-1) and total N (2.70 ± 0.10 g kg-1); low extractable inorganic N (NH4+-N 0.6 ± 0.10 mg kg-1; NO3--N 1.8 ± 0.35 mg kg-1).
  - Primary field management: 500 kg ha-1 PK fertilizer in March 2010.
- Biochar properties:
  - Feedstock: hardwood (oak, cherry, ash) thinnings; Bodfari Charcoal, UK.
  - Production: calcined through 180 °C volatiles release, then ~400 °C for 24 h.
  - Fresh biochar: <2 mm; GMC <5%; bulk density 0.24 g cm-3.
  - Composition: total C ~723 g kg-1; total N ~7.12 g kg-1; pH ~9.25; CEC ~145 cmol+/kg.
  - NH4+ and NO3- largely below detection limits.
  - Additional properties (exchangeable cations, PAHs, BETX, metals) reported in supplementary information.

## Experimental design

- Experiment 1: Soil cores with wetting/drying cycles
  - Full factorial design with n = 4 replicates.
  - Factors:
    - Temperature: 4, 10, 16 °C.
    - Moisture: field moist (23% GMC) and wetted (28% GMC).
  - Biochar treatment: half of the cores received biochar mixed into the top 7 cm at 2% dry soil weight (~22 t ha-1); control cores without biochar.
  - Setup: bulk density measured; cores stored at 4 °C before and during the experiment.
  - Wetting protocol: periodic wetting events during incubation; initial gas sampling started after a 6-day equilibration period to account for initial respiration flush.
  - Gas sampling: 6, 26, 51, 64, 127 days; additional samples around wetting events (72 and 86 days) with ~120 ml water to reach 28% GMC; ~48 h window for post-wetting flux modeling.

- Experiment 2: Uniform water holding capacity (WHC) incubations
  - Soil: 0–10 cm depth; stored at 4 °C, then sieved for uniformity.
  - Biochar treatments: 0, 1, 2, 5, 10% of total dry soil weight (n = 4 per treatment).
  - Incubation: 16 °C, dark; 3 days equilibration after mixing and warming.
  - WHC determination: standardized procedure to establish maximum WHC under lab conditions.
  - Drying/wetting: biochar-amended soils wetted to 87% WHC (WFPS ≈ 78 ± 1%).
  - Gas sampling: 0, 12, 24, 36, 48, 60, and 168 h after wetting.

## Measurements and analyses

- Gas analyses
  - CO2: measured with a PerkinElmer Autosystem GC (two FID detectors; 130 °C and 300 °C with methaniser).
  - N2O: measured with a PerkinElmer Autosystem XL GC (ECD at 360 °C).
  - Columns: Porapak Q (2 m).
  - Calibration: certified gas standards.
  - Calculation:
    - Experiment 1: gas fluxes from linear accumulation of concentrations (0–60 minutes); cumulative flux per m2 calculated by summing fluxes across 0–48 h after wetting.
    - Experiment 2: cumulative gas production from headspace concentrations (t0 to sampling time).

- Chemical analyses
  - pH: measured in 1:2.5 soil/biochar suspension.
  - Extractable inorganic N: NH4+-N and NO3--N by 2 M KCl, analyzed colorimetrically.
  - Total C and N: analyzed on oven-dried samples using CN analyzer (905–950 °C furnace protocol).

- Physical measurements
  - Bulk density: determined for each treatment.
  - WHC and water-filled pore space (WFPS) calculations referenced standard methods.

- Statistical analyses
  - Software: R (version 2.14.0).
  - Data handling: log10 transformation of flux data where appropriate.
  - Experiment 1: linear mixed-effects models for gas fluxes; three-way ANOVA for cumulative flux within 48 h of wetting and for chemical properties (pH, total C/N, extractable NH4+, NO3-).
  - Experiment 2: one-way ANOVA with biochar level as factor; Tukey HSD for pairwise treatment differences.
  - Data interpretation guided by established ecological/statistical references.

## Key considerations and methodological notes

- Rationale: By combining temperature, moisture, and biochar amendment in a controlled setting, the study aims to identify how biochar influences N2O and CO2 emissions under varying aeration and substrate conditions.
- Pre-equilibration: A period allowed for initial CO2 flush to diminish, improving interpretation of biochar effects on gas fluxes.
- Data quality and reproducibility: Replication (n = 4), detailed gas sampling schedules, standardized chemical analyses, and rigorous statistical treatment support robust inference about biochar’s impact on soil greenhouse gas emissions.
- Data provenance and gaps: The study provides explicit soil and biochar characterizations, experimental conditions, and measurement methodologies, enabling replication or meta-analysis; measurements focus on both gas flux dynamics and soil chemical/physical states relevant to gas production and transport.