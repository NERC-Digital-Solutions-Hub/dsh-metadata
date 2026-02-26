# Pantheon database (version 3.7.4)

## What is Pantheon
- A repository of mostly habitat-related traits for macro-invertebrate species.
- Data organized around hierarchical habitat traits, broad resources, and labels, plus feeding guilds, conservation status, threat status, legal protection, and associations.
- Aims to support understanding of species-habitat associations and conservation context, with outputs suitable for exploration by end users (e.g., dashboards, reports).

## Data groups and structures
- Hierarchical habitat traits: three levels—Broad biotope (e.g., tree-associated, open, wetland, coastal), Habitat (e.g., saltmarsh), Resources (structural/environmental factors). Some cases include a fourth-level resource. ResourceHeading entries act as collection titles for groups of resources.
- Broad resources and labels: Broad resources span habitats and are split into plant-associated and saprophagous groups. Labels capture categories like synanthropic, parasite, ubiquitous, extinct, unknown, vagrant/introduced.
- Feeding guilds: Provided for larvae and adults where available.
- Conservation status: Includes global, European, GB red lists; GB legal protection listings; Section 41 (NERC Act) priority designations.
- Threat status: Primarily IUCN post-2001 criteria (with some pre-1994 mappings in parentheses); categories include EX, RE, CR, EN, VU, NT, DD, LC, NA, NE, plus provisional statuses for some taxa.
- Rare or scarce GB status: Nationally Rare (NR), Nationally Scarce (NS), Extinct, Not reviewed, New to Britain, Not native, with clarifications for marine and non-native taxa.
- Section 41 priority species: Some species flagged for priority status or for research-only purposes.
- Species quality score (SQS): A numeric conservation-status-based score reflecting rarity or conservation concern, with defined mappings (e.g., 0, 1, 4, 8, 16, 32).
- Associations: Documented associations between invertebrates and other taxa (species, genus, family, or higher groups) without explicit relationship definitions.
- Fidelity scores: Indicators of how strongly species are associated with particular habitats or habitat features, drawn from multiple published indices (with explicit definitions and references).

## Data sources and curation
- Invertebrate Species-habitat Information System (ISIS), originally from Natural England, providing habitat-based assemblage classifications.
- Published ecological literature and reliable internet sources for habitat traits, host plants/animals, and life-history factors.
- Expert input used when sources conflicted; majority consensus used when information varied.
- Some data reflect expert knowledge and may carry biases; free-text notes were progressively codified into hierarchical trait structures.

## Data files and schema
- PantheonHabitatTraits_v3.7.4.csv
  - Contents include: SpeciesName, PreferredName, Taxon version keys (TVK), Family, TraitName, TraitType (e.g., broad biotope, habitat, resource, broad resource, label, SQS, feeding guild, fidelity score), TraitValue, ParentTraitID, ResourceHeading.
  - Unique record key: SpeciesTraitID.
- PantheonConservationStatus_v3.7.4.csv
  - Contents include: SpeciesName, PreferredName, TVK, ReportingCategory (GB Red List, European Red List, Global Red List, GB Status, Legal Protection, Section 41, Section 41 - research only), Designation, DesignationAbbreviation.
- PantheonAssociations_v3.7.4.csv
  - Contents include: AssociationID, SpeciesName, TVK, PreferredName, PreferredTVK, Family, AssociatedTreeType (broadleaved, coniferous, or both), AssociatedTaxaType (animal, plant, fungi), AssociatedTaxa.

## Key data types and fields (selected)
- SpeciesName, PreferredName, TVK: taxonomic identification and preferred nomenclature.
- TraitName, TraitType, TraitValue: describe hierarchical habitat trait, broad resources, labels, feeding guilds, fidelity scores, and SQS values.
- ParentTraitID: links traits within the hierarchy.
- ResourceHeading: marks traits that act as a heading for a collection of resources.
- ConservationStatus fields: ongoing designations across multiple threat categories and protection regimes.
- Designation/Abbreviation: concise codes for statuses.
- Association fields: capture known inter-taxa associations without explicit semantics.
- Fidelity score definitions and references: detailed scoring scales for habitat associations (e.g., riverine sediments, woodland seepage, coastal cliff, calcareous/acid mire, etc.).

## Notable feature details
- Hierarchy enables multi-level queries: broad biotopes, specific habitats, and nested resources.
- ResourceHeading entries provide logical groupings for complex trait trees.
- Fidelity scores and many specialized indices (with explicit references) support nuanced habitat association analyses.
- SQS offers a structured, numeric measure of species conservation status integration beyond simple categories.
- Associations capture complex ecological links but do not define the nature of each association.

## Usage considerations and caveats
- Scope: dataset derived from English species; not fully marine, though includes lagoons, brackish water, and saltmarsh.
- Basis: largely expert opinion and literature-derived knowledge; bias possible, especially for less-studied taxa.
- Synonyms and duplications: synonyms are present; some traits may duplicate across synonyms.
- Taxon Version Keys (TVKs): some species may lack TVKs because they are not yet entered in the UK Species Inventory.
- Specific Assemblage Types: multivariate analyses underpin only the Specific Assemblage Types; other components rely on descriptive codes or expert interpretation.

## Practical implications for Data Support (data product opportunities)
- Build self-serve dashboards that let users filter by species, habitat level (broad biotope, habitat), and trait type (fidelity, SQS, feeding guild).
- Create hierarchical viewers to explore trait trees (Broad biotope → Habitat → Resources) with resource headings highlighted.
- Enable cross-referencing of conservation status and threat status with legal protections and Section 41 designations for policy or planning use.
- Provide data quality notes and provenance links for each trait (source references, coding notes, and expert input).
- Integrate associations as contextual enrichment rather than primary decision variables; include provenance and potential caveats.
- Offer exportable data subsets (habitat traits, conservation status, associations) for dashboards, reports, or GIS workflows.
- Maintain data hygiene by tracking synonyms and TVK coverage, and flag records without TVKs for curation.

## Diagrams and references
- Hierarchy diagrams for habitat trait data (e.g., tree-associated - shaded woodland floor hierarchy).
- References for data sources and methods:
  - Webb, J.R. & Lott, D.A. (2006) The Development of ISIS: a habitat-based invertebrate assemblage classification system for assessing conservation interest in England.
  - Webb, J and Brown, A. (2016) The conservation status of British invertebrates.