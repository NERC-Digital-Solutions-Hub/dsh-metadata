# Primary data is a table of observed interactions between Drosophila species (vinegar fly) and hymenopteran parasitoids across two elevation transects

## Overview
- Primary data describe observed interactions between Drosophila pupae and hymenopteran parasitoids across two elevation transects in the Australian Wet Tropics.
- Each row represents a single Drosophila pupae screened for parasitoid presence; subset species identifications were determined via DNA metabarcoding.
- A hierarchical sampling scheme plus two supplementary tables (environmental recordings and genome sequences) accompany the main data.
- Data curated and analyzed by Chris Terry; sequencing conducted by Jan Hrček’s lab; permits granted by Queensland authorities.

## Study design and sampling
- Location: Australian Wet Tropics World Heritage area, Queensland, Australia, spanning two elevation gradients: Paluma Range and Kirrama Range.
- Elevation range: 59–916 m above sea level.
- Site count: 14 sites (7 per transect) within enclosed forest across elevation ranges.
- Trap design: bottle traps (1.5 L), banana bait, cardboard for pupation, rain-shield, ant-exclusion coating; traps hung 1.5 m above ground, minimum 5 m apart, at least 5 m from roads.
- Trap exposure: long (24 days), medium (14–15 days), or short (11–12 days); weather affected data at P070.
- Sampling period: March 11–April 12, 2016 (mid-late wet season).
- Sample processing: 15 traps per site (5 from each exposure category) selected; some traps excluded for ants/mammal raids, dryness, or flooding.
- Pupal handling: pupae stored individually in 96-well plates in ethanol at −15°C; sorted on collection day or later.

## Study sites and geolocation
- Paluma Range (K transect) and Kirrama Range (K transect) with explicit site codes (K070, K150, K230, K310, K390, K570, K670, K730) and elevation points (e.g., 70 m, 150 m, 230 m, etc.).
- Kirrama coordinates (examples): K070, −18.2022, 145.885; K150, −18.1959, 145.869; K230, −18.1979, 145.859; K310, −18.1988, 145.8526; etc.
- Paluma coordinates (examples): P070, −18.9837, 146.235; P090, −18.9922, 146.2911; P250, −19.0083, 146.2782; P780, −19.0087, 146.2269; P880, −19.0064, 146.2122.
- Elevation range across sites: 59–916 m.

## Data collection and processing
- Host and parasitoid identification: performed via DNA metabarcoding for a core subset; additional samples screened via PCR for parasitoid presence, with sequencing to identify host and parasitoid.
- Core network: random selection of 182 pupae per site (total 722 hosts identified; 179 parasitized; 147 parasitoids identified).
- Enrichment: additional samples (total 2659; 339–564 per site) screened by PCR for parasitoids; those found parasitized sequenced.
- Overall outcome: combined into an enriched quantitative network using core network host frequencies and host-specific parasitism rates; interaction frequencies derived from both core and enriching sets.

## Data files and structure
- PupaeIdentification.csv
  - Rows: one row per pupae.
  - Key columns: SampleID (unique sample ID), Transect, Site, Elevation (m), ExposureLength (Short/Medium/Long), TrapID, Host (Drosophila species; NA if unknown), Parasitoid (pseudo-species), Parasitised (PCR result for parasitoid DNA), Group (Screen Only, Core, Enriching).
- DataLoggerRecords.csv
  - Rows: hourly environmental readings.
  - Key columns: Date (YYYY-MM-DD HH:MM:SS), Temp (°C), Humidity (%), SerialNumber (data logger), Site, Trap, Transect.
- SequencesTable.csv
  - Details of sequences used for Drosophila species identification.
  - Columns include: Species, Location, Sample Code, Locus, Year_of_collection, Genbank_accession_no., Seq (sequence data).
- Supplementary context
  - Two supplementary tables provide temperature and humidity recordings (environmental context) and a table of genome sequences used for identification.

## Hierarchical network construction and analysis
- Core network construction
  - Random selection of 182 pupae per site; full identification of host and parasitoid via DNA metabarcoding.
  - Results: 722 hosts identified; 179 parasitized; 147 parasitoids identified.
- Enrichment phase
  - PCR screening of all available additional samples (2659 total); targeted identification of parasitized samples.
- Integrated network
  - An enriched quantitative network combines core host frequencies, parasitism rates, and interaction data from both core and enriching sets to describe host-parasitoid interactions across sites and elevations.

## Provenance and permissions
- Permits: WITK16977516 from Queensland Department of Environment and Heritage Protection (to Chris Jeffs).
- Personnel and affiliations: Sampling by Chris Jeffs; sequencing by Jan Hrček; data curation and analysis by Chris Terry (University of Oxford, then QMUL).
- Data source reference: Jeffs et al. 2020 (preprint) for molecular methods; DOI: 10.1101/2020.07.21.213678.

## Geospatial and temporal context for GIS use
- Spatial features: multiple sites with precise coordinates and elevation values across two transects; trap locations detailed per site.
- Temporal features: sampling window in March–April 2016; hourly environmental data logged during the sampling period.
- Potential GIS applications: mapping species interactions and parasitism across elevation gradients; integrating with climate data (temperature, humidity) and sequence metadata for spatial analyses of host-parasitoid networks.

## Usage notes for GIS specialists
- Data integration: join PupaeIdentification.csv with DataLoggerRecords.csv on Site/Transect/Trap to map environmental context to observed interactions.
- Network visualization: construct host–parasitoid interaction networks per site or transect using core and enriched interaction data; stratify by elevation and exposure duration.
- Data quality and standards: note exclusion criteria for traps; use the hierarchical sampling framework to compare core versus enriched interaction frequencies.
- Citation and data access: reference Jeffs et al. (2020) preprint for methodological details; link to GenBank accession records in SequencesTable.csv for sequence verification.