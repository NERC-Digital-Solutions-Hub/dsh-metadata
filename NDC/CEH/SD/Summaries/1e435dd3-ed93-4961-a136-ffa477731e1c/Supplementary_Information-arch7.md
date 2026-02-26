# Description of the data

## Overview
- Dataset from a laboratory analysis investigating the presence of trypanosomes and prevalence of tsetse endosymbionts in tsetse flies.
- Sampling in Hurungwe District, Mashonaland West Province, Zimbabwe, February 2014 to November 2014.
- Two tsetse species studied: Glossina pallidipes and Glossina morsitans morsitans.
- Trypanosome species examined: T. brucei s.l. (including T. b. rhodesiense), T. vivax, T. congolense, T. simiae (Tsavo and non-Tsavo), and T. godfreyi.
- Endosymbionts tested: Sodalis glossinidius and Wolbachia spp.
- Research context: part of DD-DAC project on relationships between trypanosomiasis, wellbeing, and ecosystems; funded by NERC and ESPA.

## Spatial and sampling design
- Sampling along a 110 km transect on the southern escarpment of the Zambezi Valley.
- Sampling framework:
  - 10 km intervals along transect for traps.
  - 12 sites with 3 km fly rounds.
  - Fly rounds repeated 11 times over a 7-month period.
- Additional traps deployed in selected sites.
- Spatial focus is a single district; coordinates are not provided in the summary.

## Data collection and laboratory methods
- Specimen handling:
  - Flies stored in cryotubes with desiccants; surface sterilised prior to processing.
  - Individual flies crushed for DNA extraction using Qiagen DNeasy kits; DNA stored at -20°C.
- Molecular assays:
  - Endosymbiont detection: FliC-based PCR for Wigglesworthia glossinidius; GroEL PCR for S. glossinidius; FtsZ and wsp PCRs for Wolbachia.
  - Trypanosome detection and speciation: ITS-PCR for species discrimination; SRA gene PCR for human serum resistance in T. brucei s.l.
  - PCR controls included (positive and negative); products visualised on 1.5% agarose gels.
- Data processing:
  - Four samples excluded due to insufficient DNA.
  - Analyzed dataset comprises 101 Glossina morsitans morsitans and 108 Glossina pallidipes.
- Data file:
  - Hurungwe_tsetse_PCR.csv containing variables and descriptions.

## Data structure and variables (Table 1)
- Species: Gmm (Glossina morsitans morsitans) or Gp (Glossina pallidipes).
- Sex: Male or female.
- Trypanosoma_vivax: 1 = positive, 0 = negative.
- Trypanosoma_godfreyi: 1 = positive, 0 = negative.
- Trypanosoma_simiae_(Tsavo): 1 = positive, 0 = negative.
- Trypanosoma_simiae: 1 = positive, 0 = negative.
- Trypanosoma_congolense: 1 = positive, 0 = negative.
- Trypanozoon: 1 = positive, 0 = negative.
- Trypanosoma_brucei_rhodesiense: 1 = positive, 0 = negative.
- Sodalis_glossinidius: 1 = positive, 0 = negative.
- Wolbachia_ftsZ: 1 = positive, 0 = negative.
- Wolbachia_wsp: 1 = positive, 0 = negative.

## How this data can be used in GIS
- Map distribution of tsetse species and the prevalence of infections and endosymbionts across the transect.
- Create prevalence surfaces or barcoded maps by species, sex, and pathogen/endosymbiont status.
- Integrate with environmental layers along the 110 km transect to explore ecological drivers of infection and symbiont prevalence.
- Assess spatial clustering or hotspots of trypanosome presence in relation to sampling sites.
- Combine with additional occurrence data to support policy, public health planning, or ecological research within Zimbabwe’s sleeping sickness focus.

## Data quality and limitations
- Molecular analysis completed on a subset of collected flies (101 Gmm and 108 Gp); four samples excluded due to insufficient DNA.
- Sampling along a single transect within one district over a defined period (2014); may limit generalizability beyond the study area and time frame.
- Spatial coordinates are not provided in the dataset summary; relies on the described transect and site framework for spatial interpretation.
- Binary presence/absence data per pathogen and endosymbiont; does not provide pathogen load or intensity.

## References (for methods and context)
- Baldo et al. 2006; Choudhury and Welburn; various foundational PCR primers and methods cited (e.g., ITS-PCR for trypanosomes, SRA gene assay, GroEL for Sodalis, Wolbachia FtsZ/wsp).
- Shereni et al. 2016; related spatial distribution and infection work in Hurungwe District.
- Dennis et al. 2014; Sodalis prevalence and trypanosome presence in tsetse (Zambia) as methodological references.
- Njiru et al. 2005; ITS1 rDNA PCR for detecting African trypanosomes.