# HYPROP-FIT User's Manual

- Overview
  - HYPROP-FIT is a Windows software package for analyzing data from evaporation experiments to derive unsaturated soil hydraulic properties using the simplified evaporation method (SEM).
  - It reads data from HYPROP-VIEW (.tvp), converts to HYPROP-FIT project formats (.bhdx for single campaigns, .bhdix for multiple campaigns), and can import separate retention and conductivity data (.RETC.csv, .COND.csv) or .fit/.fitx files.
  - Core capabilities:
    - Specify required evaluation parameters (e.g., column length, tensiometer positions, tare weights).
    - Visualize raw tensiometers and weight data; define start/stop evaluation points.
    - Recalculate tensions and net weight for retention and conductivity data; handle temporal interpolation and data aggregation.
    - Compute and visualize retention and conductivity curves; fit hydraulic models; report parameter values with uncertainties.
    - Export graphs, raw data, calculated data, fitted functions, and parameters.
  - Underlying science: SEM built on the simplified Wind method with enhancements (boiling retardation, air-entry considerations, integral method for bias reduction, Hermitian spline interpolation, automatic validity-range detection for conductivity data).

- Installation and Access
  - Installation: HYPROP.msi installer; requires Windows Installer and .NET Framework 4.0.
  - Access rights: Public User (default values, limited edits) vs Power User (full editing rights, including data corrections and cross-device datasets). Changes by Power Users can affect results; requires knowledge of processing steps.

- Starting and Managing a Project
  - On first start, you get a welcome screen; last-used dataset auto-loads unless the previous exit was abnormal.
  - File types and compatibility:
    - HYPROP raw projects: .bhdx (new) and .bhdi (older iteration)
    - Older HYPROP-VIEW imports: can convert tvp -> .bhdx
    - Independent data: .RETC.csv, .COND.csv
    - Multi-campaign projects: .bhdix
  - Upward compatibility: HYPROP-FIT 3.0+ can open older .bhd/.bhdi/.fit but saves in new formats; older HYPROP-FIT versions cannot open .bhdx.

- Processing Registers (Workflow)
  - Information
    - Nine groups of project parameters; HYPROP Parameters include Empty soil sampling ring weight (must be set per measurement), sample/ring weights, device weights, tensiometer air-entry settings, density, and metadata (site, soil type, etc.).
    - Measurement and geometry specifics (sample ring type, surface area, column height, tensiometer positions).
    - Measurements about tensiometer and scale uncertainties; zero-offset corrections if needed (with cautions about hydrostatic conditions).
    - Sensor unit and scale metadata for information only (not used in calculations).
  - Measurements
    - Two tensiometer readouts and net weight data are shown as graphs plus numerical values.
    - Data windows for raw tensiometer data and weight data; editing rights differ by user mode (Power User can edit; Public User cannot).
    - Interpretation guidance for tensiometer behavior (cavitation point marks end of directly evaluable data; automatic stop-point detection).
  - Evaluation
    - Calculation of retention (theta) and conductivity (K) data using SEM.
    - Absolute water contents can be derived from different options (initial water content via oven-dried dry soil weight, externally specified initial theta, or automatic estimation assuming full initial saturation).
    - Ability to add independent data points (e.g., WP4 or pressure plate data) and to import from .csv.
    - Interpolation options for raw data (affecting how mean values are computed).
  - Fitting
    - Fitting hydraulic models to data; SHYPFIT2.0 provides PDI-type models (retention and conductivity) including uni- and bimodal variants with capillary and adsorptive components; includes van Genuchten, Kosugi, and others, with scaling and adsorption options.
    - Nonlinear global optimization (SCE algorithm) to find parameter sets; no need for initial guesses.
    - Options to enable integral fitting (mean column water content) vs classic point-wise fitting; requires column length for integral approach.
    - Model selection and parameter bounds: default broad ranges suitable for most soils; adjustable by power users; resetting occurs if model is changed.
    - Output: fitted parameter values with 95% confidence intervals, RMSE for retention and conductivity, AICc for model selection, and optional uncertainty shading.
    - Parameter correlation matrix to assess identifiability; watch for high parameter correlations (over-parameterization).
    - Graphs show HYPROP data, added data, and fitted curves; can export results.
  - Export
    - Export formats: CSV, Excel (.xls/.xlsx), HYPROP export (CSV-based), and HYDRUS MATER.IN for HYDRUS simulations.
    - Export configuration includes filename templates, directory selection, and content selection (raw data, calculated data, fitted curves, base points, etc.).
    - Base points on export enable calculation of water contents at specified pF values (e.g., field capacity, wilting point).
  - Post-Processing and Templates
    - Post-processing actions can be defined to occur after exporting.
    - History tracking of recent exports; templates for export configuration can be saved and reused.

