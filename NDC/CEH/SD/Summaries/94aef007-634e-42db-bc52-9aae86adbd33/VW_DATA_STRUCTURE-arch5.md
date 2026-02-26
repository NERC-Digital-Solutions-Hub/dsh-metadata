# Explanatory Information: Species codes

- Purpose and scope
  - Provides mappings between numeric species codes and species names or synonyms to enable consistent taxonomy across datasets.
  - Includes cross-references to alternative coding systems (e.g., Bry_902, Vas_XXXX) to support interoperability and harmonisation.

- How to read the mappings
  - Each line shows a code followed by a primary name and one or more alternative names or codes (e.g., "2254, Riccardia chamedryfolia = Riccardia multifida" or "2699, 1 = Salix cinerea ssp oleifolia (s)").
  - Some codes map to multiple synonyms or to multiple alternative codes, illustrating the crosswalk between taxonomic concepts and repositories.

- Representative patterns and examples
  - 2254, Riccardia chamedryfolia = Riccardia multifida (and related variants)
  - 1121, Riccardia chamedryfolia = Rosa arvensis
  - 2746, Riccardia chamedryfolia = Rosa (and related variants)
  - 1137, Riccardia chamedryfolia = Rubus idaeus
  - 2699, 1 = Salix cinerea ssp oleifolia (s); 2699, 2 = Vas_1786; 2699, 3 = Salix cinerea subsp. oleifolia
  - 3348, Viola riviniana x rupestris; 3348, Vas_2682
  - The list includes many plant species, bryophytes, algae-like taxa, and their numerous synonyms or cross-references

- Practical implications for Data Stewards
  - Use the codes to reconcile species data from different sources and portals.
  - Maintain clear mappings to ensure consistent downstream analyses and reporting when aggregating datasets.

# Explanatory Information: Quality Codes

- Purpose and scope
  - Defines standardized quality indicators and their textual meanings to accompany data downloads and analyses.
  - Helps data users understand reliability, completeness, and any potential issues affecting data interpretation.

- Key structure and examples
  - Codes with descriptions, e.g.:
    - 100, Description = No information available - data lost.
    - 101, Description = No sample/reading taken - equipment out of action / unable to visit equipment.
    - 102, Description = Sample lost or inadvertently discarded.
    - 103, Description = Partial loss of sample.
    - 104, Description = Sample frozen when collected.
    - 120, Description = Change of land use in vicinity.
    - 129, Description = Condensation in tube.
    - 133, Description = Evidence of disease in plot/transect section.
    - 136, 1 = Cell not surveyed due to obstruction.
    - 150, Description = Wind-throw.
    - 201, Description = Biting insects affected sampling/recording.
    - 203, Description = No flow observed in river - standing water only.
    - 501–507, Descriptions = Laboratory: issues such as no sample, sample lost, partial loss, contamination, insufficient sample, equipment failure.
    - 999, Description = Unusual event - see the quality text.
  - Many codes are granular and context-specific, often accompanied by sub-notes or conditional interpretations (e.g., multiple facets of a single issue).

- Practical implications for Data Stewards
  - Attach quality codes to data records to flag uncertainties, losses, or methodological issues.
  - Reference the associated quality text and windows (where provided) to guide data cleaning, filtering, or sensitivity analyses.
  - Use 999 and its quality text as a trigger for special review or stakeholder notification when unusual events are recorded.

- Overall takeaway for governance
  - The dataset provides a comprehensive, standardized scheme for recording data quality, enabling transparent provenance and better data discovery, reuse, and trust among data users.