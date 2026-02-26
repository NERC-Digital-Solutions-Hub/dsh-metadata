# Supporting documentation for dataset Molecular analysis of Glossina morsitans morsitans tsetse from Mambwe District, Zambia, 2013.

## Overview
- Describes prevalence of trypanosomes and Sodalis glossinidius in Glossina morsitans morsitans tsetse flies, and host blood meal analysis.
- Collected during two intensive surveys in Mambwe District, Eastern Province, Zambia in 2013.
- Part of the Dynamic Drivers of Disease in Africa Consortium (DDDAC); contributes to the Zambia trypanosomiasis case study.
- Aimed at monitoring infection rates and feeding patterns to assess risk to humans and livestock; blood meal analysis to identify host species.

## Geographical scope and context
- Region: Luangwa Valley, eastern Zambia.
- Geographic extent: Longitude 31.826 to 32.094; Latitude -13.248 to -13.828.
- Sampling design: Transect from the plateau region (approximately 900 m altitude) down to the valley floor near Mfuwe Airport (approximately 550 m altitude); transect starts at Wazaza, follows the road through Msoro to Mfuwe, ending at M'nkanya turning.
- Transect details: Approximately 6 km long; sampling stops every ~200 m; fly rounds located at ~1 km intervals perpendicular to the road.
- Sampling seasons: May/June (cold dry season) and November (hot dry season) in 2013.

## Data collection and laboratory methods
- Field methods: Black screen fly rounds used to sample tsetse flies following established Glossina methodologies; GPS coordinates recorded for each stop; sampling conducted at the same time of day (7 am).
- Specimen processing: Fly DNA extracted from pooled samples; samples stored at -20°C until PCR.
- Molecular analyses:
  - Trypanosoma detection: ITS1 PCR to screen for multiple Trypanosoma species; species-specific primers used for T. vivax and for T. brucei complex (T. b. brucei, T. b. rhodesiense). If ITS1 ~700 bp, further subtyping for T. congolense savannah, forest, and Kilifi.
  - Sodalis glossinidius detection: PCR targeting the GroEL gene (~290 samples subjected to PCR).
  - Blood meal analysis: PCR targeting cytochrome b gene on samples with evidence of feeding; positive samples sequenced and identified via BLAST against public databases.
- Controls: All PCRs included negative and positive controls; amplicons visualized on 1.5% agarose gels.

## Data structure and variables
- Data file: CSV named DDDAC_tsetse_molecular_data2013.csv.
- Key variables:
  - Sample_id: Unique observation identifier.
  - Survey: "One" for May/June survey or "Two" for November survey.
  - TCS: PCR results for Trypanosoma congolense savannah.
  - T vivax: PCR results for Trypanosoma vivax.
  - T. b. brucei: PCR results for Trypanosoma brucei brucei.
  - T. b. rhodesiense: PCR results for Trypanosoma brucei rhodesiense.
  - Sodalis: PCR results for Sodalis glossinidius (value "Not analysed" if not tested).
  - Cyt b sequence: Resulting cytochrome b sequence; "Negative" if no sequence obtained; "Not analysed" if insufficient DNA for blood meal analysis.
  - Scientific name: Scientific name of the animal from which the tsetse fly fed (if determined).
  - Common name: Common name of the host (if determined).
- Geographic data within the dataset: Sampling stops with GPS coordinates at each stop; two-season coverage allows temporal GIS analyses.

## Spatial data considerations and GIS applications
- Each observation is geolocated along a defined transect, enabling:
  - Mapping spatial distribution of infections (Trypanosoma species) and Sodalis prevalence.
  - Spatial-temporal analyses comparing the two surveys (May/June vs. November).
  - Integration with other GIS layers (land-use change, elevation, hydrology, human/livestock population data) to explore drivers of tsetse infection dynamics.
  - Linking host blood meal data to determine spatial patterns in host availability and feeding.
- Data can be joined to other spatial datasets via Sample_id or by matching coordinates and survey period.

## Potential uses and analyses for GIS specialists
- Create maps showing prevalence hotspots for specific Trypanosoma species and Sodalis across the transect.
- Visualize transect-based sampling along elevation gradients and landscape features.
- Assess relationships between infection patterns and land-use changes or environmental variables using overlay analyses.
- Compare seasonal shifts in infection and feeding patterns between the two surveys.
- Prepare thematic layers (e.g., infection status, blood meal hosts) for policy briefings or public-facing GIS dashboards.

## Limitations and considerations
- Two surveys conducted in a single year; seasonal comparison is possible but temporally limited.
- Some data fields may be marked as "Not analysed" or "Negative," indicating incomplete testing or undetermined results.
- Sampling is along a single transect in a defined district; extrapolation beyond the transect requires caution.
- Some Cyt b results depend on DNA quality; sequences may be unavailable or inconclusive for certain samples.

## References
- Field and laboratory methods cited (sampling transects, ITS1 PCR, species-specific primers, cytochrome b analysis) and related sampling studies are provided in the document references.