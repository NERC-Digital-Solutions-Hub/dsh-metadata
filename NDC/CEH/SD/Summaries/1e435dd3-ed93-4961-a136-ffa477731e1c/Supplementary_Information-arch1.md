# Description of the data

- A dataset detailing a molecular analysis of tsetse flies collected in Hurungwe District, Mashonaland West Province, Zimbabwe, from February to November 2014.
- Species studied: Glossina pallidipes (Gp) and Glossina morsitans morsitans (Gmm).
- Investigated pathogens and endosymbionts:
  - Trypanosome species: Trypanosoma brucei s.l., T. b. rhodesiense, T. vivax, T. congolense, T. simiae (Tsavo), T. simiae, and T. godfreyi.
  - Endosymbionts: Sodalis glossinidius and Wolbachia spp.
- Context: Hurungwe District is Zimbabwe’s sleeping sickness focus with rising case numbers preceding the study; part of the Dynamic Drivers of Disease in Africa Consortium (DDDAC) research on trypanosomiasis, wellbeing, and ecosystems; funded by NERC (NE/J000701/1) with ESPA support.

## Sampling and laboratory methods

- Field sampling:
  - Traps: Epsilon traps and fly rounds deployed along a 110 km transect with 10 km intervals; 3 km fly rounds conducted at 12 sites and repeated 11 times over seven months; additional traps in selected sites.
  - Specimens: 101 Gmm and 108 Gp tsetse flies analyzed molecularly; microscopic examination of 2092 flies for trypanosome infections.
- Laboratory workflow:
  - DNA extraction from tsetse using Qiagen DNeasy kits; samples stored at -20°C.
  - Endosymbiont detection:
    - FliC PCR for Wigglesworthia glossinidius (primary endosymbiont).
  - Trypanosome detection and speciation:
    - ITS-PCR to discriminate trypanosome species/subspecies by amplicon size.
    - SRA gene PCR for samples positive for T. brucei s.l. to indicate human serum resistance.
  - Additional symbiont analyses:
    - Sodalis glossinidius: GroEL PCR.
    - Wolbachia: FtsZ and wsp PCR.
  - Quality controls: Negative and positive controls included for all PCRs; amplicons visualized on 1.5% agarose gel with GelRed; sizes compared to a 100 bp ladder.
- Sample handling:
  - Tsetse stored in cryotubes with desiccants; surface sterilized prior to DNA extraction; samples processed individually.

## Dataset and variables

- File: Hurungwe_tsetse_PCR.csv
- Variables (binary outcomes: 1 = positive, 0 = negative):
  - Species: Gmm (Glossina morsitans morsitans) or Gp (Glossina pallidipes)
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

- Contextual notes:
  - The dataset accompanies a Table 1 that describes these variables.
  - The samples exclude four cases where FliC results suggested insufficient DNA for molecular analysis.

## Context, aims, and uses

- Objective: Determine which trypanosome species are present in the tsetse population and assess associations with endosymbionts (Sodalis glossinidius and Wolbachia).
- Broader aim: Contribute to understanding the relationship between trypanosomiasis, wellbeing, and ecosystems within a sleeping sickness focus area.

## Potential analyses and applications

- Estimate prevalence of each trypanosome species and endosymbiont across tsetse species and sexes.
- Explore associations between trypanosome infections and endosymbiont presence (e.g., co-infection patterns).
- Compare molecular (PCR-based) results with microscopic infection status.
- Investigate species-specific differences (Gp vs Gmm) in parasite and symbiont carriage.
- Assess potential signals for human-infective T. brucei s.l. via SRA-positive results.
- Use as a basis for modeling transmission risk within the Hurungwe sleeping sickness focus.

## Data quality, limitations, and considerations

- Limitations:
  - Study confined to a single district and a defined 2014 time window.
  - Some samples excluded due to insufficient DNA (4 samples).
  - Binary outcome data may limit granularity (no parasitemia intensity or quantitative measures).
- Data quality considerations:
  - Rigorous PCR controls and gel-based validation described.
  - Field sampling design provides spatially structured sampling (10 km transects, 110 km extent).

## References

- Baldo L, Dunning Hotopp JC, Jolley KA, Bordenstein SR, Biber SA, Choudhury RR, Hayashi C, Maiden MC, Tettelin H & Werren JH (2006). Multilocus sequence typing system for the endosymbiont Wolbachia pipientis. Applied and Environmental Microbiology 72, 7098-110.
- Cheng Q, Ruel TD, Zhou W, Moloo SK, Majiwa P, O'Neil SL & Aksoy S (2000). Tissue distribution and prevalence of Wolbachia infections in tsetse flies, Glossina spp. Medical and Veterinary Entomology, 14: 44-50.
- Dennis JW, Durkin SM, Horsley Downie JE, Hamill LC, Anderson NE, MacLeod ET. (2014) Sodalis glossinidius prevalence and trypanosome presence in tsetse from Luambe National Park, Zambia. Parasite and Vectors, 7: 378.
- Hamidou Soumana I, Loriod B, Ravel S, Tchicaya B, Simo G, Rihet P & Geiger A (2014) The transcriptional signatures of Sodalis glossinidius in the Glossina palpalis gambiensis flies negative for Trypanosoma brucei gambiense contrast with those of this symbiont in tsetse flies positive for the parasite: possible involvement of a Sodalis -hosted prophage in fly Trypanosoma refractoriness? Infection Genetics and Evolution, 24: 41-56.
- Matthew CZ: PhD Thesis. Biological and Molecular Aspects of Sodalis glossinidius. 2007, The University of Edinburgh, College of Medicine and Veterinary Medicine.
- Njiru ZK, Constantine CC, Guya S, Crowther J, Kiragu JM, Thompson RC & Dávila AM (2005) The use of ITS1 rDNA PCR in detecting pathogenic African trypanosomes. Parasitology Research, 95: 186-192.
- Picozzi K, Carrington M & Welburn SC (2008) A multiplex PCR that discriminates between Trypanosoma brucei brucei and zoonotic T. b. rhodesiense. Exp Parasitol, 118: 41-46.
- Shereni W, Anderson NE, Nyakupinda L, Cecchi G (2016). Spatial distribution and trypanosome infection of tsetse flies in the sleeping sickness focus of Zimbabwe in Hurungwe District. Parasit Vectors, 9(1):605.