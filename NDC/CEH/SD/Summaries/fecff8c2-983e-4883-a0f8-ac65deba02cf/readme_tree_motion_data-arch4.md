# This repository contains a tree motion data from 6 data sets, organised by site name

## Overview
- A repository containing tree motion data from six data sets, organized by site name.
- Data are split into wind and tree motion data, stored in separate daily files; file names include site name, tree ID or wind, and date (e.g., Kershope_T25_1990_5_23).
- Each file’s first column is time and date (format: YYYY-MM-DD HH:mm:ss.SSS); subsequent columns hold tree motion or wind data with units embedded in variable names.
- Calibration coefficients, where available (from experiments pulling the tree with a known force), are provided in the TreeSummary table.
- Australian wind data are stored per-tree because trees were not spatially near enough to share wind measurements.
- The data have not been pre-processed, allowing user-defined preprocessing choices to influence results.

## Data structure and storage
- File naming convention encodes site, tree/wind identifier, year, month, day.
- Time column uses precise timestamp format; data columns follow with motion measurements and units in names.
- Calibration details are centralized in a TreeSummary table for applicable datasets.
- Australian wind data organization differs from other datasets (per-tree storage).
- Some files are longer than Excel’s row limit, so opening in Excel will result in missed data.

## Pre-processing, calibration, and quality
- No universal pre-processing applied in the repository; users must decide preprocessing steps.
- A varying offset due to sensor drift will need removal from tree motion data.
- A suggested approach is a 10-minute high-pass filter to remove slow variations; there is literature discussion referenced for more details.
- Calibration may be available for some data (via known-force calibration in TreeSummary).

## Data accessibility and usability
- Because preprocessing is user-directed, results can vary across users and analyses.
- Large file sizes pose usability challenges in common tools (e.g., Excel limitations).
- The repository links to a published guidance document and related literature for context and recommended practices.

## Metadata, provenance, and references
- References include:
  - Jackson, T. et al. 2021. The motion of trees in the wind: a data synthesis (Biogeosciences). DOI: 10.5194/bg-18-4059-2021
  - Australian data description: James, K. et al. 2006. Mechanical stability of trees under dynamic loads (Am. J. Bot.). DOI: 10.3732/ajb.93.10.1522
  - Kershope and Rivox data: Gardiner, B. A. et al. 1997. Forestry: An International Journal of Forest Research.
  - Kyloe and Clocaenog: Hale, S. E. et al. 2012. European Journal of Forest Research.
- Additional large tree motion data sets available at various DOIs and repositories (links provided).

## Practical takeaways for data leaders
- Treat the collection as a multi-dataset data system with heterogeneous storage formats (per-day files, per-tree wind data in Australia).
- Maintain robust metadata (e.g., TreeSummary calibration details, units in variable names) to support data discoverability and reuse.
- Encourage and document user-driven preprocessing pipelines (e.g., offset removal, high-pass filtering) to enable consistent analyses and reproducibility.
- Plan for data governance around large file handling, tool compatibility (avoid Excel for full datasets), and clear guidance on preprocessing decisions.
- Leverage referenced literature to justify preprocessing choices and to align analyses across datasets.
- Consider cross-dataset coordination to streamline access, standardize metadata, and reduce duplicated effort while supporting communities of practice around tree motion data.