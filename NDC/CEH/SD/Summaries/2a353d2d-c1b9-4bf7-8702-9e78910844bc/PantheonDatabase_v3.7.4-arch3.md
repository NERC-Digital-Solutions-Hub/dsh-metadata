# Pantheon database (version 3.7.4)

- A curated collection of mostly habitat-related traits for macro-invertebrate species, organized to support conservation assessment, monitoring, and decision-making.

## What the database contains

- Hierarchical habitat traits
  - Three levels: Broad biotope, Habitat, Resources (with nested sub-resources; some fourth-level resources exist).
  - Broad biotopes include tree-associated, open, wetland, and coastal habitats; species can appear in multiple broad biotopes.
  - Habitats are concrete, recognizable units (e.g., saltmarsh); Resources are structural elements or environmental factors (e.g., emergent vegetation).
  - ResourceHeading entries function as top-level groupings for resources.

- Broad resources and labels
  - Broad resources span all habitats and are split into plant-associated and saprophagous groups.
  - Labels cover non-habitat associations (e.g., synanthropic, parasite, ubiquitous, extinct, unknown, vagrant/introduced).

- Feeding guilds
  - Feeding guild data for larvae and adults where available, drawn from the same sources as habitat traits.

- Conservation status and threat status
  - Global, European, and GB IUCN-like threat statuses (EX, RE, CR, EN, VU, NT, DD, LC, NA, NE) with detailed definitions.
  - Pre- and post-1994 criteria mappings; provisional statuses indicated with a 'p' where applicable.
  - National rarity (NR/NS) and related GB status categories; notes on “New to Britain” and Not native classifications.
  - Legal protection information (Wildlife and Countryside Act schedules; European protected species) and Section 41 priority species under the NERC Act.
  - Section 41 entries include research-only designations for some moths.

- Species quality score (SQS)
  - A numeric score (0–32) based on conservation status and rarity, with documentation of the scoring rules and what each value represents (from not native or unknown to highly rare/threatened).

- Associations
  - Known associations between invertebrate species and other taxa (species, genus, family, or larger groups); no explicit definition for the nature of each association.

- Fidelity scores
  - Fidelity indices drawn from published sources (examples include riverine, seepage, coastal cliff, coarse woody debris, calcareous/acid mire, etc.), with explicit score definitions and references.
  - When used, original sources must be acknowledged.

- Data structure and files
  - PantheonHabitatTraits_v3.7.4.csv: habitat traits, broad resources, labels, fidelity scores, SQS, with fields for species, trait, trait type, trait value, parent-child trait relationships, and resource headings.
  - PantheonConservationStatus_v3.7.4.csv: species-level conservation designations across categories (GB/European/global Red Lists, legal protection, Section 41).
  - PantheonAssociations_v3.7.4.csv: species associations with other taxa, including associated tree type and taxa type.

## How data are sourced and assembled

- Primary source: Invertebrate Species-habitat Information System (ISIS), originally developed by Natural England; BATs replaced by Habitats, SATs retained with labeled distinctions.
- Supplemented by published ecological literature extracting life-cycle-relevant habitat traits, host/feeding associations, and related environmental factors.
- Data harmonization involves expert input when sources conflict; majority-rule approaches used when multiple sources disagree.
- Some entries include synonyms; dataset may contain duplicates due to synonymy.
- Some species lack Taxon Version Keys (TVKs); metadata notes reflect this.

## Usage notes and considerations for monitoring frameworks

- Geographic scope: Derived from English species; not fully marine environments (limited coverage for lagoons, brackish water, and saltmarsh).
- Source bias: Based on expert knowledge rather than purely statistical evidence; multivariate-driven Specific Assemblage Types provide some robust analyses.
- Metadata and data quality considerations
  - Potential biases from expert-derived data; synonyms and duplications may complicate use.
  - Some trait data rely on older classifications; updates may be needed to reflect taxonomic changes.
  - Not all taxa have TVKs; some data entries may be incomplete or require cross-referencing with the UK Species Inventory.
- Data governance and sharing
  - Data provenance is explicit, with clear references to sources; users should acknowledge original sources when using fidelity indices.
  - Public sharing considerations are mentioned in the context of broader monitoring data; ensure proper attribution and data-use compliance.

## Practical implications for monitoring frameworks

- Enables trait- and habitat-based indicators for monitoring invertebrate conservation, linking life cycles to habitat structure and environmental factors.
- Facilitates integration of conservation status, legal protections, and rarity into monitoring dashboards and reports.
- Supports cross-referencing species associations and fidelity scores to identify ecologically important habitats and potential monitoring targets.
- Provides a structured, multi-level taxonomy of habitat traits that can be used to standardize reporting and comparisons over time.

## References

- Webb, J.R. & Lott, D.A. (2006) The Development of ISIS: a habitat-based invertebrate assemblage classification system for assessing conservation interest in England. Journal of Insect Conservation, 10:179-188.
- Webb, J and Brown, A. (2016) The conservation status of British invertebrates. British Wildlife August 2016, pages 410-421.