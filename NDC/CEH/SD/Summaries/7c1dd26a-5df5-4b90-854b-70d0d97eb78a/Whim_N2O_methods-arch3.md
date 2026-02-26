# Nitrous oxide emissions from a peatbog after thirteen years of experimental nitrogen deposition - Materials and methods

- Field site: Whim bog, Scottish Borders; transition between lowland raised bog and blanket bog on 3–6 m peat; mean air/soil temperatures around 8.6°C/7.7°C; annual rainfall ~1092 mm; acidic peat (pH ~3.4); vegetation dominated by Calluna vulgaris and associated Sphagnum species.
- Purpose: Describe the experimental design, measurement methods, data collection, and analysis used to quantify N2O fluxes under controlled nitrogen deposition treatments over  thirteen years.

## Study site and vegetation context

- Location and environmental context provided (latitude/longitude; peat depth; hydrology; plant community composition).
- Vegetation cover recorded to track community responses over time.

## Experimental design and treatments

- Overall design: Randomised block with four blocks; 28 plots in total; four deposition treatments plus controls.
- Dry deposition ( NH3 ):
  - Delivered via a free-air release system emitting NH3 from a cylinder diluted with ambient air.
  - Emission sector defined by wind direction (SW sector; 180–215 degrees); deposition measured downwind.
  - NH3 concentrations monitored at multiple distances (0.1 m above vegetation) using passive samplers.
- Wet deposition (NH4+ and NO3−):
  - Implemented with a sprinkler system delivering concentrated NH4Cl or NaNO3 solutions in rainwater.
  - Three treatment levels designed to achieve total N deposition rates of 16, 32, and 64 kg N ha−1 y−1, plus ambient N deposition (8 kg N ha−1 y−1) for controls.
  - Four blocks; one treatment level per block; ~120 applications per year (every 15 minutes when conditions allowed).
- Treatment duration: Initiated June 2002 and continued year-round (except near freezing).

## Measurements and data collection

- Gas flux measurements:
  - Method: Static chamber technique; PVC collars installed in plots.
  - Sampling: Monthly flux measurements; four 20 mL samples per chamber per occasion.
  - Calculation: Flux estimated from initial rate of change in concentration (dC/dt0) using chamber volume and ground area (F = (dC/dt0) × (ρV/A)).
  - Considerations: Time resolution ~10 minutes; non-linearity accounted for with regression methods; potential underestimation acknowledged.
- Soil and foliage measurements:
  - Soil water chemistry: NH4+ and NO3− concentrations via ion chromatography; detection limits reported.
  - Vegetation data: Percent cover for each species within chamber locations, measured periodically.
  - Ancillary chamber data: Spatial coordinates, deposition fluxes (Fnh3, Fnh4, Fno3), total N deposition, and other metadata.
- Deposition verification:
  - Dry deposition: Gradient profiling of NH3 downwind from fumigation source; kriging interpolation assuming homogeneous deposition velocity.
  - Wet deposition: Automated spray system triggering, with real-time monitoring of solution volume and rainfall to ensure accurate dose.

## Laboratory instrumentation, calibration, and quality control

- Gas analysis: Nitrous oxide quantified by gas chromatography (HP 5890 II) with standard gas series for calibration.
- Calibration:
  - Four-point calibration with standard mole fractions; standards run about every 20 samples.
  - Conversion of GC responses to mole fractions using calibration data.
- Flux computation and fitting:
  - Primary flux estimates from linear and non-linear models to accommodate concentration-time curves (dC/dt0).
  - Multiple models employed: linear, quadratic, asymptotic, HMR model, and best-fit selection.
  - Uncertainty handling: Uncertainty quantified via multiple regression approaches; 95% confidence intervals reported where applicable.
- Data processing notes:
  - Measurements screened for outliers; outliers removed prior to analysis.
  - Statistical practice incorporates both fixed effects (environmental drivers) and random effects (plot/block structure).

## Statistical analysis

- Primary model: Linear mixed-effects model to relate N2O flux to soil temperature, water table depth, and nitrogen deposition fluxes (NH3, NH4+, NO3−).
- Random effects: Plot-level and block-level random effects to account for repeated measures and experimental design.
- Model specification example: Flux as a function of soil temperature, water table depth, and nitrogen deposition terms, with appropriate random effects structure.
- Data handling: Large dataset with 729 flux measurements after cleaning; model decisions guided by goodness-of-fit and study design considerations.

## Data products and structure

- Main data files (examples of included datasets):
  - ancilliaryData-byChamber.csv: Chamber-level metadata, experimental grid, deposition fluxes (Fnh3, Fnh4, Fno3), total N deposition, location coordinates.
  - ancilliaryData-byChamber-byDate.csv: Chamber-by-date metadata, gas deposition forms, plot and block identifiers, deposition flux values per date.
  - RCfluxOutput.csv: Various flux estimates by deposition model (linear, quadratic, asymptotic, HMR, best-fit) with confidence intervals and model fit statistics.
  - vegetation-speciesPercentCover-Whim-byChamber.csv: Species percent cover by chamber and form.
  - chemistry-NH4mgNperl-Whim-byChamber-byDate.csv: Soil water ammonium concentrations by chamber and date.
  - chemistry-NO3mgNperl-Whim-byChamber-byDate.csv: Soil water nitrate concentrations by chamber and date.
  - chemistry-pH-Whim-byChamber-byDate.csv: Soil water pH by chamber and date.
- Plan figure: Layout of N deposition plots (Figure 1) referenced in the study.

## Challenges and practical considerations for monitoring frameworks (lessons for authors)

- Data availability and accessibility:
  - The study demonstrates extensive data collection across multiple interconnected datasets, highlighting the need for clear metadata and provenance to enable reuse.
- Metadata and data standards:
  - Detailed metadata accompany each file, but public sharing of underlying datasets can be a barrier; explicit data governance and open data standards are important to reduce duplication and facilitate reuse.
- Data integration and transformation:
  - Complex datasets require consistent units, careful alignment of temporal and spatial coordinates, and documentation of data transformations (e.g., kriging for deposition, model selection criteria for flux estimates).
- Data governance and transparency:
  - The use of multiple models for flux estimation and detailed QC steps emphasizes the importance of transparent methods and accessibility of code or workflows to reproduce results.
- Communication of complex results:
  - The study integrates field measurements, laboratory analyses, and statistical models; clear communication (tables of variables, model outputs, and uncertainties) is essential for decision-making and policy relevance.

## Key takeaways for monitoring framework authors

- Design long-term, controlled field experiments with explicit deposition pathways (dry and wet) to isolate drivers of environmental health indicators.
- Use multiple, transparent measurement and analysis approaches (e.g., several flux models) to robustly estimate key fluxes and quantify uncertainty.
- Maintain comprehensive metadata and data dictionaries; prepare data in interoperable formats to ease sharing and governance.
- Acknowledge and document potential data gaps, transformations required, and limitations of measurement techniques to inform policy decisions and future monitoring strategies.