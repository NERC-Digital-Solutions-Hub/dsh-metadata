# Metadata for 'Data for lead (Pb) in terrestrial wildlife and resultant taxonomic models' Beresford and Barnett, 2018 which comprise 8 files: Pb_dataset.csv, Genus_output.csv, Family_output.csv, Order_output.csv, Genus_output_no_duck.csv, Family_output_no_duck.csv, Order_output_no_duck.csv and Family_no_Ericaceae.csv Please also see supporting document Data_references.csv.

## Overview
- Presents a REML-based linear mixed effects modeling approach to predict radionuclide (Pb) activity concentrations in wildlife, as an alternative to the empirical concentration ratio (CR) method.
- Provides model outputs (REML means) for terrestrial wildlife at three taxonomic levels (order, family, genus) with site treated as a random factor and taxon as a fixed factor.
- Data can be in CR values or concentrations, with requirements that, at a given site, data exist for two or more taxa and at least one taxon appears at another site.
- Data and methods are designed to enable scientifically grounded extrapolation across taxa and sites, with robustness checks for potential biases.

## Data assets and structure
- Eight CSV data files plus a supporting reference file:
  - Pb_dataset.csv: detailed input data (references, habitat, wildlife, taxon, site, data type, concentration values, N, SD, etc.).
  - Genus_output.csv, Family_output.csv, Order_output.csv: REML mean values (REMLmean) by taxonomic level.
  - Genus_output_no_duck.csv, Family_output_no_duck.csv, Order_output_no_duck.csv: REML means with duck (Anas) data removed to test influence.
  - Family_no_Ericaceae.csv: REML means with Ericaceae data removed to test influence at the family level.
  - Data_references.csv: supporting documentation of data references.
- Column definitions provided for Pb_dataset.csv to interpret fields like RefID, Habitat, Wildlife, N, Value(FM) or Data type, Isotope, Site, Taxon levels, etc.

## Data sources and provenance
- Primary data source: Wildlife Transfer Database (WTD), a large compilation of wildlife concentration ratio values for terrestrial, marine, and freshwater ecosystems.
- Supplementary data from Spain, the Chernobyl Exclusion Zone, and North East England studies; additional plant data from Spain; older Pb data with concentrations in fresh mass.
- Excluded data: sites contaminated with heavy metals; certain datasets where data could not meet taxon-site cross-comparison requirements.
- Data reconstruction: where entries represented means of multiple samples without SDs, individual CR values were reconstructed to align with the dataset’s needs (per Wood et al. 2013 methodology).

## Modeling approach and outputs
- REML fitting performed in IBM SPSS (v24) using Linear Mixed Model framework; fixed effect = taxon, random effect = site.
- Input data requirements: for REML runs at a given taxonomic level, data must exist for two or more taxa within a site and at least one taxon must be present at another site; data can be CR values or concentrations, with consistency within a site.
- Model evaluation: Akaike Information Criterion (AIC) used to compare model quality; several runs performed with and without site as a random factor to validate the model structure.
- Output interpretation: REML means represent a relative scaling value of concentration ratios across taxa after adjusting for site effects; results are provided at genus, family, and order levels.

## Data preparation and quality control
- Ensured comparability by reconciling data types (CR vs. concentration) within sites.
- Reconstructed multiple-sample entries to individual CR values when needed to maximize usability.
- Conducted sensitivity analyses by excluding duck-related data (Anas) and by excluding Ericaceae data to assess robustness of REML means.
- Documentation notes that removing Ericaceae or Anas could influence data representation; in practice, effects were generally minor, supporting robustness of the approach.

## Taxa-specific robustness and considerations
- Duck-related data (Anas) identified as unusually high in REML means under certain conditions; analyses were re-run with duck data removed to assess impact.
- Ericaceae dominated the dataset (e.g., about 50% of data at the family level); separate fits without Ericaceae data tested robustness; results remained broadly consistent, indicating overall robustness of REML estimates.

## Metadata and documentation
- Each provided file includes descriptive column headings and explanations to facilitate reuse and interpretation.
- Supporting Data_references.csv complements Pb_dataset.csv with source references.
- The documentation covers data provenance, transformation steps, and modeling choices important for data stewardship and governance.

## Usage notes and limitations
- Suitable for cross-taxa extrapolation of Pb concentrations in terrestrial wildlife, while acknowledging data gaps (two or more taxa per site; cross-site taxa overlap).
- Limitations include potential biases from data dominance (e.g., Ericaceae) and potential non-interoperable data across studies; robustness tests mitigate but do not eliminate these concerns.
- Users should reference the eight data files and supporting Data_references.csv for full context and provenance when integrating into new analyses or catalogues.