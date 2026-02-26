# Data for lead (Pb) in terrestrial wildlife and resultant taxonomic models

- Purpose and approach
  - Presents a REML (restricted maximum likelihood) linear mixed effects modeling approach to predict Pb concentrations in terrestrial wildlife, offering a less uncertain alternative to empirical concentration ratios (CRs) by accounting for site/study effects.
  - Provides a methodology to extrapolate transfer parameters across taxa (order, family, genus) on a common relative scale.

- Data sources and scope
  - Primary data source: Wildlife Transfer Database (WTD) with over 100,000 CR values for wildlife across terrestrial, marine, and freshwater systems.
  - Focused subset: terrestrial Pb data suitable for REML modeling, comprising 928 usable entries (1195 CR values) from 15 sites; augmented with Spain, Chernobyl, and northeast England studies, plus data for additional plant species from Spain and other Pb measurements.
  - Total input data for Pb analyses: 1422 data values from 24 sites, including both stable Pb and 210Pb values; sites contaminated with heavy metals were excluded.

- Data preparation and inclusion criteria
  - Datasets must include concentrations or CRs for two or more taxa at a given site; datasets are included only if there is at least one taxon in common with another site.
  - Input data can be CR values or concentrations, with the requirement that, within any given site, all data are consistently either CR values or concentrations.
  - In cases where the original data were multiple samples or means without SDs, a reconstruction method (as in Wood et al. 2013) was used to generate multiple individual CR values to preserve data granularity.

- Modeling specifics
  - Fixed factor: taxon (at genus, family, or order level); random factor: site/study.
  - Output: REML-adjusted mean values for each taxon, representing a relative scaling (REML mean) on a common basis across sites.
  - Model evaluation: Akaike information criterion (AIC) used to compare model quality; models re-run with site as a random factor removed to test robustness.
  - Data considerations affecting model design: not all data could be used for species-level modeling due to taxonomic resolution; some sites contributed data for multiple genera but from a single family or order.

- Data quality considerations and robustness checks
  - Duck data (Anas, Anatidae, Anseriformes) showed inflated REML means in some cases, likely due to lead shot exposure; models were re-run with duck data removed. In most cases, removing duck data had minimal impact on REML means for other taxa.
  - Ericaceae data dominated the dataset (e.g., ~681 of 1420 CR values at the family level); refitting the model without Ericaceae data demonstrated the robustness of REML results, with relatively minor changes to REML means. REML means are provided both with and without Ericaceae data.

- Outputs and data products
  - Pb_dataset.csv: column definitions include RefID, habitat, wildlife, ICRPRAP, sample size, Value(FM) or concentration, SD, data type (CR or concentration), isotope, site, taxon classifications (Order, Family, Genus, Species).
  - Taxon-specific REML outputs (relative scaling values)
    - Genus_output.csv and Genus_output_no_duck.csv: REMLmean per genus; no_duck version excludes Anas data from fitting.
    - Family_output.csv and Family_output_no_duck.csv: REMLmean per family; no_duck version excludes Anas data.
    - Order_output.csv and Order_output_no_duck.csv: REMLmean per order; no_duck version excludes Anas data.
    - Family_no_Ericaceae.csv: REMLmean per family with Ericaceae data removed (to assess influence of data dominance by this family).
  - Data_references.csv (supporting document listing references used to build and contextualize the dataset).
  - These outputs provide ready-to-use relative transfer parameters to support data exploration, comparison across taxa, and potential integration into broader risk assessment tools.

- Reuse and application guidance
  - Outputs enable cross-taxa comparison on a common scale, supporting policy and risk assessment work that requires standardized transfer parameters without relying solely on CR-based approaches.
  - The REML framework allows incorporating site-level variability, improving extrapolation where species- or site-specific data are sparse.
  - Users should be aware of data caveats (e.g., potential biases from duck data or dominant families) and consult the no_duck and no_Ericaceae variants for sensitivity analyses.

- References and methodological context
  - Data draw from the Wildlife Transfer Database and related radiological transfer literature; REML modeling choices and robustness checks are described, with software implementation noted (IBM SPSS Statistics, Linear Mixed Model with REML).