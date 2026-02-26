# This repository contains a tree motion data from 6 data sets, organised by site name.

## Overview
- Tree motion data from 6 datasets organized by site name; wind and tree data stored in separate files for each day.
- Filenames follow the pattern including site name, tree ID or wind, year, month, day (example: Kershope_T25_1990_5_23).
- Each file’s first column is time (YYYY-MM-DD HH:mm:ss.SSS); remaining columns are tree motion or wind data with units included in variable names.
- Some data are calibration-adjusted; calibration coefficients are provided in the TreeSummary table.
- Australian wind data are stored in per-tree folders because trees were not sufficiently close to share wind measurements.
- Data have not been pre-processed; user choices in pre-processing can affect results.

## Data organization and naming details
- Day-by-day files for wind and tree data; Australian data organized by tree in separate folders.
- Large files may exceed Excel’s row limit, causing data to be missed if opened in Excel.

## Data contents and formats
- Time column uses the format YYYY-MM-DD HH:mm:ss.SSS.
- Subsequent columns contain tree motion or wind measurements with units indicated in variable names.
- Calibration coefficients (where applicable) are documented in the TreeSummary table.

## Pre-processing guidance
- A varying offset (sensor drift) should be removed from tree motion data.
- Recommended approach: 10-minute high-pass filter to remove variations on timescales slower than 10 minutes.
- There is ongoing discussion in the accompanying publication and references; consult Jackson et al. (2021) for full context.
- Some files are too large for Excel; use appropriate data tools to load entire datasets.

## Calibration and metadata
- Some datasets were calibrated by pulling the tree with a known force; calibration coefficients are available in TreeSummary.
- Australian data require per-tree wind data handling due to spatial separation of trees.

## Practical considerations for data use
- The data are raw and not pre-processed; users should determine suitable preprocessing steps.
- Expect patchy data, multiple formats, and access across different systems; plan to resolve formatting and integration needs.
- To ensure reproducibility and comparability, follow the referenced literature for recommended preprocessing and interpretation.

## References
- Jackson, T. et al. (2021). The motion of trees in the wind: a data synthesis. Biogeosciences.
- James, K. et al. (2006). Mechanical stability of trees under dynamic loads. American Journal of Botany.
- Gardiner, B. A. et al. (1997). Field and wind tunnel assessments of the implications of respacing and thinning for tree stability. Forestry.
- Hale, Sophie E. et al. (2012). Wind loading of trees: influence of tree size and competition. European Journal of Forest Research.
- Additional large tree motion datasets: links provided in the document.