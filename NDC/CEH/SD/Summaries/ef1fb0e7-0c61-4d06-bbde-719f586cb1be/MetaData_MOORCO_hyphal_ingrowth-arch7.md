# Fungal hyphal in-growth at the Glensaugh and Ballogie MOORCO 'BIG' experimental tree planting sites

## Overview
- Single CSV dataset containing data for both Glensaugh and Ballogie sites (MOORCO-BIG experiment).
- Records: 20; data describe fungal hyphal in-growth into sand-filled bags during 2021 growing season.
- Purpose: quantify fungal ingrowth as part of Moorland colonisation/tree-planting study using sand bag ingrowth method.
- Part of the MOORCO-BIG experiment at NE Scotland, relating to fenced/unfenced plots with Birch, Pine, and Heather control treatments.

## Data Scope
- Sites: Glensaugh and Ballogie (NE Scotland). Background MOORCO BIG experiment spans Glensaugh, Ballogie, Invercauld; this dataset covers two sites.
- Deployment period: 26 May 2021 – 9 Nov 2021 (bags deployed in field; blanks kept in lab for same period).
- Plot-level data: measurements reported as mean fungal ingrowth per plot (mg C per bag).

## Data Structure and Variables
- Data file: 1 CSV containing records for both sites.
- Key fields (described and units):
  - Site, Description: Site name; Site, Units: none; NA as missing value code.
  - Species, Description: Tree species in plot; Species, Units: none; NA as missing value code.
  - Sample.ID, Description: Unique sample ID; Sample.ID, Units: none; NA as missing value code.
  - Start.date, End.date: Bag deployment window; Units: dd-mmm-yy; NA as missing value code.
  - Mean.ingrowth.mg.C: Fungal ingrowth (mg C per bag); Units: mg C per bag; NA as missing value code.

## Methods
- Hyphal ingrowth assessment using sand-filled ingrowth bags (5 x 5 cm nylon mesh, 37 μm mesh).
- Bags (18 g builders sand) deployed at four points within each plot; inserted at 45° angle with top just below litter layer.
- Post-field processing: bags retrieved, frozen within 4–8 hours, freeze-dried 72 h; 2.5 g sand from each bag sonicated in 40 ml deionised water to extract hyphae.
- Hyphae dried and C content measured with Flash Smart elemental analyser.
- Four blanks (unfielded bags) analyzed for background C; blank average subtracted from all samples.
- Reported values are the mean ingrowth per plot.

## Site Context and Treatments
- Site coordinates (for context): Glensaugh NO675801; Ballogie NO550930.
- BIG experiment background: aims to understand mechanisms/rates of change during succession from moorland to woodland; includes Pinus sylvestris and Betula pubescens, with Heather controls.
- Treatments within each block:
  - Grazing regime: unfenced (grazing) vs fenced (no grazing by large herbivores).
  - Within each block: planted birch (1 m spacing), planted pine (1 m spacing), heather control, low-density birch (single trees), clumped birch (clumps of 4 trees; only at Glensaugh).
- Replication:
  - 4 blocks at Invercauld and Glensaugh; 3 blocks at Ballogie.
  - Each block contains the treatments above.
- Note: The dataset focuses on the hyphal ingrowth measurements rather than all plot-level metadata; complementary MOORCO BIG datasets provide broader context.

## Data Quality and Processing Notes
- Blank correction applied to all samples using blanks.
- Data represent plot-level means; variability across individual bags within a plot is not provided in this file.
- Missing values indicated as NA where applicable.

## GIS Usage and Considerations
- Suitable for spatial visualization of fungal ingrowth across MOORCO BIG plots at Glensaugh and Ballogie.
- Can be joined with plot-level attributes (tree species, planting density, grazing treatment, block/replication) for GIS-based analyses and map displays.
- Temporal context limited to deployment window and sampling period; per-sample dates are available via Start.date and End.date.

## Provenance and Contact
- Authors/Owners: Lorna Street, Tom Parker, Ruth Mitchell; Maintainer: Lorna Street.
- Organization: James Hutton Institute.
- Source: Dataset documenting fungal hyphal ingrowth in the MOORCO-BIG experiment.