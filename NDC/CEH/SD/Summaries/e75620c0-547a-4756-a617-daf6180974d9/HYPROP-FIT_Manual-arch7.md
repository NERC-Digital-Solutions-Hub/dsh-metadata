HYPROP-FIT User's Manual

- Purpose and scope
  - Software tool for analyzing evaporation-based soil hydraulic measurements and fitting unsaturated hydraulic properties.
  - Reads data from HYPROP-View (tension and weight records) and outputs soil water retention and hydraulic conductivity curves, with parameter estimates and uncertainty.
  - Provides export options for further GIS or modeling workflows (CSV, Excel, HYDRUS MATER.IN, and more).

- Data inputs and formats
  - Raw data: HYPROP measurement campaigns from HYPROP-View (.tvp).
  - Processed projects: HYPROP binary projects (.bhdx for single campaigns; .bhdi/.bhdix for iterations/multiple campaigns).
  - Separated data: retention and conductivity data in ASCII (_RETC.csv, _COND.csv) or as HYPROP-FIT project files (.fit, .fitx).
  - Compatibility: HYPROP-FIT 3.0+ uses extended formats (.bhdx, .bhdix, .fitx); older projects open but are converted to new formats upon saving.
  - Import from older HYPROP-VIEW: Convert tvp files to .bhdx via Extras > Convert tensioVIEW Project.

- Processing workflow (five registers)
  - Information
    - Define project metadata and HYPROP parameters (e.g., sample name, measurement start/stop, geometry, empty ring weight, device tared weights, air-entry values, density assumptions).
    - Distinguishes Public User vs Power User permissions (editing rights and data manipulation).
    - Units and region-specific decimal separators are user-facing considerations.
  - Measurements
    - Visualization and editing of measured tensions (two tensiometers) and weights.
    - Stop point detection: automatic cavitation point of the upper tensiometer; can be manually adjusted.
    - Air-entry point option (Power User) to extend measurable range; vertical guidance lines shown; interpolation between stop and air-entry points.
  - Evaluation
    - Calculate retention (θ(h)) and conductivity (K(h)) from measured tensions and weights using the SEM framework.
    - Absolute water contents: options to compute from dry soil weight or externally supplied initial water content; automatic initial θs estimation possible if dry weight is unavailable.
    - Add independent data points (e.g., external WP4 or pressure plate data) and base points for export.
    - Interpolation settings for raw data (e.g., Hermitian spline vs polynomial vs piecewise linear).
  - Fitting
    - Simultaneous fitting of retention and conductivity models to data.
    - Model library includes Brooks-Corey, Fredlund-Xing, van Genuchten variants, Kosugi, unimodal/bimodal, scaled/unscaled capillary parts, and adsorption components (PDI family).
    - SHYPFIT2.0 handles model selection and parameter estimation using global optimization (SCE) with parameter bounds.
    - Options for integral vs classic fitting (mean column water content vs point values).
    - Uncertainty handling: RMSE, AICc, BIC, KIC; 95% confidence intervals for parameters; optional uncertainty bands on fit graphs; parameter correlation matrix.
    - Field capacity and plant available water values are computed from the fitted curves.
  - Export
    - Export graphs, raw/calculated data, fitted curves, and parameters in multiple formats.
    - Export formats include: CSV, XLS/XLSX, HYPROP-FIT internal CSV exports (<name>_Config.csv, <name>_Tension.csv, <name>_Weight.csv), HYDRUS MATER.IN, and a multi-sheet Excel file with detailed content (config, raw data, spline data, retention/conductivity, fitted curves, parameters, uncertainties, base points).
    - Templates and post-processing options for automated workflows.

- Multiset data handling and comparisons
  - HYPROP-FIT supports assembling multiple campaigns into a single HYPROP binary iteration project (.bhdix) for joint processing.
  - Campaigns can be activated/deactivated; data from different campaigns appear in distinct colors for comparison.
  - Fitting can be performed across all displayed campaigns simultaneously.

- Model fitting details and model selection
  - Parameter estimation is constrained by physically meaningful bounds; some parameters may be fixed by user.
  - Supports both unimodal and bimodal, scaled/unscaled, and adsorption-enabled variants.
  - Outputs include parameter values, 95% confidence intervals, RMSE for retention and conductivity, and AICc for model comparison.
  - Correlation matrix informs about parameter identifiability and potential over-parameterization.

- Practical considerations for GIS and data use
  - Units and decimal separators align with Windows regional settings.
  - Outputs are designed for integration with modeling tools (e.g., HYDRUS via MATER.IN) and standard data formats suitable for GIS-based analyses and map-based visualization.
  - Metadata fields (Notes) allow site coordinates, sampling dates, soil type, land use, and other contextual data to accompany datasets.
  - Documentation and references support understanding of the SEM and PDI-based models (Peters and Durner framework).

- Key outputs and deliverables
  - Retention and conductivity curves with uncertainties
  - Fitted model parameters and confidence intervals
  - Field capacity and PAW estimates from fits
  - Exportable graphs and tabular data for GIS pipelines and hydrologic modeling
  - Ability to include base points at specified pF values for targeted exports
  - Hydrus-compatible data file (MATER.IN) for downstream simulations

- References and methodological basis
  - SEM (Schindler, Peters & Durner) with enhancements (Hermitian interpolation, integral method, air-entry considerations)
  - PDI models for retention and conductivity (van Genuchten, Kosugi, Durner; unimodal/bimodal; capillary/film/adsorption components)
  - SHYPFIT2.0 as the fitting engine (global optimization; model selection via information criteria)

- Access and installation notes
  - Windows-based application; installation via setup with .msi
  - Two user modes: Public User and Power User; Power User offers broader data editing capabilities
  - Import/export supported across multiple data formats and campaign configurations