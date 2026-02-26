# Experimental design

- Purpose and scope
  - Investigates toxicity of ZnO nanoparticles and non-nanoparticles to Earthworm Eisenia andrei.
  - Follows OECD guideline 222: Earthworm reproduction test (Eisenia fetida/andrei), 2004.
  - 28-day exposure with measurements of survival, reproduction, and weight change to assess toxicity of zinc compounds.

- Soil preparation and composition
  - Soil per OECD 222: 10% Sphagnum moss peat, 70% industrial quartz sand, 20% kaolinite clay (dry weight).
  - Wetting and rehydration: moisture adjusted to ~50% of maximum water-holding capacity.
  - pH adjusted to 6.1 ± 0.05.
  - Each jar started with 500 g dry-equivalent soil and ~147 ml water to reach target moisture.
  - Jars prepared and labeled; 603 g prepared soil per jar used for dosing.

- Materials and characterization
  - ZnO materials: NanoSun, Z-cote, and Z-cote HP1; plus non-nano ZnO and ZnCl2 controls.
  - ZnO NP characteristics: NanoSun (low water solubility, high melting point, UV absorber; hazardous to aquatic organisms), Z-cote (mean size ~100 nm, insoluble, high melting point, UV-stable, uncoated), Z-cote HP1 (similar to Z-cote but with a triethoxycaprylylsilane coating 1–4%).
  - Z-cote HP1 coating may alter solubility and agglomeration; lack of ecotoxicological data for HP1 noted.
  - Purities: NanoSun, Z-cote, non-nano ZnO >99%; Z-cote HP1 ~97.5% due to coating.
  - Stock solutions prepared to equalize Zn mass across treatments (8.3 mg Zn/mL nominal concentration), accounting for material purity.

- Dispersing and dosing
  - Dosing via dispersion of each material in MilliQ water to ensure homogeneous distribution.
  - High-concentration stock solutions (8 mg/mL) used; sonication (Vibra-Cell) optimized for dispersion.
  - Particle size/distribution checked with Zetasizer, Nanosight, and TEM; target mean ~100 nm (consistent with Z-cote).
  - Z-cote HP1 posed dispersion challenges; full dispersion not achieved; direct dry-powder addition used as alternative.
  - ZnCl2 dissolved in DI water and dosed equivalently to NP and non-nano ZnO treatments.
  - Jars dosed and mixed in topsoil; additional water added next day to reach moisture target.

- Experimental animals and setup
  - Eisenia andrei worms sourced commercially; pre-exposed in outdoor loamy soil with peat.
  - Feeding: fresh horse manure; approximately 5 g dry manure per jar over the course of the study (batches of 3 g initially, 2 g after two weeks).
  - Worms per jar: seven worms (instead of the recommended ten) due to limited supply; average starting weight ~0.31 g.
  - Experimental design: 4 replicates per treatment/concentration; 6 nominal concentrations for NP and ZnCl2, 3 for non-nano ZnO.
  - Total design: 118 jars, randomized setup, 20 ± 1 °C, constant light, 28 days exposure.

- Endpoints and data collection
  - Primary endpoints: survival, weight change, and reproduction (cocoons per worm per week) over 4 weeks.
  - Feeding rate: measured as difference in manure added vs. remaining after two weeks (milligrams dry manure per gram worm per week).
  - Post-exposure analyses: cocoons retrieved by wet sieving; surviving worms snap-frozen for TEM; tissue samples collected for future analyses; soil samples retained for characterization.
  - Observational data recorded at multiple time points: day 0, day 14, day 28.

- Data fields and recording
  - Key fields include: experimental jar number, zinc type (salt, nanoparticle, non-nano), zinc treatment, zinc exposure concentration (mg Zn/kg), replicate number.
  - Temporal and biological metrics captured: jar weight at mixing, number of worms at day 0, total worm weight at day 0, jar weight at day 0, number alive and total worm weight at day 14 and day 28, jar weight before/after sorting at day 14 and day 28, percent survival at 14 and 28 days, number of cocoons per worm per week, percent worm weight change at 14 and 28 days.
  - Overall design counts: 118 jars; 10 control replicates; 4 replicates per treatment/concentration.

- Data analysis and statistics
  - Endpoints analyzed with analysis of variance (ANOVA) to assess treatment effects, with checks for homogeneity of variance.
  - Dose–response modeling for each material using nonlinear logistic model:
    - y = ymax / [1 + (ci / EC50)^β], with EC50 (or LC50 for survival) and slope β.
    - Asymmetric 95% confidence intervals calculated via custom GenStat 12.1 code.
  - Software: Minitab 15 for initial ANOVA; GenStat 12.1 for dose–response fitting and confidence intervals.
  - Feeding rate treated as a separate endpoint (mg dry manure per g worm per week) and calculated from manure consumption data.
  - Emphasis on lifecycle endpoints: survival, weight, reproduction (cocoons) for interpretation of toxicity across zinc forms.

- Key considerations and limitations
  - Dispersion challenges with Z-cote HP1 noted; practical approach used due to lipophilic coating hindering dispersion.
  - Particle size verification across materials; multiple analytical methods employed (Zetasizer, Nanosight, TEM) to support dispersion quality.
  - Comparability across materials ensured by equalizing Zn mass across treatments despite differing purities and coatings.