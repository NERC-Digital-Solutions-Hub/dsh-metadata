# Experimental design

- Purpose and scope
  - Dataset from a laboratory study on the toxicity of ZnO nanoparticles and non-nanoparticles to the earthworm Eisenia andrei.
  - Followed OECD guideline 222 (Earthworm reproduction test) with 28-day exposures.
  - Endpoints: survival, reproduction (cocoons per worm per week), and weight change; additional feeding rate and TEM/particle characterization data.

- Soil preparation
  - Soil composed of 500 g dry-weight per jar (equivalent to ~603 g prepared soil) with a maximum water holding capacity of 500 ml.
  - Moisture target: ~50% of WHC (147 ml water per jar).
  - Constituents by dry weight: 10% Sphagnum moss peat, 70% industrial quartz sand, 20% kaolinite clay.
  - pH adjusted to 6.1 ± 0.05.

- Materials characterized
  - ZnO materials: NanoSun, Z-cote, Z-cote HP1.
    - NanoSun: nanoparticle, photoactive, very low water solubility, high melting point; labeled hazardous to aquatic life.
    - Z-cote: ~100 nm particles, hydrophobic surface, no coating; insoluble in water; high melting point.
    - Z-cote HP1: ~130 nm average, coating of 1–4% triethoxycaprylylsilane; lipophilic coating may affect dispersion and solubility; generally low water solubility.
  - Controls: ZnCl2 (ionic Zn) and non-nano ZnO powder; purities >97–99% (HP1 ~97.5% due to coating).
  - Stock solutions were prepared to equal Zn mass concentrations across materials (8.3 mg Zn/mL nominal, accounting for purity).

- Dispersing and dosing
  - NP and ZnO dispersions prepared in MilliQ water; high-concentration stocks required ultrasonication.
  - Particle size distribution aimed for ~100 nm (as with Z-cote); verified with Zetasizer, Nanosight, and TEM.
  - HP1 posed dispersion challenges: could not achieve a stable aqueous dispersion; dosed as dry powder directly onto soil.
  - ZnCl2 dosed as dissolved solution; all dosing aligned to equal Zn mass concentrations.
  - Stock preparations: 8 mg Zn/mL in ~650 mL MilliQ water; dispersions dosed onto soil, with remaining moisture added after mixing.

- Experimental animals and setup
  - Earthworm species: Eisenia andrei, sourced commercially.
  - Seven worms per jar (instead of the recommended 10) due to limited availability; average starting weight ~0.31 g.
  - Feeding: approximately 5 g dry horse manure per jar across the experiment (2 batches: 3 g then 2 g after two weeks).
  - Exposure conditions: 20 ± 1°C, constant light, randomized layout; separate jars for each treatment and replicate.
  - Study design: five separate, similarly designed toxicity tests corresponding to the three nanoparticles, ZnCl2, and non-nano ZnO.

- Toxicity testing design and endpoints
  - Treatments: five separate tests with six nominal Zn concentrations for each NP and ZnCl2; non-nano ZnO used three concentrations.
  - Concentrations (mg Zn/kg dry soil):
    - NPs: 191, 305, 488, 781, 1250, 2000
    - Non-nano ZnO: 305, 781, 2000
  - Replication: 4 replicates per treatment; control: 10 replicates; total jars: 118.
  - Measurements and time points:
    - Survival and weight measured at 14 and 28 days.
    - Reproduction: cocoons per worm per week (over the full 4 weeks) via wet sieving.
    - Feeding rate: measured by weight of manure remaining at 14 days (two-week interval).
    - Post-experiment: surviving worms snap-frozen for potential TEM analysis; a worm from each jar selected for tissue TEM.
    - Additional soil sampling stored for further characterization.

- Data analysis and modeling
  - Endpoints analyzed: percentage survival, weight gain, and reproduction rate (cocoons per worm per week).
  - Statistical approach:
    - Initial ANOVA (Minitab 15) for all endpoints, followed by one-way ANOVA per material using concentration as fixed factor.
    - Dose–response modeling: logistic model to estimate EC50 (or LC50 for survival) with slope parameter; asymmetric 95% confidence intervals calculated via GenStat 12.1.
    - Nonlinear fitting used to derive EC50/LC50 and confidence intervals; binary data for survival treated accordingly.

- Data structure and units
  - Recorded fields in the dataset include:
    - Experimental jar number; zinc type (source); zinc treatment; zinc exposure concentration (mg Zn/kg); replicate number.
    - Jar weight at setup and at multiple time points; number of worms alive at 14 and 28 days; total worm weight at those times.
    - % worm survival at 14 and 28 days; number of cocoons per worm per week.
    - % worm weight change at 14 and 28 days.
  - Additional notes:
    - The dataset integrates multiple data streams: material characterization, dispersion quality, exposure concentrations, biological endpoints, and derived metrics (feeding rate, EC50/LC50 estimates).