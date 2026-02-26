# Supporting information

- File: BLEL_Phytoplankton_counts.csv
- Collected by: Emma Gray for the project NEC05744
- Purpose: Water samples for taxonomic identification and counting of phytoplankton to derive biovolume and biomass estimates
- Timeframe: 2016 (weekly from June to November)
- Sampling design: From the lake at depths 1 m to 6 m (metre intervals) using the automated monitoring buoy (Fig.1)

## Overview

- Dataset contains phytoplankton counts and biovolume estimates for multiple species.
- Counts and measurements were conducted with standardized laboratory procedures and software (PMX).

## Sampling and preservation

- Water samples collected at depths of 1–6 m at weekly intervals (June–November 2016).
- Samples preserved in Lugols iodine; kept in dark bottles, cooled, and shielded from light.
- Sample handling included monitoring for evaporation and topping up with Lugols or water as needed.

## Laboratory methods and species identification

- Phytoplankton counted and measured using PlanktoMetriX (PMX) software, enabling biovolume and biomass calculations.
- A baseline species database (from 2011–2015) was created in PMX to identify species common to Blelham Tarn; a total of 142 species were identified.
- Biovolume calculations followed CEN (2014) guidance; geometric shapes and equations assigned per species.
- To improve efficiency, a subsample from 1 m was used to identify present species; ten measurements per species were averaged and applied to samples from 1–5 m.

## Counting protocol and quality assurance

- Counting performed with an Olympus BX45 inverted microscope using a Lund chamber.
- Random fields of view used; larger phytoplankton counted at x100 magnification; nanophytoplankton at x400.
- Counting rule: count all organisms in a known number of random fields; if a phytoplankton lies between fields, include if at least 50% is within the field of view; exclude if less than 50% is visible.
- For each counting session, counts were limited to 100 individuals; beyond this, counts were not extended.

## Data contents and structure

- File contents include:
  - Sampling date
  - Depth (1–6 m)
  - Species name
  - AvX (µm)
  - AvY (µm)
  - AvZ (µm)
  - Biovolume (µm³/mL)
- The AvX, AvY, AvZ values are mean measurements based on 10 measurements per organism.

## Location context

- Figure 1 indicates Blelham Tarn’s location in the Lake District, with the monitoring buoy placed at the lake’s deepest point (14.5 m).

## References and methodological context

- CEN (2014) Guidance on estimation of phytoplankton biovolume.
- Lund, J. W. G. (1959) Simple counting chamber for nannoplankton.
- Ramsbottom, A. (1976) Depth charts of the Cumbrian lakes.
- Zohary, T., Shneor, M., & Hambright, D. (2016) PlanktoMetrix system for counting and measuring plankton.