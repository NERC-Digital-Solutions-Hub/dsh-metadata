# Experimental design

- Purpose: describes a laboratory dataset investigating toxicity of ZnO nanoparticles and non-nanoparticles to Eisenia andrei earthworms, following OECD guideline 222 (Earthworm reproduction test) with 28-day exposure and measures of survival, reproduction, and weight change.

- Experimental framework: five separate toxicity tests using three ZnO nanoparticles, one non-nano ZnO, and ZnCl2 ionic reference; treatments run across multiple nominal Zn concentrations with replication and randomization.

- Soil preparation: soil mixture based on OECD guideline 222 (dry weight: 10% Sphagnum moss peat, 70% quartz sand, 20% kaolinite clay); moisture adjusted to ~50% water holding capacity; pH targeted at 6.1 ± 0.05; jars designed for 500 g dry soil and ~603 g prepared soil per replicate.

- Materials characterization: ZnO materials include NanoSun, Z-cote, and Z-cote HP1, plus ZnCl2 and non-nano ZnO controls; purity and physical properties documented; stock concentrations standardized by mass of Zn (8.3 mg Zn/mL nominal) accounting for material purity.

- Dispersion and dosing: dispersion of most materials in MilliQ water with ultrasonic probe; particle size distribution monitored (target ~100 nm); Z-cote HP1 posed dispersion challenges and was dosed as a dry powder due to poor water dispersibility; dosing done directly onto soil with subsequent mixing and moisture adjustment.

- Experimental organisms: Eisenia andrei worms sourced commercially, kept in outdoor loamy soil with peat; seven worms per jar (instead of the recommended ten) due to limited supply; worms weighed ~0.31 g on average; feeding with horse manure; moisture maintained at ~86%.

- Exposure design: five tests with six nominal concentrations for most treatments (191, 305, 488, 781, 1250, 2000 mg Zn/kg dw) and three concentrations for non-nano ZnO (305, 781, 2000 mg Zn/kg dw); four replicates per treatment and control with ten replicates; exposure duration 28 days at 20 ± 1°C; mid-experiment feeding adjustment and post-exposure measurements.

- Endpoints measured: survival at 14 and 28 days; weight change percent (t 14 days and t 28 days); reproductive output expressed as cocoons per worm per week over four weeks; feeding rate estimated from manure consumption; additional tissue sampling for TEM and soil characterization.

- Data analysis approach: ANOVA (overall and per-material one-way ANOVA with concentration as fixed factor) after checking variance assumptions; dose–response modelling using a logistic function to estimate EC50 (and LC50 for survival) with nonlinear fitting in GenStat and custom code for asymmetric confidence intervals; emphasis on survival, weight, and reproduction as primary endpoints.

- Data and field structure: dataset fields described include jar identifiers, zinc type and treatment, exposure concentration (mg Zn/kg), replicate numbers, initial and final jar weights, worm counts and weights at 14 and 28 days, percent survival, cocoons per worm per week, and percent weight change.

- Additional notes on data collection: after 28 days, surviving worms snap-frozen for future TEM analysis; a subset of soil samples collected for further characterization; randomization and controlled environmental conditions emphasized to ensure comparability.

- Relevance to GIS and map-based data products (from a GIS specialist perspective): the study provides structured, numeric, geo-agnostic toxicity endpoints across different zinc forms and exposure levels; data could be integrated with soil-type or environmental-condition layers if location-specific metadata were added, enabling spatial visualization of toxicity risk gradients and exposure-response relationships in map-based formats.