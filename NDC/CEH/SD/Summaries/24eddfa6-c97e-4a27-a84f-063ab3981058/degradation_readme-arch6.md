# Degradation characteristics of bio-based teabags buried in soil, UK, November 2021 - June 2022

- Purpose of the dataset
  - Determine chemical deterioration and material changes of three anonymised bio-based PLA-cellulose teabag brands after burial in soil for 7 months under UK conditions.
  - Data support a study on deterioration and potential effects on soil organisms (earthworms), linked to the BIO-PLASTIC-RISK project.

- Data collection period and conditions
  - Burial period: November 2021 – June 2022 (7 months)
  - Burial depth: -10 cm in UK soil
  - Teabag brands: anonymised (Tbag-A, Tbag-B, Tbag-C)
  - Source material: polylactic acid (PLA) – cellulose blend teabags
  - Teabags sourced from at least five different boxes across multiple stores in Plymouth, UK (July–October 2021)

- Data files included (six CSVs)
  - Degradation_crystallinity.csv
    - Crystallinity (%), measured after 7 months in soil
    - Tbags: A and B have data; no data for Tbag-C
  - Degradation_Mass.csv
    - Time (months), initial_teabag_mass (g), final_mass (g), mass_loss (g), mass_loss_percent (%)
  - Degradation_PLA.csv
    - Time (months), PLA_content (%)
    - No data for Tbag-C
  - Degradation_prGCMS_TbagA.csv
  - Degradation_prGCMS_TbagB.csv
  - Degradation_prGCMS_TbagC.csv
    - Pyrolysis-GCxGC-TOF MS data for chemical characterization
    - Columns include 1tR (retention time 1st column), 2tR (retention time 2nd column), Compound, ions
    - Data presented for A, B, and C teabags respectively

- Key calculations and data structure
  - Mass loss percentage
    - mass_loss_percent = 100 × (1 − final_mass / initial_teabag_mass)
  - PLA content vs cellulose content
    - Teabags dissolved in chloroform (30 minutes at room temp) to separate PLA
    - PLA_content used to compute cellulose:PLA ratio via
      cellulose:PLA = mass_cellulose / (mass_cellulose + mass_PLA) : mass_PLA / (mass_cellulose + mass_PLA)
  - Crystallinity
    - Measured by Dynamic Scanning Calorimetry (DSC) with a predefined thermal program
    - Crystallinity (%) = [(ΔHm − ΔHcc) / ΔH100%] × 100
    - ΔHm: enthalpy of melting; ΔHcc: enthalpy of cold crystallisation; ΔH100% (PLA) = 93 J g−1
    - Enthalpy precision: 0.1%

- Analytical methods and instrumentation
  - DSC for crystallinity assessment (Discovery DSC25, TA Instruments)
    - Heating/cooling at 20 °C/min under nitrogen
    - Thermal cycle and calibration details provided
  - Pyrolysis-GCxGC-TOF MS for chemical composition
    - Instrumentation: Pyroprobe (600 °C, 30 s) with DISC, coupled to GC and BenchTOF2-TOF MS
    - Columns: deactivated guard column, BPX5 1D column, BPX50 2D column
    - Data processing: ChromSpace; compounds identified via NIST Mass Spectral Search
    - Analysis performed in triplicate per teabag type
  - Sample mass and measurement details
    - Teabags from each type analyzed after field retrieval: washed, dried, vacuum-sealed, stored at 4°C
    - Mass measurements: analytical balance with four decimal places; calibrations performed beforehand
  - Quality control (QC) details
    - Teabags sourced from multiple boxes/LOTS to ensure variability
    - DSC: teabag samples 1–3 mg per measurement
    - Py-GCxGC-TOF MS: triplicate analyses; regular blank/run-cleaning between teabag types

- Data provenance and publication
  - Data accompany the research output: Courtene-Jones et al. 2024
  - Title: Deterioration of bio-based polylactic acid plastic teabags under environmental conditions and their associated effects on earthworms
  - Journal: Science of the Total Environment
  - DOI: https://doi.org/10.1016/j.scitotenv.2024.172806
  - Funded by: NERC BIO-PLASTIC-RISK project, Grants NE/V007556/1 and NE/V007246/1

- Notes on data completeness and applicability
  - Data availability varies by teabag type:
    - Tbag-A and Tbag-B: crystallinity and PLA content data present; mass data present
    - Tbag-C: crystallinity and PLA content data are not provided; prGCMS data exist
  - Data are anonymised, with brands labeled A–C
  - Data structure and units are described within each file’s documentation

- How this dataset supports data use and insights
  - Enables cross-domain analysis: physical (mass loss, crystallinity) and chemical (PLA proportion, pyrolysis products) changes
  - Facilitates baseline comparisons for bio-based teabag degradation under realistic soil conditions
  - Supports integration with ecological impact analyses (e.g., effects on soil organisms)
  - Suitable for creating self-serve data products (dashboards, dashboards linking mass loss, crystallinity, and chemical composition over time) and for validating models of bioplastic degradation

- Considerations for data users
  - Be aware of missing data for Tbag-C in crystallinity and PLA content files
  - Interpret chemical composition data within the context of triplicate analyses and GC×GC-TOF MS identification limitations
  - Align units and definitions as documented when merging with external datasets (e.g., mass units, crystallinity percentages)