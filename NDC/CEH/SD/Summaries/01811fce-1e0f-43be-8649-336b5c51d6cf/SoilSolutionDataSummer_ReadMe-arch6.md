# ReadMe file for SoilSolutionDataSummer.csv

## Overview
- Dataset describes soil solution chemistry under three treatments (control, artificial sheep urine, real sheep urine) applied to a dystric histosol in unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK (556 m above sea level; 53°22'N, 3°95'W).
- Sheep were excluded from plots from 15/05/17 to avoid recent excreta confounding results.
- Sampling used Rhizon soil solution samplers to collect pore water from within urine patches and control plots.

## Study Site and Treatments
- Location: Carneddau mountains, Snowdonia National Park, Wales, UK.
- Site characteristics: unimproved grazing land; dystric histosol.
- Treatments (applied 24/07/17):
  - Control: no urine.
  - Artificial sheep urine: patchy application at 920 kg N ha-1 per patch (200 ml urine over 100 cm2 soil area per patch).
  - Real sheep urine: patchy application at 930 kg N ha-1 per patch (200 ml urine over 100 cm2 soil area per patch).

## Sampling Design and Replicates
- Sampling method: Rhizon® soil solution samplers (2.5 mm diameter, 5 cm porous section, 12 cm tubing) inserted at 45° to the soil surface, within urine patches and controls inside chambers.
- Replicates: four replicate treatments with sampling aimed to achieve successful collection from at least three replicates (minimum n = 3).
- Timeline: Treatments applied on 24/07/17; sheep excluded prior to sampling to avoid confounding excretal inputs.

## Sample Collection and Storage
- Sample collection: Soil solution collected from plots/chambers and stored frozen at -20 °C until analysis.
- Handling: All solutions analysed against certified reference standards.

## Analytical Methods
- Analytes and methods:
  - Nitrate (NO3−): measured by method of Miranda et al. (2001).
  - Ammonium (NH4+): measured by method of Mulvaney (1996).
  - Dissolved organic carbon (DOC) and total dissolved nitrogen (TN) using a Multi N/C 2100S analyser (AnalytikJena).
- Quality: Analyses performed against certified reference standards.

## Data Structure and Variables
- Data headers (columns):
  - Date: date of soil sample collection (dd/mm/yyyy)
  - Days: days after treatment application
  - Treatment: Control, ArtUrine, RealUrine
  - Chamber: plot and chamber number
  - Nitrate: mg NO3−-N L−1
  - Ammonium: mg NH4+-N L−1
  - DOC: mg C L−1
  - TN: mg N L−1

## Quality Assurance and Replicate Notes
- Key QA aspects:
  - Successful sampling achieved for at least three of the four replicate treatments.
  - Storage and analysis performed with reference standards to ensure accuracy.
- Replication intent: four replicate treatments with minimum data from at least three replicates per condition.

## Usage, Attribution, and Data Availability
- Data reuse: Authors must be acknowledged if data are reused or reproduced.
- Potential uses: enables analysis of nitrate, ammonium, DOC, and TN dynamics in response to urine-type N inputs, across time after treatment.

## References
- Miranda, K.M., Epsey, M.G., and Wink, D.A. (2001). A rapid, simple, spectrophotometric method for simultaneous detection of nitrate and nitrite. Nitric Oxide 5, 62-71.
- Mulvaney, R.L. (1996). Nitrogen - inorganic forms. In Sparks, D.L. (Ed.), Methods of Soil Analysis. Part 3. Madison, WI, USA: Soil Science Society of America Inc., pp. 1123-1184.