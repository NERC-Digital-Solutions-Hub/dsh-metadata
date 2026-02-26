# Supporting Information

- The NERC Soil Biodiversity Thematic Programme (launched 1999) focused on linking soil biodiversity with key ecological processes using a large field experiment at Sourhope, Scottish Borders.
- Primary aims: understand soil biota diversity and the functional roles of soil organisms in processes like carbon and nitrogen cycling.
- 24 research projects funded to study soil structure, processes, microfauna and flora, meso- and macro-fauna, and their roles in ecosystem functioning.
- This document documents nitrous oxide flux measurements (N2O) as part of examining how land-use management affects nitrogen cycling via nitrifiers and denitrifiers.

## Study Context

- Site: Sourhope field experiment (Macaulay Land Use Research Institute / James Hutton Institute).
- Focus: how land management alters nitrous oxide production and emission; static chamber measurements used to quantify fluxes under different treatments and environmental conditions.

## Methods

- Gas flux measurement: static chambers used to measure nitrous oxide (N2O) flux in upland agricultural grassland soil.
- Chamber placement: permanent chambers located in general sampling areas S, T, U, V within treatment sub-plots; randomization applied to assign treatments (Control, Nitrogen, Lime, Nitrogen + Lime). Chamber positions chosen to avoid soil moisture differences associated with ridges vs. furrows.
- Chamber design: 40 cm diameter polypropylene tubes, 20 cm height, PVC flanges, silicone seals, gas sampling via a tube sealed through the chamber wall, and collapsible UV-permeable lids to enable gas sampling.
- Gas sampling: N2O collected in Tedlar bags or 10 ml syringes; samples analysed by gas chromatography.
- Gas chromatography setup: Chrompak CP 9000 with Poropak Q column and electron capture detector (ECD); oven at 30°C, ECD at 350°C; carrier gas flow ~5 ml/min; sample loop 0.5 ml; backflush cleanup to minimize water interference.
- Calibration: standard gas injections (≈1 ppm N2O in 80% N2 / 20% air) at beginning and end of runs to calibrate concentrations and correct drift.
- Data collection window: May 2000 – Nov 2001.

## Experimental Design

- Treatments: Control, Lime, Nitrogen, Nitrogen + Lime.
- Field layout: randomised blocks with general sampling areas S, T, U, V; within each, sub-plots with treatments assigned via random numbers.
- Spatial considerations: ridges vs. furrows influence soil moisture; chambers placed on ridges to minimize moisture-driven biases.

## Structure of Data

- Dataset: 1006 - Soil Nitrous oxide field flux data (P2118_SOIL_N2O_FIELD_FLUX_DATA.csv).
- Content: static chamber measurements of N2O flux collected at Sourhope from May 2000 to Nov 2001.
- Key variables and descriptions:
  - EXP_ID: block/main plot/sub-plot identifier (text).
  - EXP_DATE: sampling date (date).
  - BLOCK: block number (1–5) (numeric).
  - MAIN_PLOT: main plot letter (A–F) (text).
  - SUB_PLOT: sub-plot (text).
  - CELL_X, CELL_Y: cell grid numbers (numeric).
  - TREATMENT: soil treatment (Control, Lime, Nitrogen, Nitrogen & Lime, Biocide) (text).
  - NITROUS_OXIDE_FLOW: net production/emission rate (micrograms N2O-N m^-2 h^-1) (numeric; units provided).
- Data quality: includes numeric range checks, formatting checks, and logical integrity checks.

## Quality Control and Use Restrictions

- Verification steps: numeric range checks, formatting conformity, and logical integrity checks.
- Attribution and liability: while QA procedures are applied, the data provider (NERC) does not warrant the accuracy or fitness for a given use; no liability for losses or damages from use of the data.

## Key Findings

- Liming (lime application) increased gross nitrification rates relative to controls (≈1.6 μg N d^-1) and altered the nitric/nitrous oxide flux ratio.
- Adding nitrogen increased both nitric oxide (NO) and nitrous oxide (N2O) flux.
- In all nitrogen-containing treatments, gross nitrification rates decreased relative to control and lime/nitrite treatments.

## Data Management and Accessibility

- Data are organized as a CSV dataset with accompanying metadata descriptions for each field, enabling standardised interpretation and reuse.
- The dataset is prepared for standardized reporting formats (e.g., maps, charts, reports) and stored as part of the project outputs to support long-term environmental monitoring and scrutiny of nitrogen-cycle processes under different land-use practices.
- References and related materials (e.g., Sourhope Field Data Handbook) are available to provide context and methodological detail for data users.