# This document described the lineage for each variable in both datasets.

## Overview
- Describes the lineage and measurement protocols for two Colombian Andes datasets: Tree Allometry and Leaf Traits.
- Focuses on quality control, data capture workflow, experimental design, and variable definitions.

## Quality control and data capture
- Each tree in every block plot is tagged with a unique ID; diameter at 2 cm above the base is marked to ensure consistent measurements.
- Data recorded using the Fulcrum app, a predesigned field data platform; new data stored in Fulcrum and later downloaded to Excel.
- Use of a predesign app is intended to reduce quality-control issues during transfer from field sheets.

## Experimental design and data collection timeline

- Allometry measurements
  - 360 trees per field site across four 600 m² plots with six blocks per plot.
  - Block 6 receives nutrient fertilisation (N, P, K and secondary/minor elements) monthly.
  - Each block includes one tree of each of the 15 study species (24 trees per species per site).
  - Study period: February 2019 to January 2022 with 10 measuring campaigns.
  - First census conducted at a nursery before planting at experimental sites.

- Leaf structural traits
  - 180 trees per field site; in each 600 m² plot, one tree per species across three blocks (total 12 trees per species).
  - Study period: June 2019 to January 2022 with five measuring campaigns.

## Datasets and key variables

- Tree Allometry dataset (Colombian Andes) - Table 1 lineage
  - Site: experimental locations; S1 (~14°C), S2 (~22°C), S3 (~26°C)
  - Plot: four plots per site
  - Block: six blocks per plot; Block 6 fertilised, Blocks 1–5 unfertilised
  - Id: tree identity
  - Species: 15 dominant species for the Colombian Andes
  - Date nursery: date of first census at nursery
  - Date_census number: census date
  - Total_height: height from base to top of tree
  - Height_to_first_branch: distance from base to first branch
  - Diameter: diameter at base 2 cm above soil; measurement methods include 150 mm digital caliper (<100 mm) or pro-tape for larger diameters
  - Canopy_min and canopy_max: minimum and maximum crown diameters
  - Total_leaf: leaves counted across censuses
  - Number_of_branches: branch count across censuses
  - Health_status_census: qualitative health status (e.g., disease, damage indicators)
  - Percentage_herbivore_census: percentage of leaf damage due to herbivores
  - Survival_census: alive, withering, or dead status

- Leaf traits dataset (Colombian Andes) - Table 2 lineage
  - Site, Plot, Block as above
  - Species: 15 dominant species
  - Date: census date
  - Diameter: base stem diameter with a permanent paint mark; measured with 150 mm caliper or ProTape
  - Leaf_area: projected leaf area (scanned leaves; leaf area computed with R package LeafArea)
  - Leaf_thickness: measured with a caliper (three measurements per leaf)
  - Dry_weight: leaf dry mass after drying at 70°C to constant weight
  - LMA: leaf mass per area (g m⁻²)
  - Total_leaves: leaves counted per tree across censuses
  - Number_of_branches: branch count per tree across censuses

## Data processing and metadata notes
- Measurements and units are documented per variable (e.g., mm, cm², g, g m⁻²).
- Data lineage links to specific measurement protocols and tools (e.g., Fulcrum app, calipers, ProTape, LeafArea package).