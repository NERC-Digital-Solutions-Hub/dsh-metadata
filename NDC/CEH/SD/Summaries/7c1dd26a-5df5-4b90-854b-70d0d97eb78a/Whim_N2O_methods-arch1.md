# Nitrous oxide emissions from a peatbog after thirteen years of experimental nitrogen deposition - Materials and methods

- Field site and context
  - Whim bog in the Scottish Borders; a transition between lowland raised bog and blanket bog on 3–6 m peat.
  - Climate: mean air/soil temperatures ~8.6°C/7.7°C (2003–2009); annual rainfall ~1092 mm; water table typically ~10 cm below surface; peat highly acidic (pH ~3.4).
  - Vegetation: Calluna vulgaris–Eriophorum vaginatum blanket mire with mosaics of Calluna and Sphagnum species.

- Experimental design and treatments
  - Dry deposition (NH3): free-air release system delivering NH3 from a cylinder mixed with ambient air; releases occur under specific wind, temperature, and wind-speed conditions, creating a downwind deposition gradient. NH3 concentrations measured at multiple distances (0.1 m above vegetation) using passive samplers.
  - Wet deposition (NH4+ and NO3−): randomized block design with a water sprayer system; three deposition levels targeting total N deposition of 16, 32, and 64 kg N ha−1 yr−1, plus ambient control (~8 kg N ha−1 yr−1). Four blocks, 28 plots total; spray events ~120 per year with 15-minute automatic triggering.
  - Overall duration: treatments started in June 2002 and continued year-round when conditions allowed.

- Data collection: soil water chemistry
  - Soil water sampled from dipwells in all plots; NH4+ and NO3− measured by ion chromatography; detection limits ~0.014 mg L−1 (NH4–N) and ~0.062 mg L−1 (NO3–N).
  - Vegetation percent cover recorded within chamber locations every few years.

- Data collection: greenhouse gas exchange
  - Nitrous oxide fluxes measured with static chamber method (collars ~38 cm diameter, ~25 cm high). Sampling typically monthly; 30–40 min chamber closure with four 20 mL gas samples per event.
  - Gas samples analyzed by gas chromatography; calibration with four standards per run.

- Calibration steps and values
  - Fluxes converted to molar units using dC/dt0 from concentration time-series with linear or non-linear asymptotic regression; best-fit regression selected per chamber measurement.
  - Calibration performed with a four-point standard series (N2O mole fractions: 0.199, 0.285, 0.490, 0.975 µmol mol−1).

- Analytical methods and quality control
  - Flux calculation formula: F = (dC/dt0) × (ρ V / A), where ρ is air density, V chamber volume, A ground area.
  - Time-resolution (~10 minutes) limits non-linearity detection; potential underestimation of fluxes acknowledged.
  - Mixed-effects modeling approach to handle repeated measures and hierarchical design; multiple regression options tested to address non-linearity and model fit.

- Statistical analysis
  - Linear mixed-effects model incorporating fixed effects: soil temperature (Tsoil), water table depth (zwater), NH3 deposition flux (F NH3), NH4 deposition flux (F NH4), NO3 deposition flux (F NO3).
  - Random effects: chamber location nested within experimental block (i and j) to account for repeated measurements and spatial structure.
  - Model structure expressed as: FN2O,ij = β0 + β1 Tsold,ij + β2 zwater,ij + β3 FNH3,ij + β4 FNH4,ij + β5 FNO3,ij + bi Zi,j + bij Zi,j + εij, with random terms following normal distributions.

- Nature and units of recorded values (data files and variables)
  - ancilliaryData-byChamber.csv: per-chamber metadata (ChamberID, chamberCode, BlockID, PlotID, Form of N deposition, locations, and fluxes FNH3, FNH4, FNO3, Ndep-total).
  - ancilliaryData-byChamber-byDate.csv: chamber/date-specific meta (gas name, file references, date, location, deposition forms and fluxes, Tair, Tsoil, water table depth).
  - RCfluxOutput.csv: flux estimates from various modeling approaches (linear, quadratic, asymptotic, HMR, best-fit) with 95% CIs and R².
  - vegetation-speciesPercentCover-Whim-byChamber.csv: percent cover for each species per chamber.
  - chemistry-NH4mgNperl-Whim-byChamber-byDate.csv: soil NH4+ concentrations by chamber/date.
  - chemistry-NO3mgNperl-Whim-byChamber-byDate.csv: soil NO3− concentrations by chamber/date.
  - chemistry-pH-Whim-byChamber-byDate.csv: soil pH by chamber/date.
  - Figure 1: Layout of deposition plots (described in plan.pdf).

- Additional references and methodological context
  - Cape et al. 2008; Leith et al. 2004; Levy et al. 2011; Hutchinson & Mosier 1981; Sheppard et al. 2004; Tang et al. 2001; and related methodological studies on deposition velocity, chamber flux measurements, and uncertainty in flux estimation.

- Figure and plan
  - Figure 1 presents the spatial layout of N deposition plots within the Whim experiment (referenced as plan.pdf).