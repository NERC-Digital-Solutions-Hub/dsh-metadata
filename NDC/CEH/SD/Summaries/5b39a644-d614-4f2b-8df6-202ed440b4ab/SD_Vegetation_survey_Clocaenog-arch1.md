# Details of data structure for 'Vegetation survey_Clocaenog.csv'

## Overview
- A single spreadsheet containing 22 columns detailing vegetation biomass data for Clocaenog.
- Time span: Years 1998 to 2012.
- Two data blocks:
  - Species-level biomass per unit area over time (Columns 1–12).
  - Plot-level total biomass per unit area over time (Columns 13–22).
- Empty cells indicate missing data.

## Column structure and data blocks
- Columns 1–12 (species-level data):
  - Column 1: Year (1998–2012)
  - Column 2: Measured plant species
  - Column 3: Biomass type indicator (whether total biomass or living (alive) biomass was measured)
  - Columns 4–12: Biomass measurements for experimental plots 1–9 (per unit area), corresponding to the species and year
- Columns 13–22 (plot-level total biomass data):
  - Column 13: Year (1998–2012)
  - Columns 14–22: Total biomass measurements for experimental plots 1–9 (per unit area), corresponding to the year

## Data interpretation
- All biomass values are reported per unit area.
- Column 3 distinguishes between total biomass and living biomass for the species-level data.
- The dataset provides both species-specific biomass and aggregate plot-level biomass across the same time period.

## Practical considerations for analysts
- Handle missing data carefully due to empty cells.
- When aggregating, ensure alignment by year, species, biomass type, and plot.
- Use the two data blocks to analyze species-specific trends as well as overall plot-level biomass over time.

## Context and provenance
- This document is a supplement to the supporting documentation for data series described in: Clocaenog_supporting documentation_Data series.rtf.
- Focused on the vegetation survey data for Clocaenog.