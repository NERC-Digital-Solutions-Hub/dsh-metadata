# Data for lead (Pb) in terrestrial wildlife and resultant taxonomic models

## Overview
- Metadata for a study deriving REML-based taxonomic models of Pb transfer in terrestrial wildlife.
- Data and outputs are organized to support size-appropriate, map-ready representations of relative Pb activity concentrations across taxa and sites.
- Based on the Wildlife Transfer Database (WTD) and additional studies; uses linear mixed-effects REML modeling to account for site effects and taxon.

## Data files and content
- Pb_dataset.csv: primary input data with site, taxon, concentration or concentration ratio, and related fields.
- Genus_output.csv, Family_output.csv, Order_output.csv: REML-derived mean values (REMLmean) for each Genus, Family, and Order, respectively.
- Genus_output_no_duck.csv, Family_output_no_duck.csv, Order_output_no_duck.csv: REML means with Anas (ducks) data excluded.
- Family_no_Ericaceae.csv: REML means with Ericaceae (and Anas) data treated separately or excluded.
- Data_references.csv: supporting references for data sources and methods.

## Methods and data preparation
- Approach: REML fitting of a linear mixed-effects model as an alternative to concentration ratio (CR) methods.
- Purpose: reduce uncertainty by incorporating site as a random factor and provide a scientifically based extrapolation across taxa.
- Data requirements for REML: at least two taxa at a given site, and at least one taxon present at another site; data can be CR values or concentrations (consistent within a site).
- Data sources: Wildlife Transfer Database (WTD) as the primary terrestrial data source; supplemented with Spanish sites, Chernobyl zone data, and other studies.
- Data reconstruction: when entries summed across samples, individual CR values were generated to match sample counts (e.g., 10 samples -> 10 CR values).
- Taxonomic levels examined: order, family, and genus.
- Model fitting and evaluation: performed in SPSS v24 using Linear Mixed Model with REML; model quality assessed via AIC; tests with and without site as a random factor.

## REML means and outputs
- REML mean: a relative scaling value for each taxon after adjusting for site effects, enabling cross-taxon comparisons.
- Separate outputs include:
  - Genus_output.csv (REMLmean by genus)
  - Family_output.csv (REMLmean by family)
  - Order_output.csv (REMLmean by order)
- Sensitivity analyses:
  - Anas (ducks) data removal generally had minimal effect on most taxa, though some duck-related values were unusually high due to lead shot exposure.
  - Removing Ericaceae data (nearly 50% of values at the family level) had only a minor impact on the REML means, indicating robustness.
- The dataset provides both full-data REML means and versions excluding Anas and/or Ericaceae data to support robustness checks.

## Data quality, limitations, and considerations
- Not all WTD data are usable due to site/taxon overlap requirements and cross-site representation.
- Some taxa (e.g., Ericaceae) dominated the data for the Pb dataset, necessitating sensitivity checks to ensure results are not unduly biased.
- Data types include both CR values and concentration measurements; consistency within a site is required for REML fitting.

## Using the outputs in GIS and map products
- REML means (REMLmean) can be linked to sites and taxa to produce map layers showing relative Pb transfer tendencies across regions.
- Outputs are organized by taxonomic level to support different granularity in map visualizations (e.g., genus-level maps vs. family-level summaries).
- Variant outputs (no_duck, no_Ericaceae) provide alternative layers that test the influence of dominant taxa on spatial risk patterns.
- Column explanations:
  - Genus_output.csv: Genus, REMLmean
  - Family_output.csv: Family, REMLmean
  - Order_output.csv: Order, REMLmean
  - Corresponding “no_duck” and “no_Ericaceae” files provide REMLmean values with specific taxa excluded to aid robustness checks.

## Notes and reference context
- Core references and data provenance are provided in the accompanying Data_references.csv.
- The approach offers a pathway for GIS-based risk assessment by providing statistically informed, taxon-specific transfer parameters that can be integrated with spatial layers and environmental data.