- Processing Multiple Data Sets
  - HYPROP-FIT can assemble multiple campaigns into a single HYPROP binary iteration project (.bhdix) to compare campaigns or fit a single hydraulic function to several data sets.
  - Individual campaigns can be activated/deactivated; campaigns are color-coded for distinction; fitting can be performed across all depicted data.

- Model and Theory Details (Appendices)
  - SHYPFIT2.0 SHYPFIT2.0 integrates PDI model families for retention and conductivity, including:
    - Retention: unimodal and bimodal van Genuchten (constrained and unconstrained), Kosugi, and combinations with scaling and adsorption; extends to multi-modal formulations.
    - Conductivity: capillary and film contributions; possible inclusion of isothermal vapor conductivity.
    - Optional vapor conductivity term K_vap following Saito et al. (2006).
  - General formulation:
    - Retention: theta(h) = (theta_s - theta_r) S_cap(h) + theta_r S_ad(h)
    - Conductivity: K(h) = Ks [ (1 - omega) K_rel_cap(S_cap) + omega K_rel_film(S_ad) ]
  - Parameter estimation
    - Global optimization with shuffled complex evolution (SCE) to avoid local minima.
    - Parameter bounds designed for physical plausibility; bounds depend on model type.
  - Integral vs classic fitting
    - Integral method uses mean water content over column height; requires column length data; accounts for nonuniform moisture distribution.
  - Weighing schemes
    - Three schemes to balance retention and conductivity data during fitting, including user-defined weights and normalization strategies.
  - Uncertainty and diagnostic metrics
    - Parameter uncertainties via covariance projection; confidence intervals for parameters and model outputs.
    - RMSE, Nash-Sutcliffe, r^2, AICc/BIC/KIC for model comparison.
    - Uncertainty bands on function plots (Power User option).
  - Data quality and interpretation guidelines
    - Emphasis on accurate tensiometer offsets, stable hydrostatic conditions, and careful interpretation of stop points and air-entry points.

- Outputs and Example Metrics
  - Field capacity and plant available water (derived from fitted curves at specified pF values).
  - Export-ready data formats suitable for external analysis and HYDRUS modeling.
  - Documentation of data provenance, supporting data, and model parameters to support reproducibility.

- Appendices and References
  - Appendix 1: Theoretical basics of SEM (tensiometer setup, calculation of theta and hydraulic properties).
  - Appendix 2: Automatic estimation of initial water content; formula-based estimation when oven-dried soil weight is unavailable.
  - Appendix 3: SHYPFIT2.0 User's Manual with detailed model formulas, parameter definitions, and additional model families.
  - Comprehensive references to Peters, Durner, Schindler, Iden, and colleagues for theoretical and methodological foundations.

- Practical Takeaways for Monitoring Framework Authors
  - HYPROP-FIT provides a structured, transparent workflow to convert evaporation experiment data into soil hydraulic properties, with explicit data provenance, metadata fields, and adjustable processing controls.
  - It supports rigorous model selection and uncertainty assessment, aiding transparent documentation of methodological choices in monitoring frameworks.
  - The tool accommodates data gaps and formats common in environmental monitoring (integration of multiple campaigns, external retention/conductivity data, and cross-compatibility with HYPROP and HYDRUS workflows).
  - Export options and templates facilitate sharing results and enabling reproducibility within policy-relevant monitoring programs.