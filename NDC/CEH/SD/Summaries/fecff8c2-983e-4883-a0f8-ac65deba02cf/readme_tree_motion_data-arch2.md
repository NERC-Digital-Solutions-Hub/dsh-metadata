# Tree motion data from 6 data sets

- The repository contains tree motion and wind data from six data sets, organized by site name.
- File organization: wind and tree data are stored in separate daily files, named by site name, tree ID or wind, year, month, and day (e.g., Kershope_T25_1990_5_23).
- File structure: each file’s first column is the timestamp (YYYY-MM-DD HH:mm:ss.SSS); remaining columns contain tree motion data or wind data with units indicated in the variable names.
- Calibration: some data were calibrated by pulling the tree with a known force; calibration coefficients are provided in the 'TreeSummary' table.
- Australian data: wind data for the Australian dataset are stored in per-tree folders because the trees were not close enough to share a wind measurement.
- Pre-processing stance: data have not been pre-processed; user decisions in pre-processing can affect results.
- Sensor drift: a varying offset due to sensor drift must be removed from the tree motion data; a recommended method is a 10-minute high-pass filter to remove variations slower than 10 minutes. Further discussion exists in the accompanying publication and references.
- Excel limitation: some files exceed Excel’s row limit, so data may be missed when opened in Excel.

## Data context and sources

- Publications describing the data and pre-processing requirements:
  - Jackson, T. et al. (2021) The motion of trees in the wind: a data synthesis. Biogeosciences. doi: 10.5194/bg-18-4059-2021
- Australian data details:
  - James, K. et al. (2006). Mechanical stability of trees under dynamic loads. American Journal of Botany. doi: 10.3732/ajb.93.10.1522
- Kershope and Rivox data:
  - Gardiner, B. A. et al. Field and wind tunnel assessments of the implications of respacing and thinning for tree stability. Forestry: An International Journal of Forest Research 70.3 (1997): 233-252
- Kyloe and Clocaenog data:
  - Hale, Sophie E. et al. Wind loading of trees: influence of tree size and competition. European Journal of Forest Research 131.1 (2012): 203-217

## Related datasets and availability

- Other large tree motion datasets available (as of June 2021):
  - https://doi.org/10.7910/DVN/FHJBYG
  - http://www.hydroshare.org/resource/38ae9d9fb88d49f9ad2eed1ee07475c0
  - https://doi.org/10.5683/SP2/WZIKSR
  - https://data.4tu.nl/articles/dataset/Tree_sway_of_19_Amazon_trees/12714989/1
  - https://doi.org/10.5285/657f420e-f956-4c33-b7d6-98c7a18aa07a
  - https://doi.org/10.5285/533d87d3-48c1-4c6e-9f2f-fda273ab45bc

## Implications for environmental monitoring and analysis

- Purpose: provide standardized, long-form data to assess wind-tree interactions and environmental health over time.
- For analysts:
  - Emphasize consistent data QA, cleaning, and transformation before analysis.
  - Consider integrating these datasets with additional environmental data to enhance value beyond single-use analyses.
  - Ensure access to underlying data used to produce outputs and store datasets in appropriate data portals.