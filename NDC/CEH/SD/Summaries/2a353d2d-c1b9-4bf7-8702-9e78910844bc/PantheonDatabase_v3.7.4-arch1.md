# Pantheon database (version 3.7.4)

## Overview
- A primarily habitat-focused trait database for macro-invertebrate species.
- Data drawn from the Invertebrate Species-habitat Information System (ISIS) and published literature, plus expert input.
- Contains hierarchical habitat traits, broad resources and labels, feeding guilds, conservation and threat statuses, legal protections, Section 41 priorities, a species quality score (SQS), associations with other taxa, and fidelity scores.
- Provided as three CSV files: PantheonHabitatTraits_v3.7.4.csv, PantheonConservationStatus_v3.7.4.csv, PantheonAssociations_v3.7.4.csv.

## Data Groups and Structure
- Hierarchical habitat traits
  - Three levels: broad biotope, habitat, resources; resources may nest within habitats and biotopes (often with a fourth level).
  - ResourceHeading marks certain entries as headings for groups of resources.
- Broad resources and labels
  - Broad resource groups span habitats (plant-associated and saprophagous).
  - Labels include synanthropic, parasite, ubiquitous, extinct, unknown, vagrant/introduced.
- Feeding guilds
  - Larval and adult feeding guild data where available.
- Conservation status
  - Includes global, European, GB red lists; GB legal protection; Section 41 and Section 41 (research only) designations.
- Threat status
  - Primarily IUCN post-2001 criteria (EX, CR, EN, VU, NT, DD, LC, NA, NE); some post-1994 criteria in parentheses.
  - Provisional statuses noted (e.g., certain spiders/micro-moths).
- Rare or scarce GB status
  - NR (Nationally Rare), NS (Nationally Scarce), Extinct, Not reviewed, New to Britain, Not native; pre-1994 equivalents shown when applicable.
- Legal protection
  - Wildlife and Countryside Act 1981 schedules; variation in protection by designation.
- Section 41 priority species
  - Species identified as Section 41 priority under the 2006 NERC Act; some listed as “research only.”
- Species quality score (SQS)
  - Scaled from 0 to 32, reflecting native status and rarity/conservation concern.
- Associations
  - Documented associations between species and other taxa (species/genus/family or broader groups); no explicit interpretation of the association provided.
- Fidelity scores
  - Multiple fidelity indices for assemblage groups and habitats (e.g., riverine sediments, peat bogs, grazing marsh). Each score has defined meaning and literature reference.

## Data Content Details
- Habitat traits
  - Trait types include broad biotopes, habitats, resources, broad resources, labels, SQS, feeding guilds, and fidelity scores.
  - Trait values capture the specific association for each species (and may reference hierarchical parents via TraitID relationships).
- Conservation and threat
  - Status designations cover IUCN categories and regional/national protections; rare/scarce classifications inform risk and prioritization.
- Legal and policy context
  - Emphasizes legal protection levels and Section 41 status in the GB context.
- Fidelity metrics
  - Detailed, literature-backed fidelity scores across numerous ecological features and organism groups (e.g., Diptera, Coleoptera, spiders) and habitat types (e.g., coastal cliffs, calcareous grassland, seepages).

## Data Structure and Files
- PantheonHabitatTraits_v3.7.4.csv
  - Key fields: SpeciesName, PreferredName, SpeciesTVK, PreferredTVK, Family; TraitID, TraitName, TraitType, TraitValue; ParentTraitID; ResourceHeading.
  - TraitType categories include broad biotope, habitat, resource, broad resource, label, SQS, feeding guild, fidelity score.
- PantheonConservationStatus_v3.7.4.csv
  - Key fields: SpeciesName, SpeciesTVK, PreferredName, PreferredTVK; ReportingCategory (GB Red List, European Red List, Global Red List, GB Status, Legal Protection, Section 41, Section 41 - research only); Designation; DesignationAbbreviation.
- PantheonAssociations_v3.7.4.csv
  - Key fields: AssociationID, SpeciesName, SpeciesTVK, PreferredName, PreferredTVK, Family; AssociatedTreeType; AssociatedTaxaType; AssociatedTaxa.
- Data structure notes
  - Hierarchies link via ParentTraitID.
  - ResourceHeading entries indicate overarching resource groupings.

## Usage Notes and Caveats
- Scope and bias
  - Derived from England; not fully marine (limited to lagoons, brackish water, and saltmarsh).
  - Based on expert knowledge, with multivariate analyses only for Specific Assemblage Types; may include biases.
- Data quality and duplication
  - Synonyms present; potential duplications where the same trait is listed under different names.
  - Some taxa may lack Taxon Version Keys (TVKs).
- Data availability and access
  - Some data may be more readily available to those with domain access or familiarity with UK species resources.

## Hierarchy Visuals
- Hierarchy diagrams for habitat traits are provided (e.g., tree-associated vs. shaded woodland floor) in the referenced materials.

## References
- Webb, J.R. & Lott, D.A. (2006) The Development of ISIS: habitat-based invertebrate assemblage classification.
- Webb, J. & Brown, A. (2016) The conservation status of British invertebrates.

## How Analysts Can Use This Data
- Correlate habitat traits and fidelity scores with conservation status to identify habitat-driven risk patterns.
- Build predictive models linking SQS, rarity categories, and legal protections to threat levels and distribution.
- Integrate association data to explore network effects among taxa and potential indirect impacts of actions.
- Use hierarchical trait structure to analyze patterns across broad biotopes, habitats, and resources at multiple scales.
- Cross-reference with external datasets while accounting for biases and data gaps noted in usage notes.