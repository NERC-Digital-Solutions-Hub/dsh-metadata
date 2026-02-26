# Supporting documentation for the Cryptosporidium in Welsh upland water biota data (2012-2015)

## Overview
- A sample survey linked to the wider DURESS project, testing for the protozoan parasite Cryptosporidium across multiple hosts and sample types in Welsh upland river catchments (2012-2015).
- No treatments or replication during sampling; controls in laboratory assays but not during field sampling.
- Laboratory accreditation and sequencing outsourced portion; data generated include PCR results and species/genotype identifications.

## Sampling design and sample types
- Fish (gills and gut contents): 74 fish from 11 upland river sites in 2012; dissection for gut and gill sampling, then storage and testing at the Cryptosporidium Reference Unit (CRU). Paired gut and gill samples available for selected species (e.g., salmon, brown trout, bullhead).
- Fish feces: 117 live fish sampled in 2013 by anaesthetising and collecting fecal material; samples frozen and sent for testing.
- Otter feces: 41 samples collected from riparian zones in 2013; animal source uncertain. Additional otter feces from dead otters across England and Wales (2011-2015) used to explore host potential; 92 samples tested.
- Aquatic invertebrate larvae: 290 samples from genera including Baetis, Rhithrogena, Leuctra, Hydropsyche, Simulium, Philopotamus, Plectrocnemia, Amphinemura collected in 2012; stored in ethanol for method development and testing.
- Sampling context: Largely aligned with DURESS fieldwork; otter sampling not limited to DURESS catchments.

## DNA extraction and laboratory methods
- DNA extraction methods tailored to sample type:
  - Fish gut/gill: QIAamp DNA mini kit (tissue protocol).
  - Fish/feces: QIAamp Fast DNA Stool Mini Kit.
  - Invertebrate larvae: Gentra Puregene DNA kit with in-house developed protocol (freeze-thaw and grinding).
- Molecular testing:
  - Nested PCR targeting the small subunit rRNA (ssu rRNA) gene; positive amplicons sequenced for species identification.
  - C. parvum and C. hominis samples genotyped at gp60 locus.
  - Invertebrate larvae additionally tested with real-time PCR targeting C. hominis and an internal control to assess inhibition.
  - Positive and negative controls included; sequencing outsourced to Source Bioscience; analysis at CRU.
- Accreditation: CRU previously Clinical Pathology Accreditation; now ISO15189.

## Data structure and content
- Two main CSV datasets:
  - Results_Invertebrate_Larvae.csv
  - Results_Biofilm_Fish_Mammals.csv
- Key fields:
  - Sample identifiers and metadata: Sample_number, Sample_Description, Site, Sample_group, Host, Sample_Type, CRU_Ref.
  - Molecular results: n18S_result (Neg/Pos), GP60 (gp60 results), Sequencing (result of sequencing).
  - PCR metrics: Ch_Ct_value (C. hominis real-time PCR Ct value), IC_Ct_value (internal control Ct).
  - Invertebrates: Number_of_larvae_pooled(Seeded_with_C.hominis_oocysts), plus description of larva type.
- Site descriptions are linked to a separate DURESS_CU_site_description.csv file.
- Data quality notes:
  - Uncertain mammal sources marked with a question mark (e.g., Mink?).
  - Negative/positive/Not Done statuses used across tests.
- Reference datasets describe methodologies and the sampling framework for cross-referencing results.

## Practical use and aims for analysts
- Enables analysis of Cryptosporidium presence across fish, otters, and invertebrates within upland Welsh river systems.
- Supports correlation analyses between host type, site, and molecular results; potential development of predictive models for parasite presence and transmission pathways.
- Data provenance and metadata enable reproducibility and integration with related DURESS datasets for broader ecological or epidemiological insights.