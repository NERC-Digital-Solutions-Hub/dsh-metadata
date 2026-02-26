# Fungal hyphal in-growth at the Glensaugh and Ballogie MOORCO 'BIG' experimental tree planting sites.

- Dataset consists of 1 CSV file containing data for both sites (Glensaugh and Ballogie)
- Authors/Owners: Lorna Street, Tom Parker, Ruth Mitchell; Maintainer: Lorna Street
- Contact: lstreet1@ed.ac.uk
- Period of record: not specified in the file; data cover the 2021 growing season (26 May 2021 – 9 Nov 2021 for field deployment)
- Number of records: 20

## Overview

- Objective: quantify fungal hyphal production (ingrowth) in sand-filled ingrowth bags as part of the MOORCO-BIG experiment
- Sites: Glensaugh and Ballogie in North East Scotland; MOORCO-BIG established 2005 on heather moorland
- Context: MOORCO-BIG investigates mechanisms and rates of change, and the role of herbivores in succession from moorland to woodland
- Experimental design (relevant to this dataset): fenced vs unfenced plots (grazing vs no grazing), with planted birch and pine, plus heather controls; replication n = 4 at Glensaugh and Invercauld, n = 3 at Ballogie

## Data structure and collection

- Data file: 1 CSV containing measurements for both sites
- Hyphal ingrowth method:
  - Bags: 5 x 5 cm nylon mesh, 37 µm mesh size, filled with 18 g builders sand
  - Deployment: four bags per plot, inserted at 45° with top just below litter layer
  - Deployment window: 26 May 2021 – 9 Nov 2021
  - Field blanks processed in parallel
  - Field samples frozen shortly after retrieval and freeze-dried for 72 hours
- Laboratory processing:
  - 2.5 g sand from each bag sonicated in 40 ml deionised water for 10 minutes
  - Extracted hyphae analyzed for C content using Flash Smart elemental analyser
  - Four blank samples (not field-deployed) used to calculate average blank C content, subtracted from all samples
- Output: Mean ingrowth per plot (Mean.ingrowth.mg.C)

## Variables (key fields)

- Site, Description: Site name; Units: none; Missing value code: NA
- Species, Description: Tree species in plot; Units: none; Missing value code: NA
- Sample.ID, Description: Unique sample ID; Units: none; Missing value code: NA
- Start.date, Description: Start of bag deployment; Units: dd-mmm-yy; Missing value code: NA
- End.date, Description: End of bag deployment; Units: dd-mmm-yy; Missing value code: NA
- Mean.ingrowth.mg.C, Description: Fungal ingrowth; Units: Mg C per bag; Missing value code: NA

## Background and site details

- The BIG experiment (3 sites): Ballogie, Invercauld, Glensaugh
- Site coordinates (Grid references):
  - Glensaugh: NO675801
  - Invercauld: NO170950
  - Ballogie: NO550930
- Treatments within each block:
  - Grazing by large herbivores: unfenced
  - No grazing by large herbivore: fenced
  - Within each fence/unfence plot: planted birch (1 m spacing), planted pine (1 m spacing), heather control, low density birch, clumped birch (clumps of 4 trees) – the last only at Glensaugh
- Replication: 4 blocks at Invercauld and Glensaugh; 3 blocks at Ballogie

## Data use and considerations

- Data represent mean ingrowth per plot, enabling comparisons across species, grazing regimes, and plot types within Glensaugh and Ballogie
- Blanks corrected carbon content to isolate fungal ingrowth signal
- Dataset provides a snapshot for the 2021 growing season; may be integrated with other MOORCO-BIG data for broader analyses of tree colonisation, soil carbon dynamics, and ecosystem development

## Access and responsibilities

- Maintainer: Lorna Street
- Contact: lstreet1@ed.ac.uk
- Data provenance: collected as part of the MOORCO-BIG experiment; ties to broader MOORCO project outputs and publications for detailed context