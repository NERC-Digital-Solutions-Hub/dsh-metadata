# Nitrous oxide emissions from a peatbog after thirteen years of experimental nitrogen deposition - Materials and methods

## Objective and context
- Document and quantify nitrous oxide (N2O) fluxes from a peat bog under long-term nitrogen (N) deposition treatments.
- Use standardized measurements and analyses to allow for temporal comparisons and policy-relevant environmental monitoring.

## Field site
- Whim bog, Scottish Borders: transition zone between lowland raised bog and blanket bog.
- Deep peat (3–6 m); mean annual air and soil temperatures ~8.6°C and 7.7°C; rainfall ~1092 mm.
- Water table typically ~10 cm below surface; hummocks ~20 cm higher than hollows.
- Very acidic peat (pH ~3.4) with diverse blanket mire vegetation dominated by Calluna vulgaris and Eriophorum vaginatum, among others.

## Experimental design and treatments
- Two nitrogen addition systems:
  - Dry deposition: NH3 gas using a free-air release system; concentration gradients measured downwind.
  - Wet deposition: NH4+ and NO3− added as ammonium chloride or sodium nitrate solutions via sprinkler system.
- Treatment structure:
  - Four blocks with replicated plots; 28 plots total.
  - Four levels: ambient (control, ~8 kg N ha−1 y−1) and three elevated deposition rates targeting 16, 32, and 64 kg N ha−1 y−1.
- Experimental duration: treatments initiated in June 2002 and continued year-round (except near freezing).

## Measurements and collection methods
- Soil and vegetation monitoring:
  - Soil water chemistry: NH4+ and NO3− measured by ion chromatography from subirrigation dipwells; pH and vegetation percent cover recorded.
  - Vegetation: percent cover data collected within chamber locations every few years.
- Gas flux measurements:
  - Nitrous oxide fluxes via static chamber method: PVC collars inserted in peat; chambers sealed for 30–40 minutes; four 20-ml gas samples collected per occasion.
  - Sampling frequency: typically monthly.
- Instrumentation:
  - Gas samples analyzed with a gas chromatograph; use of multiple standard gases for calibration.

## Data collection and structure
- Data files detailing measurements and metadata:
  - ancilliaryData-byChamber.csv: chamber identifiers, deposition types, block/plot info, geolocation, deposition fluxes (FNH3, FNH4, FNO3), total N deposition, and vegetation data.
  - ancilliaryData-byChamber-byDate.csv: chamber/date-specific data including gas file references, spatial identifiers, temperature (air/soil), water depth, and deposition figures.
  - RCfluxOutput.csv: flux calculations from various models (linear, quadratic, asymptotic, HMR, best-fit) with confidence intervals and model fit statistics.
  - vegetation-speciesPercentCover-Whim-byChamber.csv: species cover percentages per chamber.
  - chemistry-NH4mgNperl-Whim-byChamber-byDate.csv, chemistry-NO3mgNperl-Whim-byChamber-byDate.csv, chemistry-pH-Whim-byChamber-byDate.csv: soil water ammonium, nitrate, and pH data by date and chamber.
- Sample metadata and layout:
  - 72 chambers across 4 experimental blocks (plan layout available as figure/plan file).

## Data processing, flux calculation, and models
- Flux calculation:
  - F = (dC/dt0) × (ρV)/A, where dC/dt0 is the initial rate of concentration change, ρ is air density, V is chamber volume, A is ground area.
  - dC/dt0 estimated using linear and nonlinear (asymptotic) regression methods; best fit chosen per measurement.
- Calibration:
  - Four-point calibration for N2O mole fractions against standard gases; standards run regularly.
- Models for flux estimation:
  - Multiple approaches used in RCflux outputs: linear, quadratic, asymptotic, HMR, and best-fit methods.
- Data quality and uncertainty:
  - Uncertainties quantified; pooling of different estimation methods with best-fit chosen; potential underestimation acknowledged due to limited 10-minute time resolution.
  - Outliers removed from flux dataset prior to analysis.

## Statistical analysis
- Primary analysis: linear mixed-effects model to relate N2O flux to environmental drivers and deposition treatments.
- Fixed effects: soil temperature (Tsoil), water table depth (zwater), NH3 deposition (FNH3), NH4 deposition (FNH4), NO3 deposition (FNO3).
- Random effects: chamber locations nested within experimental blocks to account for repeated measures and spatial structure.
- Dataset size: 729 flux measurements after quality control.
- Model specification includes random intercepts and slopes to capture plot- and block-level variation.

## Units, variables, and data interpretation
- Recorded values include:
  - N2O fluxes in nmol N2O m−2 s−1 (across multiple calculation methods with confidence intervals and R2 metrics).
  - Gas concentrations, soil chemistry (NH4+, NO3−), pH, and vegetation cover.
  - Environmental covariates: soil temperature, water table depth, and deposition rates for NH3, NH4, and NO3.
- Data in standardized tabular formats enabling time-series analyses and cross-plot comparisons.

## Data accessibility and reuse considerations
- Dataset structure supports cross-site comparisons and long-term environmental monitoring.
- Raw and processed flux data, along with ancillary measurements, are organized for reuse and validation.
- The document references a plan (plan.pdf) for layout and implementation, aiding reproducibility and data sharing.

## Key monitoring insights and practical implications
- Long-term N deposition experiments quantify how N inputs influence soil N dynamics and N2O emissions in peatlands.
- Consistent measurement framework (gas flux via static chambers, soil chemistry, and vegetation metrics) enables temporal and spatial trend analyses.
- Standardized data processing and reporting (including multiple flux estimation methods and statistical modeling) illustrate robust approaches for environmental health monitoring and policy performance assessment.
- Challenges highlighted include enhancing data value through data integration with other datasets and improving data accessibility for broader reuse.