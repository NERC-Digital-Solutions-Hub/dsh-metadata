# R implementation of the Ecological Risk due to Flow Alteration (ERFA) method

## Overview
- An R implementation of the ERFA method, developed under the TEFRIC project (NERC funded) by UCL Geography, CEH, ITC, and Tonle Sap Authority.
- Geographically focused on SE Asia with Mekong River Basin example data, but applicable to any location with baseline and scenario river flow time series.
- Provides a user-friendly interface (Shiny) and a workflow to assess ecological risk from flow alterations.

## TEFRIC ERFA methodology
- Requires at least two monthly mean river flow time series at a location: baseline (historical or natural) and a scenario (e.g., a water resource project or climate projection).
- Defines a hydrological year (flexible to river regime) and user-definable low/high flow thresholds using percentiles (default: high flows at Q5, low flows at Q95; both user-adjustable).
- Computes yearly hydrological variables and derives Monthly Flow Regime Indicators (MRFIs) to summarize baseline and scenario regimes.
- Derives ten MRFIs from six hydrological variables: four medians, four interquartile ranges (IQRs), and two timing indicators (months of peak and low flows).

## Monthly Flow Regime Indicators (MFRIs)
- High-flow indicators (HF):
  - HF1: Median of the number of months above high-threshold
  - HF2: IQR of the number of months above high-threshold
  - HF3: Mode (month) of maximum flow
  - HF4: Median of maximum flow
  - HF5: IQR of maximum flow
- Low-flow indicators (LF):
  - LF1: Median of the number of months below low-threshold
  - LF2: IQR of the number of months below low-threshold
  - LF3: Mode (month) of minimum flow
  - LF4: Median of minimum-flow month
  - LF5: IQR of periods with flow below threshold

## Significance and risk classification
- Compares scenario MRFI values to baseline using user-defined thresholds:
  - For medians and IQRs: percentage change from baseline (default 30%)
  - For mode-based MRFIs (timing): absolute change in month (default 1 month)
- Produces a risk classification (applied separately for high and low flows) with:
  - No risk, Low risk, Medium risk, High risk
  - Based on how many MRFIs differ significantly from baseline:
    - 0: no risk
    - 1: low risk
    - 2–3: medium risk
    - 4–5: high risk
- Uses a traffic-light color coding to represent overall risk.

## System requirements and installation
- Implemented in R (tested with R 3.4.2 and Shiny 1.0.5; validated up to R 3.6.1 and Shiny 1.3.2).
- Requires R (or R Studio) and the Shiny package.
- TEFRIC ERFA.zip contains:
  - TEFRIC_MAIN.R (launch code), server.R, ui.R, TEFRIC ERFA Manual.PDF
  - A FUNCTIONS folder with runtime scripts, www with UI images
  - Example project directories (Mekong_7GCMs_2deg and Mekong_HadCM3_1-6deg) with INPUT subfolders for baseline/scenario data and default settings

## Data inputs and project setup
- Interactive UI (launched by TEFRIC_MAIN.R) includes:
  - Project directory selection
  - Site selection
  - Scenario selection(s)
  - Current settings and ability to save custom settings
  - Export options for plots and results
  - Option to include baseline data in plots
  - Definition of the hydrological year and low/high flow percentiles
  - Threshold definitions for significant MFRI changes
  - ERFA matrix plot and interpretation

## Example datasets and applicability
- Mekong River Basin datasets accompany the package:
  - Mekong_7GCMs_2deg: baseline with 30-year periods and scenarios from seven GCMs projecting +2°C
  - Mekong_HadCM3_1-6deg: HadCM3-based scenarios for 1–6°C increases
- Datasets are derived from MIKE SHE / MIKE 11 hydrological modelling (Thompson et al., 2013) and related work.

## Outputs and interpretation
- Produces MRFI-based comparisons between baseline and each scenario.
- Generates ERFA risk classification and associated plots (including an ERFA matrix plot) to aid interpretation.
- Results help quantify ecological risk from flow alterations and support decision-making regarding environmental flows and water resource planning.

## Acknowledgements, licensing, and references
- Developed under TEFRIC (Grant NE/R009325/1) with collaboration among UCL Geography, CEH, ITC, and TSA.
- Acknowledges workshop participants and partner organizations from Cambodian government and international NGOs.
- Licensing and detailed installation/operation instructions provided in the TEFRIC ERFA user manual.
- References key ERFA and TEFRIC publications documenting methodology and applications.