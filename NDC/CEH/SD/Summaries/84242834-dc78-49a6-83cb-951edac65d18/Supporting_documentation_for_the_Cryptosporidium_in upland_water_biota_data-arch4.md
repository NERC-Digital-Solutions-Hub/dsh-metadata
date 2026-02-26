# Supporting documentation for the Cryptosporidium in Welsh upland water biota data (2012-2015)

## Overview
- Describes a sample survey within the wider DURESS project testing Cryptosporidium in Welsh upland water biota (2012–2015).
- No field treatments or replication; laboratory controls used but not during sampling.
- Assessed Cryptosporidium presence across fish (gills, gut contents, faeces), terrestrial and aquatic mammals (otters), and aquatic invertebrate larvae; sampling largely aligned with DURESS activities.

## Data collection and sampling
- Fish sampling (gills and gut contents): 74 fish from 11 Welsh upland river sites (2012); culled by electrofishing, gut contents (n=73) and gills (n=74) dissected for testing.
  - Paired gut and gill samples: 16 salmon (17 gills), 41 brown trout, 16 bullhead.
- Fish faeces: Live sampling method developed (2013) to test more fish without culling.
  - Faecal samples from 117 trout and salmon, collected under anaesthesia and frozen for testing.
- Otter faeces: 41 collected in-situ (animal ID not always unambiguous); 92 otter faecal samples from a separate study (England and Wales, 2011–2015) used to assess otter host potential.
- Invertebrate larvae: 290 aquatic larvae from eight genera collected (June 2012) around the Llyn Brianne catchment; stored in ethanol for method development.
- Site references: Sample locations linked to a supporting site description file (Result_Bioreports site mapping).

## Data processing and testing
- DNA extraction:
  - Gill/gut samples: QIAamp DNA Mini Kit (Qiagen).
  - Fecal samples: QIAamp Fast DNA Stool Mini Kit (Qiagen).
  - Aquatic invertebrate larvae: Gentra Puregene DNA Kit (Qiagen); larvae ground in liquid nitrogen with freeze–thaw treatment.
- Molecular testing:
  - Nested PCR of small subunit rRNA (ssu rRNA) gene; positive amplicons sequenced for species identification.
  - Cryptosporidium parvum/hominis positives genotyped at gp60 locus.
  - Invertebrate larvae additionally screened with real-time PCR targeting C. hominis and an internal control.
  - Controls: positive and negative PCR controls; invertebrate-positive controls seeded with C. hominis oocysts.
- Provenance and accreditation:
  - Methods and instruments used at the Cryptosporidium Reference Unit (CRU); accreditation originally under Clinical Pathology Accreditation, now ISO15189.
  - DNA sequencing outsourced to Source Bioscience; sequence analysis performed at CRU.

## Data structure and data files
- Results_Invertebrate_Larvae.csv
  - Sample_number: unique CRU sample identifier.
  - Sample_Description: type of invertebrate larva tested.
  - Number_of_larvae_pooled(Seeded_with_C.hominis_oocysts): quantity tested, including seeded larvae.
  - Site: sampling location (mapped to a site description file).
  - n18S: nested ssu rRNA PCR result (Neg/Pos).
  - Ch_Ct_value: Ct value from C. hominis real-time PCR.
  - IC_Ct_value: Ct value from internal control PCR.
- Results_Biofilm_Fish_Mammals.csv
  - Site: sampling location (mapped to site descriptions).
  - Sample_group: source category (e.g., biofilm, fish, etc.).
  - Host: specific sample source (e.g., trout); N/A for biofilm.
  - Sample_Type: nature of the sample (e.g., biofilm, faeces).
  - CRU_Ref: unique CRU sample identifier.
  - n18S_result: nested ssu rRNA PCR result and sequencing status.
  - GP60: gp60 PCR result.
  - Sequencing: sequencing outcome (Pos/Neg/Not Done).
- Site mapping: both files reference a supporting site description file (DURESS_CU_site_description.csv).

## Data quality, controls, and governance
- Study design notes:
  - No field replication; sampling aligned with broader DURESS activities.
  - Controls used in laboratory assays; no replication at the collection stage.
- Data quality considerations:
  - Multiple sample types with different collection methods (culling vs. live sampling).
  - Potential host ID ambiguity for otter faeces; otter samples also drawn from an external study.
  - Accreditation and QA maintained at CRU; sequencing outsourced to a commercial provider.
- Data provenance and reuse:
  - Detailed methodological descriptions support replication and secondary analyses.
  - Data assets are organized into clearly defined CSV files with explicit field definitions and cross-referencing to site descriptions.

## Limitations and considerations for data leaders
- Limited field replication may affect generalizability; cross-site comparisons should consider sampling context.
- Mixed sampling provenance (in-study vs. external otter samples) may introduce variability in host attribution.
- Data discovery is facilitated by structured metadata and explicit file naming, aiding discoverability and integration with broader data systems.

## References
- Alves, M., Xiao, L., Sulaiman, I., Lal, A.A., Matos, O., Antunes, F., 2003. Subgenotype analysis of Cryptosporidium isolates from humans, cattle, and zoo ruminants in Portugal. J. Clin. Microbiol. 41, 2744-2747.
- Hadfield, S.J., Robinson, G., Elwin, K., Chalmers, R.M., 2011. Detection and differentiation of Cryptosporidium spp. in human clinical samples using real-time PCR. J. Clin. Microbiol. 49, 918-924.
- Jiang, J., Alderisio, K.A., Xiao, L., 2005. Distribution of Cryptosporidium genotypes in storm event water samples from three watersheds in New York. Appl. Environ. Microbiol. 71, 4446-4454.