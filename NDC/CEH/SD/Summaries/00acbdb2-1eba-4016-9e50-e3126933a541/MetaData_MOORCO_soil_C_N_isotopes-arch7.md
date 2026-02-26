# Carbon and nitrogen stable isotopes in soil profiles at the Glensaugh and Ballogie MOORCO 'BIG' experimental tree planting sites.

## Overview
- A single CSV dataset for two MOORCO-BIG sites (Glensaugh and Ballogie) containing 13C and 15N data for organic soil horizons (from LFH through to the top of the E horizon), plus total soil carbon and nitrogen stocks and bulk density.
- Period of record: 10–12 November 2021.
- Records: 320 observations.
- Authors/maintainer: Lorna Street, Ruth Mitchell; Maintainer: Lorna Street; contact: lstreet1@ed.ac.uk.
- Context: MOORCO-BIG experiment investigates tree colonisation effects on soil carbon and nitrogen dynamics in upland moorland. Plot-level treatments include birch, pine, and heather controls with replication at Glensaugh (n=4) and Ballogie (n=3).

## Data structure and scope
- File: 1 CSV containing data for both sites.
- Spatial scope: Glensaugh and Ballogie MOORCO-BIG plots (two sites within NE Scotland).
- Depth/horizon coverage: Organic horizons (LFH/top O) to top of mineral soil (E horizon) with field horizon separation.
- Sample organization: Each record links to a specific sample ID, plot/quadrat, horizon, and depth.
- Key measurements included:
  - Isotopes: delta-13C (VPDB) and delta-15N (air) per sample.
  - Carbon and nitrogen content: percent C, percent N, C:N ratio.
  - Carbon stock: C.stock.kg.per.m2 per horizon.
  - Bulk density: dry.bulk.density.DBf.g.per.cm3.
  - Moisture and weight metrics: per.DWT, per.SMC, g.OD.soil.plus.roots, OD.stones.g, calc.stone.vol.cm3, volume.cm3.
  - Depth and horizon descriptors: Depth.cm, Horizon (LFH: organic layers; O1/O2; E; etc).
  - Sample metadata: Site, Date, Sample.ID, Species, Quadrat, etc.
- Units: Mixed SI units as defined in the data dictionary (cm, g, cm3, %, ‰, kg/m2, etc).

## Sampling and laboratory methods
- Soil sampling: 5×5 cm steel box corers; 4 random cores per plot; sampled to full organic horizon plus top 2 cm of mineral soil.
- Horizon handling: Horizons field-separated, bagged, cooled; LFH and organic layers processed (with sieving/hammer milling and selective milling for representative sub-samples); mineral layer sieved to 2 mm.
- Processing: Air-dried at 30°C for 2–3 weeks; sub-samples milled for uniform analysis.
- Chemical analyses: Total C and N measured by automated Dumas combustion (Carlo Erba NA 1500).
- Isotope analyses: 13C and 15N isotopic composition determined by EA-IRMS (Europa EA-GSL interfaced to HS2022 IRMS). Analyses occur separately for C and N due to high C:N ratios.

## Calculations and data fields
- Carbon stock calculations:
  - Carbon Stock [g/cm2] = DBf × (%C/100) × core length (cm)
  - Carbon Stock [kg/m2] = Carbon Stock [g/cm2] × 10
  - C_stock per ha or t/ha derived from above with core volume and stone corrections.
- Dry bulk density (DBf): OD soil plus roots / (core volume − stone volume).
- Stone corrections: Stones (>2 mm) oven-dried and subtracted to obtain stone volume.
- Fresh vs oven-dried weights used to estimate moisture content and adjust for dry weight.
- Moisture metrics: Total Water Loss, Soil Moisture Content (SMC), Oven-Dry weight (ODW), etc.
- Isotope fields: delta.13.C.VPDB and delta.15.N.Air (per sample).
- Data dictionary highlights:
  - Site, Description; Date, Description; Sample.ID; Species; Quadrat; Horizon; Depth.cm; volume.cm3; g.OD.soil.plus.roots; OD.stones.g; calc.stone.vol.cm3; dry.bulk.density.DBf.g.per.cm3; per.C; per.N; CN.ratio; C.stock.kg.per.m2; per.SMC; per.DWT; delta.13.C.VPDB; delta.15.N.Air.

## Quality control
- QC approach: range checks against ecologically realistic values and histogram examinations to identify outliers.
- Outcome: No outliers or unrealistic values detected in the dataset.

## Spatial and temporal context for GIS use
- Temporal snapshot: A single sampling campaign over 3 days in November 2021.
- Spatial units: Plot/quadrat-level data nested within two NE Scotland sites (Glensaugh and Ballogie) with known MOORCO-BIG treatment structure (birch, pine, heather control; replication varies by site).
- GIS-ready considerations:
  - Potential layers: horizon-level isotope and C/N stocks per plot; plot-level bulk density and moisture metrics; horizon depth boundaries to create stratified soil profiles.
  - Attributes per horizon: horizon type, depth range, C stock, C and N percentages, C:N ratio, delta-13C, delta-15N, bulk density, moisture metrics, volume.
  - Plot-level context: site name, treatment, replication, quadrat, and sample IDs to join with field GIS layers (plots, blocks, and treatments).

## Data provenance and contact
- Data origin: MOORCO-BIG experiment on heather moorland; background on site locations and treatments provided in accompanying text.
- Maintainer contact: Lorna Street (lstreet1@ed.ac.uk).
- Related background: Experiment aims to elucidate mechanisms and rates of carbon and nitrogen dynamics during early tree establishment, with plots containing Bircha pubescens and Pinus sylvestris, plus unfenced fenced treatments.

## Summary for GIS-focused use
- This dataset provides horizon-resolved isotope and elemental data (C, N, stocks, bulk density) suitable for building soil-profile GIS layers per plot at Glensaugh and Ballogie.
- Useful products include horizon-specific C stock maps, isotope ratio distributions by depth, and plot-level comparisons of treatments.
- The data enable spatial analysis of soil carbon and nitrogen dynamics in relation to tree planting treatments and Moorko-BIG replication, with a clear structure to integrate with plot and horizon geometry in GIS workflows.