# Summary: Primary data is a table of observed interactions between Drosophila species (vinegar fly) and hymenopteran parasitoids across two elevation transects

- Purpose and scope
  - Presents primary data on interactions between Drosophila species and hymenopteran parasitoids across two elevation transects in the Australian Wet Tropics World Heritage area.
  - Elevation range: 59–916 m above sea level; transects Paluma Range (K) and Kirrama Range (P) with 14 sites total (7 per transect).
  - Data were collected March–April 2016 using field traps to build quantitative interaction networks.

- Study design and sampling
  - Hierarchical sampling approach to construct two sets of networks: a core network and an enriched network.
  - Core network: random subset of 182 pupae per site (total hosts identified: 722; 86–138 samples per site), with 179 parasitized and 147 parasitoids identified.
  - Enriching network: an additional 2,659 samples screened for parasitoid DNA (339–564 per site); parasitized samples sequenced to identify host–parasitoid pairs.
  - In total, data integrate core identifications with enrichment data to produce an enriched quantitative network combining host frequencies and parasitism rates.

- Data collection methods
  - Traps: bottle traps baited with fermented banana, with windows for entry, rain-shields, and ant deterrents; placed 1.5 m above ground, separated by ≥5 m, away from roads.
  - Trap exposure: long (24 days), medium (14–15 days), or short (11–12 days); data collected from 11 March to 12 April 2016.
  - Sample processing: pupae sorted from traps; sorted on collection day or frozen for later sorting; pupae stored individually in 96-well plates with 100% ethanol at −15°C.

- Data structure and contents
  - PupaeIdentification.csv
    - SampleID, Transect, Site (elevation m a.s.l.), ExposureLength (Short/Medium/Long), TrapID, Host (species or NA), Parasitoid (pseudo-species), Parasitised (PCR result), Group (Screen Only, Core, Enriching).
  - DataLoggerRecords.csv
    - Hourly environmental readings from data loggers (DateTime, Temperature, Humidity, SerialNumber, Site, Trap, Transect); notes on data usability per site.
  - SequencesTable.csv
    - Sequences used to identify Drosophila species (Species, Location, Sample Code, Locus, Year, GenBank accession, Sequence).

- Environmental data and supplementary resources
  - Temperature and humidity data loggers (EasyLog ELUSB-2) provided hourly environmental context for each site.
  - Supplementary tables include environmental recordings and a genome-sequence table used for Drosophila identification.

- Molecular methods and data provenance
  - Species and parasitoid identification for subsets via DNA metabarcoding; hierarchical sampling details and exact molecular methods are described in Jeffs et al. 2020 (preprint).
  - Sequencing conducted in Jan Hrček’s lab; data curated and analyzed by Chris Terry.

- Permissions and study sites
  - Permit WITK16977516 from the Queensland Department of Environment and Heritage Protection.
  - Sites located in Paluma Range and Kirrama Range within the Australian Wet Tropics, with precise site coordinates and elevations provided.

- Data handling, governance and references
  - Emphasizes data quality, metadata availability, and recording of sampling/exposure conditions to support reproducibility.
  - Core dataset provides a defensible baseline of interactions; enriching dataset expands interaction coverage.
  - Underlying data management and sharing considerations are acknowledged (including potential barriers to public data sharing and the need for metadata quality and standardization).
  - Primary reference for molecular methods is Jeffs et al. 2020 preprint (link provided).

- Notes on limitations and considerations
  - Some sites yielded limited usable data (e.g., certain datalogger periods and missing loggers).
  - Exclusion criteria applied to traps (raided, overly dry, or flooded) may affect completeness.
  - Data gaps and transformation requirements for metadata are addressed, highlighting typical challenges in assembling comprehensive monitoring datasets.