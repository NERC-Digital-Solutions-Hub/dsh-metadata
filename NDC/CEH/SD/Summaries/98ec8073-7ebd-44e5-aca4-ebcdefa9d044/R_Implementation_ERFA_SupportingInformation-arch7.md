# R implementation of the Ecological Risk due to Flow Alteration (ERFA) method

## Overview
- A software implementation (TEFRIC ERFA) of the Ecological Risk due to Flow Alteration (ERFA) method.
- Developed under the Translating Environmental Flow Research in Cambodia (TEFRIC) project, funded by NERC.
- Geographically focused on SE Asia (Mekong River Basin example data), but applicable wherever baseline and scenario river flow time series are available.
- Built as an R/Shiny application to facilitate interactive analysis, visualization, and reporting of ecological risk from flow changes.

## ERFA Method at TEFRIC
- Requires at least two monthly mean river flow time series at a location: baseline (historical or natural) and a scenario (e.g., a water resource project or climate projection).
- For each year in the simulation period, computes a set of hydrological variables and derives Monthly Flow Regime Indicators (MRFIs).
- Allows definition of the hydrological year and low/high flow thresholds using percentile-based cutoffs (e.g., high flows at Q5, low flows at Q95 by default).
- Produces ten MRFIs across high- and low-flow regimes:
  - Four medians
  - Four interquartile ranges (IQR)
  - Two modes (months of maximum and minimum flow)
- MRFIs are calculated for both high-flow and low-flow periods (HF1–HF5 and LF1–LF5).
- Significance of changes is determined by user-defined thresholds:
  - For median and IQR-based MRFIs: percentage-change from baseline (default 30%).
  - For mode-based MRFIs: absolute month-change (default one month).
- Risk classification is based on how many MRFIs differ significantly from baseline, with separate assessments for high and low flows.
- Overall risk uses a traffic-light scheme: 0 (no risk), 1 (low), 2–3 (medium), 4–5 (high).

## Monthly Flow Regime Indicators (MRFIs)
- HF5, HF4, HF3, HF2, HF1: indicators related to high-flow regime (with HF3, HF4, HF5 relating to timing and magnitude/frequency).
- LF5, LF4, LF3, LF2, LF1: indicators related to low-flow regime (with LF3, LF4, LF5 relating to timing and magnitude/frequency).
- Each MFRI captures either magnitude, frequency, timing, or duration aspects of the flow regime.

## Data inputs and processing
- Requires two time series: baseline and scenario flows (monthly means).
- Computes annual variables and then derives the ten MRFIs per year.
- Enables customization of:
  - Hydrological year definition
  - Low/high flow percentiles
  - Thresholds for significant changes in MRFIs
- Produces a per-scenario comparison to baseline, highlighting significant deviations in MRFIs.

## Outputs and visualization
- Generates plots and an ERFA matrix plot to interpret ecological risk.
- Outputs include:
  - Plots of hydrological variables and MRFIs
  - ERFA risk classification (traffic-light scheme)
  - Environment flow results suitable for export
- Ability to include baseline data in plots to aid comparative interpretation.

## System requirements and installation
- Implemented in R with the Shiny package for interactive use.
- Tested with R versions 3.4.2 to 3.6.1 and Shiny versions 1.0.5 to 1.3.2.
- Requires R (or R Studio) and the Shiny package; no separate installation beyond standard R tooling.

## File structure and datasets
- TEFRIC_ERFA.zip contains:
  - TEFRIC_MAIN.R: launcher for TEFRIC ERFA
  - server.R: core ERFA code
  - ui.R: user interface code
  - TEFRIC ERFA Manual.PDF: user manual
  - FUNCTIONS: scripts loading runtime functions
  - www: UI assets (images, etc.)
  - Mekong_7GCMs_2deg and Mekong_HadCM3_1-6deg: example project directories
    - Each contains INPUT subfolder with baseline and scenario time series plus default settings
- Example datasets:
  - Mekong_7GCMs_2deg: 30-year periods for 12 Mekong gauging stations; scenarios from seven GCMs with ~2° warming
  - Mekong_HadCM3_1-6deg: same 12 stations; HadCM3 scenarios for 1–6° warming in 1° increments
- Datasets are derived from MIKE SHE / MIKE 11 hydrological/hydraulic modelling (Thompson et al., 2013).

## User interface and usage
- Running TEFRIC_MAIN.R opens a web interface with:
  - Project directory selection
  - Site selection
  - Scenario selection (multiple)
  - Current settings and option to save custom settings
  - Export of plots and environmental flow results
  - Inclusion of baseline data in plots
  - Definition of water year
  - Hydrological plots
  - Definition of low/high flow percentiles
  - Definition of thresholds for significant MFRI changes
  - ERFA matrix plot and interpretation
- Designed to be interactive, enabling quick exploration of how different baselines and scenarios alter the MRFIs and ecological risk.

## Case study and regional applicability
- While the TEFRIC ERFA package provides Mekong Basin example data, the method is not region-locked and is applicable to any location where baseline and scenario river flow time series are available.
- Built to support policy, planning, and stakeholder communication via map- and plot-based representations of ecological risk from flow alteration.

## Acknowledgements, licensing, and references
- Acknowledges TEFRIC consortium and contributions from Cambodian and partner institutions.
- References foundational ERFA work (Laizé et al., 2014) and TEFRIC progress (Thompson et al., 2018; 2013; 2014; 2017).
- Conditions of use point users to the user manual for installation, operation, and licensing details.
- Disclaimer: no warranty; user contact encouraged for use-related information.