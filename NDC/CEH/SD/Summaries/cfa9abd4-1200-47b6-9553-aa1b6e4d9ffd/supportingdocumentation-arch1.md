# Barium Concentration and Stable Isotope Ratio Measurements of the Dissolved and Adsorbed Phases from Laboratory Batch Experiments and Himalayan River Samples from 2015-2016: Supporting Documentation

## Overview
- Contains barium concentration and stable isotope ratio measurements from laboratory batch experiments and Himalayan river samples (2015–2016).
- Aims to understand fractionation of stable Ba isotopes during adsorption–desorption between environmental mineral adsorbents and surface waters.
- Laboratory work uses clay minerals (kaolinite, montmorillonite) and iron-oxyhydroxides (goethite, ferrihydrite) with river water, groundwater, and seawater.
- Field samples (Saptakoshi and Sunkoshi rivers, Nepal) validate laboratory results as part of the PRESSurE project.

## Experimental Design

### Laboratory Experiments
- Riverine Series
  - Partitioning Subseries: varies adsorbent concentration at constant reaction duration (2000 minutes) to study Ba partitioning between dissolved and adsorbed phases; ensures ~200 ng Ba in both phases for isotope analysis.
  - Kinetic Subseries: fixed adsorbent concentrations; reaction durations range from 10 minutes to just over a month to assess time dependence of Ba isotope fractionation.
- Estuarine Series
  - Quantifies desorption of Ba from river-derived suspended sediment in estuarine conditions.
  - Clay minerals equilibrated with river-water analogue (HS50) before exposure to seawater; fixed duration (10,000 minutes) with constant clay concentration; half the experiments re-equilibrated with river water.
- Post-Reaction Processes
  - After batch reactions, separation by centrifugation followed by displacement of adsorbed Ba from surfaces for analysis.

### Himalayan River Samples
- 12 river water samples from Sunkoshi and Saptakoshi (Nepal) as part of the PRESSurE time series.
- Sampling around hydrological stations installed after the 2015 Gorkha earthquake; daily sampling during pre-monsoon/monsoon, and twice weekly during post-monsoon/dry seasons.
- Field processing: filtration (0.22 µm PES), sediment and water separation, field extraction of adsorbed cations using NH4Cl or CoHex; sequential desorption steps with immediate filtration of supernatants.
- Ba concentrations and isotope ratios measured using the same analytical methods as laboratory samples.

## Analytical Methods

### Displacement of Pre-Existing Adsorbed Ba from Minerals
- Kaolinite and montmorillonite pre-loaded with Ba; repeated additions of 1.0 M NH4Cl to desorb Ba into solution; 3 cycles with thorough washing to minimize reagent blank.

### Mineral–Water Reactions
- Waters added to mineral adsorbents in centrifuge tubes; mixing protocols vary by duration:
  - <40 min: manual shaking
  - >40 min: ultrasound treatment followed by shaking
- Post-reaction separation via centrifugation and filtration; reacted waters stored for analysis.

### Extraction of the Adsorbed Phase
- Displacement of adsorbed Ba from mineral surfaces performed using the same procedure as 4.1 (NH4Cl-based desorption).
- All water and leachates refrigerated at 5 °C prior to analysis.

### Determination of Element Concentrations
- Ba concentrations measured by ICP-OES (Agilent 5100) with matrix-matched calibration.
- TIMS isotope dilution with a Ba double spike for Ba concentration cross-checks.
- External standards (SPS-SW2, SLRS-6) used to monitor accuracy; typical uncertainties: ~7% (Ba concentration, ICP-OES) and ~2% (TIMS).

### Barium Isotope Measurements
- TIMS (Thermo Fisher Triton Plus) with double-spike correction for mass-dependent fractionation.
- Seawater samples require co-precipitation with CaCO3 to improve Ba signal amid high Na, Mg, K concentrations.
- Sample preparation includes partial dissolution, strong acid digestion, two-stage ion-exchange chromatography to isolate Ba, oxidation steps, and loading onto Re filaments.
- Procedural blank: ~0.07 ± 0.06 ng; NH4Cl blank up to 4% of sample mass.
- Standards (NIST 3104a and NBS 127) used for long-term accuracy; typical isotopic uncertainty ~0.03 ‰.

## Data Structure

### Laboratory Data
- File: BaIsoExperimentData.csv
- Key fields:
  - ID, Series, Subseries, Water, Adsorbent, Adsorbent ID
  - Water mass (g), Adsorbent mass (mg)
  - Reaction duration (min)
  - Pretreatment (Yes/No)
  - Ba diss (dissolved Ba; µmol/L)
  - Ba ad (adsorbed Ba; µmol/L)
  - d138Ba diss (‰)
  - d138Ba ad (‰)

### Field Data
- File: BaIsoNepalRivers.csv
- Key fields:
  - ID, Date (DD/MM/YYYY), River, Loc
  - SSC (g/L), Discharge (m³/s)
  - Ba diss (µmol/L)
  - Ba ad (µmol/L)
  - d138Ba diss (‰)
  - d138Ba ad (‰)

## Data Quality and Uncertainty
- Analyses conducted in clean laboratory facilities dedicated to trace metal isotope work.
- Cross-checks with standard reference materials over multiple years for accuracy.
- Uncertainty targets:
  - Ba concentrations: ~7% (2σ) by ICP-OES
  - Ba concentrations via TIMS: ~2% (2σ)
  - Isotopic measurements: ~0.03 ‰ (1σ) via standard references and blanks.

## Data Availability
- Two CSV data files included in the repository (laboratory and field data).
- Field data linked to a complimentary dataset: Knight et al., 2024 (PRESSurE River Chemistry Time Series, Nepal).

## References
- Foster et al. (2004). 226Ra and Ba concentrations in the Ross Sea measured with multicollector ICP-MS. Marine Chemistry.
- Hsieh & Henderson (2017). Barium stable isotopes in the global ocean. Earth and Planetary Science Letters.
- Knight et al. (2024). PRESSurE River Chemistry Time Series (Nepal).
- Rudge et al. (2009). The double spike toolbox. Chemical Geology.