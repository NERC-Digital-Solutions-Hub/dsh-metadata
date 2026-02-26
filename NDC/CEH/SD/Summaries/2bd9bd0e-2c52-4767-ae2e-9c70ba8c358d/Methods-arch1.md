# Data for lead (Pb) in terrestrial wildlife and resultant taxonomic models

## Overview
- Presents a REML-based linear mixed effects approach to predict lead (Pb) activity concentrations in terrestrial wildlife.
- Offers an alternative to concentration ratios (CRs), aiming to reduce uncertainty by accounting for site effects and providing a principled extrapolation method.
- Produces relative activity concentration estimates (REML means) across taxonomic levels (genus, family, order) for use in risk assessment and ecological transfer modelling.
- Includes multiple data treatments (with and without problematic taxa) to test robustness.

## Data sources and composition
- Primary data source: Wildlife Transfer Database (WTD) with extensive CR values for wildlife across ecosystems.
- Terrestrial Pb data: 928 usable entries representing 1195 CR values from 15 sites; total available dataset expanded to 1422 data values from 24 sites after adding other studies (Spain, Chernobyl, NE England) and additional taxa.
- Data types: mix of CR values and concentration values (two or more taxa per site required; data must be input as CR or concentrations consistently within a site).
- Datasets reconstructed to individual values when entries represented multiple samples (per Wood et al. 2013).
- Exclusions: contaminated sites (heavy metals) removed; many entries not species-level; for some runs, data for Anas (ducks) and Ericaceae taxa are treated separately to assess bias and influence.
- Additional references: various supporting studies and datasets (see Data_references.csv).

## Methods and model structure
- Modelling approach: REML fitting of a linear mixed effects model.
- Fixed effects: taxon (e.g., genus, family, order).
- Random effects: site/study to capture between-site variation.
- Model evaluation: compared using Akaike information criterion (AIC); some runs tested with and without site as a random factor.
- Data requirements for REML fitting: site must have data for two or more taxa and at least one taxon must appear at another site to enable cross-site extrapolation.
- Data preparation: reconstructions to generate individual CR values from multi-sample entries; consistent data input (CRs or concentrations) within each site.

## Key findings and robustness checks
- Anas (ducks) data: initial REML fits showed high values for Anas; re-fits performed with duck data removed; effects on REML means for most taxa were minimal, though duck-related values were notably higher in some instances.
- Ericaceae data: Ericaceae dominated the dataset (e.g., ~50% of CR values); re-fitting without Ericaceae produced only minor changes, demonstrating robustness of the REML approach. REML means at the family level are provided both with and without Ericaceae data.
- Output interpretation: REML means provide a relative scaling of Pb concentrations across taxa after adjusting for site effects; useful for rank-order comparisons and cross-site extrapolations.

## Output files and data structure
- Pb_dataset.csv: primary dataset with column explanations (e.g., RefID, Habitat, Wildlife, ICRPRAP, N, Value(FM) or Concentration, SD, Site, Order, Family, Genus, Species, Isotope, etc.).
- Genus_output.csv: REMLmean for each Genus.
- Family_output.csv: REMLmean for each Family.
- Order_output.csv: REMLmean for each Order.
- Genus_output_no_duck.csv: Genus REMLmeans without Anas data.
- Family_output_no_duck.csv: Family REMLmeans without Anas data.
- Order_output_no_duck.csv: Order REMLmeans without Anas data.
- Family_no_Ericaceae.csv: Family REMLmeans with Ericaceae data removed.
- Data_references.csv: supporting references for data sources.
- Summary of column headings and data types is provided to aid interpretation.

## How to use the results
- The REML means provide a relative, site-adjusted scale of Pb transfer to wildlife across taxa, enabling:
  - Ranking of taxa by relative Pb burden.
  - Extrapolation of transfer parameters to related taxa or sites with similar characteristics.
  - Integration into ecological risk assessments and models that require taxon-specific transfer parameters.
- Outputs can be consulted at multiple taxonomic levels (genus, family, order) and with/without potential biasing data (Anas, Ericaceae) to assess robustness.

## Notes, limitations, and considerations
- Data gaps at local scales and in certain taxa can limit precision; the REML approach helps mitigate some site-level variability but depends on cross-site data.
- The approach relies on combining CR and concentration data carefully; within-site consistency (CR or concentration) is required.
- Duck (Anas) data and Ericaceae-dominated data can disproportionately influence results; dedicated runs without these data help assess robustness.
- Heavy-metal contaminated sites are excluded to avoid biasing transfer parameters.

## Supporting references
- The dataset integrates WTD-derived data and multiple independent studies, with detailed references provided in Data_references.csv.