# Tree motion data

## Overview
- Repository containing tree motion data from 6 datasets, organized by site name.
- Wind and tree data are stored in separate files for each day; filenames include site name, tree ID or wind, year, month, day (e.g., Kershope_T25_1990_5_23).
- Each file's first column is the time/date in format YYYY-MM-DD HH:mm:ss.SSS.
- Following columns contain tree motion data or wind data with units indicated in the variable names.

## Data organization and file structure
- Data separated by dataset and by day; Australian wind data stored in per-tree folders because trees were not close enough to share wind measurements.
- Some data have calibration coefficients documented in a TreeSummary table when a known force was used for calibration.

## Data content and units
- Columns represent tree motion or wind measurements; variable names include units.
- Calibration coefficients available in TreeSummary for calibrated measurements.

## Calibration
- Some datasets include calibration via known applied force; calibration details are provided in the TreeSummary table.

## Australian data specifics
- Wind data for the Australian dataset are stored within per-tree folders due to spatial separation of trees.

## Pre-processing and recommended steps
- Data have not been pre-processed; user decisions in pre-processing can affect results.
- Important step: remove a varying offset caused by sensor drift from the tree motion data.
- Recommended approach: apply a 10-minute high-pass filter to remove slow variations (details discussed in accompanying publication and references).

## Data access constraints
- Some files exceed Excel's row limit, so opening in Excel may miss data.
- Datasets may require custom preprocessing and handling beyond basic spreadsheet tools.

## References and related datasets
- Primary publication describing all collated data and necessary pre-processing: Jackson, T. et al. (2021) The motion of trees in the wind: a data synthesis. Biogeosciences. DOI: https://doi.org/10.5194/bg-18-4059-2021
- Australian data: James, K. et al. (2006). Mechanical stability of trees under dynamic loads. Am. J. Bot. DOI: 10.3732/ajb.93.10.1522
- Kershope and Rivox data: Gardiner, B. A., et al. Field and wind tunnel assessments of the implications of respacing and thinning for tree stability. Forestry: An International Journal of Forest Research 70.3 (1997): 233-252.
- Kyloe and Clocaenog: Hale, Sophie E., et al. Wind loading of trees: influence of tree size and competition. European Journal of Forest Research 131.1 (2012): 203-217.
- Other large tree motion data sets (as of June 2021): several links provided (DOIs/URLs listed in the document).

## Practical usage and limitations
- Useful for correlating wind with tree motion and developing predictive insights, given calibration metadata.
- Because pre-processing choices influence results, analysts should document and justify their processing steps (e.g., offset removal, high-pass filtering).
- Data quality varies and may require unifying across multiple sources/formats for multi-site analyses.