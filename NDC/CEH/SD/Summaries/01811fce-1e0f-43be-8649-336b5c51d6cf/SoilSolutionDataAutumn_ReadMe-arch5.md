# ReadMe file for SoilSolutionDataAutumn.csv

## Overview
- Describes soil solution chemistry data collected under three treatments (Control, artificial sheep urine, nitrate and glucose) from a humic gleysol in unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK.
- Location specifics: 556 m above sea level; coordinates ~53°22'N, 3°95'W.
- Sheep excluded from 15/05/17 to prevent recent excretal events from confounding results.
- Data are intended to support soil solution chemistry analyses (nitrate, ammonium, dissolved organic carbon, total dissolved nitrogen).

## Study context and treatments
- Treatments:
  - Control: no urine application.
  - Artificial sheep urine: patches with N application of 1120 kg N ha-1; 200 mL artificial urine applied over 100 cm2 soil area per patch.
  - Nitrate and glucose: 106 kg N ha-1 and 213 kg C ha-1 applied in a 40 cm x 40 cm square.
- Treatment application date: 25/10/17.
- Data headers indicate a possible third treatment category: RealUrine (real sheep urine) in addition to ArtUrine (artificial urine); the description primarily mentions artificial urine, so users should verify dataset specifics for RealUrine.

## Sampling and storage
- Sampling method: Rhizon® soil solution samplers (2.5 mm diameter, 5 cm porous part, 12 cm tubing) inserted at a 45° angle within treatment plots inside chambers.
- Replication: Successful sampling typically achieved in at least 3 out of 4 replicates, yielding at least n = 3.
- Storage: Soil solutions stored frozen at -20 °C until analysis.

## Analytical methods
- Analytes and methods:
  - Nitrate (NO3-): determined by the method of Miranda et al. (2001).
  - Ammonium (NH4+): determined by the method of Mulvaney (1996).
  - Dissolved Organic Carbon (DOC) and Total Dissolved Nitrogen (TN): measured using a Multi N/C 2100S analyser (AnalytikJena).
- Quality control: Analyses performed against certified reference standard solutions.

## Data structure and headers
- Key headers:
  - Date: date of sample collection (dd/mm/yyyy).
  - Day: days after treatment application.
  - Treatment: 'Control', 'ArtUrine' (Artificial urine), 'RealUrine' (Real urine treatment).
  - Chamber: plot and chamber identifier.
  - Nitrate: mg NO3--N L-1.
  - Ammonium: mg NH4+-N L-1.
  - DOC: mg C L-1.
  - TN: mg N L-1.
- Data format notes: Dates use dd/mm/yyyy; units are specified for all concentrations.

## Data quality, provenance, and governance
- Data provenance:
  - Field location, treatment details, sampling method, and storage conditions are documented.
  - Analytical methods with literature references are provided for traceability.
- Quality considerations:
  - Documented minimum replication (n ≥ 3) per treatment per plot.
  - Clear reporting of storage and analysis procedures to support reproducibility.
- Rights and attribution:
  - Authors must be acknowledged if data are reused or reproduced.

## Usage notes for data stewards
- Ensure metadata align with other datasets for interoperability (treatment names, units, and date formats).
- Validate consistency between Treatment values and the presence of RealUrine vs ArtUrine in the dataset.
- Confirm unit consistency across analyses (NO3--N, NH4+-N, DOC, TN).
- Maintain access to the referenced analytical methods for reproducibility.
- Consider updating or clarifying any gaps in replicates, chamber identifiers, or missing data.

## References
- Miranda, K.M., Epsey, M.G. and Wink, D.A. (2001). A rapid, simple, spectrophotometric method for simultaneous detection of nitrate and nitrite. Nitric Oxide 5, 62-71.
- Mulvaney, R.L. (1996). Nitrogen - inorganic forms. In: Sparks, D.L. (Eds.), Methods of Soil Analysis. Part 3. Madison, WI, USA: Soil Science Society of America Inc., pp. 1123-1184.