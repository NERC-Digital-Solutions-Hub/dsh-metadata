# Elemental and isotopic data of a series of timed exchange experiments between clay, mineral water and seawater NERC Grant NE/T007214/1

## Overview
- Dataset comprises elemental and isotopic measurements from timed exchange experiments involving clay, mineral water, and seawater.
- Focuses on Sr, Mg, and Ca elemental data and Sr and Mg isotope data.
- Data collected and analyzed at the University of Cambridge.

## Data types and measurement methods
- Elemental data
  - Elements: Strontium (Sr), Magnesium (Mg), Calcium (Ca).
  - Technique: Inductively Coupled Plasma Optical Emission Spectrometry (ICP-OES, Agilent 5100).
  - Calibration: Matrix-matched synthetic standards spanning sample concentration ranges.
- Sr isotope data
  - Ratios: 87Sr/86Sr (radiogenic) and d88/86Sr (stable).
  - Technique: Multicollector ICP-MS (MC-ICP-MS, Thermo Neptune Plus) with Forced Mass Bias Zr-doped EEN.
- Mg isotope data
  - Ratios: d26/24Mg and d25/24Mg.
  - Technique: MC-ICP-MS (Thermo Neptune Plus) with Sample-Standard-Bracketing.

## Calibration, standards, and quality control
- Elemental data calibration standards
  - External reference materials: SPS-SW2 and SLRS-6.
  - Water-based matrix analyses: within ±5% of certified values.
  - Ammonium chloride matrix analyses: SPS-SW2, SLRS-6, and a 3.2 BCR-2 (SCO-013a) LiBOx (1:25) standard within ±10%.
- Sr/isotope quality control
  - Use of IAPSO Standard seawater for reference values.
  - Method includes Monte-Carlo-based error assessment (see Uncertainty section).
- Mg isotope quality control
  - Standards used include IAPSO seawater and Cam1.
  - Repeat analyses used to verify accuracy against published results.

## Uncertainty, error analysis, and validation
- Sr isotopes
  - Total error evaluated via Monte-Carlo simulation.
  - Procedure: Generate 1000 random samples per variable using mean internal precision (2SE); compute true isotope ratios and total errors from multiple simulated sets.
  - Reported reference values include IAPSO standard seawater value and associated uncertainties.
- Mg isotopes
  - Uncertainties derived from at least three repeat analyses per sample (standard deviations).
  - Validation: Repeat analyses of IAPSO seawater and Cam1 are within published error ranges.
  - Specific Mg-isotope reference results reported (examples with 2SD and sample sizes) indicate consistency with prior published data.

## References materials and reported values
- IAPSO Standard seawater used for isotope reference comparisons.
- Reported values and uncertainties include:
  - 87Sr/86Sr reference for IAPSO seawater: 0.709186 ± 0.000008 (2SD, n=9).
  - Additional reference ratio: 0.389 ± 0.06 (2SD, n=9).
  - Mg isotope references (examples): d26/24Mg and d25/24Mg values with uncertainties and sample sizes (e.g., -0.79 ± 0.07 2SD, n=5; -2.59 ± 0.12 2SD, n=3; -0.41 ± 0.05 2SD, n=5; -1.33 ± 0.09 2SD, n=3).

## GIS relevance and practical considerations
- Data types (elemental concentrations and isotope ratios) are suitable for map-based visualization of spatial and temporal trends across exchange experiments.
- Combining datasets across different matrices (water-based vs ammonium chloride-based) and standards may require careful metadata curation to maintain consistency.
- Quality assurance is emphasized through matrix-matched calibrations, external standards, and robust uncertainty quantification (Monte Carlo for isotopes and repeat analyses for Mg isotopes), enabling reliable spatial interpretation in GIS workflows.