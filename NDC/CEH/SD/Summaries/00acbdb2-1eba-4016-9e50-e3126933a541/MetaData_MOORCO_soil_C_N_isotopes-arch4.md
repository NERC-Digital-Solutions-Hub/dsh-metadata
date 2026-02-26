# Dataset Title: Carbon and nitrogen stable isotopes in soil profiles at the Glensaugh and Ballogie MOORCO 'BIG' experimental tree planting sites.

## Overview
- A single CSV file containing data for two MOORCO-BIG sites (Glensaugh and Ballogie) on North East Scotland moorland.
- Focused on 13C and 15N data for organic soil profiles, from the LFH horizon through the top of the E horizon, plus total soil carbon and nitrogen stocks and bulk density.
- Period of record: 10-Nov-2021 to 12-Nov-2021.
- Records: 320.
- Authors/maintainer: Lorna Street and Ruth Mitchell; Maintainer: Lorna Street (lstreet1@ed.ac.uk).

## What the dataset covers
- Part of the MOORCO-BIG experiment, an established tree-planting study on heather moorland initiated in 2005.
- Data pertain to fenced plots planted with Birch (Betula pubescens) and Pine (Pinus sylvestris) at 1 m spacing, plus unplanted heather controls.
- Replication: n = 4 blocks at Glensaugh; n = 3 blocks at Ballogie.
- Sites for this dataset: Glensaugh (NO675801) and Ballogie (NO550930).

## Sampling and sample handling
- Soil sampling method: 5 x 5 cm steel box cores; 4 randomly located cores per plot to full organic horizon thickness and top 2 cm of mineral soil.
- Horizons separated in the field into LFH, organic top, organic lower, and mineral layers; cores split accordingly and kept chilled until lab processing.
- Cores and horizons processed by drying, milling, sieving (2 mm), and ball-milling for analysis.

## Measurements and analyses
- Chemical analyses:
  - Total carbon (C) and nitrogen (N) via automated Dumas combustion (Carlo Erba NA 1500).
  - Stable isotope ratios for 13C and 15N using EA-IRMS (Europa EA-GSL connected to HS2022 IRMS), with 1000°C combustion and related gas handling.
- Isotopes analyzed separately due to high C:N ratios in many soils.

## Data structure and variables
- Data stored in one CSV with fields including:
  - Site, Date, Sample.ID, Species, Quadrat, Horizon (e.g., LFH, O1, O2 top/bottom, E), Depth.cm, volume.cm3, g.OD.soil.plus.roots, OD.stones.g, calc.stone.vol.cm3, dry.bulk.density.DBf.g.per.cm3, per.C, per.N, CN.ratio, C.stock.kg.per.m2, per.SMC, per.DWT, delta.13.C.VPDB, delta.15.N.Air, among others.
  - Units: various (cm, g, %, ‰), with NA for missing values.
- Horizon specifics: LFH, O1/O2 (organic top/bottom), E (top of mineral horizon), depth segmentation per horizon.

## Calculation details
- Carbon stock calculations provided:
  - Carbon Stock (g/cm2) = DBf × (%C / 100) × core length (cm)
  - Carbon Stock (kg/m2) = Carbon Stock (g/cm2) × 10
  - Carbon Stock (t/ha) = Carbon Stock (g/cm2) × 100
- Dry bulk density (DBf) derived from oven-dried soil plus roots, corrected for stone volume; stone volume estimated from oven-dried stones.
- Subsampled for oven-dry weight to estimate dry weight of cores; moisture content and soil moisture metrics included.

## Quality control and data quality
- Quality control included checks of maximum/minimum realistic ecologies values and histogram-based outlier screening.
- Reported as: no outliers or unrealistic values identified.

## Context and background
- The MOORCO project investigates mechanisms and rates of change during succession from moorland to woodland, including the role of herbivores; BIG site investigations include Pinus sylvestris and Betula pubescens trees.
- The dataset draws from the Ballogie and Glensaugh sites (part of the BIG experiment) and aligns with broader MOORCO objectives to quantify soil C and N dynamics during early tree colonisation.

## Data management and access
- Data maintained by Lorna Street (contact provided above).
- Dataset is a self-contained CSV comprising both sites; suitable for integration with wider soil carbon and isotope datasets and for informing data strategies around soil carbon stocks and isotopic provenance.
- Background site coordinates and replication structure provide context for cross-site comparability and governance of multi-site data products.