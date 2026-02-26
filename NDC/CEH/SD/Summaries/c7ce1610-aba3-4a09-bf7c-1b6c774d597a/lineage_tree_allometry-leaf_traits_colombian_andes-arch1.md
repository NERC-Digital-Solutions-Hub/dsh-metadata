# Lineage for Dataset Tree Allometry and Leaf Traits Colombian Andes

## Overview
- Describes the lineage (variable definitions and data structure) for two datasets: Tree Allometry and Leaf Traits from the Colombian Andes.
- Focuses on measurement methods, experimental design, and data variables to enable traceability and reuse.

## Study design and field setup
- Experimental locations: four plots per site (600 m² each) across multiple blocks; six blocks per plot.
- Species: 15 dominant tree species in the Colombian Andes.
- Allometry dataset: 360 trees per site (one tree of each species per block) across four plots; total of 24 trees per species per site.
- Leaf traits dataset: 180 trees per site (one tree per species per block) across four plots; total of 12 trees per species per site.
- Fertilisation treatment: Block 6 receives monthly application of N, P, K and minor elements; Blocks 1–5 are unfertilized (nutrient treatment structure).

## Timeframe and campaigns
- Allometry: February 2019 to January 2022, with 10 measuring campaigns.
- Nursery phase: initial census at nursery before field planting.
- Leaf traits: June 2019 to January 2022, with five measuring campaigns.

## Data capture and storage
- Field data recorded with the Fulcrum app (digital predesigned data collection platform); data exported to Excel.
- Quality control in the field: each tree tagged with a unique code; diameter measured at 2 cm above the base and marked to ensure consistent stem position across measurements.
- Fulcrum reduces quality-control steps during field-to-digital transfer.

## Variables and lineage structure (Tree Allometry)
- Site: Experimental location; Site values correspond to conditions (e.g., S1, S2, S3 with defined temperatures).
- Plot: Four plots per site (1–4).
- Block: Six blocks per plot; Block 6 is fertilized, Blocks 1–5 are unfertilized.
- Id: Unique tree identifier.
- Species: 15 dominant species (list includes Andesanthus lepidotus, Chrysochlamys colombiana, Clethra fagifolia, Clusia spp., Guatteria lehmannii, Hieronyma antioquensis, Ilex laurina, Inga spp., Miconia theizans, Quercus humboldtii, Weinmannia pubescens, among others).
- Date nursery / Date census: Dates for nursery census and each field census.
- Measurements (per census): Total_height, Height_to_first_branch, Diameter (permanent paint mark, measured with digital caliper or pro tape), Canopy_min and max (crown diameter range), Total_leaf, Number_of_branches, Health_status, Percentage_herbivore, Survival_status.
- Measurement specifics: Diameter measured at a fixed stem position; instruments include a 150 mm digital caliper or pro tape, with a permanent paint mark to maintain consistency across censuses.
- Data granularity: Measurements across up to 10 campaigns (allometry).

## Variables and lineage structure (Leaf traits)
- Site and Plot definitions mirror the tree allometry dataset (four plots per site; six blocks per plot; Block 6 fertilized).
- Id: Tree identifier.
- Diameter: Base stem diameter with a permanent paint mark; measured with 150 mm digital caliper for small diameters or pro tape for larger stems.
- Leaf_area: Projected leaf area per tree, derived by scanning leaves and calculating total area using the LeafArea package in R.
- Leaf_thickness: Leaf thickness measured with caliper (three measurements per leaf).
- Dry_Weight: Oven-dried leaf biomass (70°C until constant weight).
- LMA: Leaf mass per area (dry weight divided by leaf area).
- Total_leaves: Leaf count per tree across census events.
- Number_of_branches: Branch count per tree across four censuses.
- Variables are defined to capture structural and morphological leaf traits across species and treatments.

## Data quality and metadata
- Each dataset includes explicit variable lineage, definitions, units, and plausible value ranges.
- Temperature and site-related context (S1–S3 with defined temperature ranges) are included to frame environmental conditions.
- Metadata and documentation support reuse and reproducibility, with clear links between field methods and recorded variables.

## Accessibility and notes
- Data are organized to support cross-dataset analyses (tree allometry vs. leaf traits) with consistent site/plot/block structure.
- The documentation emphasizes traceability from field collection to variable definitions, enabling reproducible analyses and model development.