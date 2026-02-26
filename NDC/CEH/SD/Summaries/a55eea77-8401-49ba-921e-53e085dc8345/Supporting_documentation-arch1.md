# Supporting documentation for dataset Molecular analysis of Glossina morsitans morsitans tsetse from Mambwe District, Zambia, 2013.

## Aim
- Describe prevalence of trypanosomes and Sodalis glossinidius in Glossina morsitans morsitans tsetse flies.
- Analyze host blood meals to understand feeding patterns.
- Inform risk assessments for human and livestock health in the Luangwa Valley, Zambia.
- Contribute to the Dynamic Drivers of Disease in Africa Consortium (DDDAC) and Zambia trypanosomiasis case study; funded by NERC (NE/J000701/1) with ESPA support.

## Data collection and sampling design
- Location: Mambwe District, Eastern Province, Zambia; Luangwa Valley focus.
- Timeframe: Two surveys in 2013 — May/June (cold dry season) and November (hot dry season).
- Sampling method: Black screen fly rounds along a transect from the eastern plateau toward the valley floor; transect ~6 km, stops every 200 m, at ~1 km intervals perpendicular to the road.
- At each stop: capture tsetse, record species and counts, collect geographic coordinates, and note sampling time (7 am to match peak activity).
- Target species: Glossina morsitans morsitans; DNA extracted for PCR analyses.

## Laboratory analyses
- DNA extraction: Standard protocol using Qiagen kit after homogenization.
- Trypanosome detection: ITS1 PCR to detect Trypanosoma spp.; species-specific primers used for T. vivax, T. b. brucei, T. b. rhodesiense; if ITS1 ~700 bp, use T. congolense subgroup-specific primers to distinguish Savannah, Forest, Kilifi.
- Sodalis glossinidius detection: PCR targeting GroEL gene (approx. 290 samples subjected to PCR).
- Blood meal analysis: PCR targeting cytochrome b gene on samples with evidence of feeding; positive products sequenced (ExoSAP-IT, BigDye Terminator v3.1, ABI 3130x) and identified via BLAST.
- Controls: Each PCR run included negative and positive controls; products visualized on 1.5% agarose gels.

## Data structure and variables
- Data file: DDDAC_tsetse_molecular_data2013.csv
- Key variables:
  - Sample_id: unique observation identifier
  - Survey: 'One' (May/June) or 'Two' (November)
  - TCS- PCR results for Trypanosoma congolense savannah
  - T vivax: PCR results for Trypanosoma vivax
  - T. b. brucei: PCR results for T. b. brucei
  - T. b. rhodesiense: PCR results for T. b. rhodesiense
  - Sodalis: PCR results for Sodalis glossinidius (Not analysed if not tested)
  - Cyt b sequence: sequence result from cytochrome b PCR; 'Negative' if PCR performed but no sequence obtained; 'Not analysed' if insufficient DNA
  - Scientific name: Latin name of the host animal from which the tsetse fed
  - Common name: Common name of the host animal
- Notes: Some samples indicate 'Not analysed' or 'Not analysed' for certain measurements; results may be 'Negative' or empty.

## Geography
- coordinates: Longitude 31.826 to 32.094; Latitude -13.248 to -13.828
- Context: Luangwa Valley region in Eastern Province, Zambia.

## Potential analyses and usage
- Calculate infection prevalence by survey and by Trypanosoma species.
- Examine associations between Sodalis presence and trypanosome infections.
- Analyze feeding patterns and host species composition from blood meal data.
- Explore seasonal or spatial (along transect) variation in infection and feeding metrics.
- Integrate with other DDAC/ESPA datasets to model disease risk to humans and livestock.

## Data quality, limitations, and notes
- Some samples are labeled 'Not analysed' for certain variables; DNA quality or quantity influenced analysis feasibility.
- Blood meal analysis limited to samples with successful Cyt b amplification and sequencing.
- Data collected from two specific timepoints in 2013; may limit temporal generalizability.

## References
- Ford J, Glasgow J, Johns D, Welch J. Transect fly-rounds in field studies of Glossina. Bull Entomol Res. 1959;50(02):275-85.
- Van den Bossche P, De Deken R. Seasonal variations in the distribution and abundance of the tsetse fly, Glossina morsitans morsitans in eastern Zambia. 2002:170-6.
- Shereni W. The use of cloth screens and acetone vapour as alternatives to a bait-ox for sampling populations of tsetse flies (Diptera: Glossinidae). Trans. Zimbabwe Sci. Assoc. 1984;62:22-7.
- Muturi CN, Ouma JO, et al. Tracking the feeding patterns of tsetse flies by analysis of bloodmeals using mitochondrial cytochrome genes. PLoS One. 2011;6(2):e17284.