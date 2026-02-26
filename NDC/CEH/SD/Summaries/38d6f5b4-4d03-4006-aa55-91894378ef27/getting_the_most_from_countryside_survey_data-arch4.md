# Notes on the downloadable data

- Purpose and scope
  - Countryside Survey (CS) field data come from a sample of 1-km squares across Great Britain (GB).
  - Data are collected at two levels: whole squares and within-square features (e.g., vegetation quadrats, soils).
  - Measurements span binary and continuous variables (e.g., presence/absence, areas, lengths).

- Sampling design and representativeness
  - The CS sample squares are not a random subset of all GB 1-km squares.
  - Sampling is stratified by land classes defined by the ITE Land Classification.
  - Country-specific classification updates have occurred (England, Wales, Scotland); total classes: 21, 8, and 16 respectively.
  - Not all squares were eligible for field survey: squares >90% sea or >75% urban were excluded.
  - Estimates for GB or regions assume excluded squares are similar in vegetative land composition to sampled squares; this introduces bias only in regions with substantial sea/urban areas.

- Implications for analyses
  - Because the sample is stratified and not purely random, estimates must use stratification-aware methods (ratio estimation by land class with area-based weights).
  - Standard errors and confidence intervals have been estimated using bootstrap methods since 1998 due to skewness concerns.
  - Extrapolation to GB or regional levels relies on assumptions about excluded areas; bias is generally small but can be problematic in areas with high sea/urban proportions.

- Confidentiality and data access
  - To preserve representativeness, precise locations of CS squares are confidential.
  - External users are limited to a spatial precision no greater than 100 square kilometers; it is not possible to determine whether a square falls within finer-defined areas.

- Data processing and metadata
  - Official estimates are produced by calculating ratio estimates for each land class and aggregating by vegetative land area within each class.
  - The document references methodological sources for sampling (Cochran, bootstrap methods by Efron & Tibshirani) and the Countryside Survey 1990 Main Report.
  - Metadata and documentation should reflect the stratified design, area weights, and the bootstrap-based uncertainty estimates.

- Practical considerations for data strategy
  - Ensure clear documentation of sampling design, stratification, exclusions, and weighting to support correct analysis and interpretation.
  - Maintain and communicate the confidentiality constraints and spatial precision limits to data users.
  - Align data products with user needs (e.g., policy colleagues) by clearly indicating limitations and uncertainty.
  - Monitor updates to land-class classifications and corresponding impacts on historical comparability.