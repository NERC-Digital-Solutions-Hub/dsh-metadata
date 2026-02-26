# UK Environmental Change Network (http://www.ecn.ac.uk) Vegetation: Coarse Grain (VC) Dataset

- This document section provides detailed data dictionaries used for vegetation monitoring within ECN, focusing on taxonomy mappings and data quality governance.

## Species codes and synonym mappings

- Contains extensive mappings between numeric species codes and multiple taxon names (Latin and common references), including numerous synonyms and equivalents.
- Example patterns observed:
  - Codes such as 2741, 2631, 1168, 4305, 2729, 1171, etc., map a single numeric code to different Salix or related taxa (e.g., Salix aurita, Salix caprea, Salix cinerea, Salix herbacea, Salix viminalis, etc.) and related genera (e.g., Sambucus nigra, Sanguisorba minor, Saxifraga species, etc.).
  - Entries also include substitutions or synonyms like "5321 = Salix" variants and cultivar/ssp designations (e.g., ssp oleifolia).
  - Some lines indicate direct equivalences (e.g., Salix aurita = Salix caprea) and others show multiple possible mappings for the same code (reflecting taxonomic revisions or cross-reference needs).
- The mappings illustrate a comprehensive crosswalk to reconcile taxonomy across datasets, enabling consistent interpretation when integrating data from different sources or nomenclatures.

## Quality codes and metadata

- Defines the standard ECN quality codes used to annotate data quality issues and events.
- Codes range from 100 to 513, plus 999 for unusual events (with accompanying quality text).
- Examples of coded categories:
  - 100: No information available (data lost)
  - 101: No sample/reading taken (equipment issues)
  - 102–149: Various sample/lab/field problems (partial loss, contamination, debris, weather impacts, grazing, trampling, etc.)
  - 150–171: Field conditions and observations (woodland management, river/pond conditions, wildlife presence, etc.)
  - 200–239: Adverse conditions affecting sampling/identification (insects, lighting, confidence levels for taxon identification)
  - 501–513: Laboratory-related data issues (samples missing, lost, contaminated, measurement issues)
  - 999: Unusual event (with accompanying narrative text in quality metadata)
- The quality codes are designed to capture both procedural and observational factors that affect data reliability, provenance, and interpretability.

## Data governance and interoperability implications

- The combination of species code synonym mappings and comprehensive quality codes supports:
  - Cross-site data integration and interoperable vegetation datasets by harmonizing taxonomic references.
  - Transparent provenance and data quality assessment, enabling policy-makers to filter or weight data based on quality indicators.
  - Documentation of unusual events or non-standard procedures via text notes linked to quality codes (e.g., code 999).

## Practical considerations for monitoring framework authors

- When designing monitoring systems, include:
  - A robust taxonomic crosswalk to handle multiple synonyms and revisions, ensuring consistent interpretation of species codes across datasets.
  - Comprehensive quality metadata to document data reliability, including the ability to attach explanatory text for unusual events.
  - Training and clear governance around the application of quality codes to maintain consistency across sites and over time.