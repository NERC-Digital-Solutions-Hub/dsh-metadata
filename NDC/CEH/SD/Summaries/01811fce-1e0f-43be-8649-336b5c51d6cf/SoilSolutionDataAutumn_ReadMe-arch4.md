# ReadMe file for SoilSolutionDataAutumn.csv

## Overview
- Describes soil solution chemistry data from control (no urine), artificial sheep urine, and nitrate/glucose treatments applied to a humic gleysol in unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK.
- Location details: 556 m above sea level; coordinates 53°22'N, 3°95'W.
- Timeline: Treatments applied on 25/10/17; sheep excluded from 15/05/17 to avoid confounding excretal events.
- Sampling used Rhizon® soil solution samplers; minimum of three successful samples per treatment (out of four replicates).

## Treatments
- Control: no urine application.
- Artificial sheep urine: patches with an N application rate of 1120 kg N ha-1; 200 mL artificial urine per 100 cm2 soil surface per patch.
- Nitrate and glucose: 106 kg N ha-1 and 213 kg C ha-1 applied within a 40 cm × 40 cm square inside plots.
- Note: Data headers include a treatment category labeled as 'Control', 'ArtUrine' (Artificial urine), and 'RealUrine' (real urine), indicating a possible naming distinction in the dataset.

## Sampling and Equipment
- Rhizon® soil solution samplers: 2.5 mm diameter, 5 cm porous section, 12 cm tubing.
- Insertion: at 45° angle to the soil surface, within the treatment areas inside chambers.
- Replication: successful sampling in at least three of the four replicate treatments.

## Data Collection, Storage, and Handling
- Soil solutions stored frozen at -20 °C until analysis.
- Samples analyzed against certified reference standards to ensure accuracy.
- Date column records sample collection date; Day column records days after treatment application.

## Analytical Methods
- Ammonium (NH4+): measured by the method of Mulvaney (1996).
- Nitrate (NO3-): measured by the method of Miranda et al. (2001).
- Dissolved Organic Carbon (DOC) and Total Dissolved Nitrogen (TN): measured using a Multi N/C 2100S analyser (AnalytikJena).
- All analyses calibrated against certified reference standards.

## Data Structure and Headers
- Date: date of soil sample collection (dd/mm/yyyy).
- Day: days after treatment application.
- Treatment: 'Control', 'ArtUrine' (Artificial urine), 'RealUrine' (real urine).
- Chamber: plot and chamber identifier from which samples were taken.
- Nitrate: mg NO3--N L-1.
- Ammonium: mg NH4+-N L-1.
- DOC: mg C L-1.
- TN: mg N L-1.

## Data Quality, Provenance, and Governance
- Clear documentation of treatments, sampling design, and storage conditions to support reproducibility and data discovery.
- Provenance notes include treatment dates, sampling methodology, and analytical references.
- Acknowledgement required for authors if data are reused or reproduced.
- Potential data considerations: alignment between treatment naming in the narrative (ArtUrine, RealUrine) and the data headers (Control, ArtUrine, RealUrine); ensure consistency when integrating with other datasets.

## References
- Miranda, K.M., Epsey, M.G. and Wink, D.A. (2001). A rapid, simple, spectrophotometric method for simultaneous detection of nitrate and nitrite. Nitric Oxide 5, 62-71.
- Mulvaney, R.L. (1996). Nitrogen - inorganic forms. In: Sparks, D.L. (Eds.), Methods of Soil Analysis. Part 3. Madison, WI, USA: Soil Science Society of America Inc., pp. 1123-1184.