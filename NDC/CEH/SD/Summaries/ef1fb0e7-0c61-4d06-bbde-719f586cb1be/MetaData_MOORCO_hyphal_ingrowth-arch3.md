# Fungal hyphal in-growth at the Glensaugh and Ballogie MOORCO 'BIG' experimental tree planting sites.

## Overview
- 20 records in a single CSV file covering two MOORCO-BIG experimental sites: Glensaugh and Ballogie.
- Part of the MOORCO-BIG experiment (started 2005) to study tree colonisation, soil carbon dynamics, and the role of herbivores in moorland to woodland succession.
- Maintained by the James Hutton Institute; dataset authors/owners: Lorna Street, Tom Parker, Ruth Mitchell; maintainer: Lorna Street.

## Data structure and content
- File: 1 CSV containing data for both sites.
- Variables and units (examples):
  - Site (description: site name)
  - Species (description: tree species in plot)
  - Sample.ID (unique sample identifier)
  - Start.date / End.date (deployment window in dd-mmm-yy)
  - Mean.ingrowth.mg.C (fungal ingrowth; mg C per bag)
- Replication:
  - Glensaugh: n = 4 blocks
  - Ballogie: n = 3 blocks
- Reported values: mean fungal hyphal ingrowth per plot/bag.

## Methods and processing
- Hyphal in-growth method: sand-filled ingrowth bags (5 × 5 cm nylon mesh; 37 µm mesh; 18 g builders sand).
- Deployment: four points per plot; bags inserted at 45° angle with top below litter layer.
- Field period: 26 May 2021 to 9 Nov 2021.
- Laboratory processing: bags frozen after recovery, freeze-dried (72 h), 2.5 g sand per bag sonicated in DI water to extract hyphae, dried for 48 h, analyzed for carbon content with Flash Smart elemental analyser.
- Quality control: four blanks (not field-deployed) used to subtract average C content from samples.
- Output: mean ingrowth per plot after adjustment.

## Sites, treatments, and design
- Sites: Glensaugh (Grid: NO675801) and Ballogie (Grid: NO550930); Ballogie and Glensaugh specific coordinates provided; Invercauld mentioned in broader MOORCO BIG context but not in this dataset.
- Treatments and design within MOORCO BIG:
  - Grazing by large herbivores: unfenced vs fenced (grazing vs no grazing)
  - Within each plot: planting treatments including birch (Betula pubescens) and pine (Pinus sylvestris) at 1 m spacing, Heather control, low-density birch, and clumped birch (4 trees) at Glensaugh only
  - Replication: 4 blocks at Invercauld and Glensaugh; 3 blocks at Ballogie (per broader MOORCO BIG design)

## Data quality, governance, and access
- Maintainer: Lorna Street; contact: lstreet1@ed.ac.uk.
- Metadata provided for data provenance, measurement methods, and units.
- Data sharing and openness considerations align with the monitoring framework emphasis on transparent, well-documented datasets; however, explicit access restrictions are not stated in the record.
- Underlying data are tied to a long-term monitoring framework assessing mechanisms, rates of change, and herbivore influence in moorland-to-woodland succession.

## Context and relevance
- This dataset contributes to long-term environmental monitoring by providing a standardized measure of below-ground fungal activity (carbon content in hyphal ingrowth) across planted and control plots under different grazing regimes.
- Useful for evaluating how tree establishment and herbivory interact with soil microbial activity during early succession stages.