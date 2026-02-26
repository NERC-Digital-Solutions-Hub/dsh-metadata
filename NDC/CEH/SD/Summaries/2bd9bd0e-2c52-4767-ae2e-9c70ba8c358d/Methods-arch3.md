# Metadata for 'Data for lead (Pb) in terrestrial wildlife and resultant taxonomic models' Beresford and Barnett, 2018

## Overview
- Presents a REML-based linear mixed effects modeling approach to predict lead (Pb) concentrations in terrestrial wildlife, as an alternative to empirical concentration ratios (CRs).
- Aims to provide less uncertain, site-aware transfer parameters to support environmental radiological assessments and monitoring decisions.
- Outputs relative activity concentration scales (REML means) for different taxa, accounting for site/study as a random factor.

## Data sources and structure
- Primary data source: Wildlife Transfer Database (WTD), a large compilation of wildlife CR values across ecosystems.
- Additional data: Spain (Guillén et al. 2018; Barnett et al. 2018), Chernobyl Exclusion Zone (in prep), and other studies, plus plant data from Spain.
- Dataset characteristics:
  -Pb_dataset.csv with metadata columns (RefID, Habitat, Wildlife, ICRPRAP, N, Value(FM), SD, Data type, Isotope, Site, Order, Family, Genus, Species, etc.).
  -Total available data: 1,422 values from 24 sites; usable terrestrial Pb entries: 928 entries representing 1,195 CR values from 15 sites.
  -Data reconstruction: where entries summarize multiple samples, individual CR values were generated (e.g., if 10 samples, 10 CR values).
- Taxonomic levels analyzed: order, family, and genus.
- Data requirements for model inclusion: at least two taxa at a site, and at least one taxon shared with another site.

## Methods and modeling approach
- REML fitting of a linear mixed effects model using IBM SPSS (v24), with:
  - Fixed effect: taxon (genus, family, or order).
  - Random effect: site (to account for study/site-specific variation).
- Model evaluation:
  - Akaike information criterion (AIC) used to compare model quality (lower is better).
  - Models re-estimated with site removed to test the necessity of the random site factor.
- Outcomes:
  - REML mean values (REML means) at each taxonomic level, on a common scale, representing relative concentration scaling after adjusting for site effects.

## Key datasets and outputs
- Generated REML means for: 
  - Genus_output.csv, Family_output.csv, Order_output.csv (with corresponding REMLmean values).
  - Genus_output_no_duck.csv, Family_output_no_duck.csv, Order_output_no_duck.csv (excludes Anas duck data).
  - Family_no_Ericaceae.csv (excludes Ericaceae data).
- Data columns in Pb_dataset.csv include: RefID, Habitat, Wildlife, ICRPRAP, N, Value(FM), SD, Data type, Isotope, Site, Order, Family, Genus, Species, etc.
- Supplementary reference metadata: Data_references.csv.

## Data handling and robustness tests
- Duck data (Anas spp.) identified as contributing disproportionately to Pb REML means; re-fitting without ducks showed minimal impact on most taxa.
- Ericaceae data dominated the dataset (≈50% at the family level); re-fitting the model without Ericaceae data produced only minor changes, indicating robustness of REML means to data imbalances.
- Results include REML means both with and without Anas data, and with Ericaceae data retained or removed.

## Implications for monitoring frameworks
- Provides a statistically principled method to extrapolate transfer parameters across taxa and sites, reducing uncertainty inherent in CR-based approaches.
- Enables policy-makers and program managers to:
  - Prioritize data collection by identifying taxa and sites with informative REML estimates.
  - Communicate results clearly via standardized REML means across taxonomic levels.
  - Support broader environmental health monitoring by supplying robust, open methods for deriving transfer parameters.

## Data governance and metadata considerations
- Emphasizes the importance of metadata quality to enable replication and verification:
  - Clear descriptions of data types (CR vs concentration), units, and site/taxon identifiers.
  - Documentation of data reconstruction steps where summary data are expanded into individual observations.
- Highlights practical barriers relevant to monitoring frameworks:
  - Access to underlying datasets and complete metadata can be limited.
  - Transformation and standardization of datasets required for REML analyses may demand substantial data management effort.
  - Transparency about data provenance (original studies, site selection, and processing) is crucial for governance and reproducibility.

## Notes
- The REML-based approach yields relative, site-adjusted transfer parameters suitable for informing monitoring design and decision-making in environmental health contexts.