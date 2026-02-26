# Lineage for Dataset Tree Allometry Colombian Andes and Dataset Leaf traits Colombian Andes

## Overview
- Describes the lineage (definitions, units, and data-handling rules) for variables in two datasets: Tree Allometry and Leaf Traits from the Colombian Andes.
- Data were collected and quality-controlled across multiple field sites and campaigns, with data captured via a mobile field app and stored for downstream analysis and GIS use.

## Study design and data collection
- Experimental layout
  - Field sites in the Colombian Andes, each with four plots.
  - Each plot contains six blocks; Block 6 is fertilized with nutrients (N, P, K, and secondary/minor elements).
  - 15 dominant species represented per site.
- Allometry dataset
  - 360 trees per site (four plots; six blocks), 24 trees per species per site.
  - Monitoring period: February 2019 to January 2022 across 10 measuring campaigns.
  - Nursery census prior to planting; tree measurements conducted after planting.
- Leaf traits dataset
  - 180 trees per site (four plots; three blocks per plot; one tree per species per block; total 12 trees per species per site).
  - Monitoring period: June 2019 to January 2022 across five measuring campaigns.
- Data capture
  - Field data recorded on Fulcrum (predesigned digital field forms) and downloaded into Excel for storage and processing.
  - A predesign app workflow aims to reduce transfer-related quality concerns.

## Quality control and data capture
- Quality control measures
  - Each tree assigned a unique ID; diameter measured at 2 cm above base and marked with permanent identifiers to ensure consistency across campaigns.
  - Measurements at fixed stem position to standardize post-field measurements.
- Data capture workflow
  - Field sheets → Fulcrum app → downloaded as Excel spreadsheets.
  - Predesign app intended to streamline data transfer and reduce errors.

## Dataset 1: Tree Allometry ( Colombian Andes )
- Key variables and lineage (examples)
  - Site, Plot, Block: experimental locations and structural units; Block 6 denotes nutrient fertilisation.
  - Id: tree identity number.
  - Species: 15 dominant species; detailed list provided.
  - Date nursery / Date census: census dates (day/month/year).
  - Total_height: height from stem base to tallest leaf (mm).
  - Height_to_first_branch: distance to first branch (mm).
  - Diameter: diameter at base 2 cm above stem (mm); measurement methods described (digital caliper or ProTape).
  - Canopy_min and canopy_max: crown diameter extents (mm).
  - Total_leaf: leaves per tree across censuses.
  - Number_of_branches: branches per tree across censuses.
  - Health_status_census: qualitative health indicators (fungal/herbivore/pathogen impacts, damage, nutrient status).
  - Percentage_herbivore_census: qualitative herbivory assessment (%).
  - Survival_census: alive/dead status.
- Data characteristics
  - Measurements spanned multiple campaigns; explicit variable definitions and units provided in Table 1.

## Dataset 2: Leaf Traits ( Colombian Andes )
- Key variables and lineage (examples)
  - Site, Plot, Block: experimental locations and blocks (Block 6 fertilised as in dataset 1).
  - Id: tree identity number.
  - Diameter: base diameter with permanent paint mark (mm).
  - Leaf_area: projected leaf area per tree (cm^2) calculated from scanned leaves using R (LeafArea package).
  - Leaf_thickness: leaf thickness measurements (mm) from three measurements per leaf.
  - Dry_Weight: oven-dried leaf mass (g) at 70°C until constant weight.
  - LMA: leaf mass per area (g/m^2), derived as leaf dry weight divided by leaf area.
  - Total_leaves: leaf count per tree per census.
  - Number_of_branches: branch count per tree per census.
- Data characteristics
  - Measurements aligned with censuses across five campaigns; detailed variable definitions and units provided in Table 2.

## Data lifecycle and accessibility
- Timeframe
  - Allometry: February 2019 – January 2022.
  - Leaves: June 2019 – January 2022.
- Documentation
  - Tables 1 and 2 provide the complete lineage (definitions, units, logical ranges) for all variables in their respective datasets.
- Data usability for GIS
  - Structured by Site, Plot, Block, and Id, enabling spatial joins with site coordinates and plot boundaries.
  - Species and census dates support temporal GIS analyses and species distribution mapping over time.
  - Units and data standards are specified, facilitating integration with other spatial/biophysical datasets.

## GIS relevance and integration notes
- Provenance and traceability
  - Clear lineage and measurement protocols enhance data quality and reproducibility for GIS analyses.
- Data harmonization
  - Consistent site/plot/block schema across both datasets supports joining with environmental rasters, site shapefiles, and management layers (e.g., fertilisation blocks).
- Practical considerations
  - Fertilisation treatment (Block 6) provides a controlled variable for spatial analyses of treatment effects.
  - Leaf trait calculations ( Leaf_area via leaf scans and R) enable remote-sensing validation and plant functional trait mapping.
- Constraints
  - Datasets are region-specific to the Colombian Andes; spatial coverage limited to experimental sites described.
  - Temporal resolution tied to predefined campaigns; continuous time series would require interpolation or supplemental data.