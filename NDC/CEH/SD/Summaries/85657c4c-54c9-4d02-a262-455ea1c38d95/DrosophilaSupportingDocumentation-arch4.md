# Drosophila–parasitoid interactions across elevation gradients in the Australian Wet Tropics

## Overview
- Primary data documenting interactions between Drosophila species and hymenopteran parasitoids across two elevation transects in the Australian Wet Tropics.
- Each row represents a single Drosophila pupae screened for parasitoid presence; a subset of identifications was determined for both host and parasitoid using DNA metabarcoding within a hierarchical sampling scheme.
- Supplementary data include environmental conditions (temperature and humidity) and genome sequences used for species identification.
- Work conducted under appropriate permits; data curated and analyzed by project personnel from Oxford and Queen Mary University of London.

## Study sites and sampling design
- Location: Australian Wet Tropics World Heritage area, spanning 59–916 m above sea level.
- Two elevation transects: Paluma Range Road (K) and Kirrama Range Road (P), with a total of 14 sampling sites (7 per transect).
- Site details provided as site codes, coordinates, transect, and elevation.
- Sampling method: bottle traps baited with fermented banana, deployed 1.5 m above ground, spaced at least 5 m apart, and placed away from roadside edges.
- Traps baited with 50 g banana bait and cardboard to facilitate pupation; exposed during March 11–April 12, 2016 (mid-late wet season).
- Exposures categorized as short (11–12 days), medium (14–15 days), or long (24 days); some weather-related exclusions (e.g., no short exposure data at P070).

## Data collection and storage
- Pupae from 15 randomly selected traps per site (5 per exposure category) were sorted on collection day or frozen for later sorting.
- Pupae stored individually in 96-well plates with ethanol and kept at −15°C.
- Sorting and identification followed hierarchical steps, with some samples kept as unknowns (NA for host).
- Datapoints include trap-specific and site-specific metadata to support discoverability and re-use.

## Hierarchical network construction and data processing
- Core network: from a random subset of 182 pupae per site, with both host and parasitoid identified by DNA metabarcoding.
  - Results: 722 hosts identified (86–138 samples per site); 179 parasitized; 147 parasitoids identified.
- Enriching network: additional samples (totaling 2,659; 339–564 per site) screened for parasitoid DNA via PCR; parasitized samples sequenced to identify host and parasitoid.
- Final dataset integrates core and enriching data to form an enriched quantitative network using:
  - Relative host frequencies
  - Overall host-specific parasitism rates from the core network
  - Interaction frequencies derived from both core and enriching sets

## Data files and structure
- PupaeIdentification.csv
  - SampleID: unique ID
  - Transect, Site: transect name and site code
  - Elevation (m a.s.l.)
  - ExposureLength: Short, Medium, or Long
  - TrapID: within-site trap identifier
  - Host: Drosophila species (NA if unknown)
  - Parasitoid: parasitoid pseudonym
  - Parasitised: true/false (PCR result)
  - Group: Screen Only, Core, Enriching
- DataLoggerRecords.csv (Environmental Data)
  - Date (YYYY-MM-DD HH:MM:SS)
  - Temp (°C), Humidity (%)
  - SerialNumber: data logger identifier
  - Site, Trap, Transect
  - Hourly readings across the sampling period
- SequencesTable.csv
  - Species, Location, Sample Code, Locus, Year_of_collection
  - Genbank_accession_no., Seq
  - Details of sequences used for Drosophila identification
- Supplementary Tables (not detailed in main text)
  - Temperature and humidity recordings (data loggers)
  - Genome sequences used in host/parasitoid identification

## Data quality, limitations, and provenance
- Identification success varied; core dataset achieved substantial host and parasitoid identifications, with 722 hosts and 147 parasitoids identified in core.
- Some data gaps due to weather, trap raiding, or short exposure at a site (e.g., P070).
- Metadata-rich structure supports reproducibility, discoverability, and cross-site comparisons.
- Data are linked to the 2020 Jeffs et al. preprint and supplementary information, including SI tables and GenBank references.

## Permits, authorship, and access
- Permits: WITK16977516 from Queensland Department of Environment and Heritage Protection.
- Sampling led by Chris Jeffs; grant support by Owen Lewis (Oxford); sequencing by Jan Hrček (Czech Academy of Sciences); data curation and manuscript preparation by Chris Terry (Oxford/Queen Mary University of London).
- Data and methods described for replication and reuse; primary datasets are complemented by supplementary environmental data and sequence information.