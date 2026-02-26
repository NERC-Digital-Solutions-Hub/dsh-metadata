# Hurungwe_tsetse_PCR.csv

## Overview
- Dataset describing molecular analysis of trypanosomes and tsetse endosymbionts in tsetse flies from Hurungwe District, Mashonaland West Province, Zimbabwe (Feb–Nov 2014).
- Part of research on the relationship between trypanosomiasis, well-being, and ecosystems (DDDAC); funded by NERC project NE/J000701/1 with ESPA support.
- Aims to identify trypanosome species present in tsetse and their association with endosymbionts; supports environmental health monitoring and policy appraisal.

## Study area and sampling design
- Location: Hurungwe District is Zimbabwe’s only sleeping sickness focus; prior years showed increasing cases.
- Tsetse species sampled: Glossina pallidipes (Gp) and Glossina morsitans morsitans (Gmm).
- Sampling methods: Epsilon traps and fly rounds; transect along southern Zambezi Valley escarpment (10 km interval, 110 km length); 3 km fly rounds at 12 sites, repeated 11 times over ~7 months; additional traps deployed at selected sites.
- Laboratory subset: 101 Gmm and 108 Gp tsetse subjected to molecular analysis; 2092 flies examined microscopically for trypanosomes.

## Laboratory methods
- DNA extraction: From crushed tsetse in 1.5 ml tubes using Qiagen DNeasy kits; DNA stored at -20°C.
- Pathogen detection:
  - Endosymbiont detection: FliC PCR for Wigglesworthia glossinidius (note: some spellings in sources).
  - Trypanosome detection: ITS-PCR (to discriminate species/subspecies by amplicon size); SRA gene PCR for samples positive for T. brucei s.l.
  - Endosymbionts: GroEL PCR for Sodalis glossinidius; FtsZ and wsp PCRs for Wolbachia.
- Quality control: Positive and negative controls included for all PCRs; gel electrophoresis on 1.5% agarose with GelRed; amplicon sizes referenced to a 100 bp ladder.
- Sample curation: Four samples with negative Wigglesworthia results excluded due to insufficient DNA for further molecular analysis.

## Dataset structure and variables
- File: Hurungwe_tsetse_PCR.csv
- Variables (as described):
  - Species: Gmm (Glossina morsitans morsitans) or Gp (Glossina pallidipes)
  - Sex: Male or Female
  - Trypanosoma_vivax: Positive=1, Negative=0
  - Trypanosoma_godfreyi: Positive=1, Negative=0
  - Trypanosoma_simiae_(Tsavo): Positive=1, Negative=0
  - Trypanosoma_simiae: Positive=1, Negative=0
  - Trypanosoma_congolense: Positive=1, Negative=0
  - Trypanozoon: Positive=1, Negative=0
  - Trypanosoma_brucei_rhodesiense: Positive=1, Negative=0
  - Sodalis_glossinidius: Positive=1, Negative=0
  - Wolbachia_ftsz: Positive=1, Negative=0
  - Wolbachia_wsp: Positive=1, Negative=0

## Data quality, management and provenance
- Sample handling and DNA quality controls implemented to ensure reliable molecular results.
- Storage and processing adhered to standardized protocols; four samples excluded due to insufficient DNA.
- Data description aligns with standardised outputs (e.g., reports, maps) for monitoring environmental health and vector-borne disease risk.

## Relevance to environmental monitoring
- Provides a cross-sectional snapshot of trypanosome prevalence in two tsetse species within a major sleeping sickness focus.
- Enables analysis of associations between trypanosomes and tsetse endosymbionts (Sodalis glossinidius and Wolbachia), which may influence vector competence.
- Supports monitoring of vector-borne disease risk, ecosystem health, and potential policy responses in Zimbabwe.

## References (methods and context)
- ITS1 rDNA PCR for trypanosomes: Njiru et al., 2005
- SRA gene PCR for human serum resistance: Picozzi et al., 2008
- Sodalis detection (GroEL): Matthew, 2007
- Wolbachia detection (FtsZ and wsp): Baldo et al., 2006; Cheng et al., 2000
- Related methodological context and prior findings: Dennis et al., 2014; Hamidou Soumana et al., 2014; Shereni et al., 2016

## Potential applications and considerations
- Time-bounded snapshot (2014) within Zimbabwe’s sleeping sickness focus; caution in extrapolating beyond Hurungwe without longitudinal data.
- Useful for trend analyses of parasite and endosymbiont prevalence in vector populations; informs risk modelling and targeted interventions.
- Data supports exploration of parasite–symbiont interactions and potential implications for tsetse control strategies.