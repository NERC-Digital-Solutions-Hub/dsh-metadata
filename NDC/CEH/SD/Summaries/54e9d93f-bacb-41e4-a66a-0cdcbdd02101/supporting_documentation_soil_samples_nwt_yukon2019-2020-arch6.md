# Environmental context and metadata for permafrost soil samples, NWT & YT, Canada, 2020

- Scope and purpose
  - Dataset documenting carbon (C) and nitrogen (N) content of permafrost soil samples from the Northwest Territories and Yukon, Canada, collected in 2019 and 2020.
  - Includes 14 soil profiles across three regions (East Channel, Tuktoyaktuk, Klondike) and four soil types (orthels, turbels, yedoma deposits, and related variants).
  - Aims to support understanding of soil C and N stocks in permafrost environments and facilitate comparative analyses across different geomorphic settings.

- Data structure and contents
  - Source CSV: Soil_samples_NWT_Yukon2019-2020.csv
  - The dataset comprises 14 columns describing each sample (as detailed in the accompanying “Nature and Units of recorded values” section).
  - Key fields include:
    - Sample identifiers (year-coded and unique sample numbers)
    - Location details (latitude and longitude in Degrees Minutes Seconds)
    - Depth below ground surface
    - Date collected
    - Total sample mass
    - C content (%)
    - N content (%)
    - Short description and interpretation of the sample
    - Sampling method
    - Storage during fieldwork
  - Each sample is linked to a soil profile and site description.

- Geographic and temporal coverage
  - Regions: East Channel (EC), Tuktoyaktuk (T), Klondike (K)
  - Sampling years: 2019 (August) and 2020
  - Profiles numbered #1–#14, representing four soil profile types across multiple locations

- Collection and site context
  - Sampling methods: soil pits, coring, and horizontal drill holes into thaw slumps
  - Soil profile types:
    - Non-lake orthels
    - Drained thermokarst-lake sediments
    - Turbels on till
    - Yedoma deposits
  - Depths and active-layer characteristics (ALT) recorded for each profile
  - Ground ice observations reported per profile (where applicable)

- Analytical methods and quality control
  - CN analysis conducted at University of Exeter (processed from frozen samples after return)
  - Instrument: Thermo Scientific Flash 2000 Elemental Analyser
  - Sample preparation: homogenised soil, ~10 g subsamples, dried to constant weight
  - Quality control: EDTA standards used at start and as check standards every 10 samples
  - Reported results: Carbon and Nitrogen content expressed as percentages (C content, N content)

- Metadata and documentation
  - Detailed site descriptions, geomorphic context, vegetation, organic and mineral soil characteristics, ALT values, and permafrost indicators included for each profile
  - Environmental reconstruction context provided for Tuk Harbour area (palaeoenvironmental sequence T1–T6)
  - Sampling notes include photographer figures and site sketches to aid interpretation

- Data usability and potential products
  - Enables cross-site comparisons of C and N stocks across permafrost types and geomorphic settings
  - Suitable for integration with active-layer depth, ground ice data, and local environmental variables to model carbon and nitrogen dynamics in Arctic permafrost soils
  - Supports creation of dashboards or visualizations mapping CN content against depth, ALT, soil type, and region
  - Useful for informing permafrost carbon stock assessments and related policy or management discussions at regional scales

- Considerations and caveats
  - Profiles reflect diverse permafrost contexts with variable cryoturbation and ice-wedge features; data interpretation should consider local geomorphology
  - Some sites show multiple depths with organic-rich versus mineral-rich layers, highlighting within-profile heterogeneity
  - CN results are point measurements per sample; spatial interpolation should account for within-profile variability and uneven sampling across profiles

- Access and provenance
  - Data collected by a coordinated team (2019–2020) with processing and CN analysis performed at a dedicated laboratory
  - Frozen storage maintained from field collection through analysis, with explicit documentation of storage and transport procedures

- How to use with Data Support tools
  - Validate asks by filtering by region, soil type, or depth to extract CN profiles for a given context
  - Combine with ALT and ground ice indicators to assess relationships between permafrost features and C/N stocks
  - Generate self-serve data products (e.g., CN content heatmaps by profile) and collect user feedback for potential refinements or additional data products