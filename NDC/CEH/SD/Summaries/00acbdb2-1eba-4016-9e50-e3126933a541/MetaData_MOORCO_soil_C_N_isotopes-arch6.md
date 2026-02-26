# Carbon and nitrogen stable isotopes in soil profiles at the Glensaugh and Ballogie MOORCO 'BIG' experimental tree planting sites.

## Overview
- A single CSV dataset containing 13C and 15N isotope data for organic soil profiles (from organic horizons to the top of the E horizon) at two MOORCO BIG tree planting sites in North East Scotland: Glensaugh and Ballogie.
- Includes total soil carbon and nitrogen stocks and bulk density.
- Records: 320; period of sampling: 10–12 Nov 2021.
- Context: MOORCO BIG experiment investigates tree colonisation dynamics (birch, pine) and associated soil carbon/nitrogen dynamics on heather moorland.

## Data structure and content
- File: 1 CSV containing data for both sites.
- Key fields and units:
  - Site, Description; Date (none); Sample.ID (unique per sample)
  - Species (tree species per plot); Quadrat (1–4)
  - Horizon (LFH, Organic top, Organic lower, Mineral; O halves; E horizon)
  - Depth.cm (depth of horizon)
  - Volume.cm3, g.OD.soil.plus.roots (oven-dry soil with roots)
  - OD.stones.g (oven-dried stones)
  - calc.stone.vol.cm3 (stone volume)
  - dry.bulk.density.DBf.g.per.cm3 (bulk density)
  - per.C, per.N (percent carbon and nitrogen by mass)
  - CN.ratio (C:N ratio)
  - C.stock.kg.per.m2 (soil carbon stock per m2)
  - per.SMC (soil moisture content)
  - per.DWT (percent dry weight)
  - delta.13.C.VPDB (13C isotopic composition, ‰)
  - delta.15.N.Air (15N isotopic composition, ‰)

## Sampling and laboratory methods
- Field sampling:
  - 5 x 5 cm steel cores; 4 randomly located cores per plot; cores collected to full organic horizon thickness plus top 2 cm of mineral soil.
  - Horizons separated in the field (LFH, Organic top/bottom, Mineral) and bagged; samples kept chilled.
- Sample processing:
  - Air-dried at 30°C for 2–3 weeks; subsamples milled (Hammer mill for LFH; organic layers milled after sieving roots/stones).
  - Organic fractions: stones >2 mm removed; organic material milled and combined; oven-dried subsamples used for weight determination.
  - Mineral horizon samples sieved to <2 mm; all horizon samples ball-milled.
  - QC: a subsample used to determine oven-dry weight to estimate core dry weight.
- Chemical analyses:
  - Total C and N via automated Dumas combustion using Carlo Erba NA 1500 Elemental Analyser.
  - Stable isotope ratios measured by EA-IRMS (13C via VPDB, 15N via Air).
  - Isotopes measured separately due to high C:N ratios in soils.

## Calculations and data derivations
- Carbon stock calculations:
  - Carbon Stock (g cm-2) = DBf × (%C / 100) × core length (cm)
  - DBf (bulk density) calculation incorporating oven-dry soil mass minus stone volume.
  - Conversion to area stocks: Carbon Stock (kg m-2) and t ha-1 via unit conversions.
- Mass and moisture:
  - Fresh weight (FWT) and air-dried weight (ADWT) derived from tray weights and core weights.
  - Total Water Loss and Soil Moisture Content derived to estimate soil moisture corrections.
- Stone volume and density:
  - Stone volume computed from oven-dried stones mass and assumed density (2.55 g cm-3 for stones).

## Quality control and data integrity
- QC approach: check min/max values against ecologically realistic ranges; histogram review to identify outliers.
- Outcome: no outliers or unrealistic values identified in the dataset.

## Context and background
- MOORCO BIG experiment: established 2005 to study Moorland to woodland succession mechanisms, including Pinus sylvestris and Betula pubescens planting; investigates roles of herbivores, CO2, DOC, and soil carbon dynamics during early tree colonisation.
- Sites represented in this dataset: Glensaugh and Ballogie (in North East Scotland); replication of treatments within blocks (details in background).

## Practical considerations for data use
- Single CSV file facilitates integration with dashboards or analysis workflows for self-service data exploration.
- Clear documentation of horizons, sampling depths, and processing steps supports reproducibility and cross-site comparisons.
- Metadata includes site names, horizons, and isotopic measurements, enabling comparisons of organic layer isotopes with bulk soil properties.

## Access and contact
- Maintainer: Lorna Street
- Contact: lstreet1@ed.ac.uk