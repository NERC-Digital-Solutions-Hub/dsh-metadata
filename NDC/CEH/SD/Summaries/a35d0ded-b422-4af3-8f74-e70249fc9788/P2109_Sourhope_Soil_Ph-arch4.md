# NERC Soil Biodiversity Thematic Programme Sourhope Field Data Description

## Overview and Aims
- Document describes soil pH baseline and related data from the Sourhope Field Experiment (Scott et al., 2003).
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) aimed at understanding soil biota diversity and functional ecological roles.
- Focuses on baseline measurements (pH, moisture) across multiple blocks/plots to characterise soil properties and their variation.

## Data Collected and Measurements
- Baseline soil pH values collected on multiple sampling occasions (Mar/Sep 1999, Mar 2000, Mar/Oct 2001, Mar 2002) and moisture content calculated for Sep 1999 samples.
- Two sampling schemes:
  - Baseline sampling: 5 cm diameter, 10 cm deep soil cores from the centre of each experimental plot.
  - Sub-plot sampling: ~20–30 g from top 5 cm from two adjacent cells within each main plot (excluding Control 2 plots).
- Primary data types:
  - Baseline soil pH (wet pH using deionised water).
  - Soil moisture content (fresh vs dry weight).
- Data are presented in two CSV files (see Data Structure).

## Data Files and Structure
- P2109_BASELINE_PH.csv
  - Key columns: SAMPLE_DATE, Description, TREATMENT, BLOCK, MAIN_PLOT, CELL_X, CELL_Y, SOIL_PH, MOISTURE.
- P2109_BASELINE_PHSUB.csv
  - Key columns: SUID, SAMPLE_DATE, TREATMENT, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SOIL_PH.
- Datasets include descriptive metadata for each field (block, plot, sub-plot, grid coordinates, etc.).
- Data source referenced: Sourhope Field Data Handbook (Scott et al., 2003); available via EIDC catalogue.

## Methods and Quality Control
- pH measurement protocol:
  - Mix ~10 cm3 soil with ~40 ml deionised water, shake, settle, calibrate with buffers (pH 7 and 4), measure pH after equilibration.
  - Adjusted in March 2000 with a different soil-to-water ratio (20–30 g soil to 40 ml water).
- Soil moisture content calculation: 100 * (fresh weight - dry weight) / dry weight after oven-drying.
- Quality control:
  - Numeric range checks, formatting checks, and logical integrity checks.
  - NERC provides data but does not warrant accuracy or fitness for any particular use; no liability for data use.

## Site Details and Soil Profiles (Blocks 1–5)
- Each block provides site-level details and complete soil profile descriptions.
- Common attributes per block:
  - Grid reference, altitude, slope, drainage, soil series (SH 74711 or SH 74714), parent material, major soil subgroup, rock type.
- Depth intervals and horizons described (e.g., LF, FH, H, Ah, AB, B, BCx, C, etc.) with:
  - Depths (cm), soil description, matrix colour, structure, moisture, root presence, and stones.
- Blocks cover variations in soil type and profile development, including Brown forest soils, gleyed variants, and mineralogical differences.
- Example detail themes:
  - Horizons showing organic-rich surface layers (fibrous roots, moist conditions).
  - Transition horizons with changes in texture (sandy silt loam to loamy sand) and mottling.
  - Occasional indicators of stones/rock fragments and subangular/platy structures.

## Access, Provenance, and Usage Notes
- Data tied to the NERC Soil Biodiversity Programme and Sourhope Field Data Handbook (2003).
- Primary provenance: R. Scott, J. Bell, C. Kenny, J. Jeffers, S. Buckland and G. Burt-Smith; Sourhope Field Data Handbook 2003.
- Availability and reuse considerations:
  - Data are provided with QA processes but accuracy is not warranted by NERC.
  - Usage should acknowledge source and data copyright; consult the cited handbook for fuller methodological context.
- Relevance for data leadership:
  - Illustrates the importance of detailed metadata, horizon-level observations, and consistent data structure for multi-block field experiments.
  - Highlights need for clear data standards and discoverability when aggregating across sites and time.

## Constraints, Gaps, and Considerations for Data Leaders
- Data are geographically focused on Sourhope with multi-block variation; cross-site comparability requires standardized metadata.
- Data are historical (dates up to 2003) and may require harmonisation with newer datasets for longitudinal analyses.
- Metadata clarity is strong for pH and moisture but horizon-level soil descriptions are block-specific and may require cross-walking to standard soil taxonomies.
- Access to full methodological context relies on the Sourhope Field Data Handbook; ensure citation and linkage for reproducibility.

## Potential Uses and Implications
- Baseline characterization of soil chemistry and moisture across a field experimental setup.
- Cross-block comparisons of pH and moisture responses to treatments and plots.
- Integration with broader soil biodiversity data to examine how pH, moisture, and soil structure relate to soil biological communities.
- A case study in data governance: demonstrates comprehensive data structure (two CSV files), explicit QC steps, and clear provenance notes for a long-running field program.