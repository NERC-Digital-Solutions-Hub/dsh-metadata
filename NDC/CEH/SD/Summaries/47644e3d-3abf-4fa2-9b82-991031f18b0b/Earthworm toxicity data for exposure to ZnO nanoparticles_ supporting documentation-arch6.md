# Experimental design

- Purpose: Assess the toxicity of ZnO nanoparticles and non-nanoparticles to earthworm Eisenia andrei following OECD guideline 222 (Earthworm reproduction test).
- Treatments: 
  - ZnO-based nanoparticles: NanoSun, Z-cote, Z-cote HP1
  - Non-nano controls: ZnCl2 (ionic) and non-nano ZnO
  - Exposure concentrations: six nominal concentrations for nanoparticles (191, 305, 488, 781, 1250, 2000 mg Zn/kg dry soil); non-nano ZnO at 305, 781, 2000 mg Zn/kg; each with four replicates
  - Overall: five separate toxicity tests (one per material) plus a shared control set; total 118 jars
- Endpoints (measured over 28 days): survival, reproduction (cocoons per worm per week), weight change; feeding rate (dry manure per g worm per week)
- Organisms and setup: Eisenia andrei, seven worms per jar (instead of 10); average weight ~0.31 g; fed horse manure; outdoor culture acclimation prior to test; randomized design; temperature controlled room at 20 ± 1°C with constant light
- Dosing and exposure duration: soils dosed by dispersion in MilliQ water and direct addition to soil, with moisture adjusted to ~50% of water holding capacity; exposure duration 28 days
- Post-exposure activities: cocoons counted by wet sieving; surviving worms weighed; snap-frozen worms for potential TEM analysis; soil samples collected for soil/solution characterization

## Materials and soil preparation

- Soil mixture (OECD 222): 10% Sphagnum moss peat, 70% industrial quartz sand, 20% kaolinite clay by dry weight
- Moisture and pH: moisture at ~50% of WHC; pH adjusted to 6.1 ± 0.05
- Preparation: components not dried; peat sieved to ~1 cm; batches ~20 kg; mixed in cement mixer and by hand; jars prepared with 500 g dry soil (603 g wet) to yield ~500 ml WHC; 147 ml water added per jar to reach target moisture

## Material characterization and dispersion

- ZnO materials:
  - NanoSun: low water solubility; high melting point; no coatings; photoactive; hazardous to aquatic life
  - Z-cote: ~100 nm average size; insoluble in water; no coating
  - Z-cote HP1: ~130 nm average size; triethoxycaprylylsilane coating (1–4%); potential differences in solubility and dispersion due to coating
- Dosing preparations:
  - Target concentration: 8 mg Zn per mL in stock dispersions; purity adjustments considered
  - Dispersions: prepared in MilliQ water; high-intensity ultrasonication to achieve homogeneous dispersion; particle size distribution monitored (aim ~100 nm peak) using Zetasizer and Nanosight
  - TEM analysis performed for dispersion verification
- Dispersion challenges:
  - Z-cote HP1 difficult to disperse; sometimes delivered as dry powder due to lipophilic coating; surfactant improved but not enough for full dispersion

## Experimental animals and procedures

- Organisms: Eisenia andrei from commercial culture
- Acclimation and feeding: acclimated in loamy soil with peat amendment; fed ~5 g dry horse manure in two batches (3 g then 2 g after two weeks)
- Exposure details: jars randomized; 4 replicates per treatment/concentration; control replicated 10 times
- Measurements during exposure: feeding rate assessed by dry manure remaining after two weeks; jar moisture monitored by weight
- Sampling plan: after 2 and 4 weeks, record survival, total worm weight; after 4 weeks, cocoons counted; remaining worms snap-frozen for potential TEM analysis; soil samples collected for further characterization

## Toxicity endpoints and data collection

- Endpoints per jar:
  - Survival: number alive at 14 and 28 days; percent survival calculated
  - Growth: total worm weight and percent weight change at 14 and 28 days
  - Reproduction: cocoons per worm per week over the 4-week period
  - Feeding: feed rate (mg dry manure per g worm per week)
- Data capture fields (Nature and units):
  - Experimental jar number, zinc type, zinc treatment, zinc exposure concentration (mg Zn/kg), replicate number
  - Jar weight at mixing (g), number of worms at start, total start weight (g)
  - Jar weight after setup, number alive and total weight at 14 days
  - Jar weight after sorting, jar weight at 28 days
  - Number of worms alive at 28 days; total weight at 28 days
  - % worm survival (14 days; 28 days)
  - Cocoons per worm per week
  - % worm weight change (14 days; 28 days)

## Data analysis and endpoints calculation

- Statistical approach:
  - Initial ANOVA across treatments; check homogeneity of variance
  - One-way ANOVA per material with exposure concentration as fixed factor
  - Dose–response modeling (logistic) to estimate EC50/LC50 with GenStat; asymmetric 95% CIs
  - Nonlinear fitting for survival (binary outcome) and related endpoints
- Calculated metrics:
  - Average feeding rate (mg dry manure per g worm per week) from two intervals (0–2 weeks, 2–4 weeks)
- Data handling notes:
  - Randomized design and repeated measures across time points
  - Use of multiple endpoints to assess sub-lethal and reproductive effects

## Data quality considerations and limitations

- Dispersion challenges noted for Z-cote HP1, affecting dosing accuracy and interpretation
- For HP1, direct dry-powder dosing introduced potential dosing inconsistencies due to powder sticking to equipment
- Overall data collection aligned with OECD 222 guidance, with multiple replication and randomization to support robust inferences