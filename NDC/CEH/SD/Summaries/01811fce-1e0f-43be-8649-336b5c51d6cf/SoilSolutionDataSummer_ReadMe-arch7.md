# ReadMe file for SoilSolutionDataSummer.csv

- Purpose: Document the soil solution chemistry data collected under three treatments (control, artificial sheep urine, real sheep urine) in a dystric histosol within unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK.
- Location context: 556 m above sea level; coordinates provided (53°22'N, 3°95'W); sheep excluded from 15/05/17 to prevent recent excretal confounding.
- Data scope: Soil solution chemistry (nitrate, ammonium, dissolved organic carbon, total dissolved nitrogen) collected over time after treatment application.

## Experimental design and treatments

- Treatments:
  - Control: no urine application.
  - Artificial sheep urine: patches with N application rate of 920 kg N ha-1.
  - Real sheep urine: patches with N application rate of 930 kg N ha-1.
- Patch details:
  - Each patch corresponds to 200 ml of urine solution applied over 100 cm2 soil surface area.
  - Artificial and real urine applied in discrete patches within plots.
- Timing:
  - Treatments applied on 24/07/17.
- Replication:
  - Rhizon samplers collected from plots within four replicate treatments; successful sampling achieved in a minimum of three replicates, resulting in at least n = 3 per condition.

## Sampling and measurement methods

- Sampling technique:
  - Rhizon soil solution samplers (2.5 mm diameter; 5 cm porous section; 12 cm tubing) inserted at a 45° angle to the soil surface.
  - Samplers positioned within urine patches and control areas inside the chambers.
- Sample handling:
  - Collected soil solutions stored frozen at -20 °C until analysis.
- Analytes and methods:
  - Nitrate (NO3−) measured with the method of Miranda et al. (2001).
  - Ammonium (NH4+) measured with the method of Mulvaney (1996).
  - Dissolved organic carbon (DOC) and total dissolved nitrogen (TDN) analyzed with a Multi N/C 2100S analyser (AnalytikJena).
  - All analyses calibrated against certified reference standards.

## Data structure and headers

- Data headers and meanings:
  - Date: Date of soil sample collection (dd/mm/yyyy).
  - Days: Days after treatment application.
  - Treatment: Experimental treatment per plot ('Control', 'ArtUrine', 'RealUrine').
  - Chamber: Plot and chamber identifier from which the sample was taken.
  - Nitrate: Nitrate concentration in mg NO3−-N L−1.
  - Ammonium: Ammonium concentration in mg NH4+-N L−1.
  - DOC: Dissolved organic carbon concentration in mg C L−1.
  - TN: Total dissolved nitrogen concentration in mg N L−1.

## Data provenance and notes

- Authors must be acknowledged if data are reused or reproduced.
- Data were collected from controlled plots within a defined grazing area; results reflect localized patch effects due to discrete urine application.
- Data quality considerations:
  - Sampling success per treatment may vary (minimum n = 3), which can influence replication robustness.
  - Data represent specific microenvironments (urine patches vs. controls) within a dystric histosol.

## References

- Miranda, K.M., Epsey, M.G. and Wink, D.A. (2001). A rapid, simple, spectrophotometric method for simultaneous detection of nitrate and nitrite. Nitric Oxide 5, 62-71.
- Mulvaney, R.L. (1996). Nitrogen - inorganic forms. In: Sparks, D.L. (Eds.), Methods of Soil Analysis. Part 3. Madison, WI, USA: Soil Science Society of America Inc., pp. 1123-1184.