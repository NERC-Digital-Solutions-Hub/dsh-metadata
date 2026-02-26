# Dataset Title: Fungal hyphal in-growth at the Glensaugh and Ballogie MOORCO 'BIG' experimental tree planting sites.

## Overview
- Dataset contains 1 CSV file with data for both Glensaugh and Ballogie MOORCO 'BIG' experimental sites.
- 20 records total; data represent mean fungal hyphal ingrowth per bag/plot.
- Part of the MOORCO-BIG experiment, an experimental tree-planting study on heather moorland in NE Scotland.
- Replication: 4 blocks at Glensaugh; 3 blocks at Ballogie.
- Field period: 26 May 2021 to 9 Nov 2021; blanks processed in the lab and subtracted from samples.
- Maintained by Lorna Street; Authors: Lorna Street, Tom Parker, Ruth Mitchell; Contact: lstreet1@ed.ac.uk.
- Period of record not specified.

## Data structure and contents
- Data structure: 1 CSV file containing data for both sites.
- Key fields (variables) include:
  - Site, Description: Site name; Site Units: none; Missing value code: NA.
  - Species, Description: Tree species in plot; Species Units: none; Missing value code: NA.
  - Sample.ID, Description: Unique sample identifier; Sample.ID Units: none; Missing value code: NA.
  - Start.date, Description: Start of bag deployment (dd-mmm-yy); End.date, Description: End of bag deployment (dd-mmm-yy); Missing value code: NA.
  - Mean.ingrowth.mg.C, Description: Fungal ingrowth; Units: mg C per bag; Missing value code: NA.
- Data are reported as means per plot.

## Data provenance and governance
- Authors/owners: Lorna Street, Tom Parker, Ruth Mitchell.
- Maintainer: Lorna Street.
- Contact: lstreet1@ed.ac.uk.
- Period of record: not specified.
- Background context: Part of the MOORCO BIG experiment, which investigates moorland to woodland succession and the role of herbivores; Big experiment sites include Ballogie, Invercauld, and Glensaugh.
- Data processing/QA notes: Hyphal in-growth quantified via sand-filled ingrowth bags; correction for blank samples by subtracting mean C content from four blanks; means reported per plot.

## Methods and dataset context
- Hyphal in-growth method:
  - 5 x 5 cm nylon mesh bags with 37 µm mesh.
  - Bags filled with 18 g builders sand; wetted before deployment.
  - Deployed at four points per plot, bag orientation at 45° with top just below litter layer.
  - Bags remained in field 26 May 2021 – 9 Nov 2021; blanks handled in lab.
  - Post-recovery: bags freeze-dried; 2.5 g sand from each bag sonicated in 40 ml deionised water for 10 min to release hyphae.
  - Hyphae analyzed for C content via Flash Smart elemental analyzer; four blank samples subtracted from all samples.
- Reported values are the mean ingrowth for each plot.

## Variables and units (definitions)
- Site, Description: Site name (Glensaugh or Ballogie); Site, Units: none; Site, Missing value code: NA.
- Species, Description: Tree species in plot; Species, Units: none; Species, Missing value code: NA.
- Sample.ID, Description: Unique sample ID; Sample.ID, Units: none; Sample.ID, Missing value code: NA.
- Start.date, Description: Start date of bag deployment; Start.date, Units: dd-mmm-yy; Start.date, Missing value code: NA.
- End.date, Description: End date of bag deployment; End.date, Units: dd-mmm-yy; End.date, Missing value code: NA.
- Mean.ingrowth.mg.C, Description: Fungal ingrowth; Units: Mg C per bag; Mean.ingrowth.mg.C, Missing value code: NA.

## Site and treatment context (MOORCO BIG background)
- The BIG experiment spans three sites: Ballogie, Invercauld, Glensaugh.
- Treatments within blocks include grazing vs. fenced (grazing by large herbivores), and within fences/unfenced plots:
  - Planted birch (1 m spacing)
  - Planted pine (1 m spacing)
  - Heather control
  - Low-density birch
  - Clumped birch (only at Glensaugh)
- Replication: 4 blocks at Invercauld and Glensaugh; 3 blocks at Ballogie.

## Data governance considerations for reuse
- Metadata should link to MOORCO BIG project context and individual site coordinates:
  - Glensaugh: NO675801
  - Invercauld: NO170950
  - Ballogie: NO550930
- Ensure consistency with other MOORCO BIG data (standardized field names, units, and date formats).
- Document any data updates or corrections to maintain an auditable data lineage.
- Clarify any data sharing restrictions, embargoes, or proprietary issues identified in broader MOORCO governance.