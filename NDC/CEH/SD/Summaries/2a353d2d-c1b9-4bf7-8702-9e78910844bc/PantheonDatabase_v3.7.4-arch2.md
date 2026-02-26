# Pantheon database (version 3.7.4)

## Overview
- A habitat-centric trait database for macro-invertebrate species, focused largely on England.
- Organises habitat information across hierarchical levels (broad biotope, habitat, resources) and includes broad resources, labels, feeding guilds, conservation status, threat status, legal protections, rarity, and species associations.
- Data compiled from ISIS (habitat-based invertebrate classification) and published ecological literature, then coded into nested hierarchies; expert input resolves conflicting information.
- Not fully marine; covers lagoons, brackish water, and saltmarsh. Contains some synonyms and taxa lacking Taxon Version Keys (TVKs).

## Data structure and contents
- Pantheon provides data in three CSV files:
  - PantheonHabitatTraits_v3.7.4.csv: habitat traits, broad resources, labels, fidelity scores, and SQS scores.
  - PantheonConservationStatus_v3.7.4.csv: current conservation and legal status (IUCN criteria post-2001/1994, GB status, WCA protection, Section 41, etc.).
  - PantheonAssociations_v3.7.4.csv: known associations between invertebrates and other taxa (species/genus/family level or broader groups).

### PantheonHabitatTraits_v3.7.4.csv
- Key fields:
  - SpeciesName, SpeciesTVK, PreferredName, PreferredTVK, Family
  - TraitID, TraitName, TraitType (e.g., broad biotope, habitat, resource, broad resource, label, SQS, feeding guild, fidelity score)
  - TraitValue, ParentTraitID, ResourceHeading (flag for resource headings)
- Captures hierarchical habitat traits (three levels: broad biotope, habitat, resources) and embedded structures like resource headings.
- Also includes broad resources (plant-associated and saprophagous) and labels (e.g., synanthropic, ubiquitous, extinct, vagrant) and feeding guilds.

### PantheonConservationStatus_v3.7.4.csv
- Key fields:
  - SpeciesName, SpeciesTVK, PreferredName, PreferredTVK
  - ReportingCategory (GB Red List, European Red List, Global Red List, GB Status, Legal Protection, Section 41, Section 41 – research only)
  - Designation, DesignationAbbreviation
- Documents current threat status using IUCN criteria (post-2001; with pre-1994 criteria listed in parentheses when used) and other national protections.

### PantheonAssociations_v3.7.4.csv
- Key fields:
  - AssociationID, SpeciesName, SpeciesTVK, PreferredName, PreferredTVK, Family
  - AssociatedTreeType (broadleaved, coniferous, or both)
  - AssociatedTaxaType (animal, plant, fungi)
  - AssociatedTaxa (name of the associated taxa)
- Provides recorded associations without explicit definitions of the association type.

## Data provenance and sources
- Primary data sources:
  - Invertebrate Species-habitat Information System (ISIS)—originally for recognizing invertebrate assemblages; BATs replaced by Habitats; SATs carried over as separate from resources.
  - Published ecological literature: species traits, habitat structures, host associations, feeding guilds, etc.
- Data compilation approach:
  - Extracted from sources, converted free text into hierarchical codes, and supplemented with reliable internet sources and expert input when sources disagreed.
  - Some data reflect expert knowledge and may exhibit biases; some entries may lack TVKs or be synonyms.

## Usage notes and caveats
- Dataset is England-centered and not fully marine; includes lagoons, brackish water, and saltmarsh.
- Based largely on expert naturalist knowledge rather than strictly statistical evidence, except for Specific Assemblage Types (multivariate analyses).
- Potential duplications due to synonyms; some taxa may not yet be entered in the UK Species Inventory (no TVK).

## Hierarchy diagrams and references
- Hierarchy diagrams for habitat trait data are provided (e.g., tree-associated - shaded woodland floor hierarchy).
- References:
  - Webb, J.R. & Lott, D.A. (2006). The Development of ISIS: habitat-based invertebrate assemblage classification system for conservation assessment in England.
  - Webb, J. & Brown, A. (2016). The conservation status of British invertebrates.

## Potential analyst applications
- Standardized, time-consistent datasets to monitor environmental health and policy performance, aligned with the Analysts Monitoring the Environment archetype.
- Enables cross-dataset integration (habitat traits, conservation status, and associations) to track environmental condition and species conservation over time.
- Supports quality assurance and data cleaning workflows via defined trait types, hierarchical structure, and exposure to recognized data sources.
- Facilitates transparency in monitoring outputs (maps, charts, and reports) with clear provenance and documentation of data sources.