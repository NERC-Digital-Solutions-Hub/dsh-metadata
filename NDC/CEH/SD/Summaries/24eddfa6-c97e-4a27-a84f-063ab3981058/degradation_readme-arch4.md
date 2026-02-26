# Degradation characteristics of bio-based teabags buried in soil, UK, November 2021 - June 2022

- Overview
  - Investigates chemical deterioration and material changes of three anonymised bio-based PLA-cellulose teabags after 7 months buried in UK soil at ~10 cm depth (Nov 2021 – Jun 2022).
  - Funded by the NERC BIO-PLASTIC-RISK project; data accompany Courtene-Jones et al. (2024) in Science of the Total Environment.
  - Dataset comprises six files, with teabags sourced from at least five boxes across multiple stores to ensure variability; teabags labelled A-C as anonymised brands.

- What is in the dataset
  - Measurements covering physical and chemical changes:
    - Mass loss during 7 months of soil burial.
    - Proportion of cellulose to PLA in the teabags and how it changes after burial.
    - Crystallinity changes of the material after burial.
    - Chemical composition of teabags before burial via pyrolysis-GCxGC-TOF MS.
  - Data are organized to support material degradation analysis, with explicit data structures and units.

- Data files and structure
  - Degradation_crystallinity.csv
    - Tracks crystallinity (%) over time for anonymised teabag brands (Tbag-A, Tbag-B; no data for Tbag-C).
    - Columns: Tbag, Time (months), crystallinity (%).
  - Degradation_Mass.csv
    - Mass loss measurements for each teabag over 7 months.
    - Columns: Tbag (A/B/C), Time (months), initial_teabag_mass (g), final_mass (g), mass_loss (g), Mass_loss_percent (%).
  - Degradation_PLA.csv
    - Proportion of PLA in teabags and its change after burial (7 months).
    - Columns: Tbag (A/B), Time (months), PLA_content (%). NAN indicates no data (e.g., for Tbag-C).
  - Degradation_prGCMS_TbagA.csv, Degradation_prGCMS_TbagB.csv, Degradation_prGCMS_TbagC.csv
    - Pyrolysis-GCxGC-TOF MS data detailing compound identities and retention times for each teabag type (A, B, C).
    - Columns include retention times for two GC columns and identified compounds with associated ions; provided in triplicate analyses.
  - Notes: All teabag brands are anonymised; data units and column definitions are specified in each file.

- Methods and calculations
  - Mass loss calculation
    - mass_loss (%) = 100 - (m / m0) * 100, where m is final mass after burial and m0 is initial mass (before burial).
  - Cellulose:PLA proportion
    - After dissolving PLA in chloroform (30 min at room temperature), remaining solid mass yields PLA, enabling cellulose:PLA ratio calculation:
      cellulose:PLA = m_colulose / (m_colulose + m_PLA) : m_PLA / (m_colulose + m_PLA).
  - Crystallinity
    - Determined by Dynamic Scanning Calorimetry (DSC) with a multi-step heating/cooling program; crystallinity (%) computed as:
      Crystallinity (%) = (ΔHm − ΔHcc) / ΔH100% × 100,
      where ΔHm is the enthalpy of melting, ΔHcc is the enthalpy of cold crystallisation, and ΔH100% = 93 J g−1 (theoretical for 100% crystalline PLA).
    - Enthalpy precision: 0.1%.
  - Chemical composition (pre-burial)
    - Pyrolysis coupled to 2D GC and TOF MS (Py-GCxGC-TOF MS) used to characterize new teabag materials; 80–100 µg per sample analyzed in triplicate.

- Analytical and quality-control details
  - Sampling and provenance
    - Teabags obtained from at least five different boxes (diverse LOT codes) across Plymouth, UK (Jul–Oct 2021).
  - Sample handling
    - Post-retrieval, samples washed, dried, vacuum-sealed in Mylar within polyethylene bags; stored at 4°C.
  - Measurements and instrumentation
    - Mass: Analytical balance (four decimal places); calibrations performed prior to use.
    - DSC: 1–3 mg samples; enthalpy precision 0.1%.
    - Py-GCxGC-TOF MS: Injections in triplicate; instrument setup includes DISC, specific GC columns, and a TOF MS; data processed with ChromSpace; compounds identified via NIST library.
  - Data integrity
    - Teabags subjected to cleaning between different teabag types; blank runs performed for DSC calibration and instrument checks.
  - Data usage context
    - The dataset supports evaluation of environmental degradation of bio-based plastics and potential ecological effects (e.g., on earthworms) as described in the accompanying publication.

- Data use and provenance
  - Link to publication: Courtene-Jones et al. 2024, Science of the Total Environment.
  - Data structure documented with explicit units, definitions, and data-capture protocols to support reuse and interoperability.