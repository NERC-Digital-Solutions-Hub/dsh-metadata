# Description of data files

- Overview
  - Estimates of plant abundance (leaf area, floral units, seeds by number, mass, and energy) from field sampling on Norwood Farm, Somerset, UK (2007–2008) during a study of ecological interactions.
  - Farm managed as organic at low intensity.
  - Primary reference: Pocock et al. (2012); dataset of interactions published in Dryad (DOI provided). Full study details available in Pocock et al. (2012) and Supplementary Online Material (SOM).

- Datasets and key fields
  - leafarea.csv
    - Fields: SamplingRound, Month, Year; HabitatCode (via habitatarea.csv); PlantTaxon; PlantFamily; LEAFAREA_square_metres.
    - Method: surveys of 4 transects per habitat per month; leaf area index measured (LAI) and apportioned among species by relative abundance/heights; LAI scaling to habitat area.
  - floralunits.csv
    - Fields: SamplingRound, Month, Year; HabitatCode; PlantTaxon; PlantFamily; FLORALUNITS_total.
    - Method: surveys of 3–4 transects per habitat per month; floral units defined as flower-visiting entities insects fly between.
  - seeds.csv
    - Fields: Season, HabitatCode, PlantTaxon, PlantFamily, SEEDS_TotalCount, SEEDS_MassInKg, SEEDS_EnergyInKJ.
    - Method: vacuum-seeded samples (up to 39 per habitat/month); seeds oven-dried and identified; under-sampling corrected using a site-derived factor; mass/energy from site data and databases; scaled by habitat area; cross-year mapping (Year1/Year2) noted.
  - habitatarea.csv
    - Fields: HabitatCode; HabitatDescription; Area_in_Year1_square_metres; Area_in_Year2_square_metres.
    - Notes: Year mappings align with leafarea/floralunits (Year1 = 2007; Year2 = 2008 for these datasets; seeds data mapped to autumn 2007), with farm map referenced in related publications.

- Data provenance and methods
  - Full methods described in Pocock et al. (2010) and Pocock et al. (2012) supplementary material; Extract_from_SOM.rtf included in the dataset package.
  - Related references detail efficiency of sampling devices (e.g., seed vacuum) and the role of farm management in resource distributions.

- Data quality, completeness, and limitations
  - Seed data include a correction factor to account for under-sampling.
  - Some estimates are scaled by habitat area and may depend on cross-year habitat area estimates.
  - Metadata includes taxon names, plant family, habitat codes to support traceability and reuse.
  - Data are tied to a specific study site and period; broader generalization should consider site-specific contexts.

- Governance, usage, and access
  - Primary publication and Dryad entry provide the official data provenance and usage guidance.
  - Acknowledged funders: BBSRC (grant no. BBD0156341) and Defra (grant no. BD2303).
  - For reuse, reference Pocock et al. (2012) and consult the associated Supplementary Online Material.

- Data stewardship considerations
  - Standards and consistency: ensure unit consistency (LEAFAREA_square_metres, SEEDS_MassInKg, SEEDS_EnergyInKJ) and uniform taxon naming across files.
  - Metadata completeness: rely on habitatarea.csv as the key habitat reference; maintain links between leafarea, floralunits, seeds, and habitat areas.
  - Data updates and versioning: clearly indicate year mappings and any re-derivations (e.g., seed under-sampling corrections); document any changes to habitat area assumptions.
  - Interoperability: document data collection methods, transect dimensions, and equipment (LAI-2000) to support interoperability with similar datasets.
  - Reuse considerations: provide references to primary publications and SOM to enable proper interpretation of methods and scaling factors.

- Summary of purpose and alignment with Data Steward aims
  - The dataset supports understanding plant abundance components (leaf area, flowers, seeds) across habitats and times, aiding ecological network analyses.
  - Clear documentation of data collection, processing, and scaling facilitates discovery, interoperability, and reuse.
  - Governance-oriented notes (metadata, units, provenance, limitations) help ensure data standards are met and datasets remain usable and up-to-date for downstream users.