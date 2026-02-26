# Lineage for Dataset Tree Allometry and Leaf Traits Colombian Andes

## Overview
- Describes lineage and quality control for two datasets: Tree Allometry and Leaf Traits from the Colombian Andes.
- Covers experimental design (sites, plots, blocks), measurement protocols, variable definitions, units, and data capture/storage workflow.

## Quality control
- Each tree is assigned a unique ID; diameter is measured at 2 cm above the base and marked permanently to ensure consistent sampling across censuses.
- Data recorded via the Fulcrum mobile app; data are stored in Fulcrum and downloaded into Excel, reducing quality-control issues during transfer from field sheets.

## Data collection and experimental design

- Allometry dataset
  - 360 trees per field site; four 600 m2 plots with six blocks per plot.
  - Block 6 is fertilized (monthly additions of N, P, K and secondary/minor elements).
  - 15 study species; 24 trees per species per site (total 24 × 15 per site).
  - Monitoring period: February 2019 to January 2022 across 10 measuring campaigns.
  - First census conducted at a nursery before field planting; Table 1 outlines the variable lineage and methods.

- Leaf traits dataset
  - 180 trees per field site; in each 600 m2 plot, one tree per species in three blocks (total 12 trees per species).
  - 15 species; five measuring campaigns from June 2019 to January 2022.
  - Table 2 details the variable lineage and methods.

## Variables and lineage (Key variables)

- Tree Allometry (Table 1)
  - Site, Plot, Block, Tree ID, Species
  - Date nursery; Date census
  - Total height (mm)
  - Height to first branch (mm)
  - Diameter (mm) at a permanent paint-marked base
  - Canopy min and max diameter (mm)
  - Total leaves; Number of branches
  - Health status census; Percentage herbivore damage
  - Survival (live, withering, or dead)

- Leaf Traits (Table 2)
  - Site, Species; Date; Plot; Block
  - Diameter (mm) at base
  - Leaf area (cm2)
  - Leaf thickness (mm)
  - Dry weight (g)
  - Leaf mass per area (LMA, g m-2)
  - Total leaves; Number of branches

## Data details and definitions

- Site and plot structure: Site (experimental locations), Plot (four plots per site), Block (six blocks per plot; Block 6 fertilized)
- Species: 15 dominant species from the Colombian Andes
- Dates: Nursery census date; census date
- Measurements and instruments
  - Diameter measured with a digital caliper (up to 150 mm for small diameters); larger diameters measured with Logger's/Diameter ProTape
  - Leaf area derived from scanned leaves using the LeafArea package in R
  - Leaf thickness measured with a caliper; dry weight measured after oven-drying at 70°C
- Units and ranges: Explicitly defined (e.g., mm, cm2, g, %, etc.); positive value constraints for relevant fields
- Data provenance: Measurements tied to specific censuses and blocks; permanent marks and fixed measurement positions support reproducibility

## Governance and stewardship considerations

- Clear data lineage with explicit variable definitions, units, and measurement methods to support reproducibility, discovery, and auditing.
- Standardized metadata for sites, plots, blocks, and species to facilitate data sharing and interoperability across systems.
- Data capture via a centralized platform (Fulcrum) enhances traceability from field collection to digital storage, aiding data governance and update processes.
- Documentation supports data sharing readiness and potential catalogue deposition, while ensuring traceable provenance and measurement consistency across campaigns.