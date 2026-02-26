# Dataset Title: Fungal hyphal in-growth at the Glensaugh and Ballogie MOORCO 'BIG' experimental tree planting sites.

## Overview
- A single CSV dataset containing data for two MOORCO-BIG sites: Glensaugh and Ballogie in North East Scotland.
- Records: 20 observations.
- Authors/owners: Lorna Street, Tom Parker, Ruth Mitchell. Maintainer: Lorna Street.
- Contact: lstreet1@ed.ac.uk
- Focus: Fungal hyphal production in soil using ingrowth bags deployed in planted plots and controls.

## Data structure and variables
- Data file: 1 CSV containing data for both sites.
- Key variables and descriptions (as defined in the metadata):
  - Site Description: Site name (Glensaugh or Ballogie). Site Units: none.
  - Species Description: Tree species in plot (Birch Betula pubescens or Pine Pinus sylvestris) or Heather control. Species Units: none.
  - Sample.ID Description: Unique sample identifier. Sample.ID Units: none.
  - Start.date Description: Start of bag deployment. Start.date Units: dd-mmm-yy.
  - End.date Description: End of bag deployment. End.date Units: dd-mmm-yy.
  - Mean.ingrowth.mg.C Description: Fungal ingrowth quantified as milligrams of carbon per bag. Units: Mg C per bag.
- Data capture includes site, plot treatments, replication context, and computed mean ingrowth per plot.

## Methods and processing
- Hyphal in-growth measurement method:
  - Sand-filled ingrowth bags (5 x 5 cm, 37 μm mesh) with 18 g builder’s sand.
  - Deployed at four points per plot, 45° angle, top beneath litter layer.
  - Deployment window: 26 May 2021 to 9 Nov 2021 (bags retrieved, lab processing occurred in the same period for blanks).
- Laboratory processing:
  - 2.5 g sand per bag is sonicated in 40 ml deionised water to release hyphae.
  - Hyphae dried for 48 h and analyzed for carbon content via Flash Smart elemental analyser.
  - Four blank samples (not field-deployed) processed identically; their average C content subtracted from all samples.
- Output: Reported values represent the mean fungal ingrowth for each plot.

## Context and background
- MOORCO-BIG experiment:
  - Established 2005 on heather moorland to study mechanisms of woody plant colonisation and carbon dynamics.
  - Trials include Birch (Betula pubescens) and Pine (Pinus sylvestris) planted at 1 m spacing and unplanted heather controls.
  - Replication levels: n = 4 blocks at Glensaugh; n = 3 blocks at Ballogie.
- BIG experiment naming and sites:
  - The acronym MOORCO-BIG references three sites: Ballogie, Invercauld, Glensaugh.
  - Background focus includes the role of herbivores, CO2, dissolved organic carbon (DOC), and soil carbon dynamics during early woodland establishment.
- Site coordinates:
  - Glensaugh: NO675801
  - Invercauld: NO170950
  - Ballogie: NO550930

## Access, provenance, and maintenance
- Maintainer: Lorna Street.
- Contact provided for data queries.
- Data linked to ongoing MOORCO project on moorland colonisation and tree establishment across multiple sites.

## Data quality and usage considerations
- Period of record for the field and lab work is 2021 (May–November), but the dataset’s overall period is not explicitly stated.
- Only 20 records in the CSV; users should verify plot-level averaging and replication details against the accompanying metadata.
- Units are specific (Mg C per bag) and require consistent interpretation when combining with other datasets.
- Data represent mean ingrowth per plot, derived after subtracting blank sample values, which is important for cross-study comparability.

## Opportunities for Data Leaders
- Integrate this dataset with other MOORCO-BIG data (e.g., CO2, DOC, soil carbon dynamics) to analyse links between fungal activity and carbon cycling during early tree establishment.
- Use the clear metadata and processing steps to develop standardized data products and improve discoverability across MOORCO and partner networks.
- Leverage the replication and site-level treatment structure to explore data governance, lineage, and cross-site comparability for future data-sharing initiatives.