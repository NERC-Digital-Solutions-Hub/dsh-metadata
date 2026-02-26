# UK Environmental Change Network (http://www.ecn.ac.uk) Vegetation: Fine Grain (VF)

## Overview
- Provides a comprehensive taxonomy code lookup used to standardise species references in ECN VF vegetation data.
- Each entry links a numeric code and a taxon label (including qualifiers like (g), (s), etc.) to alternative taxonomic concepts or external identifiers (e.g., Vas_..., Bry_..., etc.).
- Supports cross-walking synonyms, vernaculars, and multiple taxonomy concepts across datasets and sources.

## Species code mappings
- Taxon-to-taxon crosswalks are extensive, covering many genera and species (e.g., Salix, Saxifraga, Solanum, Viola, Ulmus, etc.), with numerous aliasing and equivalence entries.
- Example patterns:
  - 1167, Salix aurita (g) = Salix aurita (s)
  - 2741, Salix aurita (g) = Salix caprea
  - 4305, Salix aurita (g) = Salix cinerea
  - 1171, Salix aurita (g) = Salix herbacea
  - 4003, Saxifraga stellaris = Saxifraga x urbium
- Many lines map a primary code to multiple alternative names or database identifiers (e.g., Vas_1787, Bry_926), indicating cross-references to external vocabularies or reference databases.
- The mappings include seedlings, hybrids, and broad groupings (e.g., Salix seedling/sp., unidentified broadleaf seedling) to enable flexible data interpretation.
- The dataset includes a wide range of taxa and their potential synonyms or related concepts, illustrating the complexity of plant nomenclature in the VF data.

## Quality codes
- ECN defines a standard set of quality codes to describe data quality and reliability.
- Codes are selected by site managers and describe issues that may affect data integrity (e.g., no information, equipment failure, debris in sample, weather-related impacts, non-standard sampling).
- Code ranges and examples:
  - 100: No information available - data lost
  - 101: No sample/reading taken - equipment out of action
  - 102–199: Various sampling or sample integrity issues (e.g., 103 partial loss, 104 sample frozen, 109 leaves in sample, 113 sample discoloured)
  - 120–159: Operational or environmental interference (e.g., 121 change of land use, 122 cleaner funnel, 135 tubing damaged)
  - 160–200: Trampling, flooding, or other field conditions affecting sampling
  - 200–236: Additional field conditions and observations (e.g., 201 biting insects, 233 lake level, 235 mole-hill)
  - 999: Unusual event - accompanying text explains the circumstance
- If a quality code is not sufficient to describe a situation, site managers may attach free-text quality information to accompany the code.

## How this supports the Data Support archetype
- Enables “understand the ask” by providing a well-documented, cross-referenced taxonomy substrate for cross-topic data exploration (species, vegetation, environment).
- Facilitates data discovery, cleaning, and transformation through standardized species codes and explicit quality metadata.
- Supports creation of self-serve data products and dashboards with reliable taxonomic lookups and clear data quality context.
- Encourages transparent data use and provenance by linking to external vocabularies and by documenting data quality and limitations via standardized codes and accompanying text.