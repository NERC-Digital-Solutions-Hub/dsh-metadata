# ReadMe file for SummerSoilWFPS_pH_EC.csv

- Purpose of the dataset
  - Measures soil water-filled pore space (WFPS), pH, and electrical conductivity (EC) under three treatments (control, artificial sheep urine, real sheep urine) on a dystric histosol in a grazing area within Snowdonia National Park, Wales, UK.
  - Aims to support understanding of how urine amendments affect soil physical-chemical properties.

- Experimental design and treatments
  - Treatments (n = 4 per group; real sheep urine n = 3): 
    - Control: no urine application
    - Artificial sheep urine (ArtUrine): patches with 200 ml urine-equivalent per 100 cm2; N application rate ~920 kg N ha-1
    - Real sheep urine (RealUrine): patches with 200 ml real urine per 100 cm2; N application rate ~930 kg N ha-1
  - Treatment application date: 24/07/17
  - Sheep exclusion: 15/05/17 to prevent recent excretal effects
  - Sampling: soils collected adjacent to greenhouse gas sampling chambers using an auger and processed within 24 hours

- Location and sampling context
  - Site: unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK
  - Elevation: 556 m above sea level
  - Coordinates: approximately 53°22'N, 3°95'W
  - Soil type: dystric histosol

- Measurements and calculations
  - WFPS: calculated as volumetric water content divided by soil porosity
  - Porosity: derived from assumed particle densities (mineral 2.65 g cm-3; organic 1.4 g cm-3) per Rowell (1994)
  - pH and EC: measured in 1:2.5 soil-to-distilled water suspensions using standard electrodes
  - Units:
    - WFPS: percent (%)
    - pH: pH units
    - EC: microSiemens per centimeter (µS cm-1)

- Data structure and fields (CSV headers)
  - Date: date of soil sampling (dd/mm/yyyy)
  - Days: days after treatment application
  - Treatment: Control, ArtUrine, RealUrine
  - Plot: plot identifier
  - WFPS: soil water-filled pore space (%)
  - pH: soil pH
  - EC: soil electrical conductivity (µS cm-1)

- Data provenance and usage notes
  - Data authors should be acknowledged if reused or reproduced
  - Reference for methods: Rowell, D.L., 1994. Soil Science: Methods and Applications
  - Data description emphasizes a discrete-patch urine application design and reliance on pore-porosity assumptions for WFPS calculation

- Data quality and governance considerations for data leaders
  - Metadata clarity: explicit treatment naming, dates, and unit definitions support discoverability and reuse
  - Provenance: clear documentation of sampling, processing, and calculation steps enhances reproducibility
  - Limitations to consider: small sample sizes per treatment, patch-based approach, and porosity assumptions may influence comparability across sites or years
  - Data discoverability: consistent headers and date formats aid integration with broader soil datasets and analyses across networks

- Reference
  - Rowell, D.L. 1994. Soil Science: Methods and Applications. Longman Group UKLtd. (used for porosity calculations)