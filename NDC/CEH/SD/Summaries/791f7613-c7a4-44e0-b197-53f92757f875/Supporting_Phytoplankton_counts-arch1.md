# BLEL_Phytoplankton_counts.csv

## Overview
- Dataset of phytoplankton counts from Blelham Tarn (North West England) collected in 2016.
- Sampling: weekly from June to November, at depths 1–6 m using the automated monitoring buoy (deepest point at 14.5 m).
- Objective: taxonomic identification and biovolume estimation; 142 phytoplankton species identified.
- Data produced: species counts and biovolume calculations to enable biomass estimates.

## Sampling and Preservation
- Water samples collected at metre intervals from 1 m to 6 m depth.
- Preserved with Lugols iodine in dark bottles to prevent degradation.
- In the lab, samples settled in 3 x 100 mL cylinders; supernatant decanted; samples stored cool and light-protected; evaporation checks performed and topped up as needed.

## Identification and Counting Methods
- Phytoplankton counted with PlanktoMetriX (PMX) software on an Olympus BX45 inverted microscope.
- PMX database created (using 2011–2015 data) to identify species common to Blelham Tarn.
- Total identified species: 142.
- Sub-sampling approach: a single 1 m depth sub-sample used to identify species; ten measurements per species averaged; biovolumes applied to samples from 1–5 m.
- Counting protocol: random fields of view in a Lund chamber (Lund, 1959) with a 100-field count at magnifications x100 and x400.
- Counting limits: 100 individuals per species per sample; beyond this, counts are not recorded.

## Biovolume Estimation
- Biovolume calculated using CEN (2014) guidance for geometric shapes and equations per species.
- Measurements used to derive geometry: AvX (x-dimension), AvY (y-dimension), AvZ (z-dimension) in micrometers.
- AvX, AvY, AvZ values are mean dimensions based on 10 measurements per species.
- Biovolume reported as µm^3 per mL.

## Data File Contents and Structure
- Columns include:
  - Sampling date
  - Depth (1–6 m)
  - Species name
  - AvX (µm)
  - AvY (µm)
  - AvZ (µm)
  - Biovolume (µm^3/mL)
- Depth and date align with the sampling events; AvX/AvY/AvZ are averaged measurements used for each species’ biovolume calculation.

## Location and Context
- Figure reference: Blelham Tarn location and buoy at the deepest point (14.5 m) illustrated in the accompanying figure.
- Data are intended for analyses of species composition, biomass estimation, and temporal trends in phytoplankton communities.

## Quality, Limitations, and Considerations
- High species diversity (142 identified) with a sub-sampling approach to streamline counting.
- Counting capped at 100 individuals per species per sample; may affect low-abundance species representation.
- Biovolume relies on geometric approximations per species as per standard guidance; variability in natural shapes may introduce estimation error.
- Data represent a single lake/site and a specific time window (2016, June–November), which should be considered when extrapolating to other contexts.
- Preservation, storage, and handling steps are designed to minimize evaporation and light exposure, but potential sample handling biases should be acknowledged.

## References
- CEN (2014) Water quality - Guidance on the estimation of phytoplankton biovolume.
- Lund, J. W. G. (1959) A Simple Counting Chamber for Nannoplankton. Limnology and Oceanography.
- Ramsbottom, A. (1976) Depth charts of the Cumbrian lakes. Freshwater Biological Association.
- Zohary, T., Shneor, M., Hambright, D. (2016) PlanktoMetrix - a computerized system to support microscope counts and measurements of plankton. Inland Waters.