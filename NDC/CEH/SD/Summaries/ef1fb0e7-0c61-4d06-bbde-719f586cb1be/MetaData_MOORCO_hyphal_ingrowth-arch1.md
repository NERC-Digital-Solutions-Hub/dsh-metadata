# Dataset Title: Fungal hyphal in-growth at the Glensaugh and Ballogie MOORCO 'BIG' experimental tree planting sites.

## At a glance
- 1 CSV file containing data for both Glensaugh and Ballogie MOORCO BIG sites
- 20 records
- Authors/maintainers: Lorna Street, Tom Parker, Ruth Mitchell; maintainer: Lorna Street
- Contact: lstreet1@ed.ac.uk
- Focus: Fungal hyphal production in sand-filled ingrowth bags over a growing season

## What the data cover
- Fungal hyphal in-growth into sand bags deployed at two fenced experimental tree-planting sites (Glensaugh and Ballogie) on heather moorland in NE Scotland
- Part of the MOORCO-BIG experiment, established 2005, examining mechanisms, rates of change, and herbivore roles during moorland-to-woodland succession

## Experimental context
- Sites and design
  - Glensaugh and Ballogie (Ballogie site replicates at n = 3; Glensaugh n = 4; temporal and spatial replication aligned with MOORCO BIG)
  - Treatments within blocks: grazing by large herbivores (unfenced) vs no grazing (fenced)
  - Within each fenced/unfenced plot: planted birch (Betula pubescens) and/or pine (Pinus sylvestris) at 1 m spacing, plus heather control; additional variations at Glensaugh include low-density birch and clumped birch
  - The BIG experiment spans three sites overall (Ballogie, Invercauld, Glensaugh); Ballogie included in this dataset
- Temporal scope
  - Bags deployed during May–Nov 2021
  - Field-to-lab processing occurred after retrieval, with blanks processed concurrently

## How the data were collected and processed
- Hyphal in-growth measurement
  - 5 × 5 cm nylon mesh ingrowth bags with 37 μm mesh
  - Bags filled with 18 g builders sand
  - Deployed at four points within each plot; inserted at 45° angle with top beneath litter layer
  - Pre-insertion wetting for uniform sand depth
  - Bags remained in the field 26 May 2021 – 9 Nov 2021; blanks kept in lab for same period
  - Recovery, freeze-drying (72 h), and processing
  - 2.5 g of sand from each bag sonicated in 40 ml deionised water to release hyphae
  - Hyphae analyzed for carbon content (mg C per bag) via Flash Smart elemental analyzer
  - Four blanks (not deployed in the field) processed and their average C subtracted from all samples
- Output
  - Reported value: mean ingrowth for each plot (Mean.ingrowth.mg.C)

## Variables and units
- Site: Site name (Glensaugh or Ballogie)
- Description: Site details; Site, Units = none
- Species: Tree species in plot (e.g., Betula pubescens, Pinus sylvestris)
- Sample.ID: Unique sample identifier
- Start.date: Start of bag deployment (dd-mmm-yy)
- End.date: End of bag deployment (dd-mmm-yy)
- Mean.ingrowth.mg.C: Fungal ingrowth (milligrams of C per bag)

## Data quality and notes
- Data structure: 1 CSV file with data for both sites
- Records: 20
- Missing value code: NA
- Important processing note: Blank subtraction to correct for background carbon
- Metadata completeness: Key metadata provided (sites, treatments, replication, deployment window); additional site coordinates or broader environmental covariates not included in this dataset

## Potential uses for analysts
- Compare fungal hyphal in-growth across sites (Glensaugh vs Ballogie) and treatments (grazed vs fenced; birch vs pine vs control)
- Examine effect of tree planting treatments on below-ground fungal activity during early succession
- Integrate with other MOORCO BIG data (e.g., CO2, DOC, soil carbon dynamics) to model ecosystem-wide succession processes
- Assess scale considerations and data limitations (small sample size, limited records) when drawing inferences
- Reproduce or extend analyses by linking to study metadata (replication blocks, site coordinates, and broader MOORCO BIG design)

## Provenance and contact
- Data owners/authors: Lorna Street, Tom Parker, Ruth Mitchell
- Maintainer: Lorna Street
- Contact email: lstreet1@ed.ac.uk
- Context: Background on the MOORCO BIG experiment and its role in studying moorland-to-woodland succession and herbivore impacts