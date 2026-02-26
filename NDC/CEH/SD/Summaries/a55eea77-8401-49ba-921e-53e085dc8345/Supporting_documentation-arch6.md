# Supporting documentation for dataset Molecular analysis of Glossina morsitans morsitans tsetse from Mambwe District, Zambia, 2013.

## Overview
- Describes the prevalence of trypanosomes and Sodalis glossinidius, and host blood meal analysis from Glossina morsitans morsitans tsetse flies.
- Collected during two intensive surveys in Mambwe District, Eastern Province, Zambia, in 2013.
- Aimed to monitor infection rates and tsetse feeding patterns to assess risk to humans and livestock; part of the Dynamic Drivers of Disease in Africa Consortium (DDDAC).

## Context and purpose
- Luangwa Valley is a historic human African trypanosomiasis (HAT) focus; land-use changes may influence tsetse dynamics and HAT epidemiology.
- Data contributed to the Zambia trypanosomiasis case study; funded by NERC (NE/J000701/1) with ESPA support.

## Methods

### Field sampling
- Two surveys: cold dry season (May/June 2013) and hot dry season (November 2013).
- Sampling with black screen fly rounds along a transect from the plateau to the valley floor (approx. 6 km per round; stops every 200 m; 1 km interval).
- Screens baited with phenols and acetone to improve efficiency; tsetse caught with nets and identified; GPS coordinates recorded; sampling at ~7 am.

### Laboratory analyses
- DNA extraction from tsetse fly samples; storage at -20°C.
- Trypanosoma detection:
  - ITS1 primers for initial screening of multiple Trypanosoma species.
  - Species-specific primers for T. vivax; for Trypanozoon-positive samples, primers for T. b. brucei, T. evansi, T. b. rhodesiense.
  - T. congolense subgroups (Savannah, Forest, Kilifi) when ITS1 ~700 bp.
- Sodalis glossinidius detection:
  - PCR targeting GroEL gene; ~290 samples analyzed.
- Blood meal analysis:
  - PCR targeting cytochrome b gene on samples with evidence of feeding.
  - Positive samples sequenced; ExoSAP-IT cleanup; sequencing with BigDye Terminator 3.1; terminator kit and ABI 3130x.
  - Sequences compared to public databases via NCBI BLAST to identify host species.

## Data and file details

### Dataset file
- DDDAC_tsetse_molecular_data2013.csv

### Variables
- Sample_id: unique observation identifier
- Survey: 'One' (May/June) or 'Two' (November)
- TCS-: PCR results for Trypanosoma congolense savannah
- T vivax: PCR results for Trypanosoma vivax
- T. b. brucei: PCR results for Trypanosoma brucei brucei
- T. b. rhodesiense: PCR results for Trypanosoma brucei rhodesiense
- Sodalis: PCR results for Sodalis glossinidius; 'Not analysed' if not tested
- Cyt b sequence: cytochrome b sequence result; 'Negative' if PCR done but no sequence; 'Not analysed' if insufficient DNA
- Scientific name: scientific name of the blood-meal host
- Common name: common host name; 'Not analysed' if not tested for that variable

### Geographical extent
- Longitude: 31.826 to 32.094
- Latitude: -13.248 to -13.828

## Data quality and references
- Includes positive and negative controls for PCR; gel electrophoresis visualization against a 100 bp ladder.
- Sequencing and BLAST-based host identification provide species-level information for blood meals.
- References detail sampling methodology and feeding-pattern analyses:
  - Ford et al. (1959); Transect fly-rounds
  - Van den Bossche & De Deken (2002); seasonal tsetse distribution
  - Shereni (1984); sampling alternatives
  - Muturi et al. (2011); tracking tsetse feeding via mitochondrial genes

## Potential uses and analyses
- Assess spatial and seasonal variation in trypanosome prevalence in tsetse populations.
- Examine presence/absence of Sodalis glossinidius and potential associations with trypanosome infections.
- Analyze feeding patterns by host species to identify major blood-meal sources.
- Integrate infection and feeding data with environmental or land-use factors to inform HAT risk assessments for humans and livestock.
- Create data products or dashboards enabling stakeholders to explore infection and feeding patterns interactively.

## Project context and funding
- Part of the Dynamic Drivers of Disease in Africa Consortium (DDDAC) Zambia trypanosomiasis case study.
- Funded by UK Natural Environment Research Council (NE/J000701/1) with ESPA program support.