# Ammonia concentration and deposition data from Glencorse experimental site near UKCEH, Edinburgh (2021-2022)

## Overview
- Study of how elevated atmospheric ammonia (NH3) affects birch woodland vegetation, bryophytes, lichens, and soil.
- NH3 enhancement system is wind-controlled: NH3 released only when wind direction is toward monitoring quadrats (275–345 degrees) and threshold speeds (≥0.310 m s⁻¹).

## Data collection and measurements
- NH3 concentrations measured at 1.5 m height along the monitoring transect using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers; monthly analyses from September 2021 to December 2022.
- Vertical NH3 concentration gradients measured at 5 to 3.5 cm above ground in 25 cm intervals, at distances of 4, 10, and 16 m from the source.
- Data used to drive a dry deposition model through a four-layer canopy compensation-point framework; incorporates a bi-directional resistance approach with stomatal and soil re-emission processes.

## Modelling framework and key components
- Four-layer canopy compensation-point model coupled with a bi-directional resistance deposition model.
- Deposition flux calculations follow:
  - Fχ(z) = χa / Rt, where χa is ambient NH3 concentration and Rt is total resistance to deposition.
- Layer-specific deposition paths:
  - Soil surface: quasi-laminar boundary layer resistance (Rbg).
  - Tree trunks: quasi-laminar boundary layer resistance around trunks (Rb(tt)).
  - Stomatal deposition: stomatal resistance (Rs) with Leaf Area Index (LAI) dependency.
  - Cuticular deposition: multiple parameterizations with LAI dependence and phenology adjustments.
- Parameterizations and dependencies include:
  - Boundary layer and aerodynamic terms (friction velocity, u*, z0, δ0, Sc, Re*).
  - Multiple cuticular deposition schemes (Massad et al., Jones et al., DEPAC, Sutton et al.) with day/night and light/temperature adjustments.
  - DEPAC module (2010) integration for deposition calculations.
- Referenced equations and mechanisms are drawn from established literature (e.g., Chamberlain, Fowler, Nemitz, Massad, Jones, DEPAC).

## Data outputs and structure
- Dataset contains 126 measurements of 17 NH3-related parameters.
- Provided as a CSV with columns including:
  - Distance (m) from NH3 source; positive = northeast, negative = southwest.
  - Month (and year).
  - NH3 concentrations at various heights/locations: measured at 1.5 m (NH3_conc_measured) and modeled at soil (NH3_conc_soil), understory (NH3_conc_us), trunk surfaces (NH3_conc_ts), and tree canopy (NH3_conc_tc).
  - Deposition fluxes (kg ha⁻¹): soil (Fg), understory stomatal (Fs_us), various understory cuticular (Fw_us_...), trunk stomatal (Ftt), trunk canopy (Fs_tc), trunk cuticular (Fw_tc_...), with multiple parameterizations (Massad, DEPAC, Jones, Sutton) and emission interpretations when negative.
- Data quality notes indicate periodic gaps due to power cuts and sensor replacements; data were visually QA’d to remove obvious instrument-related errors.

## Quality control and data integrity
- Visual inspection to identify and remove instrument malfunctions and data logging issues.
- Regularly scheduled power cuts caused intentional gaps; some missing values also from sensor replacement periods.

## Funding and provenance
- Funded by the UKRI Global Challenges Research Fund (GCRF) South Asian Nitrogen Hub.

## Methodology context and references
- Methodologies align with established dry/deposition models and resistance-based exchanges (Chamberlain; Fowler; Wesely & Hicks; Nemitz; Massad; Jones; Sutton; DEPAC module).
- Complete methodological details, analyses, and findings are documented in Deshpande et al. (2024).

## Relevance for environmental monitoring and policy
- Provides a standardized, traceable dataset for NH3 concentrations and deposition in forest ecosystems, enabling temporal monitoring and cross-site comparisons.
- Outputs include multiple deposition pathways (soil, understory, trunks, canopy) and multiple parameterizations, supporting consistent assessment of NH3 deposition processes and their environmental implications.
- Supports data-driven evaluation of policy performance and environmental health risk assessments through transparent QA, structured data formats, and clear measurement metadata.