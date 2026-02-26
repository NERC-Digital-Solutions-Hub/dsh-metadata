# P2109 Baseline pH and Moisture Data from Sourhope Field Experiment

## Overview
- Dataset from the NERC Soil Biodiversity Thematic Programme (established 1999) focusing on soil biodiversity and ecological processes at the Sourhope Field Experiment site in the Scottish Borders.
- Geographic scope: Sourhope Farm, Sourhope, with site details for Blocks 1–5. Grid references provided (e.g., NT8545019630) and elevation around 304–315 m.
- Primary data: baseline soil pH measurements and soil moisture content collected across plot blocks and sub-plots, plus accompanying site and soil-profile metadata.
- Temporal coverage: baseline sampling events from 1999 onward (Mar/Sep 1999; Mar 2000; Mar 2001; Mar 2002, etc.), with sub-plot sampling in Apr 2000 and Jul 2003.

## Data Contents
- Baseline pH and moisture file: P2109_BASELINE_PH.csv
  - Columns include: SAMPLE_DATE, Description, TREATMENT, BLOCK, MAIN_PLOT, CELL_X, CELL_Y, SOIL_PH, MOISTURE.
  - Baseline pH readings for center-of-plot cores; moisture values available for Sep 1999 samples and calculated from fresh/dry weights.
- Sub-plot pH file: P2109_BASELINE_PHSUB.csv
  - Columns include: SUID, SAMPLE_DATE, TREATMENT, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SOIL_PH.
  - Sub-plot level pH measurements for finer spatial resolution within main plots.

## Sampling, Methods, and QA
- Baseline sampling: soil cores (about 5 cm diameter, 10 cm deep) taken from the centre of each experimental plot; cores stored in cold conditions for later pH measurement.
- Sub-plot sampling: ~20–30 g of soil from top 5 cm from two adjacent cells within each general sampling sub-plot (S–V) across main plots (excluding Control 2).
- pH measurement method (both baseline and sub-plot): use deionised water and standard calibration (pH 7 and 4 buffers); stepwise procedure described in the dataset documentation.
- Moisture determination: fresh weight recorded; samples oven-dried at 25°C to compute moisture content as 100*(fresh - dry)/dry.
- Quality assurance: numeric range checks, data formatting, and logical integrity checks conducted; however, NERC disclaims liability for data accuracy or fitness for a particular use.

## Data Structure and Schema
- Files:
  - P2109_BASELINE_PH.csv: baseline pH and moisture data
  - P2109_BASELINE_PHSUB.csv: sub-plot pH data
- Key fields (baseline PH): SAMPLE_DATE, Description, TREATMENT, BLOCK, MAIN_PLOT, CELL_X, CELL_Y, SOIL_PH, MOISTURE.
- Key fields (sub-plot PH): SUID, SAMPLE_DATE, TREATMENT, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SOIL_PH.
- Documentation notes: detailed column descriptions and data provenance are provided; external reference to the 2003 SOURHOPE FIELD DATA HANDBOOK available via the EIDC catalogue.

## Site Details and Soil Profiles (Blocks 1–5)
- Each block includes:
  - Site details: grid reference, altitude, slope, soil drainage, soil series, major soil subgroup, rock type, and base of profile information.
  - Detailed soil profiles for the block’s Rigg Foot soil, including horizon designations (e.g., LF, FH, H, A_h, AB, B, BCx, C), depths, and descriptive notes on colour, texture, structure, moisture, rooting, and presence of stones.
- This metadata supports spatial interpretation of soil properties and enables GIS-based mapping of soil horizons and characteristics across the Sourhope site.

## GIS and Practical Considerations
- Spatial identifiers: Blocks provide explicit grid references and cell coordinates (CELL_X, CELL_Y) enabling mapping of pH and moisture at sub-plot levels within main plots.
- Coordinate transformation: UK National Grid references (NT...) may require conversion to latitude/longitude for interfacing with some GIS platforms.
- Data integration: combine baselinePH with sub-plotPH to produce higher-resolution soil-property maps; join with block/site metadata for contextual mapping (e.g., soil drainage, texture, depth, and horizon features).
- Use cases: regional soil health mapping, spatial analysis of soil pH and moisture baselines, cross-plot comparisons, integration with ecological or biodiversity datasets from the same thematic program.

## References and Access
- Source: NERC Soil Biodiversity Thematic Programme background and Sourhope Field Data Handbook.
- Specific reference: Scott, R.; Bell, J.; Kenny, C.; Jeffers, J.; Buckland, S.; Burt-Smith, G. (2003). SOURHOPE FIELD DATA HANDBOOK 2003. Available via the EIDC catalogue record.