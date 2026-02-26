# Hurungwe_tsetse_PCR.csv

## Overview
- Describes a dataset from a laboratory analysis of trypanosomes and tsetse endosymbionts in tsetse flies from Hurungwe District, Mashonaland West Province, Zimbabwe (Feb–Nov 2014).
- Part of the Dynamic Drivers of Disease in Africa Consortium (DDDAC) research on trypanosomiasis, well-being, and ecosystems.
- Funded by NERC project NE/J000701/1 with support from ESPA.
- Data file provides presence/absence results for selected trypanosome species and tsetse endosymbionts, derived from PCR analysis.

## Data content and study design
- Specimens: 101 Glossina morsitans morsitans and 108 Glossina pallidipes sampled (total 209 flies).
- Sampling design: February 2014 to November 2014 using Epsilon traps and fly rounds along a 110 km transect (sampling at 10 km intervals); 3 km fly rounds conducted at 12 sites, repeated 11 times over ~7 months; additional traps deployed at selected sites.
- Field processing: Flies stored in cryotubes with desiccants, surface sterilised, crushed, and DNA extracted using Qiagen DNeasy kits; DNA stored at -20°C.
- Primary analyses: Polymerase chain reaction (PCR) to detect:
  - Endosymbiont Wigglesworthia glossinidia (FliC gene).
  - African trypanosomes using ITS-PCR to discriminate species/subspecies by amplicon size.
  - Human-infective T. brucei s.l. using SRA gene target if T. brucei s.l. was detected.
  - Secondary bacterial symbionts: Sodalis glossinidius (GroEL PCR) and Wolbachia (FtsZ and wsp genes).
- Quality controls: Negative and positive controls included for all PCRs; results visualized on 1.5% agarose gels with GelRed; amplicon sizes referenced to a 100 bp ladder.
- Data product: CSV file titled Hurungwe_tsetse_PCR.csv with a corresponding variable table (Table 1).

## Data structure and variables
- File: Hurungwe_tsetse_PCR.csv
- Variables (binary 1 = Positive, 0 = Negative):
  - Species: Glossina morsitans morsitans (Gmm) or Glossina pallidipes (Gp)
  - Sex: Male or Female
  - Trypanosoma_vivax
  - Trypanosoma_godfreyi
  - Trypanosoma_simiae_(Tsavo)
  - Trypanosoma_simiae
  - Trypanosoma_congolense
  - Trypanozoon
  - Trypanosoma_brucei_rhodesiense
  - Sodalis_glossinidius
  - Wolbachia_ftsZ
  - Wolbachia_wsp

## Data quality, processing, and limitations
- Data processing: All samples subjected to PCR; four samples with negative FliC results were excluded from further molecular analysis due to presumed insufficient DNA.
- Documentation: Variables and definitions are explicitly described (see Table 1 in the dataset description).
- Limitations and considerations:
  - Potential sample loss or degradation since DNA stored at -20°C and some specimens excluded.
  - Representation limited to the 209 flies sampled in 2014 from this specific district and transect.
  - Results reflect presence/absence only (no quantitative load data provided in the CSV).
  - Metadata in the accompanying description (sampling design, sites, timing) supports interpretation but is not all-encompassing beyond what is described.

## Usage, sharing, and governance
- Data format: CSV with clearly defined binary outcome variables and species metadata.
- Appropriate use: Reuse should cite the original study (DDDAC, NERC ESPA funding) and the dataset file Hurungwe_tsetse_PCR.csv; suitable for analyses on host–parasite–symbiont associations in tsetse populations.
- Documentation: Descriptions of methods, primers, and references are provided to support understanding and reproduction of analyses.
- Access considerations: While not explicitly stated in the document, adherence to data provenance and proper citation is recommended; the dataset is tied to published work (Parasit Vectors 2016) and associated references.

## References and methodological background
- Baldo et al. 2006; multilocus typing for Wolbachia
- Cheng et al. 2000; tissue distribution of Wolbachia in tsetse
- Dennis et al. 2014; Sodalis glossinidius prevalence and trypanosome presence
- Hamidou Soumana et al. 2014; Sodalis-host interactions
- Matthew 2007; Sodalis glossinidius PhD work
- Njiru et al. 2005; ITS1 rDNA PCR for detecting African trypanosomes
- Picozzi et al. 2008; multiplex PCR for T. brucei subspecies
- Shereni et al. 2016; spatial distribution of trypanosome infection in Hurungwe District