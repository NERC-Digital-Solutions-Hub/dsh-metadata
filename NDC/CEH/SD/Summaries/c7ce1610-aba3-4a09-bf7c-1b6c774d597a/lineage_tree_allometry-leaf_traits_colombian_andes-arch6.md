# Lineage for Dataset Tree Allometry and Dataset Leaf traits Colombian Andes

- The document details variable lineage, quality control, and data collection methods for two datasets from the Colombian Andes: Tree Allometry and Leaf Traits.
- It explains data capture workflows, measurement protocols, and the units/definitions used to track each variable, enabling traceability and re-use.

## Lineage for Dataset Tree Allometry Colombian Andes

- Study design and scope
  - Experimental locations: four plots per site, across multiple sites.
  - Four 600 m2 plots per site with six blocks within each plot.
  - Block 6: nutrient fertilisation treatment (monthly additions of N, P, K, and minor elements); blocks 1-5 without fertilisation.
  - 15 dominant tree species represented; 360 trees per site monitored; 10 measuring campaigns from Feb 2019 to Jan 2022.
  - Nursery phase: first census conducted at nursery before field planting; additional nursery data included.
- Data capture and quality control
  - Each tree tagged with a unique ID; diameter measured at 2 cm height with a fixed stem position.
  - Measurements recorded in Fulcrum app, a mobile data collection platform; data then downloaded to Excel.
  - Field protocols ensure consistency across measurements and reduce transfer QC issues.
- Variables and lineage (examples)
  - Total_height_field_census, Height_to_first_branch, Diameter_census, Canopy_min and max_census.
  - Health_status_census_number, Percentage_herbivore_census_number, Survival_census_number.
  - Table 1 (Tree Allometry) provides detailed lineage definitions, units (e.g., mm, as appropriate), and measurement rules (e.g., use of Digital Caliper for diameters <100 mm; ProTape for larger diameters).
- Timeframe and data collection details
  - 10 measuring campaigns across Feb 2019–Jan 2022.
  - Measurements include basal diameter, height metrics, crown dimensions, counts (leaves, branches), and survival status.
- Data usage and formatting
  - Raw measurements are tied to site, plot, block, tree ID, species, and census date.
  - Data are prepared for analysis via clearly defined units and measurement protocols to support downstream dashboards, reports, or self-serve analyses.

## Lineage for Dataset Leaf traits Colombian Andes

- Study design and scope
  - Experimental sites mirror the tree allometry design: four plots per site; six blocks per plot.
  - 15 dominant species sampled; 180 trees per site for leaf trait monitoring; data collected across three blocks per site.
  - Timeframe: five measuring campaigns from June 2019 to Jan 2022.
- Data capture and quality control
  - Leaves collected and processed across censuses; measurements include leaf area, leaf thickness, and dry weight.
  - Leaf area computed from scanned leaves using the LeafArea R package (run.ij).
  - Diameter at the base measured with a 150 mm digital caliper for small diameters; larger diameters measured with a Logger’s/Diameter ProTape.
- Variables and lineage (examples)
  - Diameter (mm); Leaf area (cm2); Leaf thickness (mm); Dry weight (g); LMA (g m-2); Total leaves; Number of branches.
  - Table 2 (Leaf traits) provides full definitions, units, and valid value ranges.
- Units and measurement definitions
  - Diameter: mm; Leaf area: cm2; Leaf thickness: mm; Dry weight: g; LMA: g/m2.
  - Total leaves and Number of branches captured per census per tree.
- Data processing and analysis readiness
  - Leaf area derived from scanned leaves using an established R workflow (LeafArea package).
  - Measurements linked to site, plot, block, tree ID, species, and census date for traceability.
- Timeframe and data collection details
  - Five campaigns between 2019 and 2022, covering multiple censuses and nutritional treatment blocks (fertilization status recorded per block).
  
- Overall data quality and accessibility notes
  - Both datasets emphasize consistent tagging, fixed measurement positions, and standardized procedures to ensure comparability across sites, blocks, species, and time.
  - Data captured via a mobile data collection platform (Fulcrum) and complemented with automated calculations (LeafArea) to facilitate data quality and reuse in dashboards, reports, and self-serve analyses.