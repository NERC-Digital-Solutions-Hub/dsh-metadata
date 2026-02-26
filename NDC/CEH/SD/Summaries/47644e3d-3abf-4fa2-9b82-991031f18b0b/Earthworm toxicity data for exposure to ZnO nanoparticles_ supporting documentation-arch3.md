# Experimental design

- Objective
  - Assess toxicity of ZnO nanoparticles and non-nanoparticles to earthworm Eisenia andrei using OECD guideline 222 (Earthworm reproduction test), focusing on survival, reproduction, and weight change over 28 days.

- Experimental design and scope
  - Five separate toxicity tests conducted with three ZnO nanoparticles, non-nano ZnO, and ZnCl2 (ionic reference).
  - For most materials, six nominal exposure concentrations; non-nano ZnO used three concentrations.
  - Replication: four replicates per treatment/concentration; overall 118 jars plus 10 controls.
  - Worms: seven adult E. andrei per jar (due to limited supply), average initial weight 0.31 g; outdoor-cultured stock prior to use.
  - Randomized layout with jars assigned to treatments and maintained at 20 ± 1°C with constant light for 28 days.
  - Feeding: approximately 5 g dry horse manure per jar, split into two feedings (start and after two weeks).

- Soil preparation and moisture
  - Soil mixture: 500 g dry weight per jar composed of 10% Sphagnum moss peat, 70% industrial quartz sand, 20% kaolinite clay.
  - Moisture to approximately 50% of the soil’s water holding capacity (WHC); pH adjusted to 6.1 ± 0.05.
  - Soil mixed in batches, rewetting avoided by using measured average water content of constituents.

- Materials and exposure formulations
  - ZnO materials: NanoSun, Z-cote, Z-cote HP1; plus ZnCl2 (ionic) and non-nano ZnO as controls.
  - Purity: most materials >99%; Z-cote HP1 ~97.5% due to silane coating.
  - Nominal zinc exposure: 8.3 mg Zn per mL for stock solutions, adjusted for purity and chloride content where applicable.
  - Dispersion: high-intensity ultrasonication used to prepare concentrated ZnO dispersions in MilliQ water; aim for ~100 nm particle size; Z-cote HP1 challenging to disperse, leading to a dry-powder dosing approach for that material.

- Dosing and dispersion details
  - Stock concentrations prepared by dispersing powders in MilliQ water; dosing performed by applying stock dispersion directly onto the soil and mixing.
  - Z-cote HP1 dosing: due to poor dispersion, dry powder added directly to soil; surfactants did not achieve full dispersion.
  - ZnCl2 dosing prepared in DI water and dosed like NP and non-nano ZnO treatments.
  - Particle size and dispersion validated with Zetasizer, Nanosight, and TEM analyses for representative samples.

- Experimental endpoints and measurements
  - Endpoints recorded at two time points (14 and 28 days):
    - Survival: number of live worms per jar.
    - Weight: total worm weight per jar.
    - Reproduction: cocoons per worm per week over the 28-day period (assessed via wet sieving).
    - Feeding rate: change in manure weight over 0–14 days and 14–28 days.
  - Additional observations: jar weights to monitor moisture changes; worm counts and weights recorded at specified times; pre-sample worm for TEM analysis.

- Data collection, processing, and analysis
  - Data fields collected per jar include: Zn type, Zn treatment, exposure concentration (mg Zn/kg dw soil), replicate number, initial and subsequent jar weights, worm counts and weights at 14 and 28 days, cocoons per worm per week, and percent weight changes.
  - Statistical analyses:
    - Initial ANOVA across endpoints; homogeneity of variance checks.
    - One-way ANOVA per material with concentration as fixed factor.
    - Dose-response modelling using a logistic model to estimate EC50 (survival: LC50 for survival) with 95% CIs via GenStat; asymmetrical CIs computed with custom code.
    - Feeding rate calculated as mg dry manure per g worm per week, based on feed supplied minus remaining feed and worm weight.
  - Outputs intended to provide concentration–response relationships for each Zn form and to support risk assessment and monitoring decisions.

- Nature and units of recorded values
  - Experimental metadata and measurements include:
    - Jar numbers, Zn type and treatment, concentration (mg Zn/kg dw soil), replicate numbers.
    - Initial and subsequent jar weights, number of worms alive at 14 and 28 days, total worm weight at 14 and 28 days.
    - % worm survival at 14 and 28 days, cocoons per worm per week, and % worm weight change at 14 and 28 days.
  - Endpoints expressed as counts (worms, cocoons), weights (g), percentages (survival, weight change), and rates (cocoons per worm per week; mg Zn per kg soil).