# Landscape point feature data 1998 [Countryside Survey], Great Britain

- Overview
  - Landscape point features dataset from 538 1km squares across Great Britain, sampled in 1998/99.
  - Part of the Countryside Survey project, data owned by NERC - Centre for Ecology & Hydrology (CEH).
  - Version: 1: 04-2-2016.

- Data Content and Structure
  - Source: LANDSCAPE_PT_FEATURES_1998.csv.
  - Columns cover: location (SQUARE), survey year (YEAR), unique per-year ID, theme codes and names (THEME, THEME_NAME), primary attributes (PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME), species codes/names (SPECIES, SPECIES_NAME), abundance/cover (PROPORTION, PROPORTION_RANGE), land use (USE, USE_NAME), various veteran-tree and habitat indicators (BUFFER, TREE_DEAD, MISSING_LIMBS, DEAD_WOOD, DEAD_MISSING_BARK, LIGHTNING_STRIKES, HOLLOW_TRUNK), modal DBH (MODAL_DBH, MODAL_DBH_RANGE), veteran tree type (VETERAN_TREE_TYPE, VETERAN_TREE_TYPE_NAME), epiphyte and ivy cover (EPIPHYTE_COVER, EPIPHYTE_COVER_NAME, IVY_COVER, IVY_COVER_RANGE), canopy cover (CANOPY_LIVE, CANOPY_LIVE_RANGE), land classification (LC07, LC07_NUM), and location metadata (COUNTRY, COUNTY07, EZ_DESC_07).
  - Notable standards referenced: ITE Land Classification of Great Britain (2007) and related metadata/classifications.
  - Data usage notes: All CS data usage must be acknowledged with the specified citation.

- Data Standards, Quality, and Provenance
  - Data governance: Dataset adheres to Countryside Survey methodologies; designed for clear discovery and reuse within large dataset environments.
  - Metadata richness: Includes coded fields with both numeric codes and human-readable names for themes, attributes, species, and classifications.
  - Quality considerations: Data owners emphasize quality assurance, cleaning, transformation prior to sharing; consistent coding and alignment with external classifications (e.g., LC07) to enable interoperability.
  - Provenance: Data documented with year of survey, sampling design (538 1km squares), and references to methodological publications.

- Usage, Licensing, and Citation
  - Acknowledgement requirements: All use, copies, publications, and presentations must acknowledge Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
  - Copyright: Countryside Survey ©; Database Right/Copyright NERC-CEH. All rights reserved.
  - References and context: Publication and methodology links provided (e.g., Countryside Survey website, ITE Land Classification references, JNCC guidance), facilitating proper interpretation and downstream integration.

- Data Sharing, Discovery, and Update Considerations
  - Sharing and portals: Dataset intended for upload to relevant portals and catalogues; metadata supports discoverability and data holdings integration.
  - Updates and maintenance: Versioned release (V1 in 2016) implies the need for governance around future updates, new survey years, and reprocessing if standards evolve.
  - Limitations and constraints: Potential data availability limits to be managed (not explicitly stated here but consistent with governance principles for large, multi-system datasets).

- Governance and Stewardship Actions for Data Stewards
  - Align data practices with user needs: Document and validate how themes, attributes, and classifications map to user requirements; consider publishing mindset to enhance usability.
  - Ensure metadata completeness and clarity: Maintain codebooks for THEME, PRIMARY_ATTRIBUTE, SPECIES, LC07, and other coded fields; keep documentation for units, ranges, and interpretation.
  - Maintain data quality: Apply QA processes to verify accuracy, consistency, and formatting before sharing; resolve anomalies across many fields (binary indicators, range descriptors, and categorical codes).
  - Manage interoperability: Preserve alignment with external classifications (ITE LC07) to facilitate integration with other datasets and analyses.
  - Address data access and governance constraints: Adhere to acknowledgement and copyright requirements; manage embargoes, licensing, and metadata updates.
  - Plan for updates and scale: Prepare for new survey years and potential format changes; ensure version control and clear change logs.
  - Anticipate challenges: Mitigate incomplete user needs, ensure timely data provision from data creators, harmonize diverse systems/formats, and handle large transfer needs.

- References and Related Publications
  - Countryside Survey website and methodologies.
  - ITE Merlewood Land Classification and ITE Land Classification of Great Britain 2007.
  - JNCC guidance on biodiversity broad habitats and classifications.
  - Specific datasets and DOIs/links cited for background and methodology.