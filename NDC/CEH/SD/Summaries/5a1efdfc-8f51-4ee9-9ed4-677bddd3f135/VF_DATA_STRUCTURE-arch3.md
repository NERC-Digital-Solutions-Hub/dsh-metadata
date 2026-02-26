# UK Environmental Change Network (http://www.ecn.ac.uk) Vegetation: Fine Grain (VF)

- The VF dataset captures vegetation data for environmental change monitoring and policy evaluation, sourced from the ECN Data Centre with multiple UK government department and agency sponsors.
- Users must acknowledge data use and share one reprint of publications citing the data; accompanying quality metadata aids interpretation and reproducibility.

## Data Provenance and Governance

- Originator and data management focus:
  - Dataset Originator: ECN Data Centre (Centre for Ecology and Hydrology).
  - Dataset Owners: ECN programme sponsors (e.g., Defra, Natural England, NERC, and others).
- Data management aims:
  - Ensure data quality through QA, cleaning, transformation, and clear presentation (reports, charts, dashboards).
  - Public sharing of underlying data is required but can be a barrier for some users.
  - Metadata gaps may hinder usability; authors may need to add metadata or coordinate with originators.
  - Data governance processes establish standards, storage, sharing, versioning, and up-to-date status.

## Dataset Structure and Content

- Core data structures (three types) stored per site:
  - D1VF_xxx: Fine-grain vegetation plots (plots and species presence).
  - D2VF_xxx: Environmental data (site conditions, pedology, land use, slope, aspect, etc.).
  - D3VF_xxx: Cell features (within-plot features).
- Site identifiers: T01–T12 with distinct site names and geographic coordinates.
- Core metadata: structure references and site-level metadata; detailed core metadata described in separate docs.
- Protocol highlights:
  - Two 10m x 10m plots sampled per NVC type per site.
  - Species presence recorded in 40cm x 40cm cells within plots.
  - Vegetation surveys every three years; some sites conduct annual surveys on a subset of plots to extend temporal coverage.
  - Users should apply accompanying quality information when using data.

## Sampling Design and Temporal Coverage

- Cadence: triennial vegetation surveys; some sites perform annual sampling on subsets.
- Data scope: vegetation data at plot level, environmental context, and cell-level features.

## Metadata, Data Quality, and Governance

- Metadata: core metadata tables plus separate quality information; users should consult accompanying quality documentation.
- Data quality checks: implemented through QA, cleaning, transformation, and summarization to support clear interpretation.
- Governance: data management standards for storage, sharing, versioning, and metadata completeness; processes maintain up-to-date datasets.

## Land Use, Topography, and Feature Coding

- Land Use: Hodgson codes (1–22) describing landscape uses (e.g., Ley grassland, cereals, various woodland types).
- Topography: SLOPE and SLOPEFORM with Hodgson conventions; aspect and NVCC classifications.
- Site features: descriptors for features such as paths, walls, streams, hedges, ditches, fences, banks, and boundaries.
- Environmental context fields include pedate data (PEDATE), land-use dates, and other site factors to contextualize vegetation data.

## Species and Vocabularies

- Extensive species vocabularies with:
  - Codes mapping to Latin names and BRC concepts.
  - Multiple identifiers per taxon (Latin name, BRC concept, and common/catalogue variants).
  - Coverage from higher taxa to fine-grained species, including many plants and ecological attributes.
- The vocabulary supports detailed species-level analyses; users should reference code lists to interpret identifiers.

## Data Use and Practical Reporting

- Outputs: reports, charts, dashboards intended to communicate complex findings accessibly.
- Usage requirements: acknowledge ECN and share a reprint of publications citing the data.
- Metadata and quality information provide guidance for interpretation and reproducibility.

## Quality Codes and Data Integrity

- ECN quality codes: a standard list used by site managers to annotate data quality factors (codes such as 100, 101, 102, etc., up to 513) and occasional 999 for unusual events with accompanying explanation text.
- Application: multiple applicable codes can be attached to a dataset to reflect various data quality issues (e.g., equipment failure, sample loss, weather effects, contamination, non-standard sampling, etc.).

## Key Challenges and Considerations for Monitoring Frameworks

- Data-related challenges:
  - Data gaps or uneven temporal coverage; access limitations or delays.
  - Silos within/between organisations hindering data integration.
  - Public data sharing requirements may limit some datasets.
  - Incomplete metadata complicating verification of suitability.
  - Harmonising formats and units across datasets requiring transformation.
  - Communicating multi-dimensional findings clearly to policymakers.
  - Establishing and maintaining robust data governance to ensure storage, sharing, and updates.

## Summary for Policy Monitoring and Decision-Making

- The VF dataset offers a comprehensive, multi-layered resource for environmental monitoring across 12 long-running sites, combining plot-, environment-, and cell-level data.
- Standardized metadata and extensive species vocabularies enable robust trend analysis and policy evaluation.
- Effective use depends on high-quality metadata, strong data governance, and clear communication of results, aided by outputs like dashboards and well-documented data provenance.
- Data quality is actively managed via ECN quality codes, with transparency about data issues through accompanying quality information.