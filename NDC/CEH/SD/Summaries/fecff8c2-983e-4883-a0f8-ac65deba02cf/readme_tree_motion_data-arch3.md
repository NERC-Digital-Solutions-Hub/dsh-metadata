# This repository contains a tree motion data from 6 data sets, organised by site name.

## Overview
- Contains wind and tree motion data from six data sets, organized by site name.
- Data files are stored per day and labeled with site name, tree ID or wind, year, month, day (example: Kershope_T25_1990_5_23).

## Data structure
- Each file's first column: timestamp formatted as YYYY-MM-DD HH:mm:ss.SSS.
- Remaining columns: tree motion data or wind data; units are included in the variable names.
- Some datasets include calibration coefficients in a TreeSummary table for data calibrated using a known force.
- Australian wind data are stored per-tree in separate folders because trees were not close enough to share wind measurements.
- Data have not been pre-processed; user choices in pre-processing can affect results.

## Pre-processing and data quality considerations
- Important offset correction: a varying offset caused by sensor drift must be removed from tree motion data.
- Recommended approach: apply a 10-minute high-pass filter to remove slow-time-scale variations.
- There is discussion about preprocessing methods in the accompanying publication and references.
- Files may exceed Excel’s row limit, so opening in Excel can result in data being missed.

## Governance, provenance, and accessibility
- Calibration coefficients and some metadata are provided in the TreeSummary table.
- Data provenance links to accompanying publications describing collated data and necessary pre-processing.
- Australian, Kershope, Rivox, Kyloe, and Clocaenog datasets are described with respective references, indicating established methodologies and contexts.

## References and related datasets
- Jackson, T. et al (2021). The motion of trees in the wind: a data synthesis. Biogeosciences. DOI: 10.5194/bg-18-4059-2021
- Australian data: James, K. et al. (2006). Mechanical stability of trees under dynamic loads. Am. J. Bot.
- Kershope and Rivox data: Gardiner, B. A. et al. (1997). Field and wind tunnel assessments of respacing and thinning for tree stability. Forestry
- Kyloe and Clocaenog: Hale, Sophie E. et al. (2012). Wind loading of trees: influence of tree size and competition. European Journal of Forest Research
- Additional large tree motion datasets (links provided within the document)

## Relevance for monitoring frameworks
- Provides raw and reference material to monitor environmental dynamics (tree motion under wind) relevant to forest stability and ecological risk assessments.
- Highlights critical data governance aspects: traceability to originators, calibration documentation, and transparent preprocessing discussions.
- Identifies practical barriers for monitoring use: need for drift correction, explicit preprocessing decisions, data volume challenges, and reliance on public data sharing and metadata completeness.