# Explanatory Information: Species codes

- Purpose
  - Provides crosswalks between ECN species codes and alternative taxonomic names and references.
  - Helps analysts translate coded observations into meaningful, current or alternative nomenclature (Latin names and cross-references to other coding systems).

- What the entries show
  - Each line documents a mapping involving a numeric code and one or more taxonomic names.
  - Patterns include:
    - A code (e.g., 2254) associated with a species name and one or more alternative taxa (e.g., Riccardia chamedryfolia = Riccardia multifida).
    - Recurrent use of aliases or synonyms, illustrating cross-references across taxonomic concepts.
  - The mappings span a broad range of taxa, including bryophytes, ferns, flowering plants, lichens, and fungi, often with multiple shorthand or cross-referenced names.

- How to interpret examples
  - 2254, Riccardia chamedryfolia = Riccardia multifida
    - Code 2254 corresponds to Riccardia chamedryfolia, with Riccardia multifida as an alternative name in the cross-reference.
  - 2947, Riccardia chamedryfolia = Riccia sp.
    - Code 2947 maps to Riccardia chamedryfolia with an alternative name Riccia sp. (indicating a higher-level or alternative categorization).
  - 1121, Riccardia chamedryfolia = Rosa arvensis
    - Code 1121 links to Rosa arvensis in the same line, illustrating the presence of multiple cross-references across entries.

- Structure and content notes
  - Entries frequently include multiple cross-references labeled with equivalent or overlapping taxonomic concepts.
  - Some lines pair a code with several possible names across different taxonomic viewpoints, enabling flexible lookups depending on the taxonomy in use.

- Practical use for data work
  - Use these mappings to harmonize ECN species codes with current or alternative taxonomic catalogs before analysis or reporting.
  - Facilitate merging datasets that use different nomenclatures by applying the crosswalks.

# Explanatory Information: Quality Codes

- Purpose
  - Documents standardized quality indicators that accompany data observations to describe data reliability and measurement conditions.

- Range and meaning
  - 100–199: No or limited information available; various issues may apply.
  - 200–299, 500–507: Specific data handling or laboratory-related issues (e.g., adverse weather effects, sample preservation problems, equipment failures).
  - 501–507: Laboratory-related: no sample, lost, partial loss, contamination, insufficient sample, equipment failure.
  - 999: Unusual event – see the quality text.

- Examples of common descriptions (selected)
  - 100: No information available - data lost.
  - 101: No sample/reading taken - equipment out of action.
  - 102: Sample lost or inadvertently discarded.
  - 111: Unidentified debris in sample.
  - 119–121, 123–135: Various contextual and environmental factors or handling issues that may affect data quality (e.g., weather, burning, land-use changes, disturbances).
  - 136–169: Obstruction, flooding, mowing, grazing, trampling, etc., affecting survey sections or plots.
  - 239–241: Taxon identified with varying confidence levels (high, medium, low).
  - 501–507: Laboratory-specific problems (e.g., no sample, loss, contamination, insufficient material).
  - 999: Unusual event requiring separate quality text.

- Practical use for data work
  - Attach or filter data by quality codes to assess reliability and suitability for analyses.
  - Use the accompanying quality text (where available) to interpret the cause of data limitations and guide cleaning or weighting decisions.

- Key takeaway for analysts
  - The species codes provide a comprehensive crosswalk to multiple taxonomic expressions, while the quality codes provide a standardized framework to assess and document data reliability and context. When working with ECN data, leverage both to ensure accurate interpretation, consistent taxonomy, and appropriate treatment of data with potential quality issues.