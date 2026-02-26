# Degradation characteristics of bio-based teabags buried in soil, UK, November 2021 - June 2022

- Purpose and scope
  - Dataset describes chemical deterioration and material changes of three anonymised bio-based PLA–cellulose teabags after 7 months buried in UK soil (-10 cm).
  - Supported by NERC BIO-PLASTIC-RISK project; teabags labeled A–C but brands are anonymised.
  - Data accompany a Science of the Total Environment publication (Courtene-Jones et al., 2024).

- Data products (6 files)
  - Degradation_crystallinity.csv: changes in material crystallinity after 7 months.
  - Degradation_Mass.csv: teabag mass loss after burial (initial vs final mass; mass_loss; Mass_loss_percent).
  - Degradation_PLA.csv: proportion of PLA in teabags after burial (PLA_content); note NAN where data are missing.
  - Degradation_prGCMS_TbagA.csv, Degradation_prGCMS_TbagB.csv, Degradation_prGCMS_TbagC.csv: chemical composition of teabags via Py-GCxGC-TOF MS; data presented in the same structure for A, B, and C.
  - Data structure and units are described within each file; some data gaps exist (see below).

- Measurements and calculations
  - Mass loss calculation: mass_loss_percent = 100 × (1 − m / m0), where m is final mass after burial and m0 is initial mass.
  - Cellulose:PLA proportion: cellulose:PLA = m_cellulose / (m_cellulose + m_PLA) : m_PLA / (m_cellulose + m_PLA) after dissolving PLA in chloroform and drying to determine PLA content.
  - Crystallinity: calculated from DSC data as Crystallinity (%) = [(ΔHm − ΔHcc) / ΔH100%] × 100; ΔHm is melting enthalpy, ΔHcc is cold crystallisation enthalpy, ΔH100% for 100% crystalline PLA is 93 J/g. DSC protocol details (heating/cooling rates, nitrogen, program) are provided.
  - Py-GCxGC-TOF MS: chemical characterization using pyrolysis with two-dimensional GC and TOF MS; detailed instrumental setup and program described; samples analyzed in triplicate (80–100 μg per teabag type).
  - Data fields per file outline (examples):
    - Degradation_crystallinity.csv: Tbag (A/B, with C missing), Time (months), crystallinity (%).
    - Degradation_Mass.csv: Tbag (A/B/C), Time (months), initial_teabag_mass (g), final_mass (g), mass_loss (g), Mass_loss_percent (%).
    - Degradation_PLA.csv: Tbag (A/B), Time (months), PLA_content (%); Tbag C data not included.
    - Degradation_prGCMS_Tbag*.csv: columns for retention times, Compound, ions, etc. (structure described).

- Data provenance and quality control
  - Sampling: teabags sourced from at least five boxes across multiple stores in Plymouth, UK (July–October 2021) to capture variability.
  - Sample handling: washed, dried, vacuum-sealed in Mylar and polyethylene bags; stored at 4°C until analysis.
  - Measurements: mass calibrated with an analytical balance; DSC enthalpy accuracy ±0.1%; Py-GCxGC-TOF MS analyses run in triplicate per teabag type; cleanings between samples.
  - Anonymisation and labeling: teabag brands are anonymised (A–C); data note that Tbag-C has incomplete data for some measures (NANs in Degradation_PLA.csv and missing crystallinity data for Tbag-C).

- Data use and availability
  - Intended for understanding degradation pathways and material changes in bio-based PLA–cellulose teabags under environmental conditions.
  - Associated publication: Courtene-Jones et al. (2024) in Science of the Total Environment; DOI provided with dataset reference.
  - Data are organized for reuse by data curators, researchers, and practitioners interested in bioplastic degradation, including researchers and policy stakeholders.

- Governance, standards, and recommendations for Data Stewards
  - Metadata and documentation should be preserved alongside the dataset, including:
    - Dataset title, authors, affiliations, funding (BIO-PLASTIC-RISK), and data publisher.
    - Project context, sampling timeline, and soil burial conditions (depth, duration, location).
    - Detailed data dictionaries for each file, including variable names, descriptions, units, and calculation formulas.
    - Data lineage: original measurements, processing steps (mass loss, PLA content, crystallinity, GC-MS analysis), and any transformations.
    - Anonymisation note for teabag brands (A–C) and the rationale.
    - Quality control procedures and calibration details; instrument settings where provided.
    - Data access and reuse guidance, including licensing status (not specified in the document) and citation requirements (cite the associated publication).
  - Interoperability considerations:
    - Ensure consistent units across files (mass in grams, time in months, crystallinity in percent, PLA_content in percent).
    - Maintain consistent file naming and column naming conventions to facilitate cross-file joins (e.g., Tbag, Time).
  - Data gaps and transparency:
    - Document missing data: e.g., Tbag-C has no crystallinity data; NAN values appear in PLA content for Tbag-C.
  - Update and versioning:
    - Establish a versioned data portal entry and track future updates or additional burial conditions, if available.
  - Accessibility:
    - Link to the published article and provide a clear citation path; ensure persistent identifiers where possible.

- Practical implications for reuse
  - Suitable for meta-analyses on bioplastic degradation under soil conditions and cross-study comparisons with similar datasets.
  - Useful for policymakers and researchers evaluating environmental impact of bio-based teabags and material performance (mass loss, composition changes, crystallinity, and chemical byproducts).
  - The detailed GC–MS data support chemosemantic analyses of degradation products, with explicit instrumentation and program details enabling reproducibility.