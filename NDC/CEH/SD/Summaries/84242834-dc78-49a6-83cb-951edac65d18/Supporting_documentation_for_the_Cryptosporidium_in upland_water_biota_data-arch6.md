# Supporting documentation for the Cryptosporidium in Welsh upland water biota data (2012-2015)

## Overview
- A sample survey leveraging fieldwork from the broader DURESS project (2012–2015) to test for Cryptosporidium in Welsh upland water biota.
- No treatments or replication during sampling; laboratory controls used but not during sampling.
- Samples include fish (gills, gut contents, faeces), whole aquatic invertebrate larvae, and faeces from land/aquatic mammals (otters).
- Data are organized into two CSV files describing different sample types, with additional site descriptions in a separate file.

## Sampling and data collection context
- Part of the DURESS project with sampling framed around food webs, wildlife, and aquatic biota.
- Otter faeces obtained from broader studies (2011–2015) due to regulatory testing constraints; other otter data originate from dead specimens in England and Wales.
- No experimental treatments; the sampling frame followed the broader DURESS sampling plan except for otter samples.

## Sample types and collection methods
- Fish samples (2012): 74 fish from 11 sites collected by electrofishing; fresh gut contents (n=73) and gills (n=74) dissected and stored at -20°C; 16 salmon, 41 brown trout, 16 bullhead; gill and gut paired samples for subset.
- Fish faeces (2013): 117 fish faecal samples collected from anaesthetised fish at 8 sites; samples frozen at -20°C for testing.
- Otter faeces (2013–2015): 41 tailed samples collected in upland riparian zones; 92 otter faecal samples tested from dead otters (broader study sources).
- Invertebrate larvae: 290 aquatic invertebrate larvae (genera including Baetis, Rhithrogena, Leuctra, Hydropsyche, Simulium, etc.) collected from upland rivers, stored in absolute ethanol for method development and testing.

## Laboratory methods and quality controls
- DNA extraction:
  - Fish gut/gill: QIAamp DNA mini kit (tissue protocol).
  - Fish/mammal faeces: QIAamp Fast DNA stool mini kit.
  - Invertebrate larvae: Gentra Puregene DNA kit; includes in-house developed protocol with liquid nitrogen grinding and freeze-thaw cycles.
- Molecular testing:
  - Nested PCR targeting the small subunit rRNA (ssu rRNA) gene; positive amplicons sequenced to identify species.
  - gp60 locus genotyping for Cryptosporidium parvum and Cryptosporidium hominis-positive samples (for finer typing).
  - Invertebrate larvae additionally tested with real-time PCR for C. hominis and an internal control to check inhibition.
- Controls and accreditation:
  - Positive and negative controls used in all assays; positive controls included known DNA and larvae seeded with C. hominis oocysts.
  - Tests performed under Clinical Pathology Accreditation at CRU (now ISO15189).
  - DNA sequencing outsourced to Source Bioscience; analysis performed at the CRU.

## Data structure and file details
- Two main CSV files:
  - Results_Invertebrate_Larvae.csv
    - Fields: Sample_number, Sample_Description, Number_of_larvae_pooled(Seeded_with_C.hominis_oocysts), Site, n18S, Ch_Ct_value, IC_Ct_value.
    - Purpose: results of nested ssu rRNA PCR, sequencing, and C. hominis real-time PCR for invertebrate larvae.
  - Results_Biofilm_Fish_Mammals.csv
    - Fields: Site, Sample_group, Host, Sample_Type, CRU_Ref, n18S_result, GP60, Sequencing.
    - Purpose: results across fish tissues, biofilm, and mammal faeces; includes sequencing outcomes and GP60 results.
- Site reference data: DURESS_CU_site_description.csv provides site context for each Site entry.
- Data interpretation:
  - n18S_result: Negative or Positive for nested 18S rRNA PCR and sequencing.
  - GP60: Result for gp60 genotyping (Positive/Negative/Not Done as applicable).
  - Sequencing: Result of sequencing (e.g., Pos/Neg/Not Done; includes when unambiguous source could not be identified, a question mark may be used for mammal source).

## Provenance and references
- Data generation grounded in established Cryptosporidium methodologies:
  - Alves et al., 2003 (gp60 subgenotype analysis; human, cattle, zoo ruminants).
  - Hadfield et al., 2011 (detection/differentiation of Cryptosporidium spp. via real-time PCR).
  - Jiang et al., 2005 (distribution of Cryptosporidium genotypes in environmental samples).
- Data collection and analysis conducted at the CRU with sequencing outsourcing to Source Bioscience.

## Data use considerations
- The dataset is designed to support cross-dataset analyses within DURESS or in related environmental parasitology studies.
- Cross-referencing with DURESS_CU_site_description.csv is recommended for site-level context.
- Note on mammal host identification: when animal source could not be unambiguously identified, a question mark is appended to the mammal name in the host field.