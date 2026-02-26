# Supporting documentation for dataset Molecular analysis of Glossina morsitans morsitans tsetse from Mambwe District, Zambia, 2013.

## Overview

- Describes prevalence of trypanosomes and Sodalis glossinidius, plus host blood meal analysis from Glossina morsitans morsitans tsetse flies.
- Collected during two intensive surveys in Mambwe District, Eastern Province, Zambia in 2013.
- Aims to monitor infection rates and feeding patterns to assess risk to humans and livestock; part of the Dynamic Drivers of Disease in Africa Consortium (DDDAC) and Zambia trypanosomiasis case study.
- Funded by NERC project NE/J000701/1 with ESPA support.

## Data content and structure

- Dataset provided as a CSV: DDDAC_tsetse_molecular_data2013.csv.
- Variables include:
  - Sample_id: unique observation identifier.
  - Survey: indicating May/June (One) or November (Two) survey.
  - TCS-: Trypanosoma congolense savannah results.
  - T vivax: Trypanosoma vivax results.
  - T. b. brucei: Trypanosoma brucei brucei results.
  - T. b. rhodesiense: Trypanosoma brucei rhodesiense results.
  - Sodalis: Sodalis glossinidius results (or "Not analysed").
  - Cyt b sequence: cytochrome b sequence for blood meal analysis (or "Negative"/"Not analysed").
  - Scientific name: scientific name of the animal from which the tsetse fed.
  - Common name: common name of the animal from which the tsetse fed.
- Data include statuses such as "Not analysed" and "Negative" to indicate incomplete or failed analyses.
- Geographic coordinates are included for each sampling stop.

## Sampling and laboratory methods (provenance)

- Field design:
  - Two surveys during different seasons: cold dry season (May/June) and hot dry season (November) in 2013.
  - Fly rounds along a transect from eastern Luangwa Valley highlands to the valley floor; approximately 1 km between stops, with 6 km per round.
  - Sampling used black screen fly rounds baited with phenols and acetone; specimens collected with nets; GPS coordinates recorded; sampling timed to peak tsetse activity (7am).
- Laboratory analyses:
  - DNA extraction from tsetse samples; samples stored at -20°C.
  - PCR screening:
    - ITS1 primers to detect multiple Trypanosoma species.
    - Species-specific primers for T. vivax, T. b. brucei, T. b. rhodesiense.
    - T. congolense subgroups identified with subgroup-specific PCR when ITS1 ~700 bp.
    - ~290 samples tested for S. glossinidius targeting GroEL gene.
  - Blood meal analysis:
    - PCR targeting cytochrome b gene on samples with evidence of feeding.
    - Positive samples sequenced using BigDye Terminator and ABI 3130x genetic analyzer.
    - Sequences compared to public databases via NCBI BLAST to determine host species.
  - Quality controls included negative and positive controls for all PCR runs; gel electrophoresis used to visualize amplicons.

## Geospatial and temporal coverage

- Temporal coverage:
  - Two surveys in 2013: May/June and November.
- Spatial coverage:
  - Mambwe District, Eastern Province, Zambia.
  - Geographical extent: Longitude 31.826 to 32.094; Latitude -13.248 to -13.828.

## Data file details and fields

- File: DDDAC_tsetse_molecular_data2013.csv.
- Key fields:
  - Sample_id, Survey, TCS-, T vivax, T. b. brucei, T. b. rhodesiense, Sodalis, Cyt b sequence, Scientific name, Common name.
- Notes:
  - Cyt b sequencing results may be "Negative" or "Not analysed" if DNA was inadequate or no sequence obtained.
  - Sodalis results may be "Not analysed" if PCR was not performed.

## Data quality, limitations, and stewardship considerations

- Some samples are "Not analysed" for certain variables, indicating incomplete data.
- Blood meal analysis is contingent on successful Cytochrome b PCR and sequencing.
- Data reflect field and laboratory methodologies from 2013; provenance and methods are documented to support reproducibility and reuse.
- Useful for assessing parasite/host dynamics and HAT risk, as part of broader epidemiological studies.

## Access, usage, and provenance

- The dataset is accompanied by methodological details and references to support reuse.
- Provenance includes field sampling procedures, molecular assays, and sequence analysis protocols.

## References

- Ford J, Glasgow J, Johns D, Welch J. Transect fly-rounds in field studies of Glossina. Bull Entomol Res. 1959;50(02):275-85.
- Van den Bossche P, De Deken R. Seasonal variations in the distribution and abundance of the tsetse fly, Glossina morsitans morsitans in eastern Zambia. 2002:170-6, 2002 Jun. PubMed PMID: 12109711.
- Shereni W. The use of cloth screens and acetone vapour as alternatives to a bait-ox for sampling populations of tsetse flies (Diptera: Glossinidae). Transactions of the Zimbabwe Scientific Association. 1984;62:22-7.
- Muturi CN, Ouma JO, Malele II, Ngure RM, Rutto JJ, Mithofer KM, et al. Tracking the feeding patterns of tsetse flies (glossina genus) by analysis of bloodmeals using mitochondrial cytochromes genes. PLoS One. 2011;6(2):e17284. PubMed PMID: 21386971.