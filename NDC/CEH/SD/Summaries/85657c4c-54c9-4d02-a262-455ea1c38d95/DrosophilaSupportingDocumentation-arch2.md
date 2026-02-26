# Drosophila–parasitoid interactions across two elevation transects

- Purpose and scope
  - Primary dataset documenting interactions between Drosophila species (vinegar flies) and hymenopteran parasitoids across two elevation transects in the Australian Wet Tropics.
  - Uses a hierarchical sampling design and DNA metabarcoding to identify hosts and parasitoids; complemented by environmental data and sequence data for identification.
  - Aimed at enabling consistent environmental health monitoring and policy-relevant analyses through standardized data formats and network synthesis.

- Study design and sampling
  - Location: Australian Wet Tropics World Heritage area, two elevation gradients:
    - Paluma Range Road (Paluma Range National Park) and Kirrama Range Road (Girramay National Park).
  - Elevation range: 59–916 meters above sea level; 14 sampling sites (7 per transect).
  - Trap method: bottle traps (1.5 L) baited with banana, with windows for entry, rain-shields, and ant-prevention measures; traps hung 1.5 m above ground, spaced at least 5 m apart and at least 5 m from roads.
  - Sampling period: 11 March – 12 April 2016 (mid-late wet season).
  - Exposure durations: long (24 days), medium (14–15 days), short (11–12 days); incomplete data for short exposure at P070 due to weather.
  - Screening: 15 random traps per site (5 per exposure) were used to collect fly pupae; traps raided or overly dry/flooded were excluded.
  - Specimen handling: pupae stored individually in 96-well plates with ethanol at -15°C; some sorting conducted on collection day, others later.

- Data collection and types
  - PupaeIdentification.csv
    - One row per pupae.
    - Key fields: SampleID, Transect, Site (elevation in m), ExposureLength, TrapID, Host (Drosophila species; NA if unknown), Parasitoid (pseudo-species), Parasitised (PCR result), Group (Screen Only, Core, Enriching).
  - Environmental data
    - DataLoggerRecords.csv: hourly readings from data loggers (temperature and humidity); multiple loggers per site; notes on usable data per site (some loggers limited or missing).
  - Genetic identification
    - SequencesTable.csv: details of sequences used to identify Drosophila species (Species, Location, Sample Code, Locus, Year_of_collection, Genbank_accession_no., Seq).

- Analytical approach and network construction
  - Hierarchical Network Construction
    - Core network: random selection of 182 pupae per site for full host/parasitoid identification via DNA metabarcoding (722 hosts identified across sites; 179 parasitized; 147 parasitoids identified).
    - Enrichment phase: remaining samples (2659 total) screened for parasitoid DNA via PCR; parasitized samples sequenced to identify host and parasitoid.
    - Integration: combined into an enriched quantitative network using:
      - Relative host frequencies and host-specific parasitism rates from the core network.
      - Interaction frequencies derived from both core and enriching datasets.
  - Outputs are designed as standardized networks to support monitoring of ecological interactions over time.

- Data management and provenance
  - Data collection led by Chris Jeffs; grant held by Owen Lewis (University of Oxford); sequencing conducted in Jan Hrček’s lab (Institute of Entomology, Czech Academy of Sciences); data curated and analyzed by Chris Terry (University of Oxford/Queen Mary University of London).
  - Permits: WITK16977516 from Queensland Department of Environment and Heritage Protection.

- Study context and site details
  - Site geography and elevation
    - Two transects in the Australian Wet Tropics World Heritage area, spanning elevations from 59 to 916 m.
    - 14 sites in total (K070, K150, K230, K310, K390, K570, K670, K730 for Kirrama/Transect K; P070, P090, P250, P350, P505, P590, P650, P780, P880 for Paluma/Transect P).
  - Specific coordinates and transect designations are provided for each site.

- Accessibility and usage notes
  - Data are organized into clearly defined CSV files suitable for analysis, mapping, and policy-relevant reporting.
  - Some environmental data gaps exist due to limited data logger usability at certain sites and times; users should account for these limitations in analyses.

- Permits and ethics
  - Permit WITK16977516 issued by the Queensland Department of Environment and Heritage Protection; work conducted under this authorization.