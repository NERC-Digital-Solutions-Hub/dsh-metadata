# Experimental design

- Objective
  - Dataset from a laboratory experiment to assess the toxicity of ZnO nanoparticles and non-nanoparticles to earthworm Eisenia andrei.
  - Follows OECD guideline 222 (Earthworm reproduction test) with a 28-day exposure examining survival, reproduction, and weight change.

- Soil preparation and experimental setup
  - Soil mixture (dry weight): 10% Sphagnum moss peat, 70% industrial quartz sand, 20% kaolinite clay.
  - Moisture management: correct weight correction for moisture; target ~50% of water holding capacity (WHC); final moisture ~50% with 147 ml water per jar.
  - pH adjustment to 6.1 ± 0.05 using calcium carbonate.
  - Jars: labeled Kilner jars; total soil per jar equivalent to 500 g dry soil (603 g prepared soil).

- Materials and characterization
  - ZnO materials: NanoSun, Z-cote, Z-cote HP1 (the latter with a 1–4% triethoxycaprylylsilane coating).
  - Non-nano controls: ZnCl2 solution (ionic reference) and non-nano ZnO powder.
  - Purity: >99% for most; Z-cote HP1 ~97.5% due to coating.
  - Zn content standardized across stock solutions to enable direct comparison (8.3 mg Zn/ml nominal concentration), accounting for material purity.

- Dispersion, dosing, and delivery
  - Dosing via dispersion in MilliQ water to achieve homogeneous distribution; high-concentration stock solutions prepared for NP and ZnCl2 treatments.
  - Dispersion optimization included particle size assessment (目标 around 100 nm) using Zetasizer, Nanosight, and TEM verification.
  - Challenges: Z-cote HP1 poorly dispersible in water; ultimately dosed as a dry powder due to settling and adhesion issues.
  - ZnCl2 dosed from dissolved solution; NanoSun and Z-cote/NanoZnO stock dispersions dosed directly onto soil and mixed.

- Experimental organisms
  - Earthworm species: Eisenia andrei, sourced commercially and acclimated in outdoor loamy soil with peat amendment.
  - Feeding: horse manure, approximately 5 g dry weight per jar across two batches (3 g initially, 2 g after two weeks).
  - Population used per jar: 7 worms (instead of the recommended 10) due to limited availability; average starting weight ~0.31 g.
  - Environment: 20 ± 1°C, constant light, four-week exposure, randomized design.

- Experimental design and endpoints
  - Five separate toxicity tests: three ZnO nanoparticles (NanoSun, Z-cote, Z-cote HP1) plus non-nano ZnO and ZnCl2 controls.
  - Exposure concentrations (nominal, mg Zn/kg dry soil):
    - NP and ZnCl2: 191, 305, 488, 781, 1250, 2000 mg Zn/kg.
    - Non-nano ZnO: 305, 781, 2000 mg Zn/kg.
  - Replication: 4 replicates per treatment; controls: 10 replicates; total jars: 118.
  - Endpoints measured: survival (14 and 28 days), weight change (percent, 14 and 28 days), cocoons per worm per week (over 4 weeks). Feeding rate estimated from manure consumption between weeks 0–2.

- Calculations, statistics, and modelling
  - Endpoints: percent worm survival, average weight gain, and reproduction rate (cocoons per worm per week).
  - Statistical analyses: ANOVA (initially across endpoints and treatments; check homogeneity of variance), followed by one-way ANOVA per material with exposure concentration as fixed factor.
  - Dose–response: nonlinear logistic model to estimate EC50 (or LC50 for survival) with slope parameter, using GenStat; asymmetric 95% confidence intervals calculated with custom code.
  - Feeding rate: calculated as mg dry manure per g worm per week, based on manure consumption difference and worm weight.

- Data fields and units (nature and units of recorded values)
  - Experimental jar number; zinc type (source of zinc); zinc treatment; zinc exposure concentration (mg Zn/kg); replicate number.
  - Jar weights at multiple timepoints (t = 0, 14, 28 days) with/without worms; number of worms alive and total weight at each timepoint.
  - % worm survival at 14 and 28 days; number of cocoons per worm per week; % worm weight change at 14 and 28 days.
  - Additional parameters: initial and final counts/weights, cocoons per jar per week, feeding rate metrics.

- Key considerations for data use
  - Z-cote HP1 dispersion challenges may influence dosing accuracy for that material.
  - Lower replicate count per jar (7 worms) due to resource limits; results are nonetheless designed to provide reliable cocoon production estimates in this context.
  - Direct comparability across nanoparticle, non-nano ZnO, and ZnCl2 relies on standardized Zn content in stock solutions.