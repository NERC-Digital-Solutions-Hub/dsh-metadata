# Hurungwe_tsetse_PCR.csv

## Overview
- Dataset from a laboratory analysis of tsetse flies in Hurungwe District, Mashonaland West Province, Zimbabwe (February–November 2014).
- Aimed at identifying trypanosome species and the prevalence of tsetse endosymbionts in two tsetse species.
- Part of the Dynamic Drivers of Disease in Africa Consortium (DDDAC) research on the relationship between trypanosomiasis, well-being, and ecosystems; funded by NERC and ESPA.

## Data Content
- Molecular analysis performed on:
  - 101 Glossina morsitans morsitans (Gmm)
  - 108 Glossina pallidipes (Gp)
- Microscopic screening of 2092 flies for trypanosome infections.
- Targets analyzed:
  - Trypanosome species: T. vivax, T. godfreyi, T. simiae (Tsavo), T. simiae, T. congoleose, Trypanozoon, T. brucei rhodesiense
  - Endosymbionts: Sodalis glossinidius, Wolbachia (ftsZ and wsp markers)
- Data file: Hurungwe_tsetse_PCR.csv
  - Variables include: Species (Gmm or Gp), Sex (Male/Female), and binary indicators (Positive=1, Negative=0) for each target organism (various Trypanosoma spp., Sodalis glossinidius, Wolbachia markers).

## Methods
- Field sampling design:
  - 110 km transect along southern Zambezi Valley escarpment
  - Traps: Epsilon traps and fly rounds at 10 km intervals
  - 3 km fly rounds conducted on 12 sites, repeated 11 times over ~7 months
  - Additional traps deployed at selected sites
- Laboratory workflow:
  - Specimens stored in cryotubes with desiccants; transport to University of Edinburgh
  - Surface sterilisation with 5% sodium hypochlorite and PBS
  - DNA extraction with Qiagen DNeasy kits; stored at -20°C
  - PCR assays:
    - FliC gene to detect Wigglesworthia glossinidia (endosymbiont)
    - ITS-PCR to discriminate trypanosome species/subspecies
    - SRA gene PCR for human serum resistance in T. brucei s.l.
    - GroEL PCR for Sodalis glossinidius
    - FtsZ and wsp PCRs for Wolbachia detection
  - Controls: negative and positive controls included for all PCRs
  - Visualization: 1.5% agarose gel with GelRed; amplicon sizes compared to a 100 bp ladder
- Data handling:
  - 4 samples with negative Wigglesworthia results excluded due to likely insufficient DNA
  - Data described in Table 1 (variable definitions)

## Data Structure and Metadata
- File: Hurungwe_tsetse_PCR.csv
- Variables (examples):
  - Species: Gmm or Gp
  - Sex: Male or female
  - Trypanosoma_vivax, Trypanosoma_godfreyi, Trypanosoma_simiae (Tsavo), Trypanosoma_simiae, Trypanosoma_congolense, Trypanozoon, Trypanosoma_brucei_rhodesiense
  - Sodalis_glossinidius
  - Wolbachia_ftsZ, Wolbachia_wsp
  - Each Trypanosoma and endosymbiont variable coded as 1 (Positive) or 0 (Negative)
- References for methods and primers provided (listed in the document)

## Data Quality and Limitations
- Limited to two Glossina species sampled within a single district and time frame.
- DNA quantity issues led to discarding four samples from molecular analysis.
- Microscopically assessed infections conducted on a larger set (2092 flies) than those subjected to molecular typing.
- Data are aligned with specific PCR targets; cross-study comparability requires harmonization of marker sets.

## Relevance for Data Leaders
- Demonstrates end-to-end data lifecycle: field sampling design, specimen preservation, molecular analytics, and data capture in a structured CSV with clear variable definitions.
- Highlights data discoverability and metadata needs:
  - Clear file naming, documented variable definitions, and cited protocols support reuse and integration into broader datasets.
- Useful for cross-site comparisons of trypanosome prevalence and endosymbiont associations in tsetse populations, aiding strategy for disease risk assessment and ecological studies.
- Illustrates governance considerations:
  - Storage conditions (-20°C), data provenance (lab protocols, references), and explicit quality control steps (controls, exclusion criteria).

## Potential Applications and Next Steps
- Assess relationships between tsetse endosymbionts and trypanosome carriage.
- Compare prevalence across species and sexes; integrate with environmental or network data from the ES​​PA program.
- Incorporate into larger surveillance databases to support policy and partner network data sharing, with attention to metadata standardization and data accessibility.

## References (Methods and Markers)
- Baldo L, et al. Multilocus typing system for Wolbachia pipientis. Appl Environ Microbiol. 2006.
- Cheng Q, et al. Tissue distribution and prevalence of Wolbachia in tsetse flies. Med Vet Entomol. 2000.
- Dennis JW, et al. Sodalis glossinidius prevalence and trypanosome presence in tsetse. Parasite Vector. 2014.
- Hamidou Soumana I, et al. Sodalis transcriptional signatures in relation to trypanosome infection. Infect Genet Evol. 2014.
- Matthew CZ. PhD thesis on Sodalis glossinidius. Univ. of Edinburgh. 2007.
- Njiru ZK, et al. ITS1 rDNA PCR for detecting African trypanosomes. Parasitol Res. 2005.
- Picozzi K, et al. Multiplex PCR for distinguishing T. brucei subspecies. Exp Parasitol. 2008.
- Shereni W, et al. Spatial distribution and trypanosome infection in Hurungwe District. Parasito Vectors. 2016.