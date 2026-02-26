# Barium Concentration and Stable Isotope Ratio Measurements of the Dissolved and Adsorbed Phases from Laboratory Batch Experiments and Himalayan River Samples from 2015-2016: Supporting Documentation

## Overview
- Describes a dataset of barium concentration and stable isotope ratio measurements from both laboratory batch experiments and Himalayan river samples (2015–2016).
- Lab work investigates fractionation of stable Ba isotopes during adsorption-desorption with common mineral adsorbents (kaolinite, montmorillonite, goethite, ferrihydrite) using river, groundwater, and seawater analogues.
- Field samples come from the PRESSurE project, collected along the Saptakoshi and Sunkoshi rivers in Nepal to validate laboratory results.
- Data products include two CSV files: BaIsoExperimentData.csv (laboratory data) and BaIsoNepalRivers.csv (field data), with accompanying metadata describing methods, treatment, and data fields.
- Analytical workflow combines element concentrations (ICP-OES) and Ba isotope ratios (TIMS with a double spike), with strict QA/QC and standard references.

## Data Collection
- Laboratory Experiments
  - Riverine Series: aims to understand Ba isotope fractionation in freshwater adsorbent–water interactions.
  - Subseries:
    - Partitioning: varying adsorbent concentrations at a fixed duration (2000 min) to quantify partitioning between adsorbed and dissolved phases.
    - Kinetic: fixed adsorbent concentrations with varying reaction durations (10 min to ~1 month) to assess time dependence.
  - Estuarine Series: investigates desorption of Ba from river-derived suspended sediment in seawater; constants include clay type, river-water analogue, salinity, and long reaction duration (~10,000 min); re-equilibration with river water for half the experiments.
  - Post-Reaction Processes: separation of phases by centrifugation; extraction of adsorbed Ba from surfaces for analysis.
- Himalayan River Samples
  - 12 river water samples from Sunkoshi and Saptakoshi rivers, Nepal, collected as part of PRESSurE.
  - Sampling: stationary sites, four monsoon seasons over four years; daily sampling during pre-monsoon/monsoon, biweekly during post-monsoon/dry season.
  - Processing: filtration (0.22 µm PES), sediment and water separation, staged desorption of adsorbed cations using NH4Cl or calcite-saturated CoHex; repeated desorption steps with filtration after each step.

## Analytical Methods
- Displacement of Pre-Existing Adsorbed Ba
  - Repeated NH4Cl leaching to desorb reversibly adsorbed Ba prior to experiments.
- Mineral-Water Reactions
  - Controlled mixing of waters with mineral adsorbents; separation by centrifugation and filtration; immediate handling of reacted waters.
- Extraction of the Adsorbed Phase
  - Post-reaction desorption of adsorbed Ba using the same procedure as initial cleaning; samples kept cold until analysis.
- Determination of Element Concentrations
  - ICP-OES (Agilent 5100) for Ba concentrations; TIMS isotope dilution (double spike) for precise Ba isotope ratios.
  - Calibration with certified standards; matrix-matched lines; QA/QC routines to mitigate drift.
- Barium Isotope Measurements
  - TIMS (Thermo Fisher Triton Plus) with double-spike correction.
  - Sample preparation includes: acid digestion, CaCO3 co-precipitation for seawater, repeated evaporations and acid cleaning, ion-exchange chromatography to isolate Ba, and loading onto Re filaments.
  - Procedural blanks and standards used to monitor accuracy; long-term precision assessed with NIST 3104a and NBS 127 standards.
  - Reported uncertainty: isotope measurements have a minimum of 0.03 ‰ (2σ) based on standards; overall method blanks are low (<1–4% impact per sample).
- Data Processing
  - Samples prepared to correct for mass fractionation; isotope ratios expressed as δ138/134Ba relative to NIST 3104a.

## Data Structure
- Two CSV data files are provided:
  - BaIsoExperimentData.csv (Laboratory Data)
    - Key fields (examples): ID, Series, Subseries, Water, Adsorbent, Adsorbent ID, Water mass, Adsorbent mass, Reaction duration, Pretreatment (Yes/No), Ba diss (dissolved, µmol L-1), Ba ad (adsorbed, µmol L-1), d138Ba diss, d138Ba diss (‰), d138Ba ad, d138Ba ad (‰).
  - BaIsoNepalRivers.csv (Field Data)
    - Key fields (examples): ID, Date, River, Loc, SSC (g L-1), Discharge (m^3 s-1), Ba diss (µmol L-1), Ba ad (µmol L-1), d138Ba diss (‰), d138Ba ad (‰).
- Data labeling
  - NA indicates not applicable; NM indicates not measured.
  - Measurements conducted in clean laboratories at Cambridge; all units and abbreviations documented in the data files.
- Data provenance
  - Field data linked to the PRESSurE river chemistry time series (Knight et al., 2024).
  - Supporting methods and analyses detailed in the document and related references.

## Quality and Uncertainty
- Uncertainties
  - Ba concentrations by ICP-OES: ~7% (2σ) with matrix-matched calibration.
  - TIMS Ba concentrations by isotope dilution: ~2% (2σ).
  - Ba isotope measurements: minimum uncertainty of 0.03 ‰ (2σ) from standards.
- Blanks and contamination controls
  - TIMS combined analytical blank: 0.07 ± 0.06 ng (2σ, n=6), <1% of processed sample mass.
  - NH4Cl blank during Ba isotope analyses; overall blank contribution to samples up to ~4%.
- QA/QC
  - Repeated external standards (SPS-SW2, SLRS-6) and long-term standard runs ensure accuracy and precision.
  - Method references and controls embedded in the analytical workflow (double spike, co-precipitation for seawater, ion-exchange purification).

## Provenance, Access, and References
- Analytical work performed at the University of Cambridge, Department of Earth Sciences.
- Related references and datasets:
  - Foster, Staubwasser, and Henderson (2004) on Ba in marine systems.
  - Hsieh & Henderson (2017) on Ba stable isotopes as tracers.
  - Knight et al. (2024) PRESSurE River Chemistry Time Series (Nepal).
  - Rudge, Reynolds, and Bourdon (2009) on the double spike toolbox.
- Data availability
  - The primary data are provided as two CSV files with accompanying methodological documentation and data dictionaries.