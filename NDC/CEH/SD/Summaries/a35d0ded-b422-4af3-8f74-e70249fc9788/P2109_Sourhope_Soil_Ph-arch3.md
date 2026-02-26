# SOURHOPE FIELD DATA HANDBOOK 2003

## Aim and scope
- Document the baseline soil health measurements and extensive soil profiling from the NERC Soil Biodiversity Thematic Programme at Sourhope (Macaulay/Sourhope Field Experiment).
- Focus on understanding soil biodiversity, functional roles of soil biota, and associated ecological processes via detailed, multi-project data collection.

## What the data cover
- Baseline soil pH measurements (pH) and soil moisture (Moisture) across multiple blocks and plots.
- Two related CSV datasets:
  - P2109_BASELINE_PH.csv: baseline pH readings and moisture by date, block, main plot, cell coordinates, and treatment.
  - P2109_BASELINE_PHSUB.csv: sub-plot baseline pH readings (SUID, sub-plot, block, main plot, treatment, cell coordinates) and pH.
- Associated methodological and sampling metadata, plus extensive soil profile descriptions for Rigg Foot, Sourhope across blocks 1–5.

## Sampling design and sampling dates
- Baseline sampling conducted on multiple occasions: Mar/Sep 1999, Mar 2000, Mar 2001, Oct 2001, Mar 2002.
- Baseline sampling scope:
  - Central soil cores (5 cm diameter, 10 cm deep) per main plot; sub-plot samples (top 5 cm, ~20–30 g) for pH.
  - Blocks 1–5, main plots A–F, and sub-plots S, T, U, V (except Control 2 plots).
- Sub-plot sampling covers S T U V within each main plot.

## Methods and data collection
- Soil pH measurement:
  - Use around 10 cm3 soil, mix with de-ionised water to about 40 ml (or 20–40 ml in later sampling), let equilibrate, and measure pH with calibrated electrode.
  - Calibration with buffers around pH 7 and pH 4; adjust soil-to-water ratio as sampling date varied.
- Soil moisture determination:
  - Record fresh weight of each sample.
  - Oven-dry at 25°C and record dry weight.
  - Moisture content = 100 × (fresh − dry) / dry.
- Sample handling:
  - Baseline cores stored cold; pH readings taken later.
  - Some samples oven-dried in 1999 for moisture calculation.

## Data structure and metadata
- P2109_BASELINE_PH.csv fields include:
  - SAMPLE_DATE, TREATMENT, BLOCK, MAIN_PLOT, CELL_X, CELL_Y, SOIL_PH, MOISTURE.
- P2109_BASELINE_PHSUB.csv fields include:
  - SUID, SAMPLE_DATE, TREATMENT, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SOIL_PH.
- Data formats and column descriptions align with the Sourhope Field Data Handbook conventions (Scott et al., 2003).

## Quality control and data governance
- Quality control procedures include numeric range checks, formatting conformity, and logical integrity checks.
- Data provided with quality assurance steps; however, NERC disclaims warranty of accuracy and suitability for specific uses and takes no liability for data use.
- Emphasis on metadata completeness and data provenance to support data sharing and reuse.

## Site details and soil profile data
- Five blocks (1–5) at Sourhope (Rigg Foot and associated sites) with detailed site descriptors:
  - Grid references, altitudes (approximately 304–315 m), slope, drainage (ranging from Free to Imperfect), soil subgroups (predominantly Brown Forest Soil with varying gleying), and bedrock/parent material (andesite and related igneous materials).
- Detailed soil profile descriptions for Rigg Foot across blocks 1–5, including horizon names (LF, FH, H, Ah, AB, B, BCx, C, etc.), depths, textures, colors, structure, moisture status, roots, and presence of stones.
- Block-specific notes indicate variability in drainage, moisture, and horizon development, illustrating diverse soil conditions within the Sourhope field experiment.

## Relevance for monitoring frameworks
- Demonstrates a structured approach to baseline environmental health measurement: clearly defined sampling design, standardized field and lab methods, and explicit data schemas.
- Highlights metadata needs, data governance considerations, and openness versus barriers to data sharing, relevant to monitoring framework authors.
- Provides a concrete example of long-term soil health monitoring, with attention to methodological consistency over time and across sub-sampling units, plus rich site characterization data.

## Reference
- Scott, R.; Bell, J.; Kenny, C.; Jeffers, J.; Buckland, S.; Burt-Smith, G. (2003). SOURHOPE FIELD DATA HANDBOOK 2003. Available as Supporting Information via EIDC catalogue record.