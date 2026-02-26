# Materials and methods for soil, water and sediment data extracted from: Background exposure rates of terrestrial wildlife in England and Wales

- Purpose and scope
  - Describes how data on naturally occurring radionuclides in soil, water, sediment, and biota around England and Wales were gathered, processed, and mapped to ICRP reference animals and plants (RAPs) for dose assessment in non-human species.
  - Aims to categorize and integrate disparate data sources to support exposure assessments across terrestrial ecosystems.

- RAPs used for data categorisation
  - Reference Deer; Reference Rat; Reference Duck; Reference Frog; Reference Bee; Reference Earthworm; Reference Pine Tree; Reference Wild Grass.
  - Approach: map available data to RAPs, using broad assignments (e.g., any wild mammal to Reference Deer or Reference Rat; any wild bird to Reference Duck; any grass to Reference Wild Grass).

- Data sources and availability
  - Data drawn from multiple sources: grey literature, refereed journal articles, and in-house databases.
  - Key sources:
    - RIFE (Radioactivity in Food and the Environment) reports (UK-wide data from 1995–2004, including biota of edible concern).
    - CEH analyses of radiocaesium and other radionuclides from Sellafield and post-Chernobyl contexts.
    - G-BASE (Geochemical Baseline Survey of the Environment) soil, sediment, and water data (K, U, Th) across the UK; datasets normalised and extrapolated to England and Wales.
  - Data were attributed to RAPs when exact RAP-specific data were not available, and gaps were identified for targeted follow-up.

- Sampling and analyses
  - Targeted sampling campaign to address data gaps for Duck, Bee, Earthworm, Pine Tree, and Frog.
  - Samples collected (where available) from archives and new sampling:
    - Flying insects (80+ samples from Environmental Change Network sites)
    - Lodgepole pine trunk (5 samples)
    - Grey heron liver (20 samples)
    - Earthworms (6 samples)
    - Rabbits (4)
    - Toads (1)
    - Mallards (5)
  - Wales had limited data; efforts extended to supplement Welsh samples (e.g., rabbits, mallards, pine, earthworms).
  - Sample preparation and analyses:
    - Insects: dried and homogenised; pine trunks washed and ashed.
    - Biota: tissues prepared (liver, GI tract removal, etc.) and analysed by gamma spectrometry (hyperpure germanium detectors) to determine gamma-emitting radionuclide activities; count times ~2 days.
    - U and Th: total concentrations measured by ICP-MS after acid digestion; detection limits on the order of 10^-2 to 10^-3 mg/kg FW.
    - Assumptions:
      - Secular equilibrium between 238U and 234U in biological samples.
      - Equilibrium between parents and other 238U/232Th decay-chain members may not hold due to differing chemistries.

- Derivation of soil activity concentrations
  - BGS G-BASE baseline data underpin soil activity concentrations for 40K, 238U, and 232Th.
  - Sampling design:
    - Approximately one sample per 2 km^2 for soils; adjacent sampling and data integration from related datasets (including Wolfson Atlas) to increase coverage.
  - Normalisation and data integration:
    - Normalisation between different analytical techniques and sample types (surface vs. subsurface soils) via linear quantile transformation and other methods described in Beresford et al. (2007).
    - Extrapolation used to derive more complete coverage where direct measurements were sparse, based on relationships between soils/sediments and bedrock/superficial geology.
  - Spatial aggregation:
    - For soils and sediments: compute geometric means within 25 km^2 grid squares from the nearest five samples per parent material; combine measured and extrapolated data.
    - For waters: derive geometric mean concentrations where data are available; caveats noted due to weaker or non-existent strong geology-radioelement relationships for extrapolation.
  - Activity concentration calculations:
    - Use specific activity values: 31.6 Bq g^-1 K, 4.07 Bq mg^-1 232Th, 12.21 Bq mg^-1 238U to estimate radionuclide concentrations from total element concentrations.
    - Assumptions of quasi-equilibrium used where appropriate (e.g., 232Th series; 238U series with 234U).
  - Data presentation:
    - A structured Terrestrial biota database/worksheet with fields such as species, RAP, location (easting/northing), sampling date, activity concentrations (Bq/kg FW), tissue sampled, references, and data quality flags (LOD handling, etc.).

- Data integration, metadata, and references
  - Terrestrial biota data compiled from published literature, archives, and targeted sampling; references linked to a structured dataset with provenance notes.
  - Core references include:
    - G-BASE project documentation and methods
    - Assessments and methodological papers on naturally occurring radionuclides around England and Wales
    - RIFE series reports and associated radiological impact studies

- Limitations and considerations for reuse
  - Uneven data coverage across the UK, with notable gaps in Wales and certain RAPs.
  - Temporal gaps (data largely from 1990s–early 2000s) may affect current applicability.
  - Dependence on equilibrium assumptions for certain decay chains and on extrapolation methods where direct measurements are missing.
  - Metadata and documentation are critical to correctly map data to RAPs and to interpret grid-based aggregations and extrapolations.

- Implications for data governance and reuse
  - Demonstrates the importance of integrating heterogeneous data sources with clear RAP mappings for environmental dose assessments.
  - Highlights the need for robust metadata, standardised units, and transparent normalisation/extrapolation procedures when assembling cross-source datasets.
  - Provides a model for combining archival data with targeted sampling to fill knowledge gaps while maintaining traceability to original sources.