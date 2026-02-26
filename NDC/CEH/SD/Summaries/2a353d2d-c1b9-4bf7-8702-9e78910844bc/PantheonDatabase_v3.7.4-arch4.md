# Pantheon database (version 3.7.4)

## Overview
- A dataset of habitat-related traits for macro-invertebrate species, organized into hierarchical habitat traits, broad resources, labels, feeding guilds, conservation and threat statuses, rarity, legal protection, and associations.
- Primarily England-based; not a fully marine dataset (covers lagoons, brackish water, and saltmarsh).
- Derived from expert knowledge with identified biases and caveats; includes synonyms and some taxa without Taxon Version Keys (TVKs).

## Data structure and contents
- Provided as 3 CSV files:
  - PantheonHabitatTraits_v3.7.4.csv
  - PantheonConservationStatus_v3.7.4.csv
  - PantheonAssociations_v3.7.4.csv
- PantheonHabitatTraits_v3.7.4.csv includes:
  - SpeciesName, PreferredName, TVKs, taxonomic information, TraitID, TraitName, TraitType, TraitValue, ParentTraitID, ResourceHeading
  - Trait types include: broad biotope, habitat, resource, broad resource, label, SQS, feeding guild, fidelity score
- PantheonConservationStatus_v3.7.4.csv includes:
  - SpeciesName, TVK, PreferredName, ReportingCategory (GB Red List, European Red List, Global Red List, GB Status, Legal Protection, Section 41, Section 41 – research only)
  - Designation and DesignationAbbreviation
- PantheonAssociations_v3.7.4.csv includes:
  - AssociationID, SpeciesName, TVK, PreferredName, AssociatedTreeType (broadleaved, coniferous, or both), AssociatedTaxaType (animal, plant, fungi), AssociatedTaxa

## Hierarchy and trait types
- Hierarchical habitat traits are divided into:
  - Broad biotope (e.g., tree-associated, open, wetland, coastal)
  - Habitat (e.g., saltmarsh)
  - Resources (structural elements and environmental factors)
- ResourceHeading entries act as headers for collections of resources.
- Broad resources are split into plant-associated and saprophagous groups.
- Labels include categories like synanthropic, parasite, ubiquitous, extinct, unknown, vagrant/introduced.
- Feeding guilds provided for larvae and adults where available.
- Fidelity scores capture specific ecological associations (numerous fidelity schemes for various groups and habitats).
- SQS (Species Quality Score) aggregates conservation-related scoring across statuses.

## Data provenance and quality
- Data sources:
  - Invertebrate Species-habitat Information System (ISIS) originally developed by Natural England
  - Published ecological literature and expert input to resolve conflicting trait information
  - Additional data from reliable online sources and authors’ experience
- Data processing notes:
  - Initially free-text notes were formalized into nested hierarchies; expert opinion used when sources conflicted
  - Some data are presented as codes rather than free text
- Quality caveats:
  - Biases due to expert-based knowledge; potential data gaps or uneven coverage
  - Synonyms present; duplications possible due to synonymy
  - Not all species have TVKs; some information predates modern inventories
  - Some statuses use post-2001 IUCN criteria; some pre-1994 criteria are listed in parentheses

## Usage guidance for data leaders
- Supports organization-wide data strategy for biodiversity and habitat association analytics.
- Useful for assessing data availability, gaps, and prioritization (e.g., where trait data or TVKs are missing).
- Facilitates data governance around metadata, discoverability, and data product iteration (e.g., updating habitual traits, conservation designations, and associations).
- When using fidelity indices or conservation statuses, ensure proper attribution to original sources.
- Be mindful of scope limitations (England-focused; partial marine coverage) and potential biases in expert-derived data.

## Practical considerations and notes
- Hierarchy diagrams for habitat traits are included (e.g., tree-associated - shaded woodland floor hierarchy).
- Data structure emphasizes traceability between species and their traits via unique TraitID and ParentTraitID links.
- Usage notes highlight that the dataset is not fully marine and may contain synonyms and taxa lacking TVKs.

## References
- Webb, J.R. & Lott, D.A. (2006). The Development of ISIS: a habitat-based invertebrate assemblage classification system for assessing conservation interest in England. Journal of Insect Conservation, 10:179-188.
- Webb, J. & Brown, A. (2016). The conservation status of British invertebrates. British Wildlife, August 2016, 410-421.