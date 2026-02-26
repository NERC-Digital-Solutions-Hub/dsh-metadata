# R implementation of the Ecological Risk due to Flow Alteration (ERFA) method

- Purpose: A software implementation of the ERFA framework to assess ecological risk from river flow alterations, enabling evaluation of baseline versus scenario flow regimes and informing policy and management decisions.
- Origin and scope: Developed under the TEFRIC project (Cambodia and Mekong region focus) but applicable to any region where baseline and scenario river flow time series are available.
- Core idea: Compare two monthly flow time series (baseline and scenario) using a set of Monthly Flow Regime Indicators (MRFIs) to quantify changes in magnitude, variability, and timing, and classify ecological risk.

## Introduction

- Environmental flows describe river flow regimes needed to sustain ecosystem services; ERFA assesses ecological risk from changes to these regimes.
- ERFA builds on earlier European work and Mekong climate-change adaptations, with a user-friendly interface added through TEFRIC.
- The approach emphasizes: defining hydrological response to flow change, and identifying thresholds where ecological change may be significant.

## ERFA Method

- Data requirements:
  - At least two monthly mean river flow time series at a location: baseline (historical or natural) and a scenario (e.g., due to management or climate change).
- Hydrological processing:
  - Define the hydrological year based on river regime.
  - Set low/high flow thresholds using user-defined percentiles (default: high flows at the 5th percentile, low flows at the 95th percentile of the baseline).
- Monthly Flow Regime Indicators (MRFIs):
  - Ten indicators in total, based on six hydrological variables: four medians, four interquartile ranges (IQRs), and two modes (for timing).
  - Five indicators relate to high flows; five relate to low flows.
  - Variables describe magnitude and variability, timing (month of peak/low flow), and frequency/duration characteristics.
- Change assessment:
  - Compute absolute differences between scenario and baseline MRFIs.
  - Apply user-defined significance thresholds (default: 30% for medians/IQRs; default: one-month change for mode-based MRFIs).
- Risk classification:
  - Classify ecological risk separately for high and low flows using the number of MRFIs that differ significantly from baseline.
  - Risk levels: no risk (0 differences), low risk (1), medium risk (2–3), high risk (4–5).
  - Visual “traffic light” coding denotes overall risk.

## System requirements and installation

- Platform: R with the Shiny package; tested with R up to 3.6.1 and Shiny up to 1.3.2 on Windows and MacOS.
- Software needs:
  - R (and optionally R Studio for a more user-friendly interface).
  - Shiny package (install separately from CRAN).
- Distribution: TEFRIC ERFA is delivered as TEFRIC_ERFA.zip containing all code, data, and manuals.
- How to run:
  - Unzip TEFRIC_ERFA.zip to a working directory.
  - Run TEFRIC_MAIN.R to launch the Shiny interface.

## Files and folder structure provided with TEFRIC_ERFA.zip

- TEFRIC_MAIN.R: Launch script for ERFA.
- server.R: Core ERFA server logic.
- ui.R: User interface code.
- TEFRIC ERFA Manual.PDF: User manual.
- FUNCTIONS: R scripts providing the runtime functions.
- www: Image assets for the UI.
- Mekong_7GCMs_2deg and Mekong_HadCM3_1-6deg: Example project directories, each containing INPUT subfolders with baseline and scenario time series and a default settings file.
- Example datasets:
  - Mekong_7GCMs_2deg: 30-year periods for 12 Mekong gauging stations under seven GCM scenarios (2° C warming).
  - Mekong_HadCM3_1-6deg: Same stations with HadCM3 scenarios for 1–6° C warming increments.
- These datasets and structures illustrate how to configure new applications.

## User Interface

- When launched, the web interface provides:
  - Project directory selection (single).
  - Site selection (single).
  - Scenario selection (multiple).
  - Current settings, saving custom settings.
  - Exporting plots and environmental flow results.
  - Option to include baseline data in plots.
  - Definition of the water year and low/high flow percentiles.
  - Definition of thresholds for significant MRFI changes.
  - ERFA matrix plot and interpretation guidance.

## Outputs and monitoring framework implications

- Outputs:
  - MRFI-based metrics comparing baseline and scenario flows.
  - Quantitative risk classification (no/low/medium/high) with traffic light interpretation.
  - Plots and exportable results suitable for informing policy and management decisions.
- Relevance for monitoring frameworks:
  - Provides a structured, repeatable method to monitor ecological risk from flow alterations.
  - Facilitates transparent data use (baseline vs scenario) and explicit threshold-based decision rules.
  - Supports governance needs for data-driven decisions by enabling visualization, sharing, and documentation of results.

## Data, metadata, and governance considerations

- Data requirements are explicit (two time series plus settings); the interface supports integration and visualization of baseline data.
- Openness and sharing:
  - The tool encourages sharing underlying data used in analyses and provides outputs that can be exported; however, data governance and metadata quality are essential ensure datasets meet standards.
- Data transformation:
  - The method includes user-defined thresholds and percentile-based definitions, requiring clear metadata about how baselines and scenarios were constructed.

## Acknowledgements

- Created as part of the NERC TEFRIC project, with collaboration among UCL Geography, CEH, ITC, and Tonle Sap Authority.
- Acknowledges workshop participants and organizations contributing to refinements and data provision.

## Conditions of use

- Refer to the TEFRIC ERFA user manual for installation, operation details, and licensing.

## Disclaimer

- No warranty; user experience is encouraged to share usage details with the authors (contact provided in the document).

## References

- Foundational ERFA and TEFRIC sources detailing methodology, applications, and uncertainty analyses:
  - Laizé et al. 2014 (European rivers)
  - Thompson et al. 2018 (TEFRIC Cambodia)
  - Thompson et al. (multiple years) on Mekong and related climate-change uncertainties and river-flow projections