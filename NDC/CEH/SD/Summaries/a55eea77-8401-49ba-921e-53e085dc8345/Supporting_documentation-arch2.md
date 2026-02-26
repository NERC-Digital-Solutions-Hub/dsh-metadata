# Supporting documentation for dataset
Molecular analysis of Glossina morsitans morsitans tsetse from Mambwe District, Zambia, 2013.

## Overview
- Purpose: Describe prevalence of trypanosomes and Sodalis glossinidius in Glossina morsitans morsitans tsetse flies from Mambwe District, Eastern Province, Zambia (2013); investigate host blood meals to assess risk to humans and livestock.
- Context: Part of the Dynamic Drivers of Disease in Africa Consortium (DDDAC); contributes to the Zambia trypanosomiasis case study.
- Relevance: Supports environmental health monitoring by linking vector infection status and feeding patterns to disease risk amid land-use changes and human migration.
- Funding and collaboration: Funded by NERC (NE/J000701/1) with ESPA support.

## Data collection and sampling design
- Field campaigns: Two intensive surveys conducted in 2013—May/June (cool dry season) and November (hot dry season).
- Sampling method: Black screen fly rounds along a transect from the eastern Luangwa Valley plateau to the valley floor near Mfuwe Airport; approximately 1 km intervals; each fly round ~6 km with 200 m stops.
- Habitat and timing: Sampling aligned with peak tsetse activity, starting at 7 am; GPS coordinates recorded at each stop.
- Specimens: Tsetse flies captured and identified by species; flies homogenized for DNA extraction.
- Laboratory analysis:
  - PCR screening for Trypanosoma species using ITS1 primers; species-specific primers for T. vivax, T. b. brucei, T. b. rhodesiense.
  - ITS1-positive samples further tested to distinguish T. congolense subgroups (Savannah, Forest, Kilifi).
  - S. glossinidius detection via GroEL gene using PCR (~290 samples subjected to PCR).
  - Blood meal analysis via cytochrome b gene PCR on samples with feeding evidence; direct sequencing of positive products.
  - Sequencing and identification: ExoSAP-IT cleanup; BigDye Terminator v3.1 sequencing; sequence comparisons via BLAST against public databases.
- Quality controls: Each PCR included negative and positive controls; gel electrophoresis used to size amplicons.

## Dataset structure and contents
- File: DDDAC_tsetse_molecular_data2013.csv
- Key variables:
  - Sample_id: Unique observation identifier
  - Survey: 'One' (May/June) or 'Two' (November)
  - TCS-: PCR results for Trypanosoma congolense savannah
  - T vivax: PCR results for Trypanosoma vivax
  - T. b. brucei: PCR results for Trypanosoma brucei brucei
  - T. b. rhodesiense: PCR results for Trypanosoma brucei rhodesiense
  - Sodalis: PCR results for Sodalis glossinidius (Not analysed where applicable)
  - Cyt b sequence: Blood meal cytochrome b sequence; 'Negative' or 'Not analysed' where appropriate
  - Scientific name: Scientific name of the host animal (blood meal source)
  - Common name: Common name of host animal (blood meal source)
- Geography: Data includes longitude 31.826 to 32.094 and latitude -13.248 to -13.828
- Scope: Approximately 290 tsetse DNA samples subjected to PCR; multiple pathogens and a vector endosymbiont analyzed

## Geographical and contextual extent
- Area: Luangwa Valley, Zambia, specifically Mambwe District in Eastern Province
- Ecological and epidemiological relevance: Longstanding focus of human African trypanosomiasis (HAT) with ongoing sporadic outbreaks; land-use changes and migrant influx potentially affect tsetse dynamics and disease risk

## Outputs and potential uses for environmental monitoring
- Outputs: Molecular prevalence data for multiple Trypanosoma species, Sodalis glossinidius presence, and host-feeding patterns; linked to sampling metadata (survey period, location)
- Uses:
  - Monitor vector infection rates and feeding behavior over time
  - Inform risk assessments for human and livestock trypanosomiasis
  - Support integration with broader environmental and policy monitoring datasets
  - Enable trend analyses across seasons and geographic gradients

## Data quality, governance, and references
- QA practices: Use of standard sampling approaches; controls in PCR assays; sequencing verification; BLAST-based species identification
- Data provenance: Details of field methods, lab protocols, and sequencing steps documented; references provided for sampling and molecular techniques
- References (selected): 
  - Ford et al. Transect fly-rounds in field studies of Glossina
  - Seasonal tsetse distribution studies in eastern Zambia
  - Bloodmeal analysis via mitochondrial cytochrome b genes (Muturi et al.)
- Accessibility: Dataset provided as a CSV with clearly defined variables for reuse and analysis within environmental health monitoring workflows