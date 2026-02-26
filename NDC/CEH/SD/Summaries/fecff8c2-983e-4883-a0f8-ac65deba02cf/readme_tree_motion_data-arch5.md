# This repository contains a tree motion data from 6 data sets, organised by site name.

## Overview
- Contains tree motion data from 6 datasets, organized by site name.
- Wind and tree motion data are stored in separate daily files, labeled with site name, tree ID or wind, year, month, day.

## Data organization and file naming
- Example filename format: Kershope_T25_1990_5_23.
- Each day’s data is split into separate files for wind and tree motion.

## Data contents and metadata
- First column: time and date in format YYYY-MM-DD HH:mm:ss.SSS.
- Remaining columns: tree motion data or wind data; units are included in the variable names.
- Calibration: some tree-motion data were calibrated by pulling the tree with a known force; calibration coefficients are provided in the TreeSummary table.
- Australian wind data: stored in a per-tree folder because trees were not close enough to share wind measurements.
- Metadata considerations: TreeSummary contains calibration information; data have not been pre-processed to avoid biases from user preprocessing choices.

## Processing guidance and preprocessing notes
- Users should apply preprocessing according to their analysis needs; pre-processing choices can affect results.
- A varying offset caused by sensor drift should be removed from tree-motion data. A recommended approach is a 10-minute high-pass filter to remove slow variations (less than 10 minutes timescales). See accompanying publication for discussion and references.

## Technical considerations for accessibility
- Some files exceed Excel’s row limit; opening in Excel may result in data being missed.

## References and related datasets
- Core publication describing all collated data and necessary pre-processing: Jackson, T. et al. 2021. The motion of trees in the wind: a data synthesis. Biogeosciences. doi:10.5194/bg-18-4059-2021.
- Australian data described in: James, K. et al. 2006. Mechanical stability of trees under dynamic loads. American Journal of Botany. doi:10.3732/ajb.93.10.1522.
- Kershope and Rivox data described in: Gardiner, B. A. et al. 1997. Field and wind tunnel assessments of the implications of respacing and thinning for tree stability. Forestry: An International Journal of Forest Research, 70(3): 233-252.
- Kyloe and Clocaenog described in: Hale, Sophie E. et al. 2012. Wind loading of trees: influence of tree size and competition. European Journal of Forest Research, 131(1): 203-217.
- Other large tree motion data sets available (as of June 2021): 
  - https://doi.org/10.7910/DVN/FHJBYG
  - http://www.hydroshare.org/resource/38ae9d9fb88d49f9ad2eed1ee07475c0
  - https://doi.org/10.5683/SP2/WZIKSR
  - https://data.4tu.nl/articles/dataset/Tree_sway_of_19_Amazon_trees/12714989/1
  - https://doi.org/10.5285/657f420e-f956-4c33-b7d6-98c7a18aa07a
  - https://doi.org/10.5285/533d87d3-48c1-4c6e-9f2f-fda273ab45bc

## Governance and data stewardship notes
- Organization by site name supports discoverability and governance of multiple datasets.
- Metadata presence (e.g., TreeSummary) and calibration coefficients support data quality assessment and reuse.
- Clear notes on processing decisions, offsets, and pre-processing requirements facilitate reproducibility and proper data use.
- Awareness of data access constraints (e.g., per-tree wind data, large file sizes) informs sharing and data portal strategies.