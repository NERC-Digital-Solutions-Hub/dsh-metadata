# ReadMe file for SoilSolutionDataSummer.csv

## Overview
- Dataset contains soil solution chemistry data from three treatments: control (no urine), artificial sheep urine, and real sheep urine.
- Study area: a dystric histosol in unimproved grazing land, Carneddau mountains, Snowdonia National Park, Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W).
- Sheep excluded from plots from 15/05/17 to avoid recent excretal confounding.
- Authors must be acknowledged if data are re-used or reproduced.

## Experimental design and treatments
- Treatments:
  - Control: no urine application.
  - Artificial sheep urine: patches with N application rate of 920 kg N ha^-1 per patch (200 ml urine over 100 cm^2).
  - Real sheep urine: patches with N application rate of 930 kg N ha^-1 per patch (200 ml urine over 100 cm^2).
- Patch-based discrete applications; treatments applied on 24/07/17.
- Minimum of n = 3 samples per treatment (successful collection at least from 3 of 4 replicate treatments).

## Sampling method and locations
- Sampling method: Rhizon® soil solution samplers (2.5 mm diameter, 5 cm porous section, 12 cm tubing).
- Samplers inserted at a 45° angle relative to soil surface.
- Samplings occurred inside the urine patches and control treatments within the chambers.
- Samples collected from multiple plots and chambers (as indicated by the “Chamber” field).

## Sample handling and storage
- Collected soil solutions were stored frozen at -20 °C until analysis.
- Solutions analyzed against certified reference standard solutions for QA.

## Analytical methods
- Ammonium (NH4+): Mulvaney (1996) method.
- Nitrate (NO3-): Miranda et al. (2001) method.
- Dissolved organic carbon (DOC) and total dissolved nitrogen (TN): measured with a Multi N/C 2100S analyser (AnalytikJena).
- All analyses referenced to certified standards.

## Data structure and variables
- Data headers:
  - Date: date of soil sample collection (dd/mm/yyyy).
  - Days: days after treatment application.
  - Treatment: Control, ArtUrine, RealUrine.
  - Chamber: plot and chamber identifier.
  - Nitrate: mg NO3--N L^-1.
  - Ammonium: mg NH4+-N L^-1.
  - DOC: mg C L^-1.
  - TN: mg N L^-1.
- Date format and unit conventions specified in headers.