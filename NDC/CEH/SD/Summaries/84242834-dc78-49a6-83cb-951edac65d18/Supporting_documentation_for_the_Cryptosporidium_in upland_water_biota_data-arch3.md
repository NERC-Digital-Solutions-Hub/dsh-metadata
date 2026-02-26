# Supporting documentation for the Cryptosporidium in Welsh upland water biota data (2012-2015)

## Aim
- Report and support a sample survey of Cryptosporidium in Welsh upland water biota as part of the wider DURESS project.
- No treatments or replication during sampling; laboratory controls present in assays.

## What was sampled
- Fish tissues and contents:
  - Gills and gut contents from 74 fish across 11 upland river sites (summer 2012); samples prepared for 16 salmon (17 gills), 41 brown trout, 16 bullhead.
  - Faeces from fish collected live (117 fish) during summer 2013 via ankle anesthesia and gut massage.
- Mammals:
  - Faeces from land mammals around riparian zones (41 samples, May 2013); otter samples tested but sourced from a separate study (92 otter faecal samples) due to regulations.
- Invertebrates:
  - Aquatic invertebrate larvae (n=290) from eight genera collected June 2012; examined to assess potential parasite transport via food webs.
- Data files:
  - Results_Invertebrate_Larvae.csv for invertebrates.
  - Results_Biofilm_Fish_Mammals.csv for fish, biofilm, and mammal samples.
- Site information:
  - Site details referenced from DURESS_CU_site_description.csv.

## Sampling design and process
- Sampling framed to align with DURESS work packages; no randomization or replication reported at sampling level.
- Specimens collected, processed, and stored for testing at the Cryptosporidium Reference Unit (CRU); samples frozen at -20°C where applicable.

## Laboratory methods and assays
- DNA extraction:
  - Fish gut/gill: QIAamp DNA mini kit (tissue protocol).
  - Fish/feces: QIAamp Fast DNA Stool mini kit.
  - Invertebrate larvae: Gentra Puregene DNA kit; additional in-house grinding and freeze-thaw steps.
- Molecular testing:
  - Nested PCR targeting small subunit rRNA (ssu rRNA) gene; positive amplicons sequenced to identify Cryptosporidium species.
  - gp60 locus genotyping for Cryptosporidium parvum and Cryptosporidium hominis.
  - Invertebrate larvae also tested with real-time PCR for C. hominis and an internal control to check inhibition.
- Quality controls:
  - Positive and negative controls included; sequencing performed by CRU or outsourced (Source Bioscience for sequencing); accreditation through Clinical Pathology Accreditation (now ISO15189).

## Data structure and metadata
- Results_Invertebrate_Larvae.csv:
  - Sample_number, Sample_Description, Number_of_larvae_pooled, Site, n18S, Ch_Ct_value, IC_Ct_value.
- Results_Biofilm_Fish_Mammals.csv:
  - Site, Sample_group, Host, Sample_Type, CRU_Ref, n18S_result, GP60, Sequencing.
- Site descriptions are linked via DURESS_CU_site_description.csv; ambiguous host identifications marked with a question mark (e.g., Mink?).

## Data governance and accessibility
- Data generated and deposited as part of a broader research project (DURESS); methods and datasets are described for reuse and verification.
- Detailed metadata provided to support interpretation and cross-study integration.

## Key limitations and caveats
- Sampling lacked replication and may reflect project constraints rather than a fully randomized survey.
- Otter sample origin varied (some from non-local studies), introducing potential host-source biases.
- Host species identification for some mammal fecal samples was uncertain (denoted with question marks), affecting host attribution.
- Data transformation and metadata completeness are critical for reuse due to varied sample types and sources.

## References (methodological basis)
- Alves M, Xiao L, Sulaiman I, et al. Subgenotype analysis of Cryptosporidium isolates (2003).
- Hadfield SJ, Robinson G, Elwin K, Chalmers RM. Detection of Cryptosporidium spp. in human clinical samples (2011).
- Jiang J, Alderisio KA, Xiao L. Distribution of Cryptosporidium genotypes in watershed samples (2005).