# ReadMe file for SoilSolutionDataAutumn.csv

- The document describes soil solution chemistry data collected from a controlled grazing land experiment in Snowdonia National Park, Wales, UK. The study compares a control (no urine), artificial sheep urine, and nitrate plus glucose treatments applied to a humic gleysol in an unimproved grazing area.
- Exclusion of sheep from plots occurred from 15/05/17 to avoid recent excretal events confounding the data.

## Location and Site Details

- Location: Carneddau mountains, Snowdonia National Park, Wales, UK.
- Elevation: 556 m above sea level.
- Coordinates: 53°22'N, 3°95'W.
- Soil and land use: Humic gleysol in an unimproved grazing area.

## Experimental Treatments and Application

- Treatments described:
  - Control: no urine application.
  - Artificial sheep urine (ArtUrine): applied in discrete patches; each patch delivers 1120 kg N ha-1; 200 ml artificial urine per patch over 100 cm2 soil area.
  - Nitrate and glucose: 106 kg N ha-1 and 213 kg C ha-1, applied in a 40 cm x 40 cm square inside plots.
- Note: Data headers include a Treatment field with values such as Control, ArtUrine, and RealUrine (real sheep urine). The detailed description lists Control, Artificial sheep urine, and Nitrate + Glucose; RealUrine is a labeled category in the data header, but the treatment description focuses on the former three.
- Treatment application date: 25/10/17.

## Sampling Design and Methods

- Sampling method: Rhizon® soil solution samplers (2.5 mm diameter, 5 cm porous section, 12 cm tubing) inserted at a 45° angle within treatment plots inside chambers.
- Replication: Successful sampling achieved in at least 3 of 4 replicate treatments (minimum n = 3 per sampling group).
- Sampling timing: Date recorded; Day field indicates days after treatment application.

## Sample Handling and Storage

- Sample handling: Soil solutions collected and stored frozen at -20 °C until analysis.
- Storage and handling aimed at preserving solute integrity until analytical measurements.

## Analytical Methods

- Analytes measured:
  - Nitrate (NO3−): using the method of Miranda et al. (2001).
  - Ammonium (NH4+): using the method of Mulvaney (1996).
  - Dissolved organic carbon (DOC) and total dissolved nitrogen (TN): measured with a Multi N/C 2100S analyser (AnalytikJena).
- Calibration/QA: Analyses performed against certified reference standard solutions.

## Data Structure and Headers

- Date: Date soil samples collected (dd/mm/yyyy).
- Day: Days after treatment application.
- Treatment: Treatment applied to each plot; values include Control, ArtUrine (Artificial urine), and RealUrine (real sheep urine) as labeled in the dataset.
- Chamber: Plot and chamber number from which samples were taken.
- Nitrate: NO3− concentration (mg NO3−-N L−1).
- Ammonium: NH4+ concentration (mg NH4+-N L−1).
- DOC: Dissolved organic carbon (mg C L−1).
- TN: Total dissolved nitrogen (mg N L−1).

## Data Provenance and Usage Notes

- Authorship acknowledgment: Authors must be acknowledged if data are reused or reproduced.
- Date of treatment application: 25/10/17.
- Important caveats:
  - RealUrine label exists in the data header; treatment descriptions focus on Control, ArtUrine, and Nitrate + Glucose. Users should confirm which plots used real sheep urine if relevant to their re-use.
  - Minimum n = 3 per treatment due to replication and sampling success.

## References for Methods

- Miranda, K.M., Epsey, M.G. and Wink, D.A. (2001). A rapid, simple, spectrophotometric method for simultaneous detection of nitrate and nitrite. Nitric Oxide 5, 62-71.
- Mulvaney, R.L. (1996). Nitrogen - inorganic forms. In Sparks, D.L. (Ed.), Methods of Soil Analysis. Part 3. Soil Science Society of America Inc., pp. 1123-1184.