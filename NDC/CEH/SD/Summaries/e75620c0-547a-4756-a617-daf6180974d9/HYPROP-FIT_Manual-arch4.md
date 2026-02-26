# HYPROP-FIT User's Manual

- An in-depth software manual for HYPROP-FIT, a Windows-based tool to analyze evaporation experiments and fit unsaturated soil hydraulic properties.
- Free, public-domain software that reads HYPROP data, processes it, fits hydraulic models, and exports results for further use.

## Scope and core capabilities

- Reads raw HYPROP data from HYPROP-VIEW (TVP files) and converts them to HYPROP-FIT formats (.bhdx for single campaigns, .bhdi/.bhdix for iteration or multiple campaigns).
- Accepts separate retention and conductivity data (ASCII ._RETC.csv and ._COND.csv) and/or pre-assembled project data (.fit, .fitx).
- Performs complete data processing workflow: parameter specification, visualization, data re-calculation (tension and weight), and generation of retention and conductivity data.
- Fits hydraulic functions to data using SHYPFIT2.0 (integration with isothermal vapor conductivity, multi-model capability) and exports graphs, raw data, calculated data, fitted functions, and parameter sets.
- Supports multi-dataset projects (.bhdix) to compare campaigns and fit functions across campaigns simultaneously.

## Data formats and compatibility

- Input data formats:
  - HYPROP-VIEW raw campaigns: .tvp
  - HYPROP-FIT single campaigns: .bhdx
  - HYPROP-FIT iteration/combined campaigns: .bhdi, .bhdix
  - Independent retention and conductivity data: _RETC.csv, _COND.csv
  - Predefined data sets: .fit, .fitx
- Output and interoperability:
  - Graphs, raw data, calculated data, fitted functions, and parameters exportable in:
    - CSV and Excel (.xls/.xlsx)
    - HYPROP-FIT self-contained export formats (three files: <name>_Config.csv, <name>_Tension.csv, <name>_Weight.csv)
    - HYDRUS-ready file: MATER.IN
  - Base points and export templates can be defined for downstream use; templates can be stored for repeated exports.
- Compatibility:
  - HYPROP-FIT 3.0+ uses extended file formats (.bhdx, .fitx) but can open older HYPROP formats (.bhd, .bhdi, .fit); older files are upgraded to new formats on save.

## Data processing workflow (five registers)

- Information
  - Manage project metadata, HYPROP parameters (e.g., empty ring weight, device weights), geometric parameters, and optional notes.
  - Distinguishes between Public User and Power User rights, with Power Users able to modify more settings.
- Measurements
  - Visualize and edit raw tensiometer readings and weight data.
  - Includes interpretation guidance (tension dynamics, cavitation stop point, air-entry behavior) and automatic stop point detection.
  - Supports manual adjustment of stop and air-entry points; shows data and saturation dynamics over time.
- Evaluation
  - Calculate and visualize retention (theta(h)) and conductivity (K(h)) data.
  - Supports calculation of absolute water contents; options for initial water content from dry soil weight or externally set values; automatic initial theta estimation when possible.
  - Allows adding independent data points (e.g., WP measurements) and reading data from CSV files.
  - Interpolation choices for raw data (polynomial, piecewise linear, Hermite splines) and integration vs. classic fitting approaches.
- Fitting
  - Fit hydraulic models to data: five retention models (including Brooks-Corey, Fredlund-Xing, van Genuchten; unimodal/bimodal; scaled/unscaled; adsorption on/off) with PDI variants for capillary/films and vapor conductivity consideration.
  - Parameter estimation via global optimization (SCE) with configurable bounds; no need for initial guesses.
  - Outputs include optimized parameters, 95% confidence intervals, RMSE for retention and conductivity, and model selection metrics (AICc, BIC, KIC).
  - Visualization of fitted curves and uncertainty bands; ability to view parameter correlations.
  - Options to compute field capacity and plant-available water (PAW) from fitted curves.
- Export
  - Export graphs, raw data, and fitted results in multiple formats; customizable filename formats and directories.
  - Post-processing actions and export history are trackable.

- Multi-dataset processing (bhdix)
  - Assemble separate campaigns into a combined project; campaigns can be toggled on/off for fitting.
  - Data from campaigns are color-coded for distinction; fitting can be performed across multiple campaigns simultaneously.

## Data quality, governance, and usability

- Access control and collaboration
  - Public User vs Power User modes control write access to sensitive parameters and data edits; Power Users can adjust data and device configurations, so changes require domain expertise.
- Data integrity and validation
  - Automatic stop-point detection (cavitation) and optional air-entry point usage to extend measurement range; users can manually adjust when automatic detection is uncertain.
  - Offsets and calibration: tensiometer offsets can be corrected, but must be used cautiously to avoid systemic errors.
  - Units and regional settings: ensures correct units and decimal separators, consistent with Windows regional settings.
- Uncertainty and model selection
  - Parameter uncertainty via covariance-based methods; output uncertainty bands on function plots (Power User feature).
  - Multiple model selection criteria (AICc, BIC, KIC) to guide model choice given data and parameter count.
  - Parameter correlation matrices to diagnose over-parameterization and identifiability issues.
- Data lineage and reproducibility
  - Full traceability from raw TVP data to final fitted parameters and exportable results; supports re-running with different model choices or weights.
  - Upward compatibility with older HYPROP formats and clear documentation of file format changes.

## Practical implications for Data Leaders

- End-to-end data workflow in a single tool:
  - Ingests raw measurement data, applies metadata, performs quality checks, and outputs ready-to-use data products for reporting, modeling, and decision-making.
- Data quality and standardization:
  - Explicit handling of units, offsets, and uncertainty; supports standardized exports (CSV, Excel, HYDRUS MATER.IN) to integrate with broader data pipelines and simulations.
- Reproducibility and auditability:
  - Global optimization (SCE) with well-documented parameter bounds and model choices; transparent reporting of RMSE, AICc, BIC, KIC, and confidence intervals.
- Data integration and collaboration:
  - Supports combining campaigns (.bhdix) for cross-campaign comparisons and joint model fitting; facilitates sharing of metadata, inputs, and outputs with stakeholders and partners.
- Data strategy alignment:
  - Freely available, traceable software that adheres to documented model structures (PDI), enabling alignment with open data practices, methodological transparency, and potential extension to wider data communities.

## References and theoretical background

- The manual references foundational literature on the simplified evaporation method, SHYPFIT2.0, and PDI-based soil hydraulic modeling, including key works by Peters, Durner, Schindler, and others.
- Appendices provide mathematical formulations for PDI retention/conductivity, capillary and film conduction, isothermal vapor conductivity, and SHYPFIT2.0 model definitions.