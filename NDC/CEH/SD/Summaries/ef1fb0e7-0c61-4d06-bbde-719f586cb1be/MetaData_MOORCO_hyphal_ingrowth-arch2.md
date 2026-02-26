# Dataset Title: Fungal hyphal in-growth at the Glensaugh and Ballogie MOORCO 'BIG' experimental tree planting sites.

## Overview
- Single CSV dataset containing data for two MOORCO-BIG sites in North East Scotland: Glensaugh and Ballogie.
- 20 records reporting fungal hyphal in-growth as a mean value per plot.
- Measurements derived from sand-filled ingrowth bags deployed in fenced plots containing birch and pine trees, plus heather controls.
- Part of the MOORCO-BIG experiment investigating moorland to woodland succession and the role of herbivores.

## Data structure and contents
- File composition: 1 CSV file with data for both sites.
- Key measurement: Mean.ingrowth.mg.C (mean fungal ingrowth in milligrams of carbon per bag).
- Variables include:
  - Site, Description (site name; no units)
  - Site, Units (none)
  - Site, Missing value code (NA)
  - Species, Description (tree species in plot)
  - Species, Units (none)
  - Species, Missing value code (NA)
  - Sample.ID, Description (unique sample identifier)
  - Sample.ID, Units (none)
  - Sample.ID, Missing value code (NA)
  - Start.date, Description (start of bag deployment; dd-mmm-yy)
  - End.date, Description (end of bag deployment; dd-mmm-yy)
  - Mean.ingrowth.mg.C, Description (fungal ingrowth; Mg C per bag)
  - Mean.ingrowth.mg.C, Units (Mg C per bag)
  - Mean.ingrowth.mg.C, Missing value code (NA)

## Experimental background
- The MOORCO-BIG experiment: an experimental tree-planting site on heath moorland established in 2005 to study mechanisms and rates of change in succession from moorland to woodland, including herbivore effects.
- Locations: Ballogie, Invercauld, Glensaugh (BIG = three sites).
- Treatments within blocks:
  - Grazing by large herbivores (unfenced) vs. no grazing (fenced)
  - Within each fence/unfence plot: planted birch (Betula pubescens) and pine (Pinus sylvestris) at 1 m spacing, heather control, low-density birch, and clumped birch (only at Glensaugh)
- Replication: 4 blocks at Invercauld and Glensaugh; 3 blocks at Ballogie.

## Hyphal in-growth measurement method
- Method: sand-filled ingrowth bags (5 x 5 cm nylon mesh, 37 µm mesh) filled with 18 g builders sand.
- Deployment: four bags per plot, inserted at 45° angle under litter layer to maximize contact with soil horizons.
- Field period: 26 May 2021 to 9 Nov 2021 (blanks maintained in lab over same period).
- Sample processing: bags frozen 4–8 hours after field recovery, freeze-dried for 72 hours.
- Extraction and analysis: 2.5 g sand per bag sonicated in 40 ml deionised water to release hyphae; hyphae dried and analyzed for carbon content using Flash Smart elemental analyzer; four field blanks subtracted from all samples.
- Output: mean hyphal ingrowth per plot (in mg C per bag).

## Data quality and management
- Maintainer: Lorna Street
- Authors/owners: Lorna Street, Tom Parker, Ruth Mitchell
- Contact: lstreet1@ed.ac.uk
- Data reflects field-derived measurements with blanks subtracted; values represent mean ingrowth per plot across the four bags per plot.

## Context and potential use for environmental monitoring
- Provides standardized, plot-level data on soil fungal colonization during early stages of tree establishment.
- Useful for monitoring soil carbon dynamics and microbial responses to tree colonisation and herbivore management.
- Aligns with aims to increase dataset value through integration with other environmental datasets and provide accessible underlying data for broader analysis.