# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) macrofaunal biomass in mudflat and saltmarsh habitats..

- Purpose: Dataset documenting macrofaunal biomass to support coastal biodiversity and ecosystem service sustainability monitoring across mudflat and saltmarsh habitats.
- Coverage: 6 sites across 2 locations (Essex and Morecambe Bay) and 2 habitats (mudflat and saltmarsh).
- Sampling period: Winter and Summer 2013 as part of the CBESS field campaign.
- Sampling design: 3 cores per quadrat, across 22 quadrats, at 4 spatial scales; 3 replicates per sampling unit.
- Staff responsible: Christina Wood and Martin Solan.

## Locations and habitat details

- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS).
- Saltmarsh context: two contrasting soil types (clay soils in Essex; sandy soils in Morecambe Bay); broad differences in inundation frequency, creek structure, and dominant vegetation.
- Mudflat context: Essex mudflats with cohesive clays, mud, and silt; Morecambe mudflats with coarse, mobile sediments.

## Data collection and processing

- Primary measurement: Biomass of macrofauna (grams per square meter, g/m^2).
- Field methods: Three cylindrical sediment cores (10 cm depth, 10 cm diameter) per quadrat; fixed in 4% buffered formalin in seawater; sieved on 0.5 mm mesh; residues preserved in 70% IMS; organisms identified to species (or major group if damaged) and stored in IMS.
- Biomass calculation: Individuals weighed to 0.0001 g after blotting; for very light samples, a default 0.0001 g was recorded; biomass converted using multiplier 127.323955 and rounded to 0.0001 g to yield g/m^2.
- Debris handling: Major debris separated into annelid, mollusc, and crustacean debris as needed.
- Quality control: Data entered independently by two people and double-checked; biomass data cross-validated against corresponding abundance data in CBESS_macrofauna_abundance.csv; species names checked against World Register of Marine Species (WoRMS).

## Dataset structure and fields

- Data format: CSV file.
- Core variables: Season (Winter W, Summer S); Location (Morecambe M, Essex E); Site (CS, WS, AH, FW, TM); Habitat (Mudflat MF, Saltmarsh SM); Quadrat Number (1–22); Scale categories (A–D with defined metre ranges); Replicate (1–3); Measurement Type (Maf = Macrofauna).
- Species list: Biomass columns for each listed species (e.g., Arenicola marina, Ampharete lindstroemi, Capitella sp., Eteone longa, etc.) plus major group debris and other taxa (e.g., Annelid debris, Mollusc debris, Crustacea debris, Nematoda, Nemertea).
- Documentation: Row Number field for input order; explicit species and debris biomass fields with corresponding numeric formats.

## Data quality, calibration and provenance

- Calibration: NA (not applicable for this dataset).
- Quality checks: Double data entry and cross-verification with abundance data; taxonomic verification against WoRMS; accepted names cross-checked.
- Provenance: Collected as part of CBESS field campaign; designed to represent contrasting habitat types and sediment conditions across two UK regions.

## Relevance to monitoring objectives and use

- Alignment with monitoring aims: Provides standardized, comparable biomass data to assess environmental health and the status of coastal biodiversity over time, with clear documentation of methods and sites.
- Data value and accessibility: Dataset designed to be combined with other CBESS data and made available for broader analyses; emphasizes accessibility to underlying data and transparent data provenance.
- Scope for integration: The dataset supports cross-site and cross-habitat comparisons, contributing to assessments of ecosystem service sustainability in coastal environments.