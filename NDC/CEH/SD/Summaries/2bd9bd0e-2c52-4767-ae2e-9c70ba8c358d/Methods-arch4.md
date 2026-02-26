# Metadata for 'Data for lead (Pb) in terrestrial wildlife and resultant taxonomic models' Beresford and Barnett, 2018 which comprise 8 files: Pb_dataset.csv, Genus_output.csv, Family_output.csv, Order_output.csv, Genus_output_no_duck.csv, Family_output_no_duck.csv, Order_output_no_duck.csv and Family_no_Ericaceae.csv Please also see supporting document Data_references.csv

## Purpose and approach
- Presents a REML-based linear mixed effects modeling approach as an alternative to empirical concentration ratios (CRs) for predicting radionuclide activity in wildlife.
- Aims to provide less uncertain, site-adjusted estimates and a scientifically grounded extrapolation methodology for Pb in terrestrial wildlife.
- Uses REML to account for site/study as a random factor and taxon as a fixed factor, delivering relative activity concentration estimates (REML means) across taxa.

## Data sources and content
- Primary data source: Wildlife Transfer Database (WTD), a large compilation of whole-organism fresh-mass CR values for wildlife across terrestrial, marine, and freshwater ecosystems.
- For Pb in wildlife: 928 usable terrestrial entries representing 1195 CR values from 15 sites; augmented with data from Spain, Chernobyl, northeast England, Spain plant data, and additional Pb samples.
- Total input dataset: 1422 data values from 24 sites, including both stable Pb and 210Pb values (treated similarly). Excludes sites contaminated by heavy metals.
- Data reconstruction: when entries represented multiple samples, data were split into individual CR values to create a consistent dataset.
- Data types: input can be CR values or concentrations; within a site, all data must be consistently CR values or concentrations.

## REML model specifics
- Taxon levels analyzed: order, family, and genus (with data limitations affecting level availability).
- Fixed factor: taxon (genus, family, or order); Random factor: site/study.
- Model outputs: REML means that represent a relative scaling value for a given taxon after adjusting for site effects.
- Data usability requirements: a site must have data for at least two taxa, and at least one taxon must be present at another site to be included in a run.
- Model fitting: conducted in IBM SPSS (Linear Mixed Model with REML); compared models using Akaike information criterion (AIC).

## Data preparation and constraints
- Species-level modeling was limited because more than 900 data values could not be attributed to specific species; hence genus/family/order levels were emphasized.
- Sensitivity analyses explored data influence:
  - Duck data (Anas) disproportionately high in some taxa; all models were refitted after removing Anas data. The overall effect on REML means was minimal for most taxa.
  - Ericaceae data were abundant; models were re-fitted without Ericaceae to assess robustness. Removal had relatively minor impact; REML means are provided with and without Ericaceae data.

## Outputs and files
- Eight data files included:
  - Pb_dataset.csv
  - Genus_output.csv
  - Family_output.csv
  - Order_output.csv
  - Genus_output_no_duck.csv
  - Family_output_no_duck.csv
  - Order_output_no_duck.csv
  - Family_no_Ericaceae.csv
- Each file contains REML mean values (REMLmean) by taxon, on a common relative scale.
- Column explanations provided for Pb_dataset.csv (e.g., RefID, Habitat, Wildlife, ICRPRAP, N, Value(FM), SD, Data type, Isotope, Site, Order, Family, Genus, Species) and for each taxon-level output file (Genus, Family, Order with and without duck/Ericaceae considerations).

## Robustness and validation
- Demonstrates resilience of REML approach to data heterogeneity:
  - Removing duck-related data minimally affects most REML means, supporting robustness of the overall method.
  - Excluding Ericaceae data likewise shows only modest changes, indicating stability across substantial taxon data skew.

## Practical implications for data leadership
- Provides a reproducible, site-adjusted framework for extrapolating Pb concentrations across wildlife taxa when data are sparse or unevenly distributed.
- Emphasizes the importance of documenting data provenance, taxonomic level suitability, and the handling of dominant taxa to ensure robust risk assessment or regulatory applications.
- Highlights the need for clear data governance around data types (CR vs concentration), site comparability, and metadata (to support future cross-site analyses and updates).

## References and notes
- Contains extensive references related to WTD, ERICA, ICRP reference organisms, and previous Pb transfer studies.
- Includes notes on data types, handling of special cases (e.g., Anas, Ericaceae), and methodological considerations for REML model fitting and interpretation.