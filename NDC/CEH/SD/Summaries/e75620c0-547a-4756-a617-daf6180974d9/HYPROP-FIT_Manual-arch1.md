# HYPROP-FIT User's Manual

- HYPROP-FIT is a Windows-based software to analyze evaporation-experiment data and fit unsaturated soil hydraulic properties.
- Core capabilities include parameter specification, visualization of raw data, re-calculation of tensions and weights, calculation of retention and conductivity data, fitting hydraulic functions, and exporting graphs, data, and parameters.
- Works with data from HYPROP-View (.tvp), HYPROP binary projects (*.bhdx, *.bhdi), and separate retention/conductivity data (*.fitx, _RETC.csv, _COND.csv).
- Implements the Simplified Evaporation Method (SEM) with extensions (air-entry, boiling retardation) and integrates SHYPFIT2.0 (PDI models) for fitting.

## Installation and Access

- Installation: use the Microsoft Installer (HYPROP.msi) or setup.exe; ensure Windows Installer and .NET Framework 4.0 are available.
- User access modes:
  - Public User: default values; fewer edit permissions.
  - Power User: advanced editing of parameters and data; can modify outliers and cross-device data. Changes can impact results; should be used by knowledgeable users.

## Data and Projects

- Data types processed:
  - Raw HYPROP data from HYPROP-View (.tvp)
  - HYPROP binary projects (.bhd, .bhdx) and iteration projects (.bhdi, .bhdix)
  - Separate retention and conductivity data in ASCII (.RETC.csv, .COND.csv) or in project format (.fit, .fitx)
- File format updates:
  - HYPROP-FIT 3.0 introduces .bhdx and .fitx formats with upward compatibility from older formats (.bhd, .bhdi, .fit).
- Importing older campaigns:
  - Convert tensioVIEW tvp files to HYPROP binary projects via Extras > Convert tensioVIEW Project (tvp) files.
- Multi-campaign handling:
  - Join campaigns into a single .bhdix iteration project; data from campaigns are color-coded and can be activated/deactivated for joint fitting.

## Getting Started: Starting, Opening, Processing

- Start: HYPROP-FIT launches with a welcome screen; loads last used dataset if regular shutdown occurred.
- Project structure: five registers per project — Information, Measurements, Evaluation, Fitting, Export.
- Data loading: open existing .tvp, .bhdx, .bhdi, or .fitx; import separate RETC/COND data as needed.
- Compatibility: HYPROP-FIT 3.0 files open in v3.0+; older projects can be opened but will be saved in new formats (.bhdx, .fitx).

## Processing Data (Registers)

- Information: specify project and HYPROP parameters (e.g., sample name, start/stop times, geometric parameters, empty ring weight, head weights, tensiometer air-entry options, density assumptions). Distinct editable fields for Public User vs Power User.
- Measurements: visualize and edit raw data (tensions from two tensiometers and sample weights) via four windows; supports zooming and editing by Power Users; automatic stop-point (cavitation) detection for the upper tensiometer; manual adjustments possible.
- Evaluation: compute retention (θ(h)) and conductivity (K(h)) data from measured tensions and weight changes; supports:
  - Absolute water content calculations (initial water content, porosity, dry bulk density, and dry soil weight)
  - Automatic initial water content estimation (assuming full saturation) when dry soil weight is unavailable
  - Addition of independent data points (RETC/COND) and reading from .csv files
  - Interpolation settings for raw data (e.g., Hermite splines, polynomial, or linear)
- Fitting: fit hydraulic models to data and visualize results
  - Model types: multiple retention and conductivity models within the PDI framework (van Genuchten, Kosugi, Durner bimodal/unimodal variants, Brooks-Corey, Fredlund-Xing, etc.)
  - PDI approach: combines capillary and adsorptive retention with capillary and film conductivities; optionally includes isothermal vapor conductivity
  - Curve fitting via SHYPFIT2.0, using global optimization (SCE) to avoid local minima
  - Model options include scaling (scaled vs unscaled), adsorption (ads) and bimodal/unimodal variants; can include or exclude vapor conductivity
  - Integral vs classic fit: integral fit uses mean water content over the column, accounting for column height; classic fit uses point water contents
  - Parameter bounds: default wide ranges; user can constrain or fix parameters
  - Output metrics: RMSE for retention (RMSE θ) and conductivity (RMSE K in log scale), AICc, BIC, KIC for model selection; parameter correlations; optional uncertainty bands on fitted curves
  - Field capacity and PAW: automatically computed from fitted curves (WC at pF 1.8, 2.5, 4.2; PAW between specified pF values)
- Export: various formats
  - CSV, Excel (xls/xlsx) with multiple sheets
  - HYDRUS MATER.IN file for direct HYDRUS simulations
  - User-defined filename formatting and base points (pF values) for export
  - Templates for export and post-processing options

## Visualization and Data Handling

- Graphs: three main graph types (tension vs. time; weight vs. time; optional data points and spline support points)
- Stop point: automatic detection at cavitation; can be manually adjusted
- Air-entry point (Power User): optionally include the air-entry tension as extra measurement points; vertical lines mark air-entry times; requires long enough measurement to observe air-entry
- Data points and spline support points: can be toggled on/off for clarity
- Data point editing: Power Users can edit, insert, or delete lines in tension and weight data windows; changes update graphs in real time

## Modeling and Parameter Estimation

- SHYPFIT2.0 integration: selects and fits PDI-based models to θ(h) and K(h); no requirement for initial guesses
- Objective function: weighted sum of squared residuals for θ and K; supports multi-objective fit with adjustable weighting
- Global optimization: shuffled complex evolution (SCE) to avoid dependence on initial guesses
- Parameter bounds and correlations: default boundaries ensure physical plausibility; a correlation matrix is available to diagnose over-parameterization
- Model selection criteria: AICc (with small-sample correction), BIC, and KIC provided
- Uncertainty handling:
  - Parameter uncertainties via covariance matrix (linear approximation)
  - Function uncertainties via covariance propagation to model outputs
  - Optional 95% confidence bands on fitted curves (Power User)

## Output and Export

- Export options include:
  - Graphs and raw data
  - Calculated data and fitted functions
  - Base points and pF references for external use
  - HYDRUS MATER.IN compatibility format
- Export settings: filename format, directory, content selections, and post-processing steps are configurable within a session

## Multiple Data Sets and Projects

- HYPROP binary iteration projects (.bhdix) enable combining several campaigns for joint fitting
- Individual campaigns remain unchanged; combined projects allow cross-campaign comparisons
- Data from campaigns are color-coded and selectable in the file explorer

## References and Scientific Context

- HYPROP-FIT builds on the Simplified Evaporation Method (SEM) and its extensions (air-entry, boiling retardation)
- SHYPFIT2.0 implements PDI-based retention and conductivity models, including unimodal/bimodal van Genuchten, Kosugi, and related variants
- The tool supports integral fitting to account for non-uniform moisture distribution within a column and is designed to provide uncertainty assessment and model-selection metrics