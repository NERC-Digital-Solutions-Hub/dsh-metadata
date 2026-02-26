# HYPROP-FIT User's Manual Version 3.0, June 2015

## Overview
- HYPROP-FIT is a Windows-based software tool for analyzing evaporation-experiment data and fitting unsaturated soil hydraulic properties.
- It reads HYPROP-View data (.tvp), converts to HYPROP-FIT formats (.bhdx for single campaigns, .bhdix for multiple campaigns), and can import separate retention and conductivity datasets (.RETC.csv and .COND.csv or .fit/.fitx).
- Main workflow: specify evaluation parameters, visualize raw data, compute retention and conductivity data, fit hydraulic models, and export graphs and data.
- Supports combination of multiple campaigns for joint fitting; upward compatibility with older HYPROP data formats.

## Data inputs and formats
- Input data types:
  - Raw HYPROP measurements: HYPROP-VIEW (.tvp)
  - HYPROP project data: binary HYPROP files (.bhd, .bhdx, .bhdi, .bhdix)
  - Separated data: retention and conductivity datasets in ASCII (.RETC.csv, .COND.csv) or HYPROP-FIT project formats (.fit, .fitx)
- File compatibility:
  - HYPROP-FIT 3.0+ uses .bhdx and .bhdix; older .bhd/.bhdi can be opened but are saved in new formats.
  - Old tensioVIEW (.tvp) can be converted into .bhdx via the Extras menu.
- Outputs:
  - Exported data and graphs in CSV, Excel (.xls/.xlsx), and HYPROP-FIT specific formats (including three files: <name>_Config.csv, <name>_Tension.csv, <name>_Weight.csv).
  - HYDRUS-compatible file MATER.IN.
  - Flexible base points for water contents at selected pF values.
- Data organization:
  - Projects are organized into five registers: Information, Measurements, Evaluation, Fitting, Export.
  - Multiple datasets campaigns can be bundled into a single .bhdix project for simultaneous processing.

## Metadata and data governance (Information register)
- Metadata groups and editable access:
  - General Information: sample name, start/stop times, duration, site/soil notes, etc.
  - Weight and Volume Corrections: volume corrections and tare weight adjustments.
  - Geometric Parameters: cylinder type, soil surface area, column height, tensiometer positions.
  - HYPROP Parameters: empty soil ring weight (must be specified per measurement), measurement head weight, air-entry pressures, density of solids, etc.
  - Measurement Uncertainty: tensiometer and scale uncertainties.
  - Tensiometer Offset Correction: optional offsets for upper/lower tensiometers.
  - Sensor Unit Information and Scale Information: device serials, names, and firmware versions.
  - Notes: free-text fields for provenance and context (recommended for data classification and future reuse).
- Data governance implications:
  - Public Users can edit a subset of fields; Power Users can modify more parameters and potentially data records.
  - Accurate per-measurement values (e.g., Empty soil ring weight) are critical since errors directly affect water content calculations.
  - Units and regional decimal separators must be respected; changes are reflected across calculations.
  - Documentation of data provenance, device configurations, and measurement context is encouraged to enable discovery and reuse.

## Data processing workflow and quality assurance
- Measurements (Data capture and editing):
  - Visualize tensions from two tensiometers and weight changes.
  - Stop point detection: automatic cavitation point marks end of directly evaluable tension data; can be adjusted manually.
  - Cavitation requires properly prepared tensiometers (gas-free) to ensure valid data.
  - Air-entry point optional for extended data range (Power User); vertical lines indicate air-entry times; interpolation used between last reliable data and air-entry point.
- Evaluation (Retention and conductivity calculation):
  - Apply the simplified evaporation method (SEM) to derive retention and conductivity curves from tensions and weights.
  - Compute absolute water contents using options for initial water content (from dry weight, externally set values, or automatic estimation assuming full saturation).
  - Optional incorporation of independent data points (CSV import or manual entry) to augment retention/conductivity data.
- Fitting (Hydraulic models and parameter estimation):
  - Fit parametric models for θ(h) and K(h) (PDI family and variants) to data; SHYPFIT2.0 handles model selection and parameter estimation.
  - Multimodel fitting with non-linear optimization; supports incorporating multiple data types with weighting schemes.
  - Parameter uncertainty: 95% confidence intervals; correlation matrices; model selection criteria (AICc, AIC, BIC, KIC).
  - Options for interpolation methods (classic point-based vs. integral mean water content over column) and mean suction calculations.
  - Field capacity and plant available water are derived from fitted retention curves.
- Export (Sharing and downstream use):
  - Export graphs, raw data, calculated data, fitted curves, and parameters.
  - Supports templates and base points; exported data can be re-imported into HYPROP-FIT for reproducibility.
  - Post-processing options can automate actions after export.

## Practical considerations and caveats
- Data integrity and accuracy:
  - Tensiometer offsets, sensor calibrations, and unit handling are critical; small errors amplify into incorrect conductivity and water content estimates.
  - The automatic stop-point and air-entry detections may require manual adjustment if measurement conditions are imperfect.
  - Correct dry soil weight and other geometry/density parameters are essential to avoid cascading errors in porosity and water content calculations.
- Model and data limitations:
  - The method assumes time-invariant hydraulic properties and validity of Richards-flow-based interpretation within SEM, with caveats for high-suction ranges and vapor conductivity considerations.
  - Numerical fitting involves potential over-parameterization; model selection criteria and parameter correlations help guard against overfitting.
- Multidataset capability:
  - HYPROP-FIT supports combining campaigns (.bhdix) for joint fitting; data from different campaigns are color-coded and can be toggled for inclusion in analyses.

## Data management, interoperability, and governance in practice
- Versioning and compatibility:
  - HYPROP-FIT 3.0 introduces new file formats (.bhdx/.bhdix) with upward compatibility from older HYPROP data, but older HYPROP-FIT versions cannot read .bhdx files.
- Standards and metadata richness:
  - Rich, structured metadata in Information, including per-measurement ring weights and device settings, supports data discovery and reuse across projects.
- Accessibility and roles:
  - Distinct user roles (Public vs Power User) balance ease of use with protection of data integrity; governance practices should document who altered measurements and why.
- Data sharing and reuse:
  - Export formats (CSV, Excel, HYDRUS MATER.IN) and base-point definitions facilitate reuse in modeling workflows and cross-software analyses.
- Provenance and traceability:
  - The History section within Export provides an export activity trail; the combination of campaigns into .bhdix preserves campaign provenance.

## References and underlying methodology
- Core methodology relies on the simplified evaporation method (SEM) for deriving soil hydraulic properties, including improvements like integral fitting and Hermitian interpolation to reduce bias near saturation.
- SHYPFIT2.0 provides the model-fitting backbone (PDI framework, multiple retention and conductivity models, and uncertainty analysis).
- Key literature and methodological notes underpinning the tool include Peters & Durner, Schindler et al., and related works on pore-scale hydraulic modeling and data interpretation.