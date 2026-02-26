# This repository contains a tree motion data from 6 data sets, organised by site name.

## Overview
- Contains tree motion data from 6 data sets, organized by site name.
- Wind and tree data are stored in separate files for each day; filenames include site name, tree ID or wind, year, month, day (example: Kershope_T25_1990_5_23).
- Each file: first column is timestamp in format YYYY-MM-DD HH:mm:ss.SSS; remaining columns are tree motion data or wind data with units indicated in the variable names.

## Data organization and content
- Australian wind data: stored in a folder with data for each tree because trees were not close enough to share a wind measurement.
- Calibration: some data were calibrated by pulling the tree with a known force; calibration coefficients are provided in the 'TreeSummary' table.
- Data status: not pre-processed; user choices in pre-processing can affect results.
- Size considerations: some files exceed Excel’s row limit; data may be missed if opened in Excel.

## Pre-processing guidance
- Sensor drift causes a varying offset in tree motion data; removal is necessary.
- Recommended approach: apply a 10-minute high-pass filter to remove variations on time-scales longer than 10 minutes.
- There is discussion about preprocessing in accompanying literature; see the references for details.

## Practical notes for GIS specialists
- Time stamps enable time-enabled GIS analyses; data can be mapped and animated over time.
- Data can be joined across datasets by site name and tree ID (or wind) to build composite spatial views, though differing resolutions and formats should be harmonized.
- Calibration coefficients in TreeSummary help interpret magnitudes of motion data.
- Large, multi-file datasets require batch processing or programmatic loading; avoid relying on Excel for complete analysis.

## References
- Jackson, T. et al. (2021). The motion of trees in the wind: a data synthesis. Biogeosciences. https://doi.org/10.5194/bg-18-4059-2021
- James, K. et al. (2006). Mechanical stability of trees under dynamic loads. Am. J. Bot. doi:10.3732/ajb.93.10.1522
- Gardiner, B. A., et al. (1997). Field and wind tunnel assessments of the implications of respacing and thinning for tree stability. Forestry: An International Journal of Forest Research 70.3: 233-252.
- Hale, Sophie E., et al. (2012). Wind loading of trees: influence of tree size and competition. European Journal of Forest Research 131.1: 203-217.
- Other large tree motion data sets available at the time of writing (June 2021): https://doi.org/10.7910/DVN/FHJBYG; http://www.hydroshare.org/resource/38ae9d9fb88d49f9ad2eed1ee07475c0; https://doi.org/10.5683/SP2/WZIKSR; https://data.4tu.nl/articles/dataset/Tree_sway_of_19_Amazon_trees/12714989/1; https://doi.org/10.5285/657f420e-f956-4c33-b7d6-98c7a18aa07a; https://doi.org/10.5285/533d87d3-48c1-4c6e-9f2f-fda273ab45bc