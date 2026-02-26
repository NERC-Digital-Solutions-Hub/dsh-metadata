# Degradation characteristics of bio-based teabags buried in soil, UK, November 2021 - June 2022

## Study purpose and context
- Investigates chemical deterioration and material changes of three anonymised bio-based PLA–cellulose teabags after 7 months buried at -10 cm in UK soil (Nov 2021–Jun 2022).
- Supported by the NERC BIO-PLASTIC-RISK project.
- Data intended to support understanding of environmental fate and degradation of bio-based plastics, with potential relevance for policy and monitoring frameworks.

## Datasets and structure
- Six CSV data files:
  - Degradation_crystallinity.csv
  - Degradation_Mass.csv
  - Degradation_PLA.csv
  - Degradation_prGCMS_TbagA.csv
  - Degradation_prGCMS_TbagB.csv
  - Degradation_prGCMS_TbagC.csv
- Teabags are anonymised (A, B, C). Time points up to 7 months; multiple measurements per teabag type.
- Teabags sourced from at least five boxes across different LOT codes; analyzed post-collection under controlled QA conditions.

## Measurements and methods
- Mass loss
  - Calculation: mass_loss% = 100 × (1 − m/m0), where m is final mass after burial and m0 is initial mass.
- PLA content
  - Determined by dissolving PLA in chloroform to estimate cellulose:PLA ratio from dried masses.
- Crystallinity
  - Measured by Dynamic Scanning Calorimetry (DSC) with a defined heating/cooling program.
  - Crystallinity (%) computed as: ((ΔHm − ΔHcc) / ΔH100%) × 100; ΔHm = melting enthalpy, ΔHcc = cold crystallisation enthalpy, ΔH100% = 93 J g−1 for 100% crystalline PLA.
  - Enthalpy precision of 0.1%.
- Chemical composition
  - Pyrolysis coupled to 2D gas chromatography and time-of-flight MS (Py-GCxGC-TOF MS) for teabag A/B/C.
  - Sample amount: 80–100 µg for Py-GCxGC-TOF MS; pyrolysis at 600 °C for 30 s.
  - Data processed with ChromSpace; compounds identified via NIST library.
- Data structure and units
  - Crystallinity file: Tbag, Time (months), crystallinity (%). Note: no data for Tbag-C.
  - Mass file: Tbag, Time (months), initial_teabag_mass (g), final_mass (g), mass_loss (g), Mass_loss_percent (%).
  - PLA file: Tbag, Time (months), PLA_content (%). Note: no data for Tbag-C.
  - prGCMS files: retention times, compound names, ions, etc. (per teabag A/B/C).

## Data structure and contents (key details)
- Degradation_crystallinity.csv
  - Columns: Tbag (A/B), Time (months), crystallinity (%).
  - Missing crystallinity data for Tbag-C.
- Degradation_Mass.csv
  - Columns: Tbag (A/B/C), Time (months), initial_teabag_mass (g), final_mass (g), mass_loss (g), Mass_loss_percent (%).
- Degradation_PLA.csv
  - Columns: Tbag (A/B), Time (months), PLA_content (%).
  - Data not available for Tbag-C.
- Degradation_prGCMS_TbagA.csv, Degradation_prGCMS_TbagB.csv, Degradation_prGCMS_TbagC.csv
  - Contain retention times (1tR, 2tR), Compound, and ions for each teabag type; data presented in a uniform structure.

## Quality control and provenance
- Sampling from diverse sources (≥5 boxes) across Plymouth, UK (Jul–Oct 2021).
- Post-collection handling: washed, dried, vacuum-packed and stored at 4°C.
- Instrument calibration and measurement accuracy:
  - Mass measurements calibrated; DSC enthalpy precision 0.1%.
  - Py-GCxGC-TOF MS analyses performed in triplicate per teabag type.
- Detailed methodological parameters provided for traceability and reproducibility.

## Data usage and relation to the publication
- Data accompany Courtene-Jones et al. (2024) Science of the Total Environment: Deterioration of bio-based polylactic acid plastic teabags under environmental conditions and their associated effects on earthworms.
- DOI: https://doi.org/10.1016/j.scitotenv.2024.172806

## Policy and monitoring implications
- Provides a multi-endpoint dataset (mass loss, crystallinity, PLA content, and chemical fingerprint) to monitor environmental degradation of bio-based plastics in soil.
- Demonstrates the importance of standardized metadata, transparent data sharing, and data governance to enable reuse in monitoring frameworks.
- Highlights data gaps and practical challenges (e.g., incomplete data for some teabag types) that policymaking and monitoring programs should plan for, including cross-institution data harmonisation and metadata completeness.