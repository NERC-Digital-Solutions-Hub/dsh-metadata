# Pantheon database (version 3.7.4)

- A collection of mostly habitat-related traits for macro-invertebrate species, designed to support map-based data products and spatial analyses.

## Data groups and structure

- Hierarchical habitat traits
  - Three hierarchical levels: broad biotope, habitat, and resources; resources nested within habitat, habitat within resources.
  - Some cases include a fourth resource level; broad biotopes include categories like tree-associated, open, wetland, and coastal.
  - Species can occur in more than one broad biotope.
  - Diagrammed hierarchy diagrams are provided with the dataset.

- Broad resources and labels
  - Broad resources span all habitats; divided into plant-associated and saprophagous.
  - Labels include synanthropic, parasite, ubiquitous, extinct, unknown, and vagrant/introduced.

- Feeding guilds
  - Feeding guild data for larvae and adults where available.

- Conservation and threat status
  - IUCN-based threat statuses post-2001 (with pre-2001 equivalents in parentheses when applicable).
  - Region-specific statuses (GB and European) and legal protection notes, including Wildlife and Countryside Act 1981.
  - Section 41 priority species under the Natural Environment and Rural Communities Act 2006 (with some “research only” classifications for certain moths).

- Rare or scarce GB status
  - Categories such as NR (Nationally Rare), NS (Nationally Scarce), and various historical designations; distinctions between post-1994 and pre-1994 criteria.

- Species quality score (SQS)
  - A composite score reflecting conservation relevance and rarity, ranging from 0 to 32, with documented interpretation.

- Associations
  - Known associations between invertebrate species and other taxa (species, genus, family, or broader groups); no explicit definition of the association type.

- Fidelity scores
  - Multiple fidelity indices drawn from published sources (e.g., riverine sediments, coastal soft cliffs, seepage habitats, calcareous/acid grasslands, etc.) with explicit score definitions and references.

## Data files and schema

- PantheonHabitatTraits_v3.7.4.csv
  - Fields include: SpeciesName, PreferredName, Family, TraitName, TraitType (e.g., broad biotope, habitat, resource, broad resource, label, SQS, feeding guild, fidelity score), TraitValue, ParentTraitID, ResourceHeading.
  - ResourceHeading marks resource headings (y/yes).
  - ParentTraitID links hierarchical traits.

- PantheonConservationStatus_v3.7.4.csv
  - Fields include: SpeciesName, PreferredName, ReportingCategory (GB/European/Global Red List, GB Status, Legal Protection, Section 41, etc.), Designation, DesignationAbbreviation.

- PantheonAssociations_v3.7.4.csv
  - Fields include: AssociationID, SpeciesName, PreferredName, PreferredTVK, Family, AssociatedTreeType, AssociatedTaxaType, AssociatedTaxa.

## Usage notes and caveats

- Geographic scope: dataset derived from England-based species.
- Marine coverage: not fully comprehensive; includes lagoons, brackish water, and saltmarsh but not a complete marine scope.
- Knowledge basis: largely expert-derived rather than purely statistical; potential biases exist.
- Synonyms and duplications: synonyms present; some trait data may duplicate under different names.
- Taxon version keys: some taxa may lack TVKs because they are not yet in the UK Species Inventory.

## GIS-typical applications

- Map-based visualization of habitat traits, resources, and conservation status proxies (IUCN categories, Section 41 species).
- Spatial prioritization and habitat association analyses using broad biotopes, habitats, and fidelity scores.
- Integration with other datasets via TVKs and taxonomy fields (SpeciesTVK, PreferredTVK).
- Use of SQS and fidelity scores as thematic indicators for biodiversity value or conservation urgency.

## Diagrams and references

- Hierarchy diagrams for habitat trait data are provided (e.g., Tree-associated – shaded woodland floor hierarchy).
- References:
  - Webb, J.R. & Lott, D.A. (2006) ISIS development for habitat-based invertebrate assemblage classification.
  - Webb, J. & Brown, A. (2016) The conservation status of British invertebrates.