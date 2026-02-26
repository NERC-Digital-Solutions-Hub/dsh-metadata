# Supporting documentation for dataset Molecular analysis of Glossina morsitans morsitans tsetse from Mambwe District, Zambia, 2013

## Purpose and monitoring context
- Describes prevalence of trypanosomes and Sodalis glossinidius in Glossina morsitans morsitans tsetse flies.
- Includes host blood meal analysis to assess feeding patterns.
- Aims to monitor infection rates and feeding behavior to evaluate risk to human and livestock populations in the Luangwa Valley, an area with historical human African trypanosomiasis (HAT) activity and recent land-use changes.
- Part of the Dynamic Drivers of Disease in Africa Consortium (DDDAC) and contributes to the Zambia trypanosomiasis case study.
- Funded by NERC NE/J000701/1 with ESPA support.

## What was measured
- Prevalence of several Trypanosoma species:
  - T. congolense Savannah
  - T. vivax
  - T. b. brucei
  - T. b. rhodesiense
- Presence of the symbiont Sodalis glossinidius
- Host blood meal sources via cytochrome b analysis (and sequencing)

## Sampling design and field methods
- Two intensive surveys conducted in 2013:
  - May/June (cold dry season)
  - November (hot dry season)
- Fly rounds along a transect from the plateau to the valley floor, sampled at ~1 km intervals.
- Each fly round is 6 km long with stops every 200 m.
- Sampling used black screen fly rounds baited with phenols and acetone; flies captured with nets.
- Geographic coordinates recorded at each stop; sampling started at 7 am to match peak tsetse activity.

## Laboratory methods
- DNA extraction from tsetse samples, stored at -20°C.
- PCR screening:
  - ITS1 primers to detect multiple Trypanosoma species
  - Species-specific primers for T. vivax
  - ITS1-positive samples subjected to species-specific primers to identify T. b. brucei, T. evansi, T. b. rhodesiense
  - PCR products for T. congolense subgroups (Savannah, Forest, Kilifi) based on ~700 bp ITS1 product
- Sodalis detection via GroEL gene PCR (approx. 290 samples analyzed)
- Blood meal identification:
  - Cytochrome b PCR on samples with evidence of feeding
  - Positive samples sequenced and identified via BLAST against public databases
- Quality controls included negative and positive controls; products visualized by agarose gel electrophoresis

## Data file and variables
- Dataset: DDDAC_tsetse_molecular_data2013.csv
- Variables:
  - Sample_id (unique observation identifier)
  - Survey (One = May/June, Two = November)
  - TCS (Trypanosoma congolense savannah)
  - T vivax (Trypanosoma vivax)
  - T. b. brucei
  - T. b. rhodesiense
  - Sodalis (Sodalis glossinidius); values include 'Not analysed'
  - Cyt b sequence (blood meal PCR result); values include 'Negative' or 'Not analysed'
  - Scientific name (host species)
  - Common name (host species)
- Notes: Some entries are marked as not analysed and some sequences may be negative or unavailable due to DNA quality

## Geographical extent
- Latitude: -13.248 to -13.828
- Longitude: 31.826 to 32.094

## Data provenance, context, and accessibility
- Linked to the broader DD DAC project and Zambia trypanosomiasis case study
- Data collected through standardized field sampling and molecular methods
- Data structure includes explicit status flags (e.g., Not analysed, Negative) to indicate data completeness and quality
- Dataset intended to support monitoring of disease risk and vector-host dynamics, with potential implications for public health and livestock management

## References and methodological context
- Sampling and molecular methods reference established protocols and prior studies (cited in the dataset documentation)
- Provides methodological justification for transect fly-round sampling and targeted PCR assays for Trypanosoma species and Sodalis glossinidius
- Blood meal analysis aligned with published approaches using cytochrome b sequencing and BLAST identification