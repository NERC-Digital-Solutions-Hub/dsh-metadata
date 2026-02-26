# Lineage for Dataset Tree Allometry and Dataset Leaf Traits Colombian Andes

## Scope and purpose
- Document describes the variable lineage for two datasets: Tree Allometry and Leaf Traits in the Colombian Andes.
- Aims to support standardized environmental monitoring data: clear variable definitions, units, measurement methods, and quality assurance for temporal comparisons.

## Data collection design and quality assurance

- Quality control
  - Each block plot’s trees tagged with unique IDs; diameter at 2 cm above base marked to ensure consistent posterior measurements.
  - Data captured in Fulcrum app; new data stored on the platform and downloaded to Excel; predesign app helps reduce QA issues during transfer.

- Allometry measurements
  - 360 trees per field site, across four 600 m2 plots with six blocks per plot.
  - Block 6 provides monthly nutrient fertilisation (N, P, K + secondary/minor elements); blocks 1–5 unfertilised.
  - Each block contains one tree of each of the 15 species (24 trees per species per site).
  - Timeframe: February 2019 to January 2022; 10 measuring campaigns.
  - First census conducted at a mid-elevation nursery before planting; Table 1 details variable methodologies.

- Leaf structural traits
  - 180 trees per field site; one tree per species per block within each 600 m2 plot, across three blocks (total 12 trees per species per site).
  - Timeframe: June 2019 to January 2022; five measuring campaigns.
  - Table 2 details variable methodologies.

## Datasets and variable lineage

- Tree Allometry (Table 1)
  - Key fields: Site, Plot, Block, Id, Species, Date nursery, Date_census_number, Total_height, Height_to_first_branch, Diameter, Canopy_min, Canopy_max, Total_leaf, Number_of_branches, Health_status_census, Percentage_herbivore_census, Survival_census.
  - Units and logical ranges defined (e.g., height in mm, diameter in mm, percentages for herbivory, survival categories).

- Leaf Traits (Table 2)
  - Key fields: Site, Plot, Block, Id, Species, Date, Diameter, Leaf_area, Leaf_thickness, Dry_Weight, LMA, Total_leaves, Number_of_branches.
  - Leaf_area derived from scanned leaves using the LeafArea R package; Diameter measured with digital caliper or ProTape depending on size.
  - Units and logical ranges defined (e.g., Leaf_area in cm2, Leaf_thickness in mm, Dry_Weight in g, LMA in g/m2).

## Site, plot, block, and species context

- Site definitions
  - S1 = 14°C, S2 = 22°C, S3 = 26°C.
- Plot structure
  - Four plots per site.
- Block treatment
  - Blocks 1–5: no fertilisation; Block 6: fertilised.
- Species
  - 15 dominant Colombian Andes species listed in the dataset documentation (specific names provided in tables).
- Census timing
  - Allometry: 10 campaigns; Leaf traits: 5 campaigns.
  - Nursery census conducted prior to field planting.

## Data management and accessibility

- Data are stored in Fulcrum and can be exported to Excel for analysis.
- Variable definitions and data lineage are explicitly documented (Tables 1 and 2) to support reproducibility, cross-site comparisons, and potential data sharing.