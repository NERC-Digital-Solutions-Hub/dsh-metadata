# Dataset Title: Carbon and nitrogen stable isotopes in soil profiles at the Glensaugh and Ballogie MOORCO 'BIG' experimental tree planting sites.

## Overview
- A single CSV file containing data for both Glensaugh and Ballogie MOORCO-BIG sites.
- Period of record: 10-Nov-2021 to 12-Nov-2021.
- Total records: 320.
- Measures 13C and 15N in organic soil profiles (O horizons to top of E horizon), plus total soil carbon and nitrogen stocks and bulk density.
- Sites feature experimental plots with birch and pine trees, plus unplanted heather controls, to study tree colonisation effects on soil carbon and isotopes.

## Dataset Details and Context
- MOORCO-BIG experiment: established 2005 on heather moorland in NE Scotland; fenced plots planted with Betula pubescens (birch) and Pinus sylvestris (pine) at 1 m spacing, plus heather controls. Replication: 4 blocks at Glensaugh and Invercauld, 3 blocks at Ballogie.
- Data generated from fenced/unfenced treatments within blocks, focusing on mechanisms and rates of change during succession from moorland to woodland, with emphasis on carbon and isotope dynamics.

## Sampling, Processing, and Laboratory Methods
- Soil sampling: 5 x 5 cm steel box cores; 4 random cores per plot, sampled to full organic horizon thickness plus top 2 cm of mineral soil.
- Horizon separation in the field: LFH, organic top, organic lower, and mineral horizons; LFH and organic layers split into sub-sections (top/bottom) where identifiable.
- Field handling: horizons bagged and kept chilled until lab processing.
- Laboratory processing: air-dried at 30°C for 2–3 weeks; organic horizons milled to <2 mm; samples ball-milled; a subset oven-dried for moisture and bulk density calculations.
- Chemical analyses: total C and N via automated Dumas combustion (EA-IRMS system). Isotopic ratios measured for 13C and 15N separately due to high C:N ratios.

## Data Calculations and Stocks
- Carbon stock calculations: Carbon Stock (kg m^-2) derived from dry bulk density, carbon content, and core length; results converted to t/ha as standard.
- Core metrics: core length, stone volume (adjusted for stones >2 mm), bulk density (stones removed), moisture content, and dry weight estimates used to determine oven-dry weight.
- Metadata for calculations: includes depth, horizon, and sample identifiers; isotopic values reported as delta13C VPDB and delta15N Air.

## Data Quality, Metadata, and Structure
- Quality control: checks of min/max values against ecologically realistic ranges; histogram inspection for outliers; no outliers identified.
- Data fields recorded include: site, date, sample ID, tree species, quadrat, horizon, depth (cm), horizon volume, oven-dry soil plus roots, oven-dried stones, stone volume, dry bulk density, percent carbon, percent nitrogen, C:N ratio, soil carbon stock (kg m^-2), percent soil moisture content, percent dry weight, delta13C VPDB, delta15N Air.
- Data structure notes: missing values coded as NA; horizon designation includes LFH, O1, O2, E, etc.

## Data Structure and Variables
- Core variables include: Site name, Date, Sample.ID, Species, Quadrat, Horizon, Depth.cm, volume.cm3, g.OD.soil.plus.roots, OD.stones.g, calc.stone.vol.cm3, dry.bulk.density.DBf.g.per.cm3, per.C, per.N, CN.ratio, C.stock.kg.per.m2, per.SMC, per.DWT, delta.13.C.VPDB, delta.15.N.Air.

## Access, Use, and Governance
- Maintained by Lorna Street; contact: lstreet1@ed.ac.uk.
- Dataset description indicates transparent methodology, QA procedures, and explicit data processing steps to support reproducibility and verification.
- Data are organized to support comparative analyses across treatments (birch, pine, heather controls) and sites (Glensaugh, Ballogie).

## Relevance to Monitoring Frameworks
- Provides concrete, standardized measures for monitoring soil carbon and nitrogen dynamics in relation to afforestation and land-use change.
- Includes explicit metadata, processing pipelines, and quality checks essential for evaluating policy impacts on soil health and greenhouse gas potential.
- Facilitates cross-site comparisons and temporal assessments, addressing common monitoring framework challenges like data gaps, metadata completeness, data provenance, and data governance.