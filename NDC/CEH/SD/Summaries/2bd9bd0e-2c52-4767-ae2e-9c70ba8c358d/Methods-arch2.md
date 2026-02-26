# Data for lead (Pb) in terrestrial wildlife and resultant taxonomic models

- Purpose and use
  - Provide REML-based, taxon-specific estimates of lead (Pb) activity in terrestrial wildlife to support environmental health assessments and policy evaluation.
  - Move beyond simple concentration ratio (CR) approaches by fitting a linear mixed-effects model that accounts for site-level variability and yields relative activity concentration scales (REML means) across taxa and taxonomic levels (genus, family, order).

- Data sources and scope
  - Wildlife Transfer Database (WTD): large compilation of whole-organism, fresh-mass Pb CR values for terrestrial, marine, and freshwater wildlife.
  - Supplementary data from Spain, the Chernobyl Exclusion Zone, and northeast England; additional plant data from Spain; other Pb data from published/unpublished studies.
  - Final usable dataset: 1,422 data values from 24 sites, including both stable Pb and 210Pb values; sites contaminated by heavy metals excluded.
  - Data preparation: where entries summarize multiple samples, individual CR values are reconstructed (e.g., an entry for 10 samples yields 10 CR values) to enable REML fitting.

- Modeling approach
  - REML fitting of linear mixed-effects models with:
    - Fixed factor: taxon (at genus, family, or order level, depending on data availability).
    - Random factor: site/study.
  - Data requirements for a site: data for more than one taxon, and at least one taxon present at another site.
  - Input data can be CR values or concentrations; at a given site, all data must be consistently CR values or concentrations.
  - Model selection and robustness checks:
    - Akaike information criterion (AIC) used to compare models (lower AIC better).
    - Refit analyses with site removed to test the random effect.
    - Separately assess the influence of Anas (ducks) data due to potential lead-shot contamination effects.
    - Assess robustness to Ericaceae data dominance by refitting at the family level without Ericaceae data.

- Outputs and data products
  - Primary outputs: REML means for taxa at different taxonomic levels, representing relative scaling values after adjusting for site effects.
  - Data files (Pb_dataset and taxonomic outputs):
    - Pb_dataset.csv: core input data with metadata and column explanations.
    - Genus_output.csv: REML means by genus.
    - Family_output.csv: REML means by family.
    - Order_output.csv: REML means by order.
  - Robustness/alternative models:
    - Genus_output_no_duck.csv: REML means with Anas (ducks) data removed.
    - Family_output_no_duck.csv: REML means with Anas data removed (family level).
    - Order_output_no_duck.csv: REML means with Anas data removed (order level).
    - Family_no_Ericaceae.csv: REML means at the family level with Ericaceae data excluded.
  - Supporting references: Data_references.csv documents data sources and cited studies.

- Pb_dataset.csv: column explanations (highlights)
  - RefID: reference identifier within the Wildlife Transfer Database.
  - Habitat: generic habitat descriptor.
  - Wildlife: broad wildlife category.
  - ICRPRAP: relevant ICRP Reference Animal and Plant (if applicable).
  - N: number of samples on which Value(FM) is calculated.
  - Value(FM): concentration ratio or concentration value (defined on a fresh mass basis for CR or mg/kg for concentration).
  - SD: standard deviation for Value(FM).
  - Data type: CR or concentration.
  - Isotope: Pb isotope.
  - Site: site identifier.
  - Order, Family, Genus, Species: taxonomic classifications.
  - Notes: data type conventions and any special characters/missing values.

- Key methodological notes and considerations
  - REML approach reduces uncertainty relative to CR-only models by incorporating site-level random effects.
  - Duck-related data can inflate REML means; removing Anas data has minimal impact on most taxa but is explicitly evaluated.
  - Ericaceae data dominate the dataset (e.g., ~50% of values); re-fitting without Ericaceae assesses robustness, with relatively minor changes observed in results.
  - Data inclusion criteria ensure cross-site comparability and avoid overfitting to single taxa or sites.

- Practical implications for monitoring and analysis
  - Provides a consistent, site-adjusted, relative scale of Pb bioavailability across taxa to support environmental health monitoring and policy performance assessments.
  - Enables extrapolation to related taxa and ecosystems through a statistically grounded framework, while clearly communicating uncertainty and data limitations.
  - Useful for prioritizing monitoring across taxa and sites based on REML-derived relative concentrations, with explicit documentation of data sources and model assumptions.