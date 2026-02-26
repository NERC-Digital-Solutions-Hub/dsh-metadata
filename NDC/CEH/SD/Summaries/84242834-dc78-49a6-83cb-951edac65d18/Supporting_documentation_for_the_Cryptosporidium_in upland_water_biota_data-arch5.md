# Supporting documentation for the Cryptosporidium in Welsh upland water biota data (2012-2015)

## Overview
- Describes a sample survey linked to the wider DURESS project, testing for the protozoan parasite Cryptosporidium across multiple sample types collected from Welsh upland river ecosystems (2012–2015).
- No treatments or replication during sampling; controls were included in laboratory assays.
- Data were generated from fish (gills, gut contents, faeces), aquatic invertebrates, and mammal faeces (otters), with archival testing at the Cryptosporidium Reference Unit (CRU).

## Data collection and sample types
- Fish samples:
  - Gills and gut contents from 74 fish (11 sites) collected by electrofishing in summer 2012; paired gut and gill samples for a subset (16 salmon, 41 brown trout, 16 bullhead).
  - Fish faeces collected non-lethally from 117 fish (trout and salmon) in summer 2013 while under anaesthetic.
- Land and aquatic mammal samples:
  - 41 faecal samples from terrestrial/aquatic mammals near river riparian zones (morphology used to identify source; some uncertainty).
  - 92 otter faecal samples from a separate study (2011–2015) due to testing regulations; used to explore otter as a potential host.
- Invertebrate sampling:
  - 290 aquatic invertebrate larvae (genera Baetis, Rhithrogena, Leuctra, Hydropsyche, Simulium, Philopotamus, Plectrocnemia, Amphinemura) collected in June 2012 for method development and screening.
- Site scope:
  - Sampling across 11 Welsh upland river sites; results linked to a site description file (DURESS_CU_site_description.csv).

## Laboratory methods and data provenance
- DNA extraction:
  - Gut/gill tissues: QIAamp DNA mini kit (Qiagen).
  - Fish/mammal faeces: QIAamp Fast DNA Stool Mini Kit (Qiagen).
  - Invertebrate larvae: Gentra Puregene DNA kit with in-house developed protocol; includes liquid nitrogen grinding and freeze-thaw cycles.
- Molecular testing:
  - Nested PCR targeting the small subunit rRNA (ssu rRNA) gene; positive amplicons sequenced for species ID.
  - gp60 locus genotyping for Cryptosporidium parvum and C. hominis-positive samples.
  - Invertebrate larvae: real-time PCR targeting C. hominis with an internal control to check for inhibition.
  - All assays included positive and negative controls; CRU accreditation (formerly Clinical Pathology Accreditation; now ISO15189).
  - DNA sequencing outsourced to Source Bioscience; subsequent analysis performed at CRU.
- Data handling and structure:
  - Two primary CSV data files:
    - Results_Invertebrate_Larvae.csv: fields include Sample_number, Sample_Description, Number_of_larvae_pooled(Seeded_with_C.hominis_oocysts), Site, n18S, Ch_Ct_value, IC_Ct_value.
    - Results_Biofilm_Fish_Mammals.csv: fields include Site, Sample_group, Host, Sample_Type, CRU_Ref, n18S_result, GP60, Sequencing, plus interpretation (Neg/Pos/Not Done; with uncertainty marked by a question mark when host source is ambiguous).

## Data quality, governance, and limitations
- Quality assurance:
  - Use of multiple validated methods (nested PCR, gp60 genotyping, real-time PCR) with sequencing confirmation.
  - Inclusion of positive/negative controls in all assays.
  - Accreditation history indicates adherence to rigorous laboratory standards (Clinical Pathology Accreditation transitioning to ISO15189).
- Data provenance and transparency:
  - Clear documentation of sample origins, processing steps, and testing protocols.
  - Structured, machine-readable data files with explicit field definitions; site references link to a separate site description file.
- Limitations and uncertainties:
  - Animal source identification for some mammal faeces was not unambiguous (noted with a question mark in host designation).
  - Otter fecal samples were sourced from a broader study outside the primary DURESS sampling scope.
  - Some sample types may reflect complex ecological relationships (e.g., potential transport of parasites via invertebrates) requiring careful interpretation.
  
## Reuse and stewardship implications
- The dataset is organized for discoverability and reuse, with:
  - Standardized sample identifiers (CRU references) and site codes.
  - Comprehensive metadata describing sample type, host, collection context, and PCR results.
  - Clear documentation of laboratory methods and accreditation status to support reproducibility.
- Suitable for prevalence and transmission studies of Cryptosporidium in upland freshwater ecosystems, cross-referencing with the DURESS project data.
- For future updates or extended analyses, the same structure can accommodate additional sample types or sites, given the documented data schema and referencing scheme.