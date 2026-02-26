# Lineage for Dataset Tree Allometry Colombian Andes and Dataset Leaf traits Colombian Andes

## Overview
- Document describes the lineage for variables in two datasets (Tree Allometry and Leaf Traits) and outlines quality control, data capture, and data structure to enable traceability and reproducibility.

## Study Design and Data Collection

- Allometry dataset
  - 360 trees per field site, across four 600 m² plots with six blocks per plot.
  - Six blocks per plot; Block 6 = fertilised with nutrients (monthly N, P, K and secondary/minor elements).
  - 15 study species; 24 trees per species per site.
  - Data collection: February 2019 to January 2022; 10 measuring campaigns.
  - Initial census conducted at a mid-elevation nursery before planting.
- Leaf traits dataset
  - 180 trees per field site; four plots per site; three blocks per plot; 15 species; 12 trees per species.
  - Data collection: June 2019 to January 2022; five measuring campaigns.
- Data capture and storage
  - Field data captured using Fulcrum app (digital predesign field data collection).
  - New data stored in Fulcrum and downloaded to Excel spreadsheets.
  - Use of a predesign app intended to reduce quality control issues during transfer from field sheets.

## Variables and Lineage

- Tree Allometry (Table 1)
  - Core identifiers: Site, Plot, Block, Tree ID, Species, Date nursery, Date census number.
  - Measurements and traits: Total height, height to first branch, diameter (measured at 2 cm above base), canopy min/max, total leaves, number of branches, health status, percentage herbivore damage, and survival status.
  - Data structure includes explicit codings for Site, Plot, Block, and Species, with defined logical ranges and units.
- Leaf Traits (Table 2)
  - Core identifiers: Site, Species, Date, Plot, Block, Tree ID.
  - Measurements and traits: Diameter, leaf area, leaf thickness, dry weight, leaf mass per area (LMA), total leaves, and number of branches.
  - Leaf area calculated from scanned leaves using the LeafArea package in R.
  - Diameter measurement specifics: 150 mm caliper for small diameters; larger trees measured with a pro tape; permanent paint mark at base for reference.
  
## Measurement Methods and Standards

- Diameter
  - Measured at a fixed position on the stem (2 cm height) for allometry data; precision using 150 mm digital caliper or pro tape.
- Leaf Area
  - Leaves scanned; area computed via R (LeafArea package).
- Leaf Thickness
  - Measured with a caliper; three measurements per leaf.
- Dry Weight
  - Leaves dried in an oven at 70°C until constant weight.
- Other traits
  - Height and branching metrics captured for structural trait analysis.
- Data quality controls
  - Trees tagged with unique numerical codes; diameter position standardized to a fixed stem position to ensure consistency across measurements.
  - Data captured via a digital tool to enhance accuracy and traceability.

## Temporal Scope and Sampling Campaigns

- Tree Allometry: 10 measuring campaigns between February 2019 and January 2022.
- Leaf Traits: 5 measuring campaigns between June 2019 and January 2022.
- Nursery phase and initial germination documented before field planting.

## Data Management and Governance

- Data are organized with explicit metadata and variable lineage, including site, plot, block, and species-level definitions and ranges.
- Data are stored in a centralized digital platform (Fulcrum) with downstream export to Excel, enabling documentation of provenance and reproducibility.
- Clear provenance is provided for each variable, including measurement techniques, units, and logical ranges.
- While the document demonstrates good lineage and metadata for monitoring purposes, it also implicitly highlights common governance considerations (data sharing readiness, metadata completeness, and data transformation needs) relevant to monitoring framework authors.

## Relevance for Monitoring Frameworks

- Illustrates end-to-end data lineage from experimental design to variable definitions and measurement methods, supporting traceability and accountability.
- Demonstrates practical quality control practices (unique IDs, fixed measurement positions, digital data capture) that enhance data reliability for monitoring.
- Highlights the importance of comprehensive metadata (definitions, units, logical ranges) to enable reuse and integration into broader health and environmental monitoring frameworks.
- Addresses typical governance challenges relevant to monitoring frameworks, such as data accessibility, metadata adequacy, data transformation requirements, and clear data-sharing considerations.