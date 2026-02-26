# Barium Concentration and Stable Isotope Ratio Measurements of the Dissolved and Adsorbed Phases from Laboratory Batch Experiments and Himalayan River Samples from 2015-2016: Supporting Documentation

## Overview
- Presents barium concentrations and stable isotope ratios from controlled laboratory batch experiments and Himalayan river samples.
- Aims to understand Ba isotope fractionation during adsorption-desorption between common environmental minerals and surface waters.
- Field samples from the Saptakoshi and Sunkoshi rivers in Nepal validate laboratory results; part of the PRESSurE project.

## Data scope and structure
- Two data streams:
  - Laboratory experiments (BaIsoExperimentData.csv): dissolved and adsorbed Ba concentrations and d138Ba for various adsorbents and water types.
  - Himalayan river field samples (BaIsoNepalRivers.csv): dissolved and adsorbed Ba concentrations and d138Ba from river water and suspended sediment.
- Data structure details:
  - Fields labeled NA where not applicable and NM where data are available but not measured.

## Laboratory Experiments
- Riverine Series
  - Purpose: assess Ba isotope fractionation in freshwater during adsorption/desorption.
  - Subseries:
    - Partitioning: varies adsorbent concentration at fixed duration (2000 min) to balance dissolved vs adsorbed Ba for isotope measurement.
    - Kinetic: varies reaction duration at fixed adsorbent concentrations (10 min to ~1 month).
- Estuarine Series
  - Purpose: quantify desorption of Ba from river-derived sediments in estuarine conditions.
  - Procedure: clay minerals equilibrated with river water analogue (HS50) then exposed to seawater; some runs re-equilibrated with river water.
- Post-Reaction Processes
  - Separation of water and adsorbent by centrifugation.
  - Displacement of adsorbed Ba from surfaces for separate analysis of adsorbed vs dissolved phases.

## Himalayan River Samples (Field Data)
- 12 river water samples from Sunkoshi and Saptakoshi, Nepal (PRESSurE project).
- Sampling design:
  - Hydrological stations installed after 2015 Gorkha earthquake; monitored for four monsoon seasons.
  - Sampling at stationary locations; daily during pre-monsoon and monsoon, twice weekly during post-monsoon/dry season.
  - Water column samples combined from 6 subsamples; in-situ filtration through 0.22 µm PES membranes to separate sediment and water.
- Adsorbed cations desorption:
  - Two procedures: 1) 1.0 M NH4Cl; 2) calcite-saturated 0.0167 M CoHex.
  - Desorption steps include repeated treatments and immediate filtration of all supernatants.

## Analytical Methods
- Element concentrations
  - Ba measured by ICP-OES (Agilent 5100) and isotope-dilution TIMS for cross-verification.
  - Calibration with certified standards; matrix matching; drift control via argon humidification and NH4Cl dilution.
  - Uncertainty: ~7% (ICP-OES) for Ba concentrations; ~2% for TIMS.
- Isotope measurements
  - TIMS (TRITON Plus) with double spike to correct mass-dependent fractionation.
  - Seawater samples required CaCO3 co-precipitation to enhance Ba signal prior to chromatography.
  - Sample prep included multiple acid digestion steps, ion-exchange chromatography, drying, and loading onto Re filaments.
  - Procedural blank: ~0.07 ± 0.06 ng; NH4Cl blanks up to 4% contribution to measured Ba.
  - Isotopic precision: ~0.03 ‰ for δ138Ba measurements.
- Quality controls and references
  - Standards: NIST 3104a and NBS 127 measured repeatedly; long-term accuracy and precision assessed over three years.

## Data Files and Contents
- BaIsoExperimentData.csv (Laboratory Data)
  - Key fields: ID, Series, Subseries, Water, Adsorbent, Adsorbent ID, Water mass, Adsorbent mass, Reaction duration, Pretreatment, Ba diss (dissolved Ba), Ba ad (adsorbed Ba), d138Ba diss, d138Ba ad.
- BaIsoNepalRivers.csv (Field Data)
  - Key fields: ID, Date, River, Loc, SSC (suspended sediment concentration), Discharge, Ba diss, Ba ad, d138Ba diss, d138Ba ad.
- Field and lab data distinguishable by their respective CSVs; NA and NM used where appropriate.

## Data Quality and Uncertainty
- Isotope measurements corrected for mass bias with double spike methodology.
- Uncertainties:
  - Ba concentrations: 7% (ICP-OES).
  - TIMS measurements: 2%.
  - Isotopic measurements: minimum ~0.03 ‰ precision.
- Comprehensive QA through repeated standards, blanks, and cross-checks with established reference materials.

## Relevance for Environmental Monitoring
- Provides a standardised dataset linking Ba concentrations with stable isotope signatures in both dissolved and adsorbed phases.
- Enables assessment of Ba sources, lifecycle, and exchange between rivers, sediments, and estuarine systems.
- Supports time-series and spatial comparisons when integrated with complementary datasets (e.g., PRESSurE river chemistry time series).
- Facilitates data reuse and integration with other monitoring datasets by documenting data structure, methods, and QA details.

## notes and references
- Related methodological and tracer studies cited, including Ba isotope applications and double-spike TIMS approaches.
- Complimentary dataset: PRESSurE River Chemistry Time Series (Nepal) referenced for broader context.