HYPROP-FIT User's Manual

## Aim and Scope
- Software tool for Windows to analyze evaporation experiments and fit unsaturated soil hydraulic properties using the simplified evaporation method (SEM).
- Outputs include retention and conductivity curves, fitted hydraulic parameters with uncertainties, and exports of graphs/data for policy/monitoring workflows.
- Integrates data from HYPROP measurement campaigns (HYPROP-View .tvp files) and supports separate retention/conductivity data; also compatible with legacy HYPROP formats.

## Data Inputs and Formats
- Input data types:
  - Raw HYPROP data from HYPROP-VIEW (.tvp) campaigns.
  - HYPROP binary projects (.bhd, .bhdx) and binary iteration projects (.bhdi, .bhdix).
  - Separate retention (_RETC.csv) and conductivity (_COND.csv) data, or project files (.fit, .fitx).
  - Older data can be imported via conversion tools; new version uses extended .bhdx/.bhdix formats with upward compatibility from older files.
- Data processing follows SEM principles using measured tensions and weights to derive water contents and hydraulic properties.

## Installation and Access
- Installation via Microsoft Installer (HYPROP.msi); requires Windows Installer and .NET Framework 4.0.
- Two user modes:
  - Public User: uses default values; restricted editing.
  - Power User: advanced editing and data manipulation; responsible for parameter changes and outlier handling.
- Program start loads last dataset unless previous exit was abnormal.

## Getting Started: Projects and Data Management
- File menu workflows:
  - Open/modify/store HYPROP projects (information, measurements, evaluation, fitting, export registers).
  - Extras menu for converting tensioVIEW tvp files and joining campaigns into a single .bhdix project.
  - Help menu for manual access and update checks.
- Reading legacy data:
  - Convert tensioVIEW tvp files to HYPROP binary projects (.bhdx); new projects can be stored in a new folder.
- Data types and compatibility:
  - Supports single-campaign (.bhdx) or multi-campaign (.bhdix) datasets; multi-campaign projects allow simultaneous fitting across campaigns.

## Data Processing Workflow
- Registers concept:
  - Information: project metadata, HYPROP parameters, geometric and device constants, and user-editable inputs (e.g., Empty soil sampling ring weight per measurement).
  - Measurements: visualization and editing of tensions (two tensiometers) and weight data; data windows for manual edits by Power Users.
  - Evaluation: calculation of retention θ(h) and conductivity K(h); includes data interpolation options and optional inclusion of independent data.
  - Fitting: selection of hydraulic models, parameter estimation, and uncertainty analysis.
  - Export: export of graphs, raw data, calculated data, and fitted curves in multiple formats.
- Key data considerations:
  - Measurements window shows tensions, temps, and timing; a cavitation point in the upper tensiometer marks the typical stop point for direct evaluation.
  - The stop point can be manually adjusted; automatic stop-point detection is available.
  - Air-entry point (Power User) can extend the measurement range by using the air-entry pressure as an additional tension measurement point; vertical reference lines indicate these times; can be reset if auto-detection is inaccurate.
  - Weight graphs display net weight (soil + water) and total weights; stage-1 and stage-2 evaporation are interpreted from the weight loss trend.

## Visualization and Quality Assurance
- Tension graph: shows upper and lower tensiometer tension over time; data points can be shown individually on demand.
- Weight graph: shows net weight and total weight with stop/air-entry lines; data can be edited and re-visualized.
- Data interpretation: cavitation behavior, boiling retardation, and hydrostatic conditions inform data validity; incorrect tensiometer prep can affect end results.
- Data windows (tensiometer and weight) allow direct editing by Power Users; edits update graphs in real time.

## Evaluation and Data Integration
- Evaluation computes retention θ(h) and conductivity K(h) from the measured tensions and weights within the start/stop window.
- Absolute water contents:
  - Option 1: derive initial water content from dry soil weight; enables calculation of porosity, dry bulk density, etc.
  - Option 2: user-specified initial water content (may not permit all derived parameters).
  - Automatic initial θs: if dry soil weight is unavailable, the software can estimate initial θs assuming full saturation (approximate).
- Independent data integration: users can add external retention/conductivity points or import from CSV files; units (pF, % for θ, and log10 cm/d for K) must be consistent.
- Interpolation options for raw data: polynomial, piecewise linear, or Hermitian splines (configurable in Evaluation).
- Evaluation results feed into the fitting step and exported outputs.

## Fitting Hydraulic Models
- SHYPFIT2.0 is used for model selection and parameter fitting; model space includes:
  - PDI family models: van Genuchten (constrained and unconstrained), Kosugi, and Durner bimodal/unimodal variants; scaling and adsorption options; inclusion of isothermal vapor conductivity.
  - Options include capillary, film, and combined conductivity components; vapor contribution can be added as a separate term.
- Model fitting:
  - Simultaneous fitting of θ(h) and K(h) (or single dataset).
  - Optimization uses a global algorithm (SCE) to avoid local minima; boundaries for parameters are user-adjustable but physically constrained.
  - Integral vs classic fitting:
    - Classic: pointwise θ̂i(b) versus measured θi.
    - Integral: mean θ over the soil column, integrating θ(h) across the column height; used when measurements represent means (e.g., evaporation setups).
- Weighing schemes:
  - Scheme 1: user-defined weights based on measurement errors (inverse variances).
  - Scheme 2: normalized weights to balance data types and pF increments; scales data class ranges.
  - Scheme 3: user-defined class weights with pF-based weighting.
- Model selection and uncertainty:
  - Fit quality metrics: RMSE for θ and log K, Nash-Sutcliffe, r^2, AICc (corrected for small samples), BIC, and KIC.
  - Confidence intervals for parameters (95% level) and propagation to output curves via covariance matrices.
  - Parameter correlation matrix to assess over-parameterization and identifiability.
  - Optional uncertainty bands on fitted functions (Power User).
- Output visuals:
  - Graphs show measured data, HRPROP-derived points, and fitted curves; user can toggle visibility and export results.
- Field capacity and plant available water (PAW):
  - Immediately computed from fitted curves at specified pF values (e.g., 6, 33, 1500 kPa) as WC@pF and PAW between ranges.

## Output and Export
- Export formats:
  - CSV: raw, calculated, and base data; for re-import into HYPROP-FIT.
  - XLS/XLSX: multi-sheet Excel export with configuration, raw data, spline data, retention/conductivity data, fitted curves, model parameters, uncertainties, and base points.
  - HYDRUS MATER.IN: HYDRUS-ready table for retention, water capacity, and conductivity data.
  - Customizable base points for export (pF values and corresponding θ/K data) with templates.
- Export options and post-processing:
  - Template-based and per-session default settings; ability to batch export and manage histories.
- Processing multiple datasets:
  - Ability to assemble multiple campaigns into a single .bhdix project; datasets shown in colors; fitting can be performed across all depicted campaigns simultaneously; individual campaigns remain separable and editable.

## Multi-Dataset Management
- HYPROP-FIT supports assembling and processing multiple campaigns as a single binary iteration project (.bhdix).
- Campaigns can be activated/deactivated in the file explorer; data from different campaigns are colored distinctly; fitting can be performed across all included campaigns.

## Practical Considerations and Best Practices
- Precision in input parameters is critical: errors in ring weight, device masses, sample geometry, and densities propagate directly to absolute water contents and derived parameters.
- Tensiometers must be well-prepared to reveal cavitation; offsets can bias conductivity calculations; offset corrections should be used cautiously.
- Always use consistent units and respect regional decimal separators; the software adheres to Windows regional settings.
- The manual emphasizes the scientific basis and references key works by Peters, Durner, Schindler, and colleagues for methodological grounding.

## References and Appendices (Summary)
- Appendices cover theoretical basics of SEM, automatic initial θ estimation, and SHYPFIT2.0 manual with detailed mathematical models for PDI-based retention and conductivity, plus alternative models (Brooks & Corey, Fredlund & Xing).
- The SHYPFIT2.0 model library includes multiple retention and conductivity formulations, scaling, adsorption, and multi-modal combinations; provides extensive equations for K(h), C(h), and Γ(h) with details on analytical and numerical solutions.
- The document cites foundational works on evaporation methods, hydraulic properties, and model selection criteria (AICc, BIC, KIC), as well as practical guidance on data handling and interpretation.