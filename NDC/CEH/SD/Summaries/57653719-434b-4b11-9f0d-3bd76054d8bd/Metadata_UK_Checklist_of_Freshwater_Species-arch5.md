# METADATA FOR 'UK CHECKLIST OF FRESHWATER SPECIES' DATASET

## Overview and Purpose
- Collaborative dataset compiled between 2015-2017 by Iain Gunn, Laurence Carvalho, Chris Raper, Gavin Siriwardena, and Ian Winfield, led under the NERC Highlights Hydroscape project (NEC05609).
- Primary aim: enable querying of freshwater species data in the Biological Records Centre (BRC) and via the UK Lakes Portal, and to update freshwater species lists for UKSI partners (e.g., Recorder 6, NBN Atlas, iRecord).
- Invertebrate component updated by Iain Gunn, drawing on earlier code lists and expert input.
- The work supports data discovery, interoperability, and continued data sharing across organizations and portals.

## Scope and Structure
- The UK Checklist of Freshwater Species is a compilation of all freshwater-associated species in the UK, excluding algae.
- Structured to align with NHM coding requirements and designed to support cross-portal querying.
- Eight major freshwater groups identified; algae are excluded, and other microorganisms (bacteria, fungi, viruses) are not included.
- The dataset was assembled by creating separate Excel lists for each group, then combining them into a single dataset.
- Main dataset columns follow NHM coding conventions: TAXON_GROUP_NAME, TAXON_LIST_KEY, TAXON_LIST_VERSION_KEY, TAXON_LIST_ITEM_KEY, TAXON_VERSION_KEY, PREFERRED NAME, SORT_CODE, TAXON_LIST_ITEM_KEY LONG_NAME, ITEM_NAME, AUTHORITY.

## Taxonomic Groupings and Inclusion Rules
- Algae: Not included in the UK Checklist of Freshwater Species; an updated freshwater algae inventory is being prepared separately.
- Amphibians: 20 freshwater species included; 6 native, the rest introduced; Pelophylax lessonae noted as possibly native to Norfolk.
- Birds: Freshwater birds compiled from the UKSI bird list with an additional BTO input, totaling 194 species/sub-species considered regularly occurring or breeding in or near UK freshwater habitats (vagrants excluded).
- Fish: Divided into Actinopterygii (bony fish) and Agnatha (jawless fish). 100 Actinopterygii taxa documented (80 native or established; 38 considered non-native; 19 hybrids; 1 subspecies). Some species inhabit brackish conditions and are included as they appear in freshwater records. Non-native introductions listed per Britton et al. (2010). The European bitterling is updated to Rhodeus amarus.
- Invertebrates: The largest grouping (~5810 taxa) organized into 28 informal groups (e.g., Coleoptera, Diptera, Ephemeroptera, Molluscs, Crustaceans, etc.). The core basis is the Davies/Edwards/Maitland/Furse freshwater invertebrate code list (updated 2011) cross-referenced with the UKSI master list; some discrepancies addressed via nomenclature checks.
- Macrophytes: Second largest group (~2216 taxa) subdivided into nine groups (clubmoss, fern, flowering plant, horsetail, lichen, liverwort, moss, quillwort, stonewort). Flowering plants are the largest subgroup (1249 taxa). Basis includes EU freshwater macrophyte taxa, validated against major floras (e.g., Preston & Croft; Preston et al.).
- Mammals: Eight freshwater-associated mammals included; four are non-native. Beavers (Castor fiber) have been reintroduced/escaped and are now considered native in parts of Scotland.
- Reptiles: Six species (and one subspecies) included; most are non-native, with the native grass snake (Natrix natrix) as an exception.

## Data Sources, Provenance, and Nomenclature
- Taxon lists and groupings derived from established authorities and monitoring frameworks:
  - UKSI (UK Species Inventory) master list
  - NBN database for non-native status and确认ation of records
  - UKTAG classification paper and related resources for invasive non-native species
  - CEH-derived invertebrate codes (Davies/Edwards/Maitland/Furse) for alignment with UKSI
  - Standard floras and taxonomic references for macrophytes and other groups
- Emphasis on including taxa with confirmed wild occurrences in the UK.
- Nomenclature reconciliations performed to resolve discrepancies between legacy datasets and current UKSI.

## Data Quality, Curation, and Updates
- Data curated to maintain accuracy, consistency, and interoperability across portals (BRC, UK Lakes Portal, UKSI-related partners).
- Inclusion decisions based on:
  - Broad freshwater definition (ditches, lakes, ponds, streams, riparian zones, wetlands, etc.)
  - Reconciliation with authoritative taxon lists and recent literature
  - Verification against presence in the wild in the UK and updates to invasive/non-native status
- Separate, curated group lists are integrated into a single, up-to-date dataset to support ongoing discovery and querying.

## Access, Use, and Intended Beneficiaries
- Designed to support querying freshwater species data across multiple platforms:
  - Biological Records Centre (BRC)
  - UK Lakes Portal
  - UKSI partners (Recorder 6, NBN Atlas, iRecord)
- Facilitates up-to-date metadata and alignment across data portals, improving discoverability and reuse by researchers, policy makers, and conservation practitioners.

## Governance, Acknowledgments, and References
- Acknowledges contributions from CEH (Edinburgh, Lancaster), NHM, BTO, and associated collaborators.
- References and data sources include:
  - UK Lakes Portal and BRC for data access and interoperability
  - NBN Atlas, Recorder 6, and UKSI for nomenclature and records
  - UKTAG and related freshwater invasive species literature for non-native status
  - Key taxonomic references used for cross-checking macrophytes, birds, fishes, and invertebrates
- The dataset reflects a deliberate governance approach to standardization, provenance, and ongoing updates to support reliable discovery and reuse.