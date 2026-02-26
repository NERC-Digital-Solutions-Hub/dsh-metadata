# Pantheon database (version 3.7.4)

- Purpose and scope
  - A collection of habitat-related traits for macro-invertebrate species.
  - Groups include hierarchical habitat traits, broad resources and labels, feeding guilds, conservation status, threat status, rare/GB status, legal protection, Section 41, species quality score (SQS), associations, and fidelity scores.
  - Designed to support understanding of species-habitat relationships and conservation status, with data derived from multiple sources.

- Data structure and files
  - PantheonHabitatTraits_v3.7.4.csv: habitat traits, broad resources, labels, fidelity scores, SQS, feeding guilds. Key fields include SpeciesName, SpeciesTVK, PreferredName, Family, TraitID, TraitName, TraitType, TraitValue, ParentTraitID, ResourceHeading.
  - PantheonConservationStatus_v3.7.4.csv: conservation status per species with ReportingCategory, Designation, DesignationAbbreviation.
  - PantheonAssociations_v3.7.4.csv: species associations with other taxa; fields include AssociationID, SpeciesName, SpeciesTVK, PreferredName, Family, AssociatedTreeType, AssociatedTaxaType, AssociatedTaxa.

- Taxonomic identifiers and naming
  - SpeciesTVK and PreferredTVK are UK Species Inventory keys.
  - Some species may lack TVKs if not yet entered in the UK Species Inventory.

- Hierarchical habitat model
  - Habitat traits are organized into three levels: broad biotope, habitat, and resources.
  - ResourceHeading entries serve as headings for resource groupings within the hierarchy.
  - Broad biotopes include categories such as tree-associated, open, wetland, and coastal habitats.

- Broad resources and labels
  - Broad resources span all habitats; split into plant-associated and saprophagous.
  - Labels cover categories like synanthropic, parasite, ubiquitous, extinct, unknown, and vagrant/introduced.

- Feeding guilds
  - Feeding guild data are provided for larvae and adults where available.

- Conservation, threat, and rarity statuses
  - Threat statuses mostly follow IUCN post-2001 criteria (EX, CR, EN, VU, NT, DD, LC, NA, NE); pre-1994 equivalents may be shown in parentheses.
  - Rare or scarce GB status includes NR (Nationally Rare) and NS (Nationally Scarce), plus categories like Extinct, Not reviewed, Not native, and New to Britain.
  - Section 41 priority species defined under the Natural Environment and Rural Communities Act; some are marked as "research only."
  - Species Quality Score (SQS) maps conservation status to a numeric score (0 to 32, with intermediate values described) to reflect overall conservation concern and native/rarity status.

- Legal protection
  - Legal protection through Wildlife and Countryside Act 1981 schedules and European protected species status.

- Associations
  - Associations describe known links between invertebrate species and other taxa (species, genus, family, or higher groups); the dataset records the association without a formal definition of the nature of the association.

- Fidelity scores
  - Fidelity metrics quantify species’ associations with particular habitats or conditions (e.g., exposed riverine sediments, grazing marsh ditches, seepages, coastal cliff habitats, coarse woody debris, etc.).
  - Each fidelity score has definitions, ranges, and references to supporting literature.

- Usage notes and limitations
  - Derived from English fauna; not fully covering marine environments (limited lagoons, brackish water, saltmarsh).
  - Based on expert knowledge rather than purely statistical evidence; biases may be present except for Specific Assemblage Types (multivariate analyses).
  - Synonyms and duplications may exist; some species may lack TVKs if not yet entered in UK inventory.

- Data provenance and references
  - ISIS origins and evolution: ISIS replaced the BATs classification; SATs were integrated into Pantheon.
  - Data drawn from ISIS, published literature, reliable internet sources, and expert input; where sources disagree, consensus from experts was used.
  - Key references: Webb & Lott (2006); Webb & Brown (2016).

- Hierarchy diagrams
  - Habitat trait diagrams are provided (e.g., Tree-associated - shaded woodland floor hierarchy) to illustrate the hierarchical relationships.

- Governance and stewardship considerations for Data Stewards
  - Maintain clear metadata and versioning (Pantheon v3.7.4) and provenance links to ISIS and literature sources.
  - Ensure referential integrity across traits (TraitID, ParentTraitID) and ResourceHeading indicators.
  - Manage updates and potential data embargoes; document changes and maintain consistent taxonomic identifiers (TVKs).
  - Be aware of data quality caveats: biases from expert-derived data, synonyms, and possible missing TVKs.
  - Facilitate interoperability by aligning with the three-file structure and clear field definitions for discovery and reuse.