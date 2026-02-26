# Background

- The NERC Soil Biodiversity Thematic Programme (established 1999) focused on intensive study at Sourhope Field Experiment to understand soil biota diversity and the functional roles of soil organisms in ecological processes, complementing broader monitoring of aboveground productivity and diversity.
- Twenty-four projects investigated soil structure, processes (e.g., carbon and nitrogen cycles), and roles of micro-, meso-, and macro-fauna and flora across the experimental plots.

## Datasets and measurements

- Baseline soil pH data are collected from Sourhope across multiple sampling occasions and sub-plots.
- Primary datasets described:
  - P2109_BASELINE_PH.csv: baseline soil pH readings with associated metadata.
  - P2109_BASELINE_PHSUB.csv: baseline pH readings at sub-plot level with sub-plot metadata and moisture data.
- P2109_BASELINE_PH.csv includes: SAMPLE_DATE, TREATMENT, BLOCK, MAIN_PLOT, CELL_X, CELL_Y, SOIL_PH, MOISTURE.
- P2109_BASELINE_PHSUB.csv includes: SUID, SAMPLE_DATE, TREATMENT, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SOIL_PH.
- Data provenance references: Scott et al., 2003; Sourhope Field Data Handbook 2003, available via the EIDC catalogue.

## Sampling and methods

- Baseline sampling dates for pH: March and September 1999, March 2000, March 2001, March 2002.
- Additional baseline sampling: Mar 1998 (pre-experiment) for baseline pH context; moisture measured in Sep 1999.
- Sub-plot sampling: April 2000 and July 2003 (within all general sampling sub-plots except Control 2 plots).
- pH measurement method (wet pH in deionised water):
  - Roughly 10 cm3 soil from the core, mixed with ~40 ml (or 20–30 g soil with ~20 ml water in later method).
  - Equilibrate 5 minutes, calibrate meter with pH 7 and 4 buffers, read pH.
- Moisture content method:
  - Measure fresh weight, oven-dry at 25°C, measure dry weight.
  - Moisture content = 100 * (fresh - dry) / dry weight.

## Data structure and contents

- Two CSV data structures:
  - Baseline pH: P2109_BASELINE_PH.csv
    - Columns: SAMPLE_DATE, Description, SAMPLE_DATE Units, TREATMENT, BLOCK, MAIN_PLOT, CELL_X, CELL_Y, SOIL_PH, MOISTURE.
  - Baseline sub-plot pH: P2109_BASELINE_PHSUB.csv
    - Columns: SUID, Description, SAMPLE_DATE, TREATMENT, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SOIL_PH.
- Quality assurance performed: numeric range checks, formatting conformity, logical integrity checks.
- Important caveat: NERC makes no warranty on data accuracy or fitness for use; liability for any use is disclaimed.

## Site context: Sourhope blocks and soil profiles

- The study covers Block 1–5 at Sourhope with detailed site characterization:
  - Block 1: NT8545019630; altitude ~304m; slope ~4°; drainage Moderate; major soil subgroup Brown forest soil; rock type andesite; profile includes horizons from LF through CR with varying textures and root abundances.
  - Block 2: NT8551019610; altitude ~306m; slope ~7°; drainage Free; Brown forest soil; similar horizon sequence with varying texture and stones.
  - Block 3: NT8549019590; altitude ~308m; slope ~7°; drainage Free; Brown forest soil; distinct horizon set with loamy peat in H horizon and multiple mineral horizons.
  - Block 4: NT8546019550; altitude ~312m; slope ~8°; drainage Imperfect; Brown forest soil with gleying; weathered profile characteristics and presence of gleyed horizons.
  - Block 5: NT8544019520; altitude ~315m; slope ~5°; drainage Imperfect; Brown forest soil with gleying; complex horizon sequence with various mottles and clay/clay loam textures.
- Each block provides a soil profile description (horizons, colors, textures, structure, roots, stones) to support interpretation of pH and moisture data in the context of soil properties and drainage status.

## How to use the data for analysis

- Examine spatial and temporal variation in baseline soil pH across blocks, main plots, and sub-plots, and relate to soil drainage status and texture.
- Investigate associations between pH/moisture readings and horizon characteristics or soil subgroups (e.g., Brown forest soils, gleyed variants).
- Use sub-plot data to assess within-plot heterogeneity and the influence of subplot-level factors (SUB_PLOT) on pH values.
- Cross-reference with soil profile descriptions to interpret pH patterns in relation to texture, structure, root density, and moisture regime.
- Leverage metadata for traceability and reproducibility (block, plot, sampling date, treatment) and link to the Sourhope Field Data Handbook (Scott et al., 2003) for methodological context.
- Consider data quality caveats and limitations when making inferences, especially given potential scale mismatches and the need for broader data to generalize findings.

## Access and references

- Data quality and metadata: QA steps described; disclaimers on accuracy and liability by NERC.
- Primary references for context: Scott et al., 2003; Sourhope Field Data Handbook 2003.
- Data availability: via EIDC catalogue (for baseline pH datasets and related documentation).