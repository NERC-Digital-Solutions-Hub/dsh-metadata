# Dataset Title: Carbon and nitrogen stable isotopes in soil profiles at the Glensaugh and Ballogie MOORCO 'BIG' experimental tree planting sites.

## Overview
- 1 CSV file containing isotope and soil data for two MOORCO BIG experimental tree planting sites (Glensaugh and Ballogie) in North East Scotland.
- Covers 10–12 November 2021; total of 320 records.
- Focuses on 13C and 15N data in organic soil profiles (from organic horizons to top of E horizon), plus total soil carbon and nitrogen stocks and bulk density.
- Context: part of the MOORCO BIG experiment exploring soil carbon dynamics during early tree colonisation; plots include Birch and Pine planted at 1 m spacing and unplanted Heather controls; replication is 4 blocks at Glensaugh and Invercauld, 3 at Ballogie.

## Data structure and contents
- File: 1 CSV containing data for both sites.
- Columns cover:
  - Site name, date, sample ID, tree species (if any), quadrat number, horizon, depth (cm), horizon depth ranges, volume of horizon, oven-dry soil (+ roots), oven-dry stones, stone volume, dry bulk density, percent carbon (C), percent nitrogen (N), C:N ratio, soil carbon stock (kg/m2), soil moisture content (%), dry weight percent, delta13C (VPDB, ‰), delta15N (Air, ‰).
  - Additional fields describing core and sampling details (e.g., core ID, whether mineral sample was taken, comments).
- Horizons included: LFH (litter/fermentation), Organic top, Organic lower, Mineral (top two cm of mineral soil or deeper as applicable), with field-identified subdivisions (top half/bottom half, etc.).

## Methods and processing
- Sampling: 5 x 5 cm steel box cores; 4 random cores per plot; cores taken to full organic horizon depth plus top 2 cm of mineral soil.
- Field processing: Horizons separated, bagged, chilled until lab processing.
- Soil processing: Air-dried at 30°C for 2–3 weeks; LFH milled; Organic layers sieved (<2 mm after removing >2 mm stones/roots); samples ball-milled for analysis.
- Sub-sampling: Oven-dried subsamples for weight determinations; selected sub-samples milled for isotope analysis.
- Isotope analysis: Total C and N measured by automated Dumas combustion (EA-IRMS) with a Europa EA-GSL interfaced to HS2022 IRMS; separate analyses for 13C and 15N due to high C:N ratios.
- Quality control: Basic checks for realistic ranges; histogram inspection; no outliers identified in QC.

## Experimental design and sites
- MOORCO BIG experiment details:
  - Established in 2005 on heath moorland; sites include Glensaugh, Ballogie, and Invercauld.
  - Treatments: fenced (no grazing) vs unfenced (grazing) within each block; within plots: planted birch (Betula pubescens), planted pine (Pinus sylvestris) at 1 m spacing, Heather control, low-density birch, and clumped birch (Glensaugh only).
  - Replication: 4 blocks at Glensaugh and Invercauld; 3 blocks at Ballogie.
- This dataset specifically samples two MOORCO BIG sites (Glensaugh and Ballogie) with fenced/unfenced contexts and tree/veg treatments.

## Derived indicators and calculations
- Carbon stock calculations:
  - Carbon Stock (g/cm2) = Dry bulk density (DBf) × (% C / 100) × core length (cm)
  - Carbon Stock (kg/m2) = Carbon Stock (g/cm2) × 10
  - Carbon Stock (t/ha) = Carbon Stock (g/cm2) × 100
- Dry bulk density (DBf) computed from oven-dried soil plus roots, excluding stone volume.
- Stone volume estimated from oven-dried stone mass.
- Moisture and oven-dry weight determinations used to convert fresh weights to dry weights for stock calculations.

## Data quality and metadata
- Data sources and processing steps are documented, with notes on horizon delineation and lab workflows.
- Metadata include variable descriptions, units, and missing value codes (NA).
- Data maintainers: Lorna Street (lstreet1@ed.ac.uk) and Ruth Mitchell.

## Potential data use for analysis
- Compare isotopic signatures (δ13C, δ15N) across horizons (LFH, Organic, Mineral) and depths between Glensaugh and Ballogie.
- Examine relationships between C and N stocks, soil density, moisture, and horizon depth within planted versus control plots.
- Investigate effects of tree species (Birch vs Pine) and grazing treatments on soil C/N dynamics during early forest establishment.
- Integrate with other MOORCO BIG datasets to model carbon and nitrogen cycling under afforestation on moorland soils.

## Access and contact
- Maintainer: Lorna Street (lstreet1@ed.ac.uk).