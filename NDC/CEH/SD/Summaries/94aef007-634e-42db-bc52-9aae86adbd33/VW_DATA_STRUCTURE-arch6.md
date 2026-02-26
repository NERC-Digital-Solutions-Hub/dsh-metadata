# Explanatory Information: Species codes

- Purpose: Provides a mapping between numeric species/taxon codes and their scientific names, including synonyms and cross-references, to support consistent data labeling in ECN vegetation datasets.
- Content scope:
  - Numeric codes (e.g., 2254, 2947, 5448, etc.) are linked to species names or taxon concepts (e.g., Riccardia chamedryfolia, Rosa arvensis, Rubus idaeus) and often include alternative names or synonyms (e.g., Riccardia multifida, Rosa canina agg., Rubus idaeus).
  - Subcodes and alternatives: Some entries show multiple subcodes for the same base code (e.g., 2699, 1 = Salix cinerea ssp oleifolia; 2 = Vas_1786; 3 = Salix cinerea subsp. oleifolia), indicating alternative taxonomic treatments or data provenance.
  - Cross-references: Many mappings imply cross-referencing to other taxonomic lists or databases, ensuring compatibility with broader taxonomic nomenclatures.
  - Taxonomic breadth: The list covers a wide range of taxa including bryophytes, ferns, gymnosperms, angiosperms, lichens, and other plant or related taxa encountered in ECN plots.
- Usage implications:
  - Enables robust data integration across sites and time by standardizing taxon labels.
  - Supports downstream analyses, reporting, and data sharing by ensuring consistent naming conventions and alias handling.
  - Facilitates mapping to external taxonomies (e.g., BRC or other references) through explicit name mappings and synonyms.

# Explanatory Information: Quality Codes

- Purpose: Defines the coding scheme used to annotate data quality issues encountered during field sampling, laboratory processing, and data handling.
- Code ranges and meanings:
  - 100–199: No information available or sampling issues (e.g., 100 No information available; 101 No sample/reading taken; 102 Sample lost; 103 Partial loss of sample; 104 Sample frozen; 105–118 various contamination or in-sample issues; 119–135 contextual or environmental disturbances).
  - 136–169: Field-related disturbances or non-survey events (e.g., obstruction, flooding, mowing, grazing, trampling, weather-related disruptions).
  - 170–189: Hydrological or instrument-related conditions (e.g., river/lake conditions, rain, snow, gauge issues).
  - 190–199: Additional observational or sampling anomalies (e.g., trace rainfall, water in funnel, non-standard sampling date/time).
  - 200–233: Adverse conditions affecting sampling/recording, biological presence in traps, or wildlife interactions.
  - 234–237: Miscellaneous or estimated counts, taxon identification confidence notes.
  - 501–507: Laboratory-related issues (e.g., no sample in lab, sample lost, contamination, insufficient material, equipment failure).
  - 508–513: Laboratory/chemical analysis specifics (e.g., deposits on filters, non-standard sub-sampling, measurement constraints).
  - 999: Unusual event; see quality text for details.
- Usage implications:
  - These codes provide context for data quality, enabling users to filter, weight, or interpret measurements based on data reliability.
  - The associated descriptions (e.g., “No sample/reading taken,” “Sample lost or discarded,” “Adverse weather conditions affected sampling”) support reproducibility and transparent data provenance.
  - The quality notes can be consulted to assess data suitability for specific analyses and to understand potential biases or gaps in the dataset.