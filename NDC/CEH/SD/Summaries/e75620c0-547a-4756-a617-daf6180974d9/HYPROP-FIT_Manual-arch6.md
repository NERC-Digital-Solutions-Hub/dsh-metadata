# HYPROP-FIT User's Manual

- Overview
  - Software tool for analyzing evaporation experiments and fitting unsaturated soil hydraulic properties.
  - Reads data from HYPROP-View projects (.tvp) and stores as HYPROP-FIT files (.bhdx for single, .bhdi/.bhdix for multiple campaigns).
  - Supports separate retention and conductivity data, exportable as .fitx or via standard formats.
  - Implements the Simplified Evaporation Method (SEM), extends range with air-entry points, boiling retardation, and automatic validity checks.
  - Freely available from UMS website.

- Input Data and File Formats
  - Types of data:
    - Raw HYPROP TVP data from HYPROP measurement campaigns.
    - HYPROP binary projects (.bhd, .bhdx), iteration projects (.bhdi, .bhdix).
    - ASCII files (_RETC.csv, _COND.csv) with retention and conductivity data.
    - Independent retention/conductivity data added in the Evaluation/Measurements or via .csv import.
  - Compatibility:
    - HYPROP-FIT 3.0+ uses extended .bhdx/.bhdix/.fitx formats; older projects open but are converted to new formats on save.
    - Old HYPROP-VIEW tvp data can be converted to .bhdx via Extras → Convert tensioVIEW Project.
  - Units and localization:
    - All numerical inputs have explicit units; decimal separators follow Windows regional settings (comma/dot).

- Installation and Access
  - Windows-based, install via HYPROP.msi; .NET Framework 4.0 or newer may be required.
  - Two user modes:
    - Public User: default values, restricted edits.
    - Power User: advanced edits, including data outliers and cross-device processing.
  - Project start behavior: loads last dataset if clean exit; otherwise starts with empty screen.

- Working with Projects
  - Opening, editing, and storing: File menu provides Open/Save and import of retention/conductivity data.
  - Registers (tabs) in a loaded project:
    - Information: nine groups of metadata and HYPROP parameters (e.g., sample name, measurement period, geometric and HYPROP-specific parameters, ring weight, tensiometer settings, density assumptions).
    - Measurements: visualization and editing of tensiometer tensions and sample weights; four windows (tension curves, weight data) with interactive zoom, pan, and data-point editing by Power Users.
    - Evaluation: calculation of water retention and conductivity data; options for initial water content and chosen calculation method (including automatic initial water content estimation).
    - Fitting: fitting hydraulic models to data; multiple model options and parameter bounds; joint fitting of retention and conductivity data; supports integral and classic fitting modes.
    - Export: export of graphs, raw and calculated data, fitted functions, and parameters in multiple formats (CSV, Excel, HYDRUS MATER.IN, etc.).
  - Extras: convert tensioVIEW data; join multiple campaigns into a single iteration project (.bhdix).

- Processing and Analysis Workflow
  - Data processing steps (common across registers):
    - Parameter specification for SEM (e.g., column length, tensiometer positions, tare weights).
    - Visualization and selection of start/stop evaluation points.
    - Recalculation of tensions and net weights for retention/conductivity data.
    - Temporal interpolation for low-resolution data and aggregation for high-resolution data.
  - Measurements:
    - Interpret tensions: cavitation in tensiometers marks reliable data end; automatic stop point detection can be adjusted manually.
    - Visualize air-entry points as optional additional tension measurements for extended ranges (Power User).
    - Weight data: stage-1 and stage-2 evaporation behavior; stage timings relate to evaporation control and surface-layer resistance.
  - Evaluation:
    - Compute retention θ(h) and conductivity K(h) from SEM data; supports using full mean column content for mean suction points.
    - Absolute water contents: options to calculate from dry soil weight, external initial θs, or automatic estimation assuming full saturation (with cautions).
    - Optional addition of independent data points or CSV-based data to augment fitting.
  - Fitting:
    - Models: PDI family (capillary + adsorptive water retention) with variants (van Genuchten, Kosugi, bimodal forms, constrained/unconstrained, scaling, adsorption).
    - Includes Brooks-Corey and Fredlund-Xing as additional retention models; vapor-phase conductivity option available.
    - Isothermal vapor conductivity can be added to K to yield K_total.
    - Parameter estimation uses global optimization (SCE) to avoid local minima; parameter bounds are provided and editable.
    - Options:
      - Integral vs classic fitting (integral is mean content across the column; requires column length).
      - Weighing schemes to balance retention vs conductivity data; default emphasizes retention data but can be tuned.
      - Uncertainty visualization with optional 95% confidence bands (Power User).
  - Export:
    - Multiple formats: CSV, Excel (.xls/.xlsx), HYPROP export (.csv trio), HYDRUS MATER.IN, and templates.
    - Users can define base points (pF values) for derived data like field capacity and wilting point; templates can be saved for repeated exports.

- Model Fitting and Evaluation Details
  - Objective function:
    - Simultaneous fitting of θ(h) and K(h) by minimizing weighted squared residuals; supports single or dual data types (retention and conductivity).
  - Global optimization:
    - Uses shuffled complex evolution (SCE) to locate the global minimum and avoid reliance on initial guesses.
  - Model selection and uncertainty:
    - Reports RMSE for retention and log(K) for conductivity; provides AICc, BIC, and KIC for model comparison.
    - Parameter uncertainties derived from covariance; displays 95% confidence intervals.
    - Parameter correlation matrix available to assess identifiability and potential over-parameterization.
  - Output visualization:
    - Fitted curves alongside data with optional uncertainty shading.
    - Function graphs show HYPROP data and added data; can export graphs for reports/dashboards.
  - Field capacity and PAW:
    - Provides calculated field capacity and plant available water (PAW) from fitted curves at specified pF values.

- Data Quality and Practical Guidance
  - Important considerations:
    - Cavitation stop point: automatic stop point detection relies on sharp cavitation; if data are not well-prepared, manual adjustment may be needed.
    - Tensiometer offsets: ensure hydrostatic conditions; offsets can bias conductivity estimates.
    - Input units and regional decimal separators must be observed.
  - Data integration:
    - The platform supports combining multiple campaigns into one iteration project for joint analysis and comparative fitting.
  - Outputs for data use:
    - Exports include ready-to-use HYDRUS inputs and comprehensive reports suitable for dashboards and policy/technical updates.

- Relevance for Data Support
  - Data integration and quality:
    - Handles diverse data sources (raw campaign data, aggregated retention/conductivity data, external measurements) and provides consistent formats for downstream analysis.
  - Data transformation:
    - Interpolates, aggregates, mean-value computations, and transforms data into retention/conductivity curves with uncertainty estimates.
  - Productization and dissemination:
    - Produces shareable data products (graphs, tables, MATER.IN) and templates for reproducible analyses across teams or projects.
  - User assistance and governance:
    - Clear distinction between Public and Power User roles supports governance, auditability, and controlled data processing.

- References and Scientific Basis
  - Seminal works and developments cited (Wind, Schindler, Peters & Durner; SHYPFIT2.0 background; PDI model framework; and related literature) to justify the models and fitting approaches used.

- Key Takeaways for Data Support Perspective
  - HYPROP-FIT provides an end-to-end pipeline: from raw campaign data to published hydraulic property functions with uncertainty estimates.
  - It supports data consolidation across campaigns and external data, enabling self-contained data products and dashboards for water retention and conductance analyses.
  - The tool emphasizes data quality checks (stop/air-entry points, offsets, units) and robust, globally optimized parameter estimation with transparent uncertainty reporting.
  - Outputs are readily consumable by external tools (HYDRUS) and in common formats (CSV, Excel), facilitating data reuse and integration into broader analytics workflows.