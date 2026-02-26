# Supporting documentation for dataset Molecular analysis of Glossina morsitans morsitans tsetse from Mambwe District, Zambia, 2013

- Purpose and context
  - Describes prevalence of Trypanosoma species and Sodalis glossinidius in Glossina morsitans morsitans tsetse flies.
  - Includes host blood meal analysis to understand feeding patterns.
  - Part of the Dynamic Drivers of Disease in Africa Consortium (DDDAC) and contributes to the Zambia trypanosomiasis case study.
  - Funded by NERC (NE/J000701/1) with support from ESPA.

- Study design and data collection
  - Two field surveys in 2013: cold dry season (May/June) and hot dry season (November) in Mambwe District, Eastern Province, Zambia.
  - Sampling along a transect from the eastern plateau to the Luangwa Valley floor, covering altitudes 900m to 550m.
  - Fly rounds conducted every 1 km, with each round 6 km long, stopping every 200 m.
  - Tsetse caught on baited screens, with concurrent GPS coordinates recorded; sampling occurred at ~7 am.
  - Objective: assess distribution/relative density of tsetse and monitor infection rates and feeding patterns.

- Laboratory methods
  - DNA extraction from tsetse homogenates following standard protocols.
  - PCR assays:
    - ITS1 primers to detect multiple Trypanosoma species.
    - Species-specific primers for T. vivax, T. b. brucei, T. b. rhodesiense.
    - T. congolense subgroups (Savannah, Forest, Kilifi) when ITS1 indicated Trypanozoon.
    - GroEL gene PCR to detect Sodalis glossinidius.
  - Blood meal analysis:
    - PCR targeting cytochrome b gene on blood-fed samples.
    - Positive samples sequenced (ExoSAP-IT cleanup; BigDye Terminator v3.1; ABI 3130x).
    - Sequences identified by BLAST comparisons against public databases.
  - Quality controls: each PCR included negative and positive controls; gel electrophoresis used to visualize amplicons.

- Data product and structure
  - Provided dataset: DDDAC_tsetse_molecular_data2013.csv.
  - Key variables:
    - Sample_id: unique observation identifier.
    - Survey: “One” (May/June) or “Two” (November).
    - TCS- (congolense savannah), T vivax, T. b. brucei, T. b. rhodesiense: PCR results.
    - Sodalis: PCR results for Sodalis glossinidius; “Not analysed” where not tested.
    - Cyt b sequence: blood meal sequence result; “Negative” if no sequence, “Not analysed” if DNA inadequate.
    - Scientific name: species of the host animal identified from the blood meal.
    - Common name: common name of the host.
  - Overall status indicators (e.g., negative/positive results; sequence availability).

- Geographical scope
  - Longitude: 31.826 to 32.094
  - Latitude: -13.248 to -13.828

- Data context, access, and usage
  - Data describe infection prevalence in tsetse populations and feeding patterns, contributing to disease risk assessment for humans and livestock.
  - Data were collected under a broader research program and linked to a wider Zambia trypanosomiasis case study.
  - Dataset supports analyses of epidemiology, vector-host interactions, and could inform surveillance and control strategies.
  - Metadata include study design, sampling methodology, primers and assays used, sequencing workflow, and references for methods.