# Nitrous oxide emissions from a peatbog after thirteen years of experimental nitrogen deposition - Materials and methods

- A long-term field experiment at Whim bog, Scottish Borders (peatland ecosystem) examining how artificial nitrogen deposition influences nitrous oxide (N2O) fluxes from peat soil.
- Objectives relevant to data stewardship: document data collection, processing, and analysis methods to support appropriate data governance, discoverability, reuse, and reproducibility.

## Study site and experimental design (data context)

- Field site: Whim bog, 3°16' W, 55°46' N; transition between lowland raised bog and blanket bog; deep peat (3–6 m), acidic soil (pH ~3.4); wet hollows vs. drier hummocks; mosaic vegetation including Calluna vulgaris, Eriophorum vaginatum, Sphagnum spp.
- Climate metadata: mean air/soil temps ~8.6°C/7.7°C (2003–2009); annual rainfall ~1092 mm.
- Treatments initiated June 2002:
  - Dry NH3 deposition: free-air release system with NH3 from cylinder, diffusing to downwind sector; NH3 concentrations measured along transects with passive samplers.
  - Wet N deposition: replicated plots in a randomized block design; irrigation with NH4Cl or NaNO3 solutions to achieve target total N deposition rates (8, 16, 32, 64 kg N ha-1 y-1) plus ambient control.
- Experimental design: 4 blocks, 28 plots total; high-frequency artificial deposition (~120 applications y-1 for wet deposition).

## Data collected and key variables (data assets)

- Gas flux measurements: nitrous oxide (N2O) fluxes using static chamber method; monthly sampling with PVC collars and chamber lids; gas samples analyzed by GC.
- Soil chemistry and moisture: soil water NH4+ and NO3- concentrations (ion chromatography); soil pH; soil temperature (Tsoil) and air temperature (Tair); water table depth (WTdepth).
- Vegetation data: percent cover by species within chamber locations (e.g., Calluna vulgaris, Sphagnum spp.).
- Deposition and flux context: NH3, NH4+, and NO3- deposition fluxes per chamber; total N deposition per chamber.
- Data processing outputs: flux estimates from multiple models (linear, quadratic, asymptotic, HMR, best-fit); fit diagnostics (R^2, confidence intervals); best-fit method indicator code.
- Files and data dictionary: detailed headers describe variables, units, and descriptions across multiple CSV files (Tables 2–8 in the document).

## Data collection methods and processing (data lineage)

- Field collection methods:
  - Dry NH3 deposition: downwind concentration profiling (0.1 m above vegetation) using passive samplers; deposition estimated from concentrations and deposition velocity; spatial interpolation via ordinary kriging.
  - Wet N deposition: automated sprayer system delivering NH4Cl/NaNO3 solutions; enhanced rainfall by ~10% in treated plots; high-frequency deposition regime.
  - Soil and plant measurements: periodic soil water sampling; vegetation surveys conducted within chamber locations.
- Lab instrumentation and calibration:
  - Gas analysis by gas chromatograph (HP 5890 II) with standard gases for calibration.
  - 4-point calibration for N2O mole fractions; standards (~0.199–0.975 µmol mol-1).
- Flux calculation and quality control:
  - Flux F calculated as F = (dC/dt0) × (ρV)/A, where dC/dt0 is initial rate of concentration change; derivatives obtained via linear and nonlinear asymptotic regression, selecting the best fit per chamber/time point.
  - Time resolution ~10 minutes; acknowledges potential underestimation of highly nonlinear fluxes.
  - Outliers removed (extreme flux values) prior to analysis.
- Statistical modeling:
  - Linear mixed-effects model with fixed effects: soil temperature (Tsoil), water table depth (zwater), ammonia-N deposition (F NH3), ammonium-N deposition (F NH4), nitrate-N deposition (F NO3).
  - Random effects: chamber location nested in block; model structure accounts for repeated measures and experimental blocking.

## Data structure and documentation (data assets and metadata)

- Data files (examples):
  - ancilliaryData-byChamber.csv: per-chamber metadata (experimental grid, plot, block, chamber coordinates, deposition fluxes, etc.).
  - ancilliaryData-byChamber-byDate.csv: chamber/date-specific metadata (gas name, file names, fluxes, temperature, deposition levels, etc.).
  - RCfluxOutput.csv: N2O fluxes computed by multiple models (linear, quadratic, asymptotic, HMR, best-fit) with confidence intervals, R^2, and methodological codes.
  - vegetation-speciesPercentCover-Whim-byChamber.csv: percent cover by species per chamber and date.
  - chemistry-NH4mgNperl-Whim-byChamber-byDate.csv, chemistry-NO3mgNperl-Whim-byChamber-byDate.csv: soil water ammonium and nitrate concentrations by chamber/date.
  - chemistry-pH-Whim-byChamber-byDate.csv: soil water pH by chamber/date.
- Data dictionaries and variable definitions:
  - Tables 2–8 outline variable names, units, descriptions, and data file contexts (e.g., ChamberID, PlotNumber, Form, Fnh3, Fnh4, Fno3, Ndep-total, Tair-degC, Tsoil-degC, WTdepth-cm).
- Units and measurement conventions:
  - Fluxes in nmol N2O m-2 s-1 (with multiple model variants).
  - Concentrations in mg N L-1 for soil NH4+/NO3-; temperature in °C; depth in cm; deposition fluxes in kg N ha-1 y-1.
- Documentation of data provenance:
  - Clear linkage between field deployment (plots, blocks, chambers) and data outputs (flux calculations, model fits, and QA details).

## Quality control, uncertainty, and limitations (data quality)

- Outlier handling: 4 flux measurements removed (>10 nmol m-2 s-1) and 2 removed (< -2 nmol m-2 s-1).
- Uncertainty and calibration:
  - Flux uncertainty addressed via multiple flux estimation models; calibration against standard gases; 4-point calibration for GC data; consideration of initial rate drift.
  - Acknowledgement of potential underestimation due to time resolution and non-linearity in concentration changes.
- Data integrity features:
  - QA steps embedded in flux calculations (choice of dC/dt0 regression method based on goodness-of-fit).
  - Comprehensive metadata to facilitate reproducibility of flux estimates and model selections.

## Governance and reuse considerations for Data Stewards

- Data governance focus:
  - Documentation-rich dataset with explicit data dictionaries, method descriptions, and modeling approaches, enabling reproducibility and auditability.
  - Explicit notes on measurement techniques, calibration, and uncertainty to support transparent data reuse.
- Reuse guidance for data consumers:
  - Use RCfluxOutput.csv for cross-model comparison of N2O flux estimates; use best-fit method field to reproduce study results.
  - Refer to ancillary files for context on plot-level deposition rates, chamber locations, environmental conditions, and vegetation context.
  - Be aware of the potential underestimation risk due to measurement cadence when interpreting flux magnitudes.
- Repository and interoperability suggestions:
  - Maintain linkage between chamber IDs (EPPS codes), plot numbers, block IDs, and full spatial-temporal metadata.
  - Preserve both raw (gas chromatograph outputs) and derived data (flux estimates, model fits) to enable re-analysis with alternative models.
  - Ensure clear versioning and plan for updating metadata if data are reprocessed or extended beyond 2002–2009.

## Endnote on accessibility (planning for sharing)

- The document indicates datasets are intended for upload to relevant portals and catalogues, with careful attention to data holdings, metadata richness, and clear variable definitions to support discoverability and reuse by Data Stewards and researchers